# Lyft

https://www.kaggle.com/c/lyft-motion-prediction-autonomous-vehicles/overview/description

<img src="https://github.com/root4kaido/Lyft/blob/master/Material/Screenshot%20from%202020-09-21%2022-39-20.png" width=75%><img src="https://github.com/root4kaido/Lyft/blob/master/Material/BP9I1484%20(1).jpg"  width=25%>
自動運転に関するコンペ．車(自分)の周りのオブジェクトの動きを予測する．おもしろそう！ 11/26まで．

- MLflowで実験管理したい．

| Notebook | Contents |
| ------ | ------ |
| [0921.ipynb](https://github.com/root4kaido/Lyft/blob/master/0921.ipynb) | zarrの中身を見る．とりあえず，sampleの，agentを確認． |
| [0922.ipynb](https://github.com/root4kaido/Lyft/blob/master/0922.ipynb) | zarrの中身を見る．scene, frame, trafficを確認．visualizeもした． |
| [0922.ipynb](https://github.com/root4kaido/Lyft/blob/master/0922_2.ipynb) | training_templateを作成した．(途中) |
| [0923.ipynb](https://github.com/root4kaido/Lyft/blob/master/0923.ipynb) | trainin_templateの続きを作成． |
| [0924.ipynb](https://github.com/root4kaido/Lyft/blob/master/0923.ipynb) | trainin_templateの続きを作成． |
| [0924.ipynb](https://github.com/root4kaido/Lyft/blob/master/0924.ipynb) | inference_templateを作成． |
| [0924_2.ipynb](https://github.com/root4kaido/Lyft/blob/master/0924_2.ipynb) | mlflowの，training_templateを作成． |
| [0925.ipynb](https://github.com/root4kaido/Lyft/blob/master/0925.ipynb) | ラスタサイズと，epoch，データ量の変更|
| [0926.ipynb](https://github.com/root4kaido/Lyft/blob/master/0926.ipynb) | inferenceだけで自信度出せるか検討→無理 |
| [0926_2.ipynb](https://github.com/root4kaido/Lyft/blob/master/0926_2.ipynb) | マルチなモデルと，lossを変更したtraining |
| [0927.ipynb](https://github.com/root4kaido/Lyft/blob/master/0927.ipynb) | ラスタサイズとか，ピクセルサイズとか変えた．pretrainをやめた． |
| [0928.ipynb](https://github.com/root4kaido/Lyft/blob/master/0928.ipynb) | resnet18→34 |
| [0929.ipynb](https://github.com/root4kaido/Lyft/blob/master/0929.ipynb) | train_loader5000ごとに評価するよう変更 |
| [1001_2.ipynb](https://github.com/root4kaido/Lyft/blob/master/1001_2.ipynb) | ベースモデルを回した |
| [1003.ipynb](https://github.com/root4kaido/Lyft/blob/master/1003.ipynb) | l5kitをカスタムした．最後のRGBを削ってみた． |
| [1004.ipynb](https://github.com/root4kaido/Lyft/blob/master/1004.ipynb) | ? |
| [1004_2.ipynb](https://github.com/root4kaido/Lyft/blob/master/1004_2.ipynb) | l5kitをカスタムした．最後のRGB以外を削ってみた． |
| [1005.ipynb](https://github.com/root4kaido/Lyft/blob/master/1005.ipynb) | validのノートブック． |
| [1005_2.ipynb](https://github.com/root4kaido/Lyft/blob/master/1005_2.ipynb) | ベースモデルpart2 |
| [1005_3.ipynb](https://github.com/root4kaido/Lyft/blob/master/1005_3.ipynb) | validで使うデータセットを作った． |
| [1006.ipynb](https://github.com/root4kaido/Lyft/blob/master/1006.ipynb) | ベースモデルpart3 |
| [1006_2.ipynb](https://github.com/root4kaido/Lyft/blob/master/1006_2.ipynb) | l5kitをカスタムした．最後のRGBを削ってみた．part2 |
| [1006_3.ipynb](https://github.com/root4kaido/Lyft/blob/master/1006_3.ipynb) | 画像サイズを変えずに，俯瞰の高さを上げた． |
| [1007.ipynb](https://github.com/root4kaido/Lyft/blob/master/1007.ipynb) | trainもvalidみたいにデータ選んだ |
| [1007_2.ipynb](https://github.com/root4kaido/Lyft/blob/master/1007_2.ipynb) | 上記のデータで学習 |
| [1007_3.ipynb](https://github.com/root4kaido/Lyft/blob/master/1007_3.ipynb) | ポイントネット解読 |
| [1007_4.ipynb](https://github.com/root4kaido/Lyft/blob/master/1007_4.ipynb) | ベースにtorchsummary |
| [1007_5.ipynb](https://github.com/root4kaido/Lyft/blob/master/1007_5.ipynb) | resnestにしてみた |
| [1008.ipynb](https://github.com/root4kaido/Lyft/blob/master/1008.ipynb) | モバイルネットv2 |
| [1008_2.ipynb](https://github.com/root4kaido/Lyft/blob/master/1008_2.ipynb) | 画像サイズ2倍 |
| [1009.ipynb](https://github.com/root4kaido/Lyft/blob/master/1009.ipynb) | ？ |
| [1009_2.ipynb](https://github.com/root4kaido/Lyft/blob/master/1009_2.ipynb) | resnet50 |
| [1010.ipynb](https://github.com/root4kaido/Lyft/blob/master/1010.ipynb) | ベースモデルたくさん回そうと思っているやつ |
| [1011.ipynb](https://github.com/root4kaido/Lyft/blob/master/1001.ipynb) | バリデーション見ようと思ったやつ |
| [1011_2.ipynb](https://github.com/root4kaido/Lyft/blob/master/1011_2.ipynb) | メトリックできたやつ． |
| [1011_3.ipynb](https://github.com/root4kaido/Lyft/blob/master/1011_3.ipynb) | アンサンブルcsvためしている |
| [1011_4.ipynb](https://github.com/root4kaido/Lyft/blob/master/1011_4.ipynb) | モバイルネットv3 |

論文
| url | name |
| ------ | ------ |
| [url](https://arxiv.org/pdf/1809.10732.pdf) | マルチモーダル予測 |
| [url](https://papers.nips.cc/paper/2019/file/757f843a169cc678064d9530d12a1881-Paper.pdf) | confidenceの改善 [ソース](https://github.com/valeoai/ConfidNet) |
| [url](https://openaccess.thecvf.com/content_CVPR_2020/papers/Marchetti_MANTRA_Memory_Augmented_Networks_for_Multiple_Trajectory_Prediction_CVPR_2020_paper.pdf) | かえるさんが貼ったやつ |
| [url](https://arxiv.org/pdf/1910.03650.pdf) | よくわからん |
| [url](https://arxiv.org/pdf/2005.04259.pdf) | VectorNet |
| [url](https://arxiv.org/pdf/1906.08469.pdf) | モバイルネット改良 |
| [url](https://arxiv.org/pdf/1808.05819.pdf) | マルチモーダル予測に，LSTMとか加えてる |
| [url](https://engineering.mercari.com/blog/entry/2018-04-24-164919/) | メルカリのマルチモーダル予測 |

- データセットの説明
https://github.com/lyft/l5kit/blob/master/data_format.md


---
09/20

データ落とした．

---
09/21

データ見てみた．zarrとかいうわけわからんのが本体と，地図で構成されている．

https://www.kaggle.com/kool777/lyft-level5-eda-training-inference#notebook-container \
↑マジ有能イケメンノートブック．これでなんとかzarrの取扱いわかりそう．

__sample,train,validate,testは，それぞれagents, agents_mask, frames, scenes, traffic_light_facesで構成されているっぽい．__

0921.ipynbで，とりあえずagentの中身を見た．
### 発見
- agentはなんかいろんな物体で，そのときの __位置，大きさ，速度，回転，ラベル__ が入っている．
- ラベルは，3種類と，不明(←これが多い)の4種類しかない！→とおもったけどこれはsampleのはなし．

---
09/22

0922.ipynbで，引き続き残りのデータを見た．
### 発見
- sceneは，host(収集した車)関係のデータ
- framは，hostの位置とか，回転とか，より詳細のデータ
- traffic lightは，信号機のデータ
- visualizeは色々できそう．まだよくわかってない．衛星写真と，よくわからないの二種類．

0922_2.ipynbで，training_templateを見た． \
所感，結構学習の仕方が違う．データセットの作り方はに種類ある．agentと，ego． \
egoは，なんか固定される．agentは，視点が動いた．

epochっていう感じじゃないのかな？？
CPUの数は0じゃないとすーぐメモリ死ぬので注意．

---
09/23

0923.ipynbで，とりあえずtraining回した． \
やっぱり，データ数が多すぎ．ただ，templateの人も，batch32:itr25000で，スコア130位出していた． \
まだ，実験の仕組みは整えていないので，一回提出した後に，作る．

---
09/24

0924.ipynbで，inferenceしてみた．→できたので，提出してみた．推論の時間バカ長い．スコアは，260くらい．データ少ないのが原因かな多分． \
0924_2.ipynbで，mlflowを組み込んだtraining作成．ちなみに，モデルのpretrainをtrueにした．これをベースにする予定． \
あと，PANDAのsolutionを聴講したので，時間あるときに気になったものを深堀する．

---
09/25

0925.ipynbで，ラスタサイズを224→448，またepoch数を減らして使うデータセットの数を増やした． \
confidenceは，inferenceだけで出せるような気がしたので，試す．

---
09/26

0926,0926_2.ipynbで，マルチ予測モデルを作った．また，lossを評価指標に合わせた．

---
09/27

0926_2.ipynbは，pretrainedを使っていた．これ，10epoで実験した結果，falseのほうが良さそう(画像サイズ224じゃないので，それはそう)
左が，pretrainなし．右が，pretrain \
<img src="https://github.com/root4kaido/Lyft/blob/master/Material/loss_nopre.png" width=25%><img src="https://github.com/root4kaido/Lyft/blob/master/Material/loss_pre.png" width=25%>

0927.ipynbで，ラスタサイズとピクセルサイズをいいかんじにしたものをtraining． \
やはり，まだagentとegoのちがいがよくわかっていない．dataloaderから取れてくるものは，画像だけではない．

---
09/28

0927.ipynbがよくなかった．謎． \
一回，いいスコアが出るはずの[ノートブック](https://www.kaggle.com/corochann/lyft-prediction-with-multi-mode-confidence/data)を回してみる． \
鍵は全データを使うことかもしれない． 

0928.ipynbは，モデルを変更したもの．

---
09/29

resnetは，18より34のがスコア良い． \
また，上記良いスコアが出るはずのものを一日回して提出したら，スコア85がでた．やはり，大量のデータをどう使うかが鍵． \
だが，一日回してまだ1/8くらいのデータしか使えていない… \
0929.ipynbは，とりあえず1/4のデータを2epoch回してみる．

---
09/30

昨日回したものは，引き続き回している． \
OpenGLを使ったラスタ化の高速化検討をしてみたが，そもそもGPUも資源少ないのと，OpenGLがインストールできなかったので断念． \
画像を保存したほうがまだ良さそう．

---
10/01

色々ごちゃごちゃになってきた． \
__とりあえず，ベースをちゃんと作ろう__

条件は，こんな感じ
- 使うデータは，trainの1/20
- 画像サイズは224
- pretrainあり
- resnet34
- マルチモデル(自信度あり)
- epoch2
- trainは，バッチサイズ32で，500ごとにバリデーションとlr変更
- validはバッチサイズ12で100イテレーション

1001_2.ipynbで上記ベース回し中．

画像サイズ，resnetの大きさ，スケジューラーらへんは一気に回せそうなので，ためす．

---
10/02

- ミスってしまったため，ベースを今回している最中．サブできなかった．
- scale GANの論文を読んだが，なかなか難しそう…
- l5kitを落としてきて，l5kitcustomを作った． \
1003.ipynbで，RGBなしの22チャンネルの入力を作って，回している．

---
10/04

- ベースをサブしたら，90くらいだった．
- 1003.ipynbをサブしたら，13000くらいの値が出てしまった．意味わからん．
- だったら，RGBの影響が強いのか？？と思ったので，この3チャンネルのみで1004_2.ipynbを回している．

---
10/05, 10/06

- 上記意味わからん原因がわかった．l5kitのバージョンアップに伴い，予測するときに座標の変換が必要になるよう．これを直して，ベースモデル(1005_2.ipynb)のスコアは65くらいだった．
- 1006_3.ipynbで，画像サイズを変えずに，俯瞰の高さを上げた(より多くのオブジェクトが入る)ものを回している．

---
10/07

- ベースモデル(1006.ipynb)で，46でた！！！！
- 1007.ipynbでtrainもvalidみたいにデータ選んでみた．
- 1007_2.ipynbで上記のデータで学習中．
- 1007_3.ipynbで，ポイントネット解読中．データセットの作り方が参考になりそう→social ganとかにつかえる？
- 1007_4.ipynbでtorchsummary
- 1007_5.ipynbで，resnestにしてみた．上と，あまりパラメータ数変わらんかった．

---
10/08

- resnestはだめだった．パラメータ多すぎ？
- 1007_5.ipynbはおしかったが，ベースを超えられず．
- ということで，1008.ipynbで，モバイルネットを試している．
- 1008_2.ipynbで，画像サイズを二倍にしてみた．

---
10/09

- モバイルネットは，なんかスコア上がった！！！44
- クリエイトチョップはきく可能性あるかもしれん．
- 1009_2.ipynbで，resnet50を回している

---
10/10

- 1010.ipynbでベースをたくさん回すんだ

---
10/11

- 1011.ipynbでバリデーション見ようとした．
- 1011_2.ipynbで，公式の予測[ノートブック](https://github.com/lyft/l5kit/blob/master/examples/agent_motion_prediction/agent_motion_prediction.ipynb)をためした．
結果，モバイルネット，画像center(0.75, 0.75)，ベースの順番でよかった．(0.48, 0.55, 0.68)
- 1011_3.ipynbで，アンサンブルしてみたが，あまり良くなかった．
- 1011_4.ipynbで，モバイルネットv3を試し中．

---
10/12

- 1010.ipynbをだしたら，まさかの20代になった．
- 1011_4.ipynbは，ベースよりは良さそうだったがモバイルネットv2のほうがよさそう
- 1012.ipynbで，モバイルネットv2+center(0.75, 0.75)を無限に回してみる．

---
10/13

- アイデアをだしたり，論文読んだりしながら，1010と1012を見守っている．
- 1010で，37位に入った．

---
10/14,15

- 1010で，30位に入った．
- ラスタを変更した．1015.ipynbで，軌跡をわけずに，色の濃淡で表現してみた．

---
10/16

- 1016.ipynbで，自信度が0.9を超えている場合，他を０にできんじゃね？と思ってやってみたが意味なし．
- 1016_2.ipynb，1016.ipynbで，1015.ipynbのラスタの要素の大きさを変えてやってみた．いま回し中．

---
10/17

- 上の結果を確認したら，ラスタは小さいほうが良いかも．
- 1017.ipynb　色の濃淡のパラメータを変えた．ちょっとよくなったけど，ため．
- 1017_2.ipynbで，ベースモデルでラスタを小さくして，0.5→0.75にした．
- 1017_3.ipynbで，自信度とエラー率がどうなっているかなどを探った．
- 1017_4.ipynbで，サブミットをこねくり回したが，あまり変わらず．
- 1017_2.ipynbがうまくイカなかった．1017_5.ipynbで，ベースモデルで0.5→0.75にして回し中．

---
10/18

- 1017_3.ipynbで，またこねくりまわしていた．
- 1018.ipynbで，ラスタを全部にして回し中．

---
10/19

- やっぱベクトルベースを頑張ろうかなと言う気持ちになった．目標，VetcoreNet
- 1019.ipynbで，pointnetこねくりまわした．
- 1019_2.ipynbで，モバイルネット沢山回し中．

---
10/20

- やってしまった…lr=5e-4で回していた…　重要そうなのだけやりなおす…1017_5.ipynbとか．あと1018.ipynbと，エージェントちっさくしたやつ．
- 1019.ipynbでなんとかpointnetまわしている．

---
10/21

- 1021.ipynbでポイントネットを評価したが，新しいやつを適用できない…
- 1021_2.ipynbは，その努力の跡．

---
10/22

- ポイントネットの評価ができなあああああああああああａｉ
- ノートブックに質問してみた…優しい世界であってくれ
- 1022.ipynbでmovilenetもっかい！


---
10/23~25

- 1024でべくたーをいろいろいじろうとしたけど，むりだ…
- 1025で画像を大きくしたけど，なぜかうまくいかない．
- 1025_2で，速度などの情報をつけたしてみた．

---
10/26

- 1026はカスタムのデータセットを回したよ
- 1026_2はカスタムじゃないl5kitだよ
- 1026_3はマップをそのたわけてconcat

---
10/27

- 1027で，train_fullお試し中．
- 1026_2で，lrをかえておためしちゅう．

---
10/28,29

- 1028で，shufflenetv2を試し中．

---
11/1

- 1101で，動いてないのをしっかり0にできればじゃっかんスコア伸びることを発見
- 1101_2で，動いてる/動いてないスコア分類回し中

---
11/02,03

- 1102で，距離が遠いほど，lossに重みをつけて学習回し中．

---
11/04

- 1104で，grandじゃなくて予測に対して1以下だったら0にする，を試したけどだめ．
- 1104_2で，アンサンブルのために，まず軌道が似ているをどう判定するか検討中．

---
11/05

- 1105で，ローパスきくんじゃね？とおもってためした．ちょっとよくなった．
- 1105_2で，テストにも適用して，サブミット．半月ぶり．
- 1105_3で，アンサンブルに向けまたこねくりまわし．

---
11/06

- 1105_3で，アンサンブル試してみた．
でも長さだけで類似度取っちゃさすがに安直すぎるわねっておもったけどスコアのびたWWWWWW
これはやってみてもいいかもしれん．


---
11/07

- アンサンブルはなんとなくいけそう．長さだけで類似度とってもそれっぽくなった．
1022と，1028に関しては，スコアの比はとらずに，距離はth15がよさそう．
上記のアンサンブルと1010は，スコアの比の10倍をconfにかけ，距離はth30がよさそう．
また，1022を1107inference，1028を1107inference2で提出しといた一応．


---
11/08,09
- 1109で，速度付け加え
- 1109_2で，ちょっとconfいじったが，あまり意味なさそう…

---
11/10,11

- 1111で，バリデーションをtrainにしてまわしはじめた

---
11/12

- おいのりをした．

---
11/13

- モードを増やして，アンサンブルのやつ使えば伸びるのでは！？！？！GPUあいてないので，実装はあした．

---
11/14

- モードを増やしてみた．1114_3.ipynbで．
- 1114.ipynbで1109_2を．1114_2.ipynbで1109でスコア出してみたら，1112_4は25だったのでつづける．

---
11/15

- 1115で7モードのスコア出した．1115_2で，アンサンブルでどうなるか試したけど，二倍くらい悪くなっちゃったねえ

---
11/16

- チームマージのお誘いきたけどこっちになんもメリットなさそうなのでグッバイ

---
11/17, 8

- 1109が21.7くらいでたので，1010とアンサンブルしたら，21.08くらいになった．でも，モデルが更新されてしまった…

---
11/19~21

- 1120で，7モードの推論
- 1120_2で，7モードとのアンサンブル．うまくいかず．
- 1121で，アンサンブルきれいバージョン
- 1121_2で，テストデータのアンサンブル
