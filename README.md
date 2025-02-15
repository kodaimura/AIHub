# MLHub

## [教師あり学習 (Supervised Learning)](https://github.com/kodaimura/AIHub/blob/main/docs/Supervised/README.md)
目的：**ラベル付きデータ**を使って学習し、予測や分類を行いたいとき
- **回帰 (Regression)**: 連続的な値（例：価格予測、株価予測）を予測したいとき
- **分類 (Classification)**: カテゴリカルなラベル（例：スパムメール分類、画像分類）を予測したいとき

## [教師なし学習 (Unsupervised Learning)](https://github.com/kodaimura/AIHub/blob/main/docs/Unsupervised/README.md)
目的：**ラベルなしデータ**からパターンや構造を学習したいとき
- **クラスタリング (Clustering)**: データを似た特徴を持つグループに分けたいとき（例：顧客セグメンテーション、異常検知）
- **次元削減 (Dimensionality Reduction)**: 高次元データを低次元に圧縮して、データの可視化や計算量削減を行いたいとき（例：PCAを用いてデータを可視化）

## [半教師あり学習 (Semi-Supervised Learning)](https://github.com/kodaimura/AIHub/blob/main/docs/Semi-Supervised/README.md)
目的：少量のラベル付きデータと大量のラベルなしデータを活用して学習したいとき
- **自己教師あり学習 (Self-Training)**: ラベル付きデータが少なく、ラベルなしデータを活用して予測モデルを訓練したいとき
- **ラベル伝播法 (Label Propagation)**: ラベル付きデータとラベルなしデータを使い、ラベルを伝播させて分類を行いたいとき
- **ラベル拡張法 (Label Spreading)**: ラベル付きデータから情報を拡張して、ラベルなしデータに対して予測を行いたいとき

## [強化学習 (Reinforcement Learning)](https://github.com/kodaimura/AIHub/blob/main/docs/Reinforcement/README.md)
目的：エージェントが環境とのインタラクションを通じて最適な行動を学習したいとき
- **モデルフリー (Model-Free)**: 環境のモデルが不明で、試行錯誤で学習を進めたいとき（例：Q-learning、Deep Q-Network）
- **モデルベース (Model-Based)**: 環境のモデルを構築して、最適な行動を予測したいとき（例：動的計画法）
- **深層強化学習 (Deep Reinforcement Learning)**: 複雑な環境において深層学習を活用して、行動方針を学習したいとき（例：ゲームAI）

## [深層学習 (Deep Learning)](https://github.com/kodaimura/AIHub/blob/main/docs/Deep/README.md)
目的：多層のニューラルネットワークを使用して、より高度な予測や分類を行いたいとき
- **畳み込みニューラルネットワーク (CNN)**: 画像データの解析（例：画像分類、物体検出）を行いたいとき
- **リカレントニューラルネットワーク (RNN)**: 時系列データやシーケンスデータ（例：音声認識、自然言語処理）を扱いたいとき
- **トランスフォーマー (Transformers)**: 大規模な言語モデル（例：GPT、BERT）を使用して、自然言語処理タスク（例：機械翻訳、テキスト生成）を行いたいとき
