# カタパッドマップ

## カタパッドマップとは

カタパッドには`湧き方向`、`優先度`、`ポジショニング数`の三つの要素があります。

### 湧き方向

`湧き方向`とはどの方向から湧いたカタパッドかを指すパラメータです。

全てのステージ、潮位で湧き方向は三つあるので三通りあることになります。

### 優先度

同一湧き方向のカタパッドには`優先度`があります。優先度が高いカタパッドが存在しないのに、優先度が低いカタパッドが出現することは絶対にありません。

もし、優先度が低いカタパッドの出現位置がコンテナから遠くて倒しにいくのがめんどくさい場合には同一湧き方向の優先度が高いカタパッドをたおし続けることで優先度が低いめんどくさいカタパッドを出現しないようにすることができます。

また、優先度が二種類あるような場合にはその湧き方向に対してカタパッドが二体まで出現できるということになります。このようなとき、その湧き方向の`キャパシティ`が 2 であるというように表現することにします。

::: warning 優先度について

優先度が高いカタパッドをたおしつづければ、低いカタパッドはでてこないことになりますが、同時に出現するような場合には防ぐことができないので注意しましょう。

ただし、同時に出現する確率はそこまで高くないのであまり気にしなくても良いかもしれません。

:::

キャパシティが N の湧き方向に N+1 体目のカタパッドが出現しようとした場合、別の湧き方向の優先度が最も低い場所に出現することがわかっています。これを`代替カタパッド`と呼ぶことにします。

### ポジショニング数

`ポジショニング数`とはある位置に出現したカタパッドが何回位置を変えるかを表した数字です。ポジショニング数が 1 であるということは、その場から移動しないことを意味します。

あるポジショニングがコンテナに近いような場合には擬似的にカタパッドを寄せる、ということができるようになります。

## ステージごとのカタパッドマップ

### シェケナダム

![](https://pbs.twimg.com/media/EZyUl7kWoAA4EBT?format=jpg&name=4096x4096)

#### 満潮

|     湧き方向     |  1  |  2  |  3  |
| :--------------: | :-: | :-: | :-: |
|   キャパシティ   |  1  |  1  |  1  |
| ポジショニング数 |  1  |  1  |  1  |
|      代替先      |  2  |  1  |  1  |

どの方向もキャパシティが 1 のため、同じ方向にカタパッドが二体出現することはありえません。

最も遠いカタパッドである 3 湧きカタパッドは代替カタパッドになりえないのですが、3 湧きカタパッドをわざと片翼で放置すれば代替先が 1 湧きのため少したおしやすくなります。

#### 通常

|     湧き方向     |  1  |  2  |  3  |
| :--------------: | :-: | :-: | :-: |
|   キャパシティ   |  1  |  1  |  1  |
| ポジショニング数 |  4  |  2  |  2  |
|      代替先      |  2  |  1  |  2  |

通常潮位でもどの湧き方向もキャパシティが 1 しかないというステージ。これがシェケナダムを難しくしている理由の一つだと言えるでしょう。

というのも例えば A にカタパッドが出現しているときに A 湧きしてオオモノが複数体でてきたとき、そのオオモノの中にカタパッドがいればカタパッドだけが全く違う湧き方向に`代替カタパッド`として出現してしまうためです。

#### 干潮

|     湧き方向     |  1  |  2  |  3  |
| :--------------: | :-: | :-: | :-: |
|   キャパシティ   |  1  |  1  |  1  |
| ポジショニング数 |  2  |  2  |  2  |
|      代替先      |  2  |  1  |  1  |

こちらもどの湧き方向もキャパシティが 1 なのですが、見渡しやすいのでカタパッドを逃すことはないと思います。

代替先は 1 が多いので 1 方向を注意しておくと良いでしょう。

### 難破船ドン・ブラコ

### 海上集落シャケト場

![](https://pbs.twimg.com/media/EZyUl7lXkAEEitm?format=jpg&name=4096x4096)

#### 満潮

|     湧き方向     |  1   |  2   |  3   |
| :--------------: | :--: | :--: | :--: |
|   キャパシティ   |  2   |  2   |  2   |
| ポジショニング数 | 1, 1 | 1, 1 | 1, 1 |
|      代替先      |  2   |  1   |  1   |

#### 通常

|     湧き方向     |  1   |  2   |    3    |
| :--------------: | :--: | :--: | :-----: |
|   キャパシティ   |  2   |  2   |    3    |
| ポジショニング数 | 2, 3 | 2, 2 | 1, 1, 1 |
|      代替先      |  3   |  3   |    -    |

3 湧きはキャパシティが 3 のため代替カタパは存在しません。

#### 干潮

|     湧き方向     |  1  |  2  |  3  |
| :--------------: | :-: | :-: | :-: |
|   キャパシティ   |  1  |  1  |  1  |
| ポジショニング数 |  2  |  2  |  2  |
|      代替先      |  2  |  3  |  2  |

厄介な真ん中の 2 湧きカタパは放置すれば 3 湧きに代替カタパがでておいしいので敢えて真ん中のカタパは片翼で放置するというのも戦略の一つ。

わざわざ意味もなく残す意味はないが、三つのカタパッドの中で最も処理する目標として優先度が低いのは間違いないです。1 湧きと 3 湧きのカタパッドはたおせばたおすだけ納品数が増えるので積極的に処理したい。

### トキシラズいぶし工房

![](https://pbs.twimg.com/media/EZyTX9uXYAADLRT?format=jpg&name=4096x4096)

#### 満潮

|     湧き方向     |    1    |    2    |    3    |
| :--------------: | :-----: | :-----: | :-----: |
|   キャパシティ   |    3    |    3    |    3    |
| ポジショニング数 | 1, 1, 1 | 1, 1, 1 | 1, 1, 1 |
|      代替先      |    -    |    -    |    -    |

どの湧き方向もキャパシティが 3 なので代替カタパはなし。対岸カタパは湧き方向の偏りもあってコンテナ側よりも倍以上出現しやすい。対岸のカタパッドはたおせるならどんどんたおしていこう。

#### 通常

|     湧き方向     |  1   |  2  |  3   |
| :--------------: | :--: | :-: | :--: |
|   キャパシティ   |  2   |  1  |  2   |
| ポジショニング数 | 2, 2 |  3  | 2, 2 |
|      代替先      |  2   |  1  |  1   |

最も近い 1 湧きへの代替カタパッドが多いため、ちょっと処理が遅れるとガンガンコンテナ横にカタパッドが出現します。

1 湧きカタパッドが 2 湧きへ代替カタパッドとして出現すると、横へスライドしながらとんでいく不思議なカタパッドが見れます。

#### 干潮

|     湧き方向     |  1  |  2  |  3  |
| :--------------: | :-: | :-: | :-: |
|   キャパシティ   |  1  |  1  |  1  |
| ポジショニング数 |  4  |  3  |  3  |
|      代替先      |  3  |  3  |  1  |

1 湧きカタパッドは実際にプレイしてみると二回しか移動しているように見えないのだが、内部的にはポジショニング数は 4 になっていて謎が多い。

### 朽ちた箱舟 ポラリス