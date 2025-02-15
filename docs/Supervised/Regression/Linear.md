# 線形回帰とは

線形回帰は、説明変数（独立変数）と目的変数（従属変数）との関係をモデル化し、目的変数を予測するための統計手法です。データの傾向を直線で表現することが目的であり、回帰分析の中でも最も基本的な手法です。

---

## 1. 線形回帰モデルの概要

線形回帰モデルでは、以下のような式で説明されます：

y = b0 + b1 * x1 + b2 * x2 + ... + bn * xn + ε

- **y**: 目的変数（予測したい値）
- **x1, x2, ..., xn**: 説明変数（独立変数）
- **b0**: 切片（y軸と交わる値）
- **b1, b2, ..., bn**: 回帰係数（説明変数ごとの影響度）
- **ε**: 誤差（モデルで説明できない部分）

単回帰では説明変数が1つ、多重回帰では説明変数が複数になります。

---

## 2. 最小二乗法

線形回帰モデルでは、目的変数とモデルによる予測値との誤差を最小化するように係数を決定します。このとき使用されるのが**最小二乗法**です。

最小二乗法では、次のステップで係数を計算します：
1. 各データ点の誤差（残差）を計算します。
2. 残差の二乗和を求めます。
3. 残差の二乗和を最小化するように係数を調整します。

これにより、予測値と実際の値のズレが最小になるモデルを構築します。

---

## 3. 過学習と正則化

### 過学習とは？
**過学習**は、モデルが訓練データに対して過剰に適合してしまい、未知のデータに対する予測性能が低下する現象を指します。過学習が発生すると、以下のような問題が生じます：
- 訓練データでは非常に良い精度を示すが、新しいデータでは性能が悪い。
- モデルがデータのノイズや外れ値に過剰反応する。

### 正則化とは？
**正則化**は、過学習を防ぐためにモデルの複雑さを抑える手法です。線形回帰においては、回帰係数（b1, b2, ..., bn）の大きさを制限することで、モデルが極端なパラメータを持つことを防ぎます。

#### 主な正則化手法

1. **リッジ回帰（L2正則化）**
   - 回帰係数の二乗和にペナルティを課します。
   - 大きな回帰係数を抑えることでモデルの安定性を向上させます。

ペナルティ項 = λ * Σ(bi^2)

2. **ラッソ回帰（L1正則化）**
- 回帰係数の絶対値の和にペナルティを課します。
- 不要な説明変数の係数を0にすることで、特徴選択（次元削減）も可能です。

ペナルティ項 = λ * Σ|bi|

3. **Elastic Net**
- L1正則化とL2正則化を組み合わせた手法。
- 特徴選択とモデルの安定性のバランスを取るのに適しています。

ペナルティ項 = λ * (α * Σ|bi| + (1-α) * Σ(bi^2))

ここで、**λ**は正則化の強さを調整するハイパーパラメータで、値が大きいほどペナルティが強くなります。

---

## 4. モデルの評価指標

線形回帰モデルの精度を評価するために、以下の指標が用いられます。

### 決定係数（R²）
- **説明力**を示す指標で、値は0～1の範囲を取ります。
- 1に近いほどモデルの予測精度が高いことを意味します。

### 平均二乗誤差（MSE）
- 残差の二乗の平均を計算したもので、モデルの誤差を定量化します。
- 値が小さいほど良いモデルといえます。

---

## 5. 主な前提条件

線形回帰を適用する際には、以下の前提条件を確認することが重要です。

1. **線形性**: 説明変数と目的変数の関係が直線的であること。
2. **独立性**: データ点が互いに独立していること。
3. **等分散性**: 誤差の分散が一定であること。
4. **正規性**: 誤差が正規分布に従うこと。

---

## 6. 実際の適用例

線形回帰は、以下のようなケースで広く使われています：
- **不動産価格予測**: 広さや立地を説明変数に、価格を目的変数として予測。
- **売上予測**: 広告費用やプロモーション効果を基に、売上を予測。
- **健康診断のデータ分析**: BMIや運動習慣を基に、血圧値を予測。

---

## 7. メリットとデメリット

### メリット
- **実装が簡単**で計算コストが低い。
- 結果が直感的に解釈しやすい。

### デメリット
- 説明変数と目的変数が非線形な関係にある場合には適用が難しい。
- 外れ値や多重共線性に敏感。
- 過学習が発生しやすい場合がある。

---

線形回帰はシンプルでありながら強力な手法ですが、過学習を防ぐために正則化の使用を検討することが重要です。また、データの特性や目的に応じて適切な手法を選択しましょう。
