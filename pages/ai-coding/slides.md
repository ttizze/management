---
theme: seriph
background: https://cover.sli.dev
title: AI時代のソフトウェアエンジニアリング
info: |
  ## AI時代のソフトウェアエンジニアリング

  AIを使ったソフトウェアエンジニアリング
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
duration: 60min
---

# AI時代のソフトウェアエンジニアリング

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub" title="Open in GitHub" class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:logo-github />
  </a>
</div>

---
transition: fade-out
---

# 自己紹介

<div class="flex flex-col items-center justify-center pt-3 gap-4">

<img src="./Xqr.png" width="200" class="mx-auto" />

<div class="text-center">

**高手 智基**

REIMEI CEO / AIエンジニア

熊本在住

趣味：瞑想と読書（純文学とSF）


</div>

</div>

---
layout: default
---

# 目次

1. AIでソフトウェアエンジニアリングのボトルネックが移動した
2. なぜ遅いのか？AIが判断できないから
3. ソフトウェアエンジニアリングとは何か
4. ソフトウェアエンジニアリングのベストプラクティスは「答えの形」を作るためにある
5. 実践フロー
6. まとめ

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">1. AIでソフトウェアエンジニアリングのボトルネックが移動した</div>

# 結論：ボトルネックは移動した

- **AIで“書く量”は爆増**
- でも“出せる速さ”は爆増していない
- **ボトルネックは「コーディング」から「仕様・検証・レビュー・運用」へ**

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">1. AIでソフトウェアエンジニアリングのボトルネックが移動した</div>

# 量は増えた

- PRマージ **43.2M/月（+23% YoY）**
- Code push **82.19M/月**
- コミット **986M/年（+25% YoY）**

<div class="text-xs text-gray-400">出典：GitHub Octoverse 2025</div>

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">1. AIでソフトウェアエンジニアリングのボトルネックが移動した</div>

# しかし全体として速くなってはいない

- **68%がAIで週10時間以上“節約”**
- **50%が非コーディングの非効率で週10時間以上“喪失”**

→ **速さが組織の摩擦で相殺される**

<div class="text-xs text-gray-400">出典：Atlassian State of DevEx 2025</div>

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">1. AIでソフトウェアエンジニアリングのボトルネックが移動した</div>

# レビュー負荷が熟練者に集中

- **コア開発者のレビュー負担 +6.5%**
- **コア開発者の“自分のコード生産性” -19%**

<div class="text-xs text-gray-400">出典：arXiv 2510.10165</div>


質の悪いPRが増えたことでレビュー負荷が増大

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">1. AIでソフトウェアエンジニアリングのボトルネックが移動した</div>

# AIレビューでも遅くなるケース

- PRクローズ時間が **5h52m → 8h20m** に増加
- AIレビューは有用でも、全体のリードタイムは悪化することがある
- ボットのコメント対応が増える
- スコープ外・無関係な指摘が混ざる

<div class="text-xs text-gray-400">出典：arXiv 2412.18531</div>

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">1. AIでソフトウェアエンジニアリングのボトルネックが移動した</div>

# コーディングは解決した
# ソフトウェアエンジニアリング全体のボトルネックはまだ解決していない

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">2. なぜ遅いのか？AIが判断できないから</div>

# なぜ遅いのか？

- 新たなボトルネック､「仕様・検証・レビュー・運用」に共通するのは **「答えが曖昧」** なこと
- 答えが曖昧だとAIは迷子になる

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">2. なぜ遅いのか？AIが判断できないから</div>

# バイブコーディング＝曖昧なまま進める典型

- MVPは作れたが､保守できない
- 実装の意図がわからない
- 壊れたら直せない

→ 正しい答えがわからないから

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">2. なぜ遅いのか？AIが判断できないから</div>

# 答えを明確にする必要がある


## これはソフトウェアエンジニアリングがやってきたこと

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">3. ソフトウェアエンジニアリングとは何か</div>

# ソフトウェアエンジニアリングとは

> "Software engineering is programming integrated over time."

<div class="text-xs text-gray-400 my-4">出典：Software Engineering at Google, Chapter 1</div>

- **Time**：時間の経過と「変化の必要性」への備え
- **Scale**：規模と効率（ソフトウェアと組織の両方）
- **Trade-offs**：不正確な見積りを前提にした、高いステークの意思決定

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">3. ソフトウェアエンジニアリングとは何か</div>

# Timeの実例：長寿命プロジェクト

- **Google Search / Linux kernel / Apache HTTP Server**
- 終わりが読めない長期運用が前提
- 依存関係・OS・言語バージョンの変化に耐える必要

<div class="text-xs text-gray-400">出典：Software Engineering at Google, Chapter 1</div>

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">3. ソフトウェアエンジニアリングとは何か</div>

# Scaleの実例：多人数・多版

- 人数が増えると、同じ作業が指数的に重くなる  
  例：レビュー待ち / マージ競合 / CI滞留 / リリース調整

<div class="text-xs text-gray-400">出典：Software Engineering at Google, Chapter 1</div>

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">3. ソフトウェアエンジニアリングとは何か</div>

# Trade-offsの実例：変更の価値 vs 影響

- 変更には**効率・安全性・将来性**の価値がある
- ただし**互換性の破壊**というコストが発生する
- 価値と痛みを評価して意思決定する

<div class="text-xs text-gray-400">出典：Software Engineering at Google, Chapter 1</div>

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">4. ソフトウェアエンジニアリングのベストプラクティスは「答えの形」を作るためにある</div>

# ソフトウェアエンジニアリングのベストプラクティスは「答えの形」を作るためにある

- **コメント**：意図を伝える
- **ADR**：決定の根拠を残す
- **CI**：成功条件を自動検証
- **テスト**：期待する振る舞いを定義
- **リファクタリング**：構造を読みやすく保つ

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">4. ソフトウェアエンジニアリングのベストプラクティスは「答えの形」を作るためにある</div>

# 答えがあるならAIに任せられる

- 検証できるなら自動化できる
- 自動化できるならAIに任せられる

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">5. 実践フロー</div>

# 実践フロー（全体像）

**壁打ち → 仕様 → 設計 → 実装 → 検証 → レビュー**

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">5. 実践フロー</div>

# 実践 1：壁打ちで仕様を確定

- 「何を作るのか」を先に固める
- AIに仕様を言語化させる
- 仕様 = 検証可能性の出発点

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">5. 実践フロー</div>

# 実践 2：仕様が固まったら実装

- 仕様 → 設計 → 実装の順序を崩さない
- コードより仕様が上位

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">5. 実践フロー</div>

# 実践 3：検証可能性を作る

- **検証できるなら自動化できる**
- 「仕様の形」を作ることが最重要

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">5. 実践フロー</div>

# AIに効くコード

- 型がある
- テストがある
- ルールがある

→ AIが正しく振る舞う前提条件

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">5. 実践フロー</div>

# でもテストは万能じゃない

- 全パターンの網羅は不可能
- テスト設計はコストが高い

→ **結局コードを読む**

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">5. 実践フロー</div>

# コードを読む力

- 仕様と実装のズレを発見
- AIの「それっぽさ」を見破る
- 変更の影響範囲を把握

---
layout: default
---

<div class="text-sm text-gray-400 mb-4">6. まとめ</div>

# まとめ

- **AIを活かすカギ＝検証可能性を上げること**
- それはソフトウェアエンジニアリングが大切にしてきたことでもある
- 最後は人間がコードを読む

---
layout: center
---

# Q&A

