# [PetFinder.my - Pawpularity Contest](https://www.kaggle.com/c/petfinder-pawpularity-score)
# ディレクトリ構造
├── Untitled1.ipynb  
├── archive  
│   └── crop  
├── petfinder-pawpularity-score  
│   ├── sample_submission.csv  
│   ├── test  
│   ├── test.csv  
│   ├── train  
│   └── train.csv  
├── train_10folds.csv  
└── train_5folds.csv  

# 使用しているデータ
## petfinder-pawpularity-scoreディレクトリ
[ここ](petfinder-pawpularity-score)
## 5fold & 10fold
[notebookのoutput](https://www.kaggle.com/abhishek/same-old-creating-folds)
## archiveディレクトリ
[ここ](https://www.kaggle.com/c/petfinder-pawpularity-score/discussion/274303)

# 概要

## Pawpularity Scoreの算出方法
Pawpularity Scoreは、各ペットプロフィールの掲載ページにおけるページビュー統計から、異なるページ、プラットフォーム（ウェブとモバイル）、およびさまざまな測定基準でトラフィックデータを正規化するアルゴリズムを使用して算出されます。
重複クリック、クローラー・ボットによるアクセス、スポンサー付きプロフィールは分析から除外されています。

## 写真のメタデータの目的
写真のメタデータはオプションで、各写真に視覚的品質と構成の主要パラメータを手動でラベル付けしています。
これらのラベルはPawpularityスコアの導出には使用されませんが、コンテンツの理解を深めたり、写真の魅力に関連付けるのに有益な場合があります。私たちの最終的な目標は、写真にインテリジェントな推奨事項（ペットの顔を正面からクローズアップする、アクセサリーを追加する、被写体のフォーカスを上げるなど）や自動補正（明るさ、コントラストなど）を生成できるAIソリューションを導入することであり、より解釈しやすい予測ができることを期待しています。

# 各カラムの説明
- フォーカス - ペットが背景の中で際立っており、近すぎず遠すぎず。
- 目 - 両目が正面またはそれに近い方向を向いており、少なくとも1つの目/瞳がきちんとクリアになっている。
- 顔 - 正面またはそれに近い方向を向いている、はっきりとした顔。
- 近い - 1匹のペットが写真のかなりの部分を占めている（おおよそ写真の幅または高さの50％以上）。
- アクション - ペットが何かアクションを起こしている最中（例：ジャンプ）。
- アクセサリー - 首輪やリードを除く、付随する物理的またはデジタル的なアクセサリー/小道具（例：おもちゃ、デジタルステッカー）。
- グループ - 1匹以上のペットが写っていること。
- コラージュ - デジタル的にレタッチされた写真（デジタルフォトフレームを使用したもの、複数の写真を組み合わせたものなど）。
- Human - 写真に写っている人間。
- オクルージョン - 特定の望ましくないオブジェクトがペットの一部を遮っている状態（例：人間、ケージ、フェンス）。すべての遮蔽物がオクルージョンとは限らない。
- 情報 - カスタムで追加されたテキストやラベル（例：ペットの名前、説明）。
- ブラー - 特にペットの目や顔など、目立ったピンボケやノイズがある状態。ブラーのエントリーでは、「目」列は常に0に設定されます。


# 使用しているコード
## baseline
[notebook](https://www.kaggle.com/manabendrarout/transformers-classifier-method-starter-train)
