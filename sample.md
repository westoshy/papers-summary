# Road Damage Detection Using Deep Neural Networks with Images Captured Through a Smartphone
## Hiroya Maeda et al. University of Tokyo, arXiv:1801.09454 (2018)

<img src="dummy.png" alt="image area" width=100% height=200>

.left-column[
### 要旨
スマートフォンで撮影された画像を入力して路面の劣化領域を検出するDeep Neural Networkの提案を行い，路面劣化画像のデータセットを整備している．ネットワークはSDDを用いており，既存データセットではなく，自前のデータセットにて学習・評価を実施している．
### 先行手法との差
従来は専用のデータセットを用意してDeep Neural Networkを学習し，適用する際にもきれいな画像を用意する必要があった．しかし実運用の観点ではスマートフォンなどの普及型のカメラを使用することが考えられる．そこで実運用面を考慮したニューラルネットワークの構築を試みている．また，学習に用いるデータベースを公開している．
### 提案技術の要点
ネットワーク構造については従来研究でstate-of-the-artの結果を出している物体検出手法であるSSDを用いている．特にスマートフォン環境での実運用を考えているためCPU負荷を意識した選択をしている．路面ダメージの種類に応じて8つのクラスに分類されるようなネットワークの構成をとっている．
]

.right-column[
### 検証方法
OSはUbuntu 16.04 NVIDIA GRID K520 GPU(15GB RAM Memory)を学習環境としている．また，定量評価指標としてはIOU(Intersection Of Union)を採用している．推論は学習と同様のPC環境とNexus 5X smartphone(MSM8992 CPU and 2 RAM GB memory)の2ケース行っている．SDD Inception V2の推論速度はMobileNetの約半分であった．

### 議論/考察
新しい道路においても活用できる．再現率，適合率で75%以上，スマートフォンアプリでの推論速度1.5secを実現した．将来的にはデータセット内で稀なタイプの劣化に対しても対応できるように手法を改良したい．

### コメント/関連資料
物体検出のデータセットにないクラスを検出しようとしたときに新たにデータセットを整備して既存手法を適用することで良い精度が出せるというモチベーションになる報告である．
- [論文リンク](https://arxiv.org/abs/1801.09454)　[(codes)](https://github.com/sekilab/RoadDamageDetector/)
- [Road crack detection using deep convolutional neural network, ICIP 2016](https://ieeexplore.ieee.org/abstract/document/7533052/)
]

---
# slide 2
test