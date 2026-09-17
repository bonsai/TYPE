# TypeのTypeをめぐる会議

## アリストテレス × ウィトゲンシュタイン × Tim Berners-Lee

### 議題

> **TypeにはTypeがあるのか？**

場所は Agora Schola。

三人は、中央に置かれた一枚の図を見る。

```text
Type
 ↓
Type
 ↓
Instance
```

---

### アリストテレス

「まず、分類しなければならない。

あるものが何であるかを問うなら、
それがどのような類に属し、
どのような種であるかを考える必要がある。」

「つまり、Typeは単独ではない。

```text
Genus
  ↓
Species
  ↓
Individual
```

という関係の中に置かれる。」

---

### ウィトゲンシュタイン

「しかし、ちょっと待ってほしい。」

「あなたはいま『Type』という言葉を使った。

では聞こう。

**この場所で、その言葉はどう使われているのか？**」

「Typeという語が、

- 分類のために使われるのか
- データ構造のために使われるのか
- 人間の概念整理のために使われるのか
- コンピュータに推論させるために使われるのか

それによって意味は変わる。」

---

### Tim Berners-Lee

「それはWebでも同じ問題になる。」

「しかしWebでは、さらに一つ問題がある。」

「人間だけがTypeを理解するのではない。

コンピュータ同士も、

```text
Person
Agent
Object
Event
Relation
```

が何を意味するのかを扱わなければならない。」

「だから対象に識別子を与え、
対象同士の関係を機械的に接続できるようにする。」

「URI、RDF、Ontologyなどは、そのための仕組みだ。」

---

### ウィトゲンシュタイン

「だが、URIを与えたからといって、
その意味が完全に決まるわけではない。」

「重要なのは、

**その記号がどのような活動の中で使われているか**

だ。」

---

### Tim Berners-Lee

「その通りだ。

だからWebは一つの巨大な分類体系だけで作る必要はない。」

「異なるコミュニティが、それぞれの語彙やOntologyを持っていてよい。

重要なのは、それらを接続できることだ。」

---

### アリストテレス

「すると、分類体系は一つではないということか。」

### Tim Berners-Lee

「そうだ。」

### ウィトゲンシュタイン

「そして、分類そのものも活動の中で使われる。」

「だから、

```text
Ontology
```

だけを見るのでは足りない。」

「そのOntologyが、

**誰によって、どこで、何のために使われているか**

を見る必要がある。」

---

### アリストテレス

「では、最初の問いに戻ろう。

**TypeにはTypeがあるのか？**」

三人は図を見る。

```text
Meta-Type
    ↓
Type Family
    ↓
Type
    ↓
Instance
```

---

### アリストテレス

「これは分類の階層として理解できる。」

### ウィトゲンシュタイン

「私は、それを固定的な本質とは呼ばない。」

「Typeという言葉自体にも、
異なる使い方があるからだ。」

### Tim Berners-Lee

「私は、それをWeb上で表現できるようにしたい。」

「Typeにも識別子を与え、
Type同士の関係を記述できる。」

---

### 三人

「つまり、問題は単純な

> Type → Type

ではない。」

「重要なのは、

```text
Type
 ↓
is_a / instance_of / subclass_of
 ↓
Type
```

という**関係そのもの**である。」

---

### ウィトゲンシュタイン

「そして、その関係が使われる場所がある。」

```text
Topos
  ↓
Role
  ↓
Context
  ↓
Language Game
  ↓
Type
  ↓
Relation
```

「幽霊のように、どこにもいないTypeなど考えなくてよい。」

---

### Tim Berners-Lee

「Webでは、その『場所』も重要になる。」

「あるTypeがどのOntologyに属し、
どのURIで識別され、
どのデータと接続されているのか。」

---

### アリストテレス

「つまり、存在論だけでは不十分だ。」

```text
Ontology
何があるか

Topology
どうつながるか

Topos
どこで存在し、使われるか

Language Game
どう使われるか

Type
何として扱うか
```

---

### 結論

三人はホワイトボードに次の式を書く。

```text
Type
=
Concept
+
Context
+
Relation
+
Use
```

そして、その上にさらに一行を書く。

```text
Type of Type
=
「Typeとは何か」を規定するType
```

ただし、それは絶対的な最上位Typeとは限らない。

```text
Meta-Type
    ↓
Family
    ↓
Type
    ↓
Sub-Type
    ↓
Instance
```

という階層にもできるし、

```text
Type ←→ Type
```

という関係ネットワークにもできる。

さらに、

```text
Topos
  ↓
Agent
  ↓
Awareness
  ↓
Language Game
  ↓
Question
  ↓
Type
  ↓
Relation
  ↓
Action
```

として、実際のAgentの活動の中でTypeが使われる。

---

## Agora Scholaでの次の問い

> **TypeをTypeとして認識するAgentは、何をawareしているのか？**

ここから `TYPE` は単なる分類体系ではなく、

**「Agentが世界を何として認識し、どのTypeを選び、どのRelationを発見し、どのActionを行うか」**

を検討する場所になる。
