---
theme: seriph
background: https://cover.sli.dev
title: AI時代のマネジメント
info: |
    ## AI時代のマネジメント

    AI技術の進化がもたらす新しいマネジメントの形を探る
class: text-center
drawings:
    persist: false
transition: slide-left
mdc: true
duration: 5min
---

# AI時代のマネジメント

AI技術の進化がもたらす<br/>新しいマネジメントの形

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    スペースキーで次へ <carbon:arrow-right class="inline"/>
  </span>
</div>

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

<div class="text-center pt-8">

<!-- ここに自己紹介を追加してください -->

</div>

---
layout: default
---

# 目次

- 問題
- 問題の本質
- コンテキストマネジメントとは
- 本質の気づき
- 実践例
- まとめ

---
layout: default
---

# 問題1：メンバーのスキルが見えにくくなった

<div class="grid grid-cols-2 gap-6 pt-4">

<div>

## 以前

- コードを見れば、その人のスキルレベルがすぐ分かった
- 具体的なフィードバックがすぐできた<br/>（例：セキュリティの本を読むといい、<br/>テストの本を読むといい）

</div>

<div>

## 現在

- AIに聞けばそれなりのコードは出てくる
- でも、本当のスキルレベルが分からない
- どう導けばいいか難しい<br/>

</div>

</div>

---
layout: default
---

# 問題2：PRレビューの負担増

<div class="pt-4">

## 二重の負担

<br/>

1. **PRの量が増えている**

<br/>

2. **さらに、スキルが見えないことで：**
   - どんなタスクを降っていいのか判断が難しい
   - レビューでどこを重点的に確認すべきなのか判断が難しい
   - → **1つ1つのレビューが難しくなっている**

<br/>

→ **量の増加 × レビューの難しさ = 負担が増大**

</div>

---
layout: default
---

# 問題の本質：情報の非対称性

<div class="pt-4">

- **メンバーの状況が見えない**
  - 何を理解しているのか
  - どう考えて実装したのか
  - どこでつまずいているのか

- **マネージャーに必要な情報が不足している**
  - 適切な判断ができない
  - 効果的なフィードバックができない


</div>

---
layout: default
---

# 本質の気づき1：AIのコンテキストマネジメントから学んだこと

<div class="pt-4">

<v-clicks>

- AIエージェントのコンテキストをマネジメントしていて思った

<br/>

- レビューが難しいのも、<br/>**メンバーのコンテキストを知らないから**では？

→ **マネージャーのコンテキストが適切にマネジメントされていない**

</v-clicks>

</div>

---
layout: default
---

# コンテキストマネジメントとは

<div class="pt-4">

## 情報を適切に伝える・共有する

<br/>

### AIのコンテキストマネジメントの具体例

- **Cursorのルール** - プロジェクトのルールや規約をAIに伝える
- **RAG（Retrieval-Augmented Generation）** - 必要な情報を検索してAIに提供
- **プロンプト設計** - 構造化された情報を段階的に提供


<br/>

- 適切なコンテキストがないと、判断や行動が難しくなる
- コンテキストを共有することで、理解が深まり、効率的に協働できる

</div>

---
layout: default
---

# 実践例1：AIへのコンテキスト提供

<div class="pt-4">

## AIエージェントにレビューさせている

<br/>

- プロンプト設計で適切なコンテキストを提供
- Cursorのルールで必要な情報を構造化
- コンテキストを適切にマネジメントすることで、<br/>AIエージェントが効果的にレビューできる

</div>

---
layout: default
---

# 実践例2：マネージャーへのコンテキスト提供（新人から）

<div class="pt-4">

## 新人にコメントを重点的につけてもらう

<br/>

### 効果

- 理解度がわかる（マネージャーが）
- なぜその実装なのかわかりやすい（マネージャーが）
- **コメントによってAIエージェントもレビューしやすくなった**<br/>（コメントと実装のズレでおかしさがわかる）

</div>

---
layout: default
---

# 実践例3：チーム全体への適用

<div class="pt-4">

<v-clicks>

- **コンテキストマネジメントの文化づくり**
  - 情報共有の習慣化
  - 質問しやすい環境づくり

<br/>

- **コメントと実装のズレを防ぐ仕組み**
  - 定期的な見直し
  - ツールやプロセスの改善

</v-clicks>

</div>

---
layout: default
---

# まとめ

<div class="text-center pt-8">

## コンテキストのマネジメントが鍵

<br/>

AI、新人、マネージャー、チーム全体<br/>
すべてにおいて**コンテキストのマネジメント**が重要

</div>

<div class="text-center pt-8 text-gray-400">
  ありがとうございました
</div>
