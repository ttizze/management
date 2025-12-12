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

<div class="flex flex-col items-center justify-center pt-8 gap-4">

<img src="./Xqr.png" width="200" class="mx-auto" />

<div class="text-center">

**高手 智基**

REIMEI CEO / AIエンジニア

デジタル民主主義 2030、チームみらいにAIエンジニアとして参加

</div>

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

# 問題：レビューの負担増

<div class="pt-4">
<v-clicks>

1. **レビュー対象が増えている**
   - AIの活用で開発や執筆の速度が上がった
   - より多くのレビューが発生するように

2. **メンバーのスキルが見えにくくなった**

   **以前**：成果物を見れば、その人のスキルレベルがすぐ分かった

   **現在**：AIでそれなりの成果物は出せるが、本当のスキルレベルが分からない

   → どこを重点的にレビューすべきなのか､何を教えるべきなのか判断が難しい

</v-clicks>
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

# 本質の気づき：レビューの大変さから

<div class="pt-4">

<v-clicks>

- AIエージェントのコンテキストをマネジメントしていて気づいた

<br/>

- レビューが難しいのは、<br/>**メンバーのコンテキストを知らないから**では？

<br/>

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

# 実践例1：マネージャーへのコンテキスト提供

<div class="pt-4">

## メンバーにコメントを重点的につけてもらう

<br/>

### 効果

- 理解度がわかる
- なぜその実装なのかわかりやすい
- メンバー自身も､コメントを付けることで理解が深まる
- **コメントによってAIエージェントもレビューしやすくなった**<br/>（コメントと実装のズレでおかしさがわかる）

</div>

---
layout: default
---

# 実践例2：チームでのコンテキスト管理

<div class="pt-4">

## コード、ドキュメント、議論をGitHubに集約

<br/>

- コンテキストが一元管理される
- レビューしやすくなる
- 情報が散らばらない

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
