---
theme: seriph
background: https://cover.sli.dev
title: AI時代のマネジメント
info: |
    ## AI時代のマネジメント

    コンテキストマネジメント
class: text-center
drawings:
    persist: false
transition: slide-left
mdc: true
duration: 5min
---

# AI時代のマネジメント

コンテキストマネジメント

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

<div class="flex flex-col items-center justify-center pt-3 gap-4">

<img src="./Xqr.png" width="200" class="mx-auto" />

<div class="text-center">

**高手 智基**

REIMEI CEO / AIエンジニア

熊本在住

趣味：瞑想と読書（純文学とSF）

友達を増やしにきているのでよろしくお願いします！

</div>

</div>

---
layout: default
---

# 目次

- 問題 :レビューの負担
- 気づき
- コンテキストマネジメントとは
- 問題の本質
- 実践例
- まとめ

---
layout: default
---

# 問題：レビューの負担

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

# 気づき：レビューの大変さから

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

# 問題の本質：コンテキストの不足

<div class="pt-4">

- **メンバーの状況が見えない**
  - 何を理解しているのか
  - どう考えて実装したのか
  - どこでつまずいているのか

- → **マネージャーに必要なコンテキストが不足している**
  - 適切な判断ができない
  - 効果的なフィードバックができない


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

<br/>

※コメントには「why not」を書くというベストプラクティスには反しているが、レビューは楽になった

</div>

---
layout: default
---

# コメントの必要性について

<div class="flex flex-col items-center justify-center pt-8">

<img src="./スクリーンショット 2025-12-12 18.38.38.png" class="mx-auto" style="max-width: 90%;" />

<br/>

<div class="text-sm text-gray-400 pt-4">
プロンプトを丸々残さなくてもいいが、<br/>
何をするための実装なのかぐらいはあるといい
</div>

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

# 実践例3：AIエージェントによるレビュー自動化

<div class="pt-4">

## GitHub集約により実現した新たな可能性

<br/>

### AIエージェントへのコンテキスト提供

- 取得したデータをAIエージェントに提供
- プロジェクト全体の文脈を理解させられる

<br/>

### レビューの自動化

- AIエージェントがコンテキストを元に自動レビュー
- コードの意図や背景を理解した上での指摘が可能
- マネージャーの負担を大幅に軽減

</div>

---
layout: default
---

# 課題：まだまだ発展途上

<div class="pt-4">

## コンテキストの適切な管理が重要

<br/>

- コメントやコンテキストの**適切な削除**も必要
- 古い情報や不要な情報が残ると、かえって混乱を招く
- コンテキストの質と量のバランスが重要

<br/>

→ **まだまだ発展途上ではある**

</div>

---
layout: default
---

# まとめ

<div class="text-center pt-8">

## コンテキストのマネジメントが鍵

<br/>

AI、メンバー、マネージャー、チーム全体<br/>
すべてにおいて**コンテキストのマネジメント**が重要

</div>

<div class="text-center pt-8 text-gray-400">
  ありがとうございました
</div>
