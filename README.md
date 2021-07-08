# [Salmon Run Overfishing](https://overfishing.netlify.app/)

ここのソースコードをもとにしたウェブサイトです。

## 必要なもの

- [Visual Studio Code](https://azure.microsoft.com/ja-jp/products/visual-studio-code/)
  - Markdown エディタとして利用する
  - VSCode を推奨ですが、お好みのエディタがあればそれも  可
- [NodeJS](https://nodejs.org/ja/download/)
  - Windows Installer(.msi)の 64bit 版を選べば良い
  - 最新版か推奨版かは好きな方をどうぞ
- [Yarn](https://classic.yarnpkg.com/en/docs/install#windows-stable)
  - Alternatives をひらいて「Windows」「Classic Stable」を選択
  - Download Installer をクリック
- [Sourcetree](https://www.sourcetreeapp.com/)
  - GUI で比較的簡単に Git が扱えるユーティリティ

上のものをすべてインストールしたら準備は完了です。

## GitHub アカウントの作成

自分が更新・作成した記事を反映させるには GitHub アカウントが必須です。

[GitHub アカウントの作成](https://github.com/signup)から新規アカウントを作成してください。

## Sourcetree の設定

### 作業環境の構築

> これは macOS 版ですが、Windows 版もほとんど同じ作業です。

Sourcetree をひらきます。

![](https://pbs.twimg.com/media/E5ns6UNWUAIXwBM?format=png)

新しいレポジトリを追加するので`New`をクリックします。

`https://github.com/tkgstrator/overfishing.git`

と入力します。

![](https://pbs.twimg.com/media/E5nt4ypXEA4M-Vx?format=png)

保存先はどこでも良いです。

![](https://pbs.twimg.com/media/E5nt8HjWQBA6a8E?format=png)

読み込みが終わったら上のタブにある`Branch`をクリックします。

![](https://pbs.twimg.com/media/E5nuAYNWEAgJ1GN?format=png)

自分だとわかる名前をつけて`Create Branch`をクリックします。

ここまでで作業環境の作成は完了です。

### アカウントの連携

Sourcetree に先ほど作成した GitHub アカウントでログインします。

認証方式は`OAuth`を選択し、`Connect Account`を押すと GitHub のサイトがひらくので認証ボタンを押します。

認証が成功したら`Save`をクリックします。

## 記事の更新・追加

先程保存した`overfishing`のフォルダを`Visual Studio Code`にドラッグアンドドロップすると以下の画面のように読み込んでくれます。

![](https://pbs.twimg.com/media/E5nvnokWEAwHALn?format=png)

いろいろ表示されていますが、記事を書いて反映されるのは`docs`フォルダ内だけです。

また、記事は`markdown`しかサポートしていないので新規作成でファイルを作成し`XXXXXX.md`のようなファイルを作成します。

分類を行いたい場合は`event/rush.md`のように`event`フォルダを作成してその下にファイルを作成してください。

### 記事の執筆方法

先程も言ったように記事は`markdown`形式しかサポートしていません。

Markdown での記事の書き方については[Markdown 記法 サンプル集](https://qiita.com/tbpgr/items/989c6badefff69377da7)が便利ですので是非参考にしてみてください。

## 執筆中の記事の確認方法

実際にどんな記事が書けているかは`Visual Studio Code`のプレビュー機能か、開発環境ビルドが利用できます。

プレビュー機能は`Visual Studio Code`の画面の右上`に虫眼鏡+本`のようなアイコンがあるとおもうのでそれをクリックします。

ただし、これは大雑把なプレビューで実際に表示されるものはこれとは異なります。

### デバッグビルド

デバッグビルドを使えば実際に表示される記事を確認できます。

`Visual Studio Code`のタブから`ターミナル`を選択し、`新規ターミナル`を選びます。

![](https://pbs.twimg.com/media/E5n3HpeVUAgY8ec?format=png)

するとウィンドウの下部に怪しげなウィンドウがひらきます。

そこで、

```sh
yarn install # 少し時間がかかりますが、最初の一回だけの入力で大丈夫です
yarn dev # 以後はこのコマンドのみを入力してください
```

あとはこの[デバッグビルド](http://localhost:3000)にアクセスすれば、実際にどんな記事が表示されるのかを確認できます。

## 執筆した記事を反映させる

執筆した記事を反映させるにはオリジナルの記事へのアクセス権限が必要です。

Twitter の DM で[@tkgling](https://twitter.com/tkgling)あてに GitHub アカウントの ID を教えていただくか[このコメント欄](https://github.com/tkgstrator/overfishing/issues/2)に一言コメントを頂ければ共同編集の権限を渡します。

### 記事をコミットする

![](https://pbs.twimg.com/media/E5nwL3gX0AImMAC?format=png)

コミットとは変更点などをまとめたドキュメントのようなものです。

記事が書けたら「新しく記事を書いた」という変更点を伝える必要があるわけです。

Sourcetree から`Commit`のボタンを押して変更点を大雑把にコメントしてください。

このとき、コミットメッセージは以下のように`半角ハイフン+半角スペース`から始めるようにしてください。

```
- 変更内容を箇条書き
```

コミットメッセージが書けたら保存して`Push`をクリックします。

`Push`先は必ず自分が作成したブランチのみを選択してください。

あとは OK を押せば自分の作業しているブランチが更新されます。

### オリジナルに反映する

ただこれでは自分が作業していた分が自分のブランチに反映されただけになります。

サイトに反映させるためには`master`と呼ばれるオリジナルのブランチに反映させなければいけません。そこで「私のブランチはオリジナルよりも優れているから、こちらの変更点をオリジナルに反映させてほしい」という要求が必要になります。

これがプルリクエスト(省略して PR とも呼ばれる)です。

プルリクエストは Sourcetree の左側のタブに表示されている`Branches`から自分が作業しているブランチを選択して右クリックしてから`Create Pull Request`を押します。

すると GitHub のページがひらくので、そこに先ほどと同じフォーマットで変更点をコメントします。

![](https://pbs.twimg.com/media/E5nzJ3iXMAww_QA?format=png)

最後に`Create pull request`をクリックすればオリジナルへの反映要求が申請されます。

その反映された内容を他の編集者がチェックし、ミスや間違いがなければ本サイトに反映されます。

## 二度目以降の作業

ただし、注意しなければいけない点があり、一つのファイルを複数の編集者が同時に編集する場合があります。

その時はコンフリクト(競合)が発生し、正しく変更点を反映できません。

なので、新たに編集する前に、

`git pull origin master --rebase`

を実行するようにしましょう。
