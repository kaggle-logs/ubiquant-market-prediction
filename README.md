# Introduction

## 概要

投資戦略にかかわらず、金融市場には変動がつきもの。
この変動にもかかわらず、プロの投資家は全体的なリターンを推定しようとする。
リスクとリターンは投資の種類やその他の要因によって異なり、安定性とボラティリティに影響を及ぼします。
リターンの予測を試みるために、金融市場の取引にはコンピュータを使ったアルゴリズムやモデルが多く存在する。しかし、新しい手法やアプローチにより、データサイエンスは定量的研究者の投資リターンの予測能力を向上させることができる。

ユビキント・インベストメント（北京）有限公司は、中国を拠点とする国内有数のクオンツ・ヘッジファンドです。
2012年に設立され、数学とコンピュータサイエンスの国際的な才能と最先端技術を駆使して、金融市場のクオンツ投資を推進しています。
ユビキタンは、投資家のために長期的に安定したリターンを創出することに取り組んでいます。このコンペティションでは、投資の収益率を予測するモデルを構築していただきます。過去の価格を用いてアルゴリズムをトレーニングし、テストしてください。優秀な作品は、この実世界のデータサイエンス問題を可能な限り正確に解決します。 成功すれば、定量的研究者のリターン予測能力を向上させることができます。これにより、あらゆる規模の投資家がより良い意思決定を行えるようになります。また、自分が金融データセットに長けていることがわかり、多くの業界で新しいチャンスが広がるかもしれません。 ユビキタスの詳細については、以下をご覧ください。

## Evaluation

各時間IDにおけるPearson correlation coeeficient の平均値で評価される。

```python
import ubiquant
env = ubiquant.make_env()   # initialize the environment
iter_test = env.iter_test()    # an iterator which loops over the test set and sample submission
for (test_df, sample_prediction_df) in iter_test:
    sample_prediction_df['target'] = 0  # make your predictions here
    env.predict(sample_prediction_df)   # register your predictions
```

# Data description

実際の投資案件の履歴データから作成された特徴量を含んだデータセットである。
このコンペでは、投資の意思決定に関連する難解な(obfuscated)評価指標の値を予測するのが目的である。
時系列解析を行うコードコンペである。

## Files
### train.csv

- `row_id` : row を同定するユニークなID
- `time_id` : データのかたまりを表すID？ 
- `investment_id` : 投資のIDコード
- `target` : 目標変数
- `[f_0:f_299]` : データから集められた匿名化されたデータ


