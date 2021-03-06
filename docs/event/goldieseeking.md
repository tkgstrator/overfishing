# キンシャケ探し

一部のステージを除いて最も納品数を伸ばすことができるポテンシャルを持ったイベントです。

## 基本情報

### カンケツセン

カンケツセンの開栓にかかるダメージは 100 であるが、いくつかの攻撃には特別な`一撃判定`があるため、ダメージに関わらず一発で開栓することができます。

例えば、カーボンローラーの轢きダメージは 60 ですが一撃判定があるため一回で開栓することができます。パブロ・ホクサイの轢き、ジェットパックの攻撃も同様に一撃判定があります。

### キンシャケ

キンシャケは残り HP がある値を下回ると金イクラを 1 つドロップし、撃破すればそれとは別に 3 つの金イクラをドロップする。

<!-- |   HP   | サイズ  | 総ドロップ数 |
| :----: | :-----: | :----------: |
|  6500  |   大    |      0       |
|  6000  |   大    |      1       |
|  5500  |   大    |      2       |
|  5000  |   大    |      3       |
|  4500  |   大    |      4       |
|  4000  | 大 → 中 |      5       |
|  3600  |   中    |      6       |
|  3200  |   中    |      7       |
|  2800  |   中    |      8       |
|  2400  |   中    |      9       |
|  2000  | 中 → 小 |      10      |
| 1666.7 |   小    |      11      |
| 1333.4 |   小    |      12      |
| 1000.1 |   小    |      13      |
| 666.8  |   小    |      14      |
| 333.5  |   小    |      15      |
|   0    |   小    |      18      | -->

::: warning キンシャケの HP

ただし、1F 以内に金イクラを 2 つ以上ドロップするようなダメージを与えても、金イクラは 1 つしかドロップしないため総ドロップ数が減ってしまう。

極端な話をすれば 6500 ダメージを一気に与えると 1 つ+撃破ボーナスの 3 つで合計 4 つの金イクラしか得られない。スーパーチャクチ(700 ダメージ)やリッターのフルチャージ(600 ダメージ)については注意が必要である。

:::

## 開栓手順

キンシャケ探しイベントが最も稼げるイベントであるため、カンケツセンの最良の手順は長らく研究されている。

その中でも最もオーソドックスと思われる手順をここでは紹介する。今回紹介する手順は「平均的に」最も稼ぎやすいと思われる手順であるが、上振れを狙うのであれば遠くからあけていては間に合わないような場合には、敢えて近くからあけていく臨機応変さも必要とされる。

## インデックスバグ

イカ研究所の不適切な乱数生成器の初期化のため、WAVE1 限定ではあるもの開栓するカンケツセン数を減らすテクニックが存在します。

### 通常

WAVE1 の通常潮位でキンシャケ探しにおける各ステージでの初手のアタリ位置の確率の表です。

どのステージでも A のカンケツセンは 100%ハズレになります。

|     | シェケナダム | ドンブラコ | シャケト場 | トキシラズ | ポラリス |
| :-: | :----------: | :--------: | :--------: | :--------: | :------: |
|  A  |   0.0000%    |  0.0000%   |  0.0000%   |  0.0000%   | 0.0000%  |
|  B  |   12.2175%   |  13.6241%  |  12.2175%  |  16.3615%  | 16.3615% |
|  C  |   12.2274%   |  14.1779%  |  12.2274%  |  17.0888%  | 17.0888% |
|  D  |   12.4400%   |  14.4848%  |  12.4400%  |  17.4402%  | 17.4402% |
|  E  |   12.6129%   |  14.6779%  |  12.6129%  |  20.5351%  | 20.5351% |
|  F  |   12.7169%   |  18.0336%  |  12.7169%  |  14.2890%  | 14.2890% |
|  G  |   15.5655%   |  12.5000%  |  15.5655%  |  14.2855%  | 14.2855% |
|  H  |   11.1076%   |  12.5017%  |  11.1076%  |     -      |    -     |
|  I  |   11.1121%   |     -      |  11.1121%  |     -      |    -     |

|   ステージ   |                                                                                                                                     |
| :----------: | :---------------------------------------------------------------------------------------------------------------------------------: |
| シェケナダム |                                                           有効活用法なし                                                            |
|  ドンブラコ  |                                                           有効活用法なし                                                            |
|  シャケト場  |                                                           有効活用法なし                                                            |
|  トキシラズ  | [C 小、D 大なら A をとばして E 開け](https://video.twimg.com/ext_tw_video/1436672798554923008/pu/vid/1280x720/re66jiaWrAp-kyCA.mp4) |
|   ポラリス   |                                                           有効活用法なし                                                            |

### 満潮

WAVE1 の満潮でキンシャケ探しにおける各ステージでの初手のアタリ位置の確率の表です。

どのステージでも最も若いインデックスのカンケツセンは 100%ハズレになります。

|     | シェケナダム | ドンブラコ | シャケト場 | トキシラズ | ポラリス |
| :-: | :----------: | :--------: | :--------: | :--------: | :------: |
|  A  |      -       |     -      |  0.0000%   |     -      |    -     |
|  B  |      -       |     -      |  28.4996%  |     -      |    -     |
|  C  |      -       |     -      |     -      |  0.0000%   |    -     |
|  D  |      -       |     -      |     -      |  28.4996%  | 0.0000%  |
|  E  |   0.0000%    |  0.0000%   |     -      |  31.4996%  | 50.0145% |
|  F  |   28.4996%   |  50.0145%  |     -      |  19.9962%  | 24.9789% |
|  G  |   31.4996%   |  24.9789%  |  31.4996%  |  20.0045%  | 25.0067% |
|  H  |   19.9962%   |  25.0067%  |  19.9962%  |     -      |    -     |
|  I  |   20.0045%   |     -      |  20.0045%  |     -      |    -     |

また、ドンブラコとポラリスにおいてはそれぞれ F と E に本来のアタリ位置の確率が足される異常事態が発生しています。

|   ステージ   |                                                                                                                                                     |
| :----------: | :-------------------------------------------------------------------------------------------------------------------------------------------------: |
| シェケナダム |                                                                   有効活用法なし                                                                    |
|  ドンブラコ  |                                                                   有効活用法なし                                                                    |
|  シャケト場  |    [同じところは二連続アタリにならないことを利用](https://video.twimg.com/ext_tw_video/1421774431970500610/pu/vid/1280x720/9KS--vwfSOc_R69A.mp4)    |
|  トキシラズ  |                                                                    参考資料なし                                                                     |
|   ポラリス   | [二回目と三回目は同じアタリ位置にならないことを利用](https://video.twimg.com/ext_tw_video/1414258079269457920/pu/vid/1280x720/91lCgegFcC4zybDM.mp4) |

### 連続しないアタリ位置

満潮の場合はドンブラコとポラリス以外では初手と二手目は必ず違う位置がアタリになります。また、三連続同じ位置がアタリになることはありません。

| 潮位 |           初手           |          二連続          | 三連続 |
| :--: | :----------------------: | :----------------------: | :----: |
| 通常 |          A 以外          |          A 以外          | A 以外 |
| 満潮 | 最も若いインデックス以外 | ドンブラコとポラリスのみ | しない |

## カンケツセン内部 ID 表

カンケツセンの内部 ID とステージごとの各アタリ位置におけるゴール位置のリストを掲載しました。

より直感的に理解したい方は[Salmon Learn](https://gungeespla.github.io/salmon_learn/)で水脈を確認しながらチェックすると良いでしょう。

::: warning アルファベット表記について

本ドキュメントでは内部 ID を元にしたアルファベットで表記しています。Salmon Learn やその他のアルファベット表記とは異なるので注意。

:::

### シェケナダム

![](https://pbs.twimg.com/media/FDh_VGxaMAA3rj3?format=png)

| 通常 |  1  |  2  |  3  |  4  |
| :--: | :-: | :-: | :-: | :-: |
|  A   |  F  |  G  |  D  |  C  |
|  B   |  E  |  F  |  C  |  I  |
|  C   |  E  |  D  |  H  |  G  |
|  D   |  C  |  A  |  -  |  -  |
|  E   |  C  |  H  |  B  |  -  |
|  F   |  A  |  G  |  H  |  B  |
|  G   |  F  |  C  |  A  |  -  |
|  H   |  I  |  C  |  E  |  F  |
|  I   |  H  |  B  |  A  |  -  |

| 満潮 | 1   | 2   | 3   | 4   |
| ---- | --- | --- | --- | --- |
| E    | H   | -   | -   | -   |
| F    | G   | H   | -   | -   |
| G    | F   | -   | -   | -   |
| H    | I   | F   | -   | -   |
| I    | H   | G   | -   | -   |

### 難破船ドン・ブラコ

<!-- ![](https://pbs.twimg.com/media/FDhs2wyacAA1ZSL?format=png) -->

### 海上集落シャケト場

![](https://pbs.twimg.com/media/FDh_VGxaIAAgbu4?format=png)

### トキシラズいぶし工房

![](https://pbs.twimg.com/media/FDh_VGyagAAl8s2?format=png)

### 朽ちた箱舟 ポラリス

![](https://pbs.twimg.com/media/FDh_VGyaMAAWduY?format=png)
