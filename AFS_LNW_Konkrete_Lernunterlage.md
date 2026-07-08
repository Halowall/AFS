# AFS LNW 具体备考学习资料

> 目标：针对 LNW 多选题，不只列复习大纲，而是给出具体知识点、德语读题模板、记忆方法和选项判断方法。  
> 使用顺序：先读本文件，再用 `AFS_LNW_Fragen_Review.md` 检查图片题 1-12。

---

## 0. 你的主要问题和解决方案

你现在遇到的核心困难不是“完全不会 AFS”，而是：

1. 德语选项句子看不懂。
2. 不知道每句话在考哪个定义。
3. 看到 `δ`、`δ*`、`K`、`K*`、`P(S)` 容易混。
4. 多选题里不确定是不是只有一个答案。

解决方案是按三层准备：

| 层级 | 你要做什么 | 目标 |
|---|---|---|
| 第一层：读懂题干 | 背高频德语句型 | 知道题目在问什么 |
| 第二层：背核心定义 | 每个模块只背最常考定义和公式 | 能判断选项类型是否正确 |
| 第三层：识别陷阱 | 背常见错误表达 | 能快速排除错选项 |

LNW 多选题的思维：

```text
不是选“最像正确答案的一个”，而是每个选项独立判断。
答案可以是 0 个、1 个、2 个、3 个或 4 个。
```

---

## 1. 德语选项阅读模板

### 1.1 最常见题干

| 德语 | 中文 | 你要做什么 |
|---|---|---|
| `Welche der folgenden Aussagen sind richtig?` | 以下哪些说法正确？ | 每个选项独立判断 |
| `Sei A ein Alphabet.` | 设 A 是一个字母表。 | 立刻想到：非空、有限 |
| `Sei A=(E,S,δ,s0,F) ein DEA.` | 设 A 是一个 DEA。 | 立刻想到：`δ:S×E→S` |
| `im Sinne der Vorlesung` | 按课件定义 | 不要套其他教材定义 |
| `Dann gilt ...` | 那么成立的是 | 判断后面的公式/命题 |

### 1.2 常见选项句型

| 德语句型 | 中文模板 | 例子 |
|---|---|---|
| `X ist ...` | X 是…… | `Ein Alphabet ist eine endliche Menge...` |
| `X hat die Form ...` | X 的形式是…… | `δ hat die Form S×E→S` |
| `Es gilt ...` | 成立的是…… | `Es gilt N∩T=∅` |
| `wird akzeptiert, wenn ...` | 当……时被接受 | `w wird akzeptiert, wenn δ*(s0,w)∈F` |
| `genau dann, wenn ...` | 当且仅当…… | 条件非常强，要双向正确 |
| `mindestens ein ...` | 至少一个…… | NEA/NKA 中经常正确 |
| `jeder ...` | 每一个…… | NEA/NKA 中经常太强 |
| `sobald ...` | 一旦…… | 小心“自动结束”这种说法 |
| `zunächst ...` | 首先…… | 常考算法步骤顺序 |
| `am Ende ...` | 最后…… | 常考最小化最后合并谁 |

### 1.3 高频陷阱词

| 德语词 | 中文 | 选择题判断 |
|---|---|---|
| `stets` | 总是、一定 | 很强，TM/KA 里常可疑 |
| `automatisch` | 自动地 | 输入读完不代表自动停机 |
| `nur dann` | 只有当 | 只说必要条件，不一定是完整定义 |
| `genau dann` | 当且仅当 | 必须正反都对 |
| `beliebig` | 任意地 | 常用于错误扩大条件 |
| `nachträglich` | 事后 | LBA 的 `k,c` 不能事后选 |
| `leer` | 空 | 注意 `λ`、`∅`、空栈不是一回事 |

记忆方法：

```text
jeder / stets / automatisch = 强词，先怀疑。
mindestens ein = 存在一个，想到 NEA/NKA。
genau dann = 定义级别，必须非常精确。
```

---

## 2. 知识卡片一：Alphabet, Wort, Sprache

### 2.1 必须背的内容

```text
Ein Alphabet ist eine nichtleere, endliche Menge von Zeichen.
Ein Wort ist eine endliche Folge von Zeichen.
λ ist das leere Wort mit Länge 0.
A* ist die Menge aller endlichen Wörter über A, inklusive λ.
A+ = A* \ {λ}.
Eine Sprache über A ist jede Teilmenge L ⊆ A*.
```

中文理解：

- Alphabet：字母表，必须非空、有限。
- Wort：有限长度的符号序列。
- `λ`：空词，长度为 0。
- `A*`：所有长度的词，包括长度 0，所以包括 `λ`。
- `A+`：不包括 `λ`。
- Sprache：`A*` 的任意子集。

### 2.2 必须区分

| 符号 | 中文 | 例子 |
|---|---|---|
| `λ` | 空词 | 一个词，长度 0 |
| `{λ}` | 只含空词的语言 | 有一个元素 |
| `∅` | 空语言 | 没有任何词 |
| `A` | 字母表 | `{a,b}` |
| `A*` | 所有有限词 | `{λ,a,b,aa,ab,...}` |

### 2.3 LNW 会怎么问

| 选项 | 判断 |
|---|---|
| `Ein Alphabet ist eine nichtleere, endliche Menge von Zeichen.` | 对 |
| `Ein Alphabet kann unendlich viele Zeichen enthalten.` | 错 |
| `Das leere Wort λ ist in A* enthalten.` | 对 |
| `Jede Teilmenge L⊆A* heißt Sprache über A.` | 对 |
| `∅ ist keine Sprache.` | 错，空集也是语言 |

### 2.4 记忆方法

```text
Alphabet = Zeichen集合，必须 endlich + nichtleer。
Stern * = 包括 0 次，所以一定有 λ。
Plus + = 至少 1 次，所以没有 λ。
Sprache = Wörter 的集合，不是 Zeichen 的集合。
```

---

## 3. 知识卡片二：Turingmaschine, Akzeptor, Entscheider

### 3.1 必须背的内容

```text
DTM: T = (E, B, S, δ, s0)
Akzeptor-TM: T = (E, B, S, δ, s0, F)
Konfiguration: (v, s, w)
Startkonfiguration bei w≠λ: (λ, s0, w)
L(T): Menge aller von T akzeptierten Wörter
```

`(v,s,w)` 的含义：

| 位置 | 含义 |
|---|---|
| `v` | 读写头左边 |
| `s` | 当前状态 |
| `w` | 从读写头当前位置开始向右的内容 |

### 3.2 接受、不接受、判定

| 德语 | 中文 | 判断标准 |
|---|---|---|
| `akzeptieren` | 接受 | 停在 `F` 中 |
| `verwerfen` | 拒绝 | 停在 `S\F` 中 |
| `nicht akzeptieren` | 不接受 | 可能拒绝，也可能不停机 |
| `entscheiden` | 判定 | 对每个输入都停机，并给出正确 Ja/Nein |

### 3.3 LNW 会怎么问

| 选项 | 判断 | 原因 |
|---|---|---|
| `Hält T in einem Zustand aus F, so akzeptiert T die Eingabe.` | 对 | 终态接受 |
| `Akzeptiert T eine Eingabe nicht, so hält T stets.` | 错 | 可能不停机 |
| `Akzeptieren bedeutet dasselbe wie Entscheiden.` | 错 | 判定更强 |
| `L(T) ist die Menge aller von T akzeptierten Wörter.` | 对 | 语言定义 |
| `Startkonfiguration ist (λ,s0,w).` | 对 | 当 `w≠λ` |

### 3.4 记忆方法

```text
TM-Konfiguration: Zustand steht in der Mitte.
(links, Zustand, Kopf+rechts)
```

判定和接受：

```text
Akzeptor darf hängen bleiben.
Entscheider muss immer halten.
```

---

## 4. 知识卡片三：LBA

### 4.1 必须背的内容

```text
Ein LBA ist eine Turingmaschine mit linear beschränktem Speicher.
Für eine Eingabe w dürfen höchstens k·|w|+c Bandfelder verwendet werden.
k und c sind feste natürliche Zahlen.
```

中文理解：

LBA 不是无限使用纸带，而是最多用和输入长度成线性关系的空间。输入越长，允许空间可以变大，但增长规则必须提前固定。

### 4.2 LNW 会怎么问

| 选项 | 判断 |
|---|---|
| `k und c sind feste natürliche Zahlen.` | 对 |
| `k und c hängen nicht von der konkreten Eingabe ab.` | 对 |
| `k und c dürfen nachträglich gewählt werden.` | 错 |
| `k und c können negative ganze Zahlen sein.` | 错 |
| `|w| darf den erlaubten Platz nicht beeinflussen.` | 错 |

### 4.3 记忆方法

```text
LBA = Linear Bound.
Linear heißt: k·|w|+c.
Bound gehört zur Maschine, nicht zur einzelnen Eingabe.
```

---

## 5. 知识卡片四：DEA

### 5.1 必须背的内容

```text
DEA: A = (E, S, δ, s0, F)
δ : S × E → S
δ* : S × E* → S
w ∈ L(A) ⇔ δ*(s0,w) ∈ F
```

中文理解：

- `δ`：普通转移函数，一次只读一个字符。
- `δ*`：扩展转移函数，可以读整个词。
- 读完整个词后，如果状态在 `F` 中，就接受。

### 5.2 `δ` 和 `δ*` 的区别

| 函数 | 输入 | 输出 |
|---|---|---|
| `δ` | 状态 + 一个 Zeichen | 一个 Zustand |
| `δ*` | 状态 + 一个 Wort | 一个 Zustand |

LNW 看到：

```text
δ(s0,w)
```

如果 `w` 是一个 Wort，通常就是类型错误。应该是：

```text
δ*(s0,w)
```

### 5.3 DEA 图题怎么做

步骤：

1. 找 Startzustand。
2. 找 Endzustand / Endzustände。
3. 看每个输入符号让状态怎么变化。
4. 总结语言。
5. 再判断每个给出的 Wort。

例子：

```text
n 不改变状态。
d 在 0 和 1 之间切换。
1 是 Endzustand。
所以接受奇数个 d 的词。
```

德语表达：

```text
Der Automat akzeptiert genau die Wörter mit ungerader Anzahl von d.
```

### 5.4 LNW 会怎么问

| 选项 | 判断 |
|---|---|
| `w∈L(A) genau dann, wenn δ*(s0,w)∈F.` | 对 |
| `δ:S×E→S` | 对 |
| `δ:S×E*→S` | 错，这是 `δ*` |
| `δ*(s0,w)=s0` 是接受条件 | 错，除非 `s0∈F`，但不是一般定义 |

### 5.5 记忆方法

```text
δ = 一个符号。
δ* = 一个词。
星号 * 对应 E*，所以 δ* 读 E*。
```

---

## 6. 知识卡片五：NEA 和 Potenzmenge

### 6.1 必须背的内容

```text
NEA: δ : S × E → P(S)
NEA mit λ-Übergängen: δ : S × (E ∪ {λ}) → P(S)
P(S) = Potenzmenge von S = Menge aller Teilmengen von S
```

例子：

如果：

```text
S = {s0, s1}
```

那么：

```text
P(S) = {∅, {s0}, {s1}, {s0,s1}}
```

### 6.2 NEA 接受条件

```text
Ein Wort wird akzeptiert, wenn mindestens ein Rechenpfad nach dem vollständigen Lesen von w in einem Zustand aus F endet.
```

中文：

只要至少有一条路径成功，就接受。不是每条路径都要成功。

### 6.3 LNW 会怎么问

| 选项 | 判断 | 原因 |
|---|---|---|
| `δ:S×(E∪{λ})→P(S)` | 对 | NEA mit λ |
| `δ:S×E→S` | 错 | 这是 DEA |
| `mindestens ein Rechenpfad` | 对 | 非确定型看存在路径 |
| `jeder Rechenpfad` | 错 | 太强 |
| `λ-Übergang liest ein Zeichen` | 错 | λ 不消耗输入 |

### 6.4 记忆方法

```text
N = nichtdeterministisch = mehrere Möglichkeiten.
Mehrere Möglichkeiten = Menge.
Menge von Zuständen = P(S).
```

---

## 7. 知识卡片六：Kellerautomat

### 7.1 必须背的内容

```text
KA: A = (E, K, S, δ, s0, F)
δ : S × (E ∪ {λ}) × K → S × K*
Konfiguration: (s, w, v)
Startkonfiguration: (s0, w, k0)
```

`δ(s,e,k)=(s',v)` 的意思：

| 符号 | 中文 |
|---|---|
| `s` | 当前状态 |
| `e` | 当前输入符号，或 `λ` 表示不读输入 |
| `k` | 栈顶符号 |
| `s'` | 新状态 |
| `v∈K*` | 用来替换栈顶的栈词 |

### 7.2 为什么左边是 `K`，右边是 `K*`

左边：

```text
... × K
```

表示每一步只看一个栈顶符号。

右边：

```text
... → S × K*
```

表示可以写回一个栈词：

- 写 `λ`：删除栈顶，pop。
- 写 `A`：栈顶保持或替换为一个符号。
- 写 `AA` 或 `Ak0`：push 多个符号。

### 7.3 两个 λ 的区别

| 位置 | 例子 | 含义 |
|---|---|---|
| 输入位置 | `δ(s,λ,A)` | 不读输入 |
| 右边栈词 | `δ(s,a,A)=(s',λ)` | 删除栈顶 |

非常重要：

```text
如果状态变了但栈不变，不写 λ，而是把原栈顶写回去。
```

例如栈顶是 `A`，要保持不变：

```text
δ(s0,a,A) = (s1,A)
```

不是：

```text
δ(s0,a,A) = (s1,λ)
```

因为右边的 `λ` 表示删除 `A`。

### 7.4 KA 接受条件

按这门课的定义：

```text
输入完全读完 + 机器停机 + 停在 F 中的状态
```

德语：

```text
A akzeptiert w, wenn A nach endlich vielen Schritten hält, nachdem w vollständig gelesen wurde, und sich beim Halten in einem Zustand aus F befindet.
```

不要把它和“leerer Keller”混淆。空栈接受是另一种约定。

### 7.5 LNW 会怎么问

| 选项 | 判断 |
|---|---|
| `δ:S×(E∪{λ})×K→S×K*` | 对 |
| `δ:S×(E∪{λ})×K→S×K` | 错，右边必须是 `K*` |
| `δ:S×(K∪{λ})×K→S×K*` | 错，第二个位置是输入，不是 Keller |
| `δ:S×(E∪{λ})×K*→S×K*` | 错，左边只看栈顶 |
| `Akzeptanz durch leeren Keller` | 本课 LNW 中通常错 |

### 7.6 记忆方法

```text
KA 每步看三样：状态、输入、栈顶。
KA 每步改两样：状态、栈顶替换成一个 Kellerwort。
```

公式记忆：

```text
links: S, Eingabe, ein Kellerzeichen
rechts: neuer Zustand, Kellerwort
```

---

## 8. 知识卡片七：NKA, NTM 的非确定思想

### 8.1 NKA

```text
NKA: δ : S × (E ∪ {λ}) × K → P(S × K*)
```

与 KA 的区别：

| KA | NKA |
|---|---|
| `S×K*` | `P(S×K*)` |
| 一个后继可能 | 多个后继可能 |

### 8.2 NTM

```text
NTM: δ : S × B → P(S × B × {R,L,N})
```

核心思想：

```text
非确定型 = 有多个可能后继。
接受 = 至少一条计算路径接受。
```

### 8.3 记忆方法

只要看到 `nichtdeterministisch`，就想到：

```text
P(...)
mindestens ein Rechenpfad
```

---

## 9. 知识卡片八：Moore 和 Mealy Automaten

### 9.1 必须背的内容

| 自动机 | 输出在哪里 | Ausgabefunktion |
|---|---|---|
| Moore | 状态上 | `γ:S→A` |
| Mealy | 转移边上 | `γ:S×E→A` |

### 9.2 LNW 会怎么问

| 选项 | 判断 |
|---|---|
| `Beim Moore-Automaten hängt die Ausgabe nur vom Zustand ab.` | 对 |
| `Beim Mealy-Automaten hängt die Ausgabe vom Zustand und Eingabezeichen ab.` | 对 |
| `Moore hat γ:S×E→A.` | 错，这是 Mealy |
| `Mealy hat γ:S→A.` | 错，这是 Moore |

### 9.3 记忆方法

```text
Moore = mehr Zustand, Ausgabe im Zustand.
Mealy = mit Eingabe, Ausgabe an der Kante.
```

最短背法：

```text
Moore: Ausgabe im Zustand.
Mealy: Ausgabe an der Kante.
```

---

## 10. 知识卡片九：DEA-Minimierung

### 10.1 必须背的步骤

```text
1. Nicht erreichbare Zustände entfernen.
2. In der Markierungstabelle zuerst Paare markieren, bei denen genau ein Zustand in F liegt.
3. Ein unmarkiertes Paar markieren, wenn es bei einem Eingabezeichen auf ein bereits markiertes Paar führt.
4. Am Ende unmarkierte Paare verschmelzen.
```

### 10.2 最重要的判断

| 德语 | 中文 | 能不能合并 |
|---|---|---|
| `markiert` | 已标记 = 可区分 | 不能合并 |
| `unmarkiert` | 未标记 = 等价 | 最后合并 |

### 10.3 LNW 会怎么问

| 选项 | 判断 |
|---|---|
| `Zunächst werden alle nicht erreichbaren Zustände entfernt.` | 对 |
| `Paare mit genau einem Endzustand werden zuerst markiert.` | 对 |
| `Unmarkiertes Paar wird markiert, wenn es auf markiertes Paar führt.` | 对 |
| `Am Ende werden die markierten Paare verschmolzen.` | 错 |

### 10.4 记忆方法

```text
markiert = unterscheidbar = nicht zusammenlegen.
unmarkiert = äquivalent = zusammenlegen.
```

---

## 11. 知识卡片十：Äquivalenzrelation

### 11.1 必须背的内容

等价关系必须同时满足三个性质：

```text
reflexiv: a ~ a
symmetrisch: a ~ b ⇒ b ~ a
transitiv: a ~ b und b ~ c ⇒ a ~ c
```

商集：

```text
X/~ = {[a]~ | a ∈ X}
```

### 11.2 LNW 会怎么问

| 选项 | 判断 |
|---|---|
| `R ist eine Äquivalenzrelation.` | 要检查三个性质 |
| `R ist nicht reflexiv, denn kein Element steht zu sich selbst in Relation.` | 可能对 |
| `X/~ = {[a]~ | a∈X}` | 对 |
| `X/~ = {[a]~ | [a]~∈X}` | 错 |

### 11.3 例子：grüner als

```text
k1 R k2 ⇔ k1 ist grüner als k2
```

判断：

- 不自反：没有东西比自己更绿。
- 不对称：如果 A 比 B 更绿，不可能 B 又比 A 更绿。
- 所以不是等价关系。

### 11.4 记忆方法

```text
等价关系 = 相等感。
如果关系像 “gleich groß / gleich farbig”，可能是等价关系。
如果关系像 “größer als / grüner als”，通常不是等价关系。
```

---

## 12. 知识卡片十一：Formale Grammatik

### 12.1 必须背的内容

```text
G = (N, T, P, S)
N: Nichtterminale / Variablen
T: Terminale
P: Produktionen / Regeln
S: Startsymbol
N ∩ T = ∅
S ∈ N
L(G) = { w ∈ T* | S ⇒*_G w }
```

### 12.2 产生式规则

一般形式语法中，产生式左边必须至少含一个非终结符：

```text
Auf der linken Seite einer Produktion muss mindestens ein Nichtterminal vorkommen.
```

所以：

```text
ab → ba
```

如果 `a,b` 都是 Terminale，那么在普通语法定义里不作为合法产生式左边。

### 12.3 LNW 会怎么问

| 选项 | 判断 |
|---|---|
| `N∩T=∅` | 对 |
| `S∈N` | 对 |
| `Auf der linken Seite darf ein Wort nur aus Terminalsymbolen stehen.` | 错 |
| `L(G)={w∈T* | S⇒*_G w}` | 对 |

### 12.4 记忆方法

```text
N = Noch nicht fertig.
T = Terminal = fertig.
S = Start, muss in N sein.
L(G) 最后只能包含 T* 里的词。
```

---

## 13. 知识卡片十二：Chomsky-Hierarchie

### 13.1 必须背的表

| Typ | 名称 | 规则限制 | 对应自动机 |
|---|---|---|---|
| Typ 0 | unbeschränkt | 无限制 | Turingmaschine |
| Typ 1 | kontextsensitiv | 不缩短，`|links|≤|rechts|` | LBA |
| Typ 2 | kontextfrei | 左边一个非终结符 | Kellerautomat |
| Typ 3 | regulär | 右线性或左线性 | endlicher Automat |

### 13.2 LNW 会怎么问

| 选项 | 判断 |
|---|---|
| `Typ 3 entspricht endlichen Automaten.` | 对 |
| `Typ 2 entspricht Kellerautomaten.` | 对 |
| `Typ 1 entspricht LBA.` | 对 |
| `Typ 0 entspricht TM.` | 对 |
| `Typ 1 darf beliebig verkürzen.` | 错 |
| `Bei Typ 2 steht links genau ein Nichtterminal.` | 对 |

### 13.3 记忆方法

从强到弱记：

```text
TM > LBA > KA > EA
Typ 0 > Typ 1 > Typ 2 > Typ 3
```

对应：

```text
0-TM, 1-LBA, 2-KA, 3-EA
```

---

## 14. 知识卡片十三：Automat zu Grammatik

### 14.1 DEA 到 Typ-3 Grammatik

必须背：

```text
Zustände werden Nichtterminale.
Eingabezeichen werden Terminale.
Startzustand wird Startsymbol.
δ(s,e)=s' wird Produktion s → e s'.
Für Endzustände gibt es Produktionen s → λ.
```

### 14.2 LNW 可能问法

| 选项 | 判断 |
|---|---|
| `Zustände werden zu Nichtterminalen.` | 对 |
| `Eingabealphabet wird zu Terminalalphabet.` | 对 |
| `Startzustand wird Startsymbol.` | 对 |
| `Endzustände brauchen keine λ-Regel.` | 通常错 |

### 14.3 记忆方法

```text
Automat läuft von Zustand zu Zustand.
Grammatik produziert von Nichtterminal zu Nichtterminal.
所以 Zustand ↔ Nichtterminal。
```

---

## 15. 知识卡片十四：Entscheidbarkeit 和 Church'sche These

### 15.1 Entscheidbarkeit

```text
Ein Problem heißt entscheidbar, wenn es eine Turingmaschine gibt, die für jede Eingabe hält und korrekt Ja/Nein antwortet.
```

中文：

可判定 = 存在一台 TM，对每个输入都停机，并给出正确答案。

### 15.2 Church'sche These

```text
Alle intuitiv berechenbaren Funktionen können durch eine Turingmaschine berechnet werden.
```

注意：

```text
Die Church'sche These ist kein mathematisch beweisbarer Satz.
```

### 15.3 LNW 会怎么问

| 选项 | 判断 |
|---|---|
| `Entscheidbar bedeutet, dass die TM für jede Eingabe hält.` | 对 |
| `Akzeptierbar bedeutet automatisch entscheidbar.` | 错 |
| `Church'sche These ist ein bewiesener mathematischer Satz.` | 错 |
| `TM dient als Modell für Berechenbarkeit.` | 对 |

---

## 16. 德语关键词小词典

| 德语 | 中文 |
|---|---|
| `Menge` | 集合 |
| `Teilmenge` | 子集 |
| `Zeichen` | 符号 |
| `Wort` | 词 |
| `Eingabe` | 输入 |
| `Zustand` | 状态 |
| `Startzustand` | 初始状态 |
| `Endzustand` | 终态 |
| `Übergangsfunktion` | 转移函数 |
| `Keller` | 栈 |
| `Kelleralphabet` | 栈字母表 |
| `Kellerbodensymbol` | 栈底符号 |
| `vollständig gelesen` | 完全读完 |
| `hält` | 停机 |
| `wird akzeptiert` | 被接受 |
| `wird verworfen` | 被拒绝 |
| `verschmolzen` | 被合并 |
| `entfernt` | 被移除 |
| `markiert` | 被标记 |
| `erreichbar` | 可达 |
| `nicht erreichbar` | 不可达 |

---

## 17. 选项判断训练模板

考试时每个选项都按这个模板处理：

```text
1. 这句话的主语是什么？
   DEA / NEA / TM / KA / Grammatik / LBA?

2. 它在说定义、函数形式、接受条件，还是算法步骤？

3. 如果是函数形式：
   定义域和值域是否正确？
   有没有漏掉 P(S)、K*、λ？

4. 如果是接受条件：
   是终态接受、空栈接受、至少一条路径，还是所有路径？

5. 如果出现强词：
   jeder / stets / automatisch / genau dann
   先特别小心。
```

---

## 18. 7 天复习安排

### 第 1 天：德语题干 + 基础语言

任务：

- 背第 1 节德语句型。
- 背 Alphabet/Wort/Sprache。
- 练习区分 `λ`、`{λ}`、`∅`。

目标：

```text
看到 Alphabet 题，10 秒内判断。
```

### 第 2 天：TM, Akzeptor, LBA

任务：

- 背 `(v,s,w)` 和 `(λ,s0,w)`。
- 背 Akzeptor vs Entscheider。
- 背 LBA 的 `k·|w|+c`。

目标：

```text
看到 hält / akzeptiert / entscheidet 不混。
```

### 第 3 天：DEA, NEA

任务：

- 背 `δ` 和 `δ*`。
- 背 NEA 的 `P(S)` 和 `mindestens ein Rechenpfad`。
- 练习读 DEA 图。

目标：

```text
看到 δ(s0,w) 能立刻判断是否类型错误。
```

### 第 4 天：KA, NKA

任务：

- 背 KA 的 `δ:S×(E∪{λ})×K→S×K*`。
- 理解两个 λ 的区别。
- 背课件中 KA 按终态接受。

目标：

```text
看到 K 和 K* 不混。
```

### 第 5 天：Minimierung, Äquivalenzrelation

任务：

- 背 markiert/unmarkiert 的含义。
- 背 reflexiv/symmetrisch/transitiv。
- 背 Quotientenmenge。

目标：

```text
知道最后合并 unmarkiert，不是 markiert。
```

### 第 6 天：Grammatik, Chomsky, Moore/Mealy

任务：

- 背 `G=(N,T,P,S)`。
- 背 `L(G)`。
- 背 Typ 0/1/2/3 对应自动机。
- 背 Moore/Mealy 区别。

目标：

```text
看到 γ:S→A 判断 Moore，看到 γ:S×E→A 判断 Mealy。
```

### 第 7 天：综合刷题

任务：

- 重新做 `AFS_LNW_Fragen_Review.md` 的 1-12 题。
- 每个错选项都写一句“为什么错”。
- 只复习本文件的“LNW 会怎么问”表格。

目标：

```text
不是背答案，而是能解释每个选项为什么对或错。
```

---

## 19. 考前最后 30 分钟只看这些

```text
Alphabet = nichtleer + endlich.
λ ∈ A*, aber λ ≠ ∅.
Sprache über A = Teilmenge von A*.
TM-Konfiguration = (v,s,w).
Startkonfiguration = (λ,s0,w).
Akzeptor kann bei Nichtakzeptanz nicht halten.
Entscheider hält auf jeder Eingabe.
LBA: k,c fest, Platz k·|w|+c.
DEA: δ:S×E→S, δ*:S×E*→S.
DEA akzeptiert w ⇔ δ*(s0,w)∈F.
NEA: δ:S×E→P(S), mit λ: S×(E∪{λ})→P(S).
NEA akzeptiert bei mindestens einem akzeptierenden Rechenpfad.
KA: δ:S×(E∪{λ})×K→S×K*.
KA links K, rechts K*.
Moore: γ:S→A, Ausgabe im Zustand.
Mealy: γ:S×E→A, Ausgabe an der Kante.
Minimierung: markiert = nicht verschmelzen, unmarkiert = verschmelzen.
Äquivalenzrelation = reflexiv + symmetrisch + transitiv.
Grammatik: G=(N,T,P,S), N∩T=∅, S∈N.
L(G)={w∈T* | S⇒*w}.
Typ 0-TM, Typ 1-LBA, Typ 2-KA, Typ 3-EA.
```
