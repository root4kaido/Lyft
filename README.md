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

