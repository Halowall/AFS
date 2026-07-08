# AFS LNW 导向型全课复习大纲

> 目标：不是按课件顺序机械复习，而是根据 LNW 多选题的提问方式，反推整门 Vorlesung 中应该重点准备什么。  
> 考试形式：`Welche der folgenden Aussagen sind richtig?`，每题 0 到 4 个正确答案都有可能。  
> 配套文件：具体图片题 1-12 的逐题答案见 `AFS_LNW_Fragen_Review.md`。

---

## 0. LNW 的真正考法

LNW 不主要考“你会不会推一个很长的证明”，而是考你能不能精确判断定义、函数类型、接受条件和符号含义。

典型题型有 8 类：

| 题型 | LNW 例子 | 你要训练的能力 |
|---|---|---|
| 定义判断 | Alphabet、Sprache、Grammatik | 看一句定义是否完整、是否多了错误条件 |
| 函数类型判断 | DEA/NEA/KA 的 `δ` | 看定义域和值域是否写对 |
| 接受条件判断 | TM、DEA、NEA、KA | 区分终态、停机、空栈、存在路径 |
| Konfiguration 判断 | TM Startkonfiguration | 记住三元组顺序 |
| 自动机图读语言 | DEA 图判断词是否接受 | 从图总结语言，而不是只逐字模拟 |
| 算法步骤判断 | DEA-Minimierung | 记住步骤顺序和“标记/未标记”的意义 |
| 数学关系判断 | Äquivalenzrelation | 检查 reflexiv/symmetrisch/transitiv |
| 形式语法判断 | `G=(N,T,R,S)`、`L(G)` | 区分终结符、非终结符、推导语言 |

做每个选项时先问自己四个问题：

```text
1. 题目对象是谁？DEA, NEA, TM, KA, Grammatik?
2. 这是确定型还是非确定型？
3. 这个公式的类型对不对？
4. 这句话是不是把“接受、停机、判定、读完输入”混在一起了？
```

---

## 1. 复习优先级

### Prio A: 必须非常熟

这些是 LNW 已经直接出现的题型，也最容易继续以多选形式出现。

| 主题 | 对应 Vorlesung/Wissensbasis | LNW 会怎么问 |
|---|---|---|
| Alphabet, Wort, `λ`, `A*`, Sprache | Abschnitt 2-5 | 哪些定义正确？`λ∈A*` 对不对？Alphabet 是否可以无限？ |
| TM Konfiguration | Abschnitt 7-10 | Startkonfiguration 是 `(λ,s0,w)` 还是其他顺序？ |
| Akzeptor-TM | Abschnitt 8, 32 | 接受、不接受、停机、判定是不是同一回事？ |
| LBA | Abschnitt 11 | `k,c` 是否固定？是否依赖输入？空间是否随 `|w|` 变化？ |
| DEA/`δ*` | Abschnitt 14-15 | `δ` 和 `δ*` 哪个读词？接受条件怎么写？ |
| NEA mit `λ` | Abschnitt 21 | `δ` 是否到 `P(S)`？是否至少一条路径接受？ |
| KA | Abschnitt 12-13 | `δ:S×(E∪{λ})×K→S×K*` 怎么判断？ |
| DEA-Minimierung | Abschnitt 17 | 标记表中哪些状态对先标记？最后合并谁？ |
| Äquivalenzrelation | Abschnitt 16 | reflexiv/symmetrisch/transitiv，商集怎么写？ |
| Formale Grammatik | Abschnitt 24-25 | `N∩T=∅`、`S∈N`、`L(G)` 定义 |

### Prio B: 同样可能按 LNW 方式出现

这些内容在图片题里不一定全部出现，但它们和已有题型非常接近，适合用同样的判断方法准备。

| 主题 | 对应 Vorlesung/Wissensbasis | 可能的 LNW 问法 |
|---|---|---|
| Potenzmenge | Abschnitt 19, 21 | `P(S)` 是什么？为什么 NEA 的结果是集合？ |
| NTM | Abschnitt 19 | 非确定型 TM 是否“至少一条计算路径接受”？ |
| NKA | Abschnitt 20 | NKA 的 `δ` 是否到 `P(S×K*)`？ |
| Moore/Mealy | Abschnitt 18 | Ausgabe 在状态还是在边上？`γ` 的类型是什么？ |
| Chomsky-Hierarchie | Abschnitt 26-27 | Typ 0/1/2/3 的规则限制和对应自动机 |
| Automat ↔ Grammatik | Abschnitt 29 | DEA 如何转 Typ-3 Grammatik？ |
| Entscheidbarkeit | Abschnitt 31-32 | `entscheidbar` 是否表示对所有输入停机？ |

### Prio C: 了解即可，但要会判断一句话真假

| 主题 | 准备程度 |
|---|---|
| Protagonisten | 记住 Turing、Church、Chomsky 等名字和关键词 |
| Deutsche Grammatik: NP/VP/PP | 会判断 `NP, VP, PP` 是短语类型 |
| 常见语言模式 | 知道正则、上下文无关、上下文有关大致对应什么自动机 |

---

## 2. 模块一：形式语言基础

对应 LNW：Aufgabe 1  
对应课件：Alphabet, Wort, Sternhülle, Sprache

### 必须掌握

```text
Alphabet: nichtleere, endliche Menge von Zeichen
Wort: endliche Folge von Zeichen
λ: leeres Wort, Länge 0
A*: Menge aller endlichen Wörter über A, inklusive λ
A+: A* ohne λ
Sprache über A: jede Teilmenge L ⊆ A*
```

### LNW 会怎么设陷阱

| 错误选项类型 | 为什么错 |
|---|---|
| Alphabet kann unendlich viele Zeichen enthalten | Alphabet 必须有限 |
| `λ` 是 Alphabet 的元素 | 通常不是，`λ` 是词，不是 Zeichen |
| `∅` 和 `{λ}` 一样 | 不一样，`∅` 没有任何词，`{λ}` 有一个空词 |
| Sprache muss endlich sein | 语言可以无限 |

### 你要会这样判断

如果题目出现：

```text
Sei A ein Alphabet.
```

马上联想：

```text
A ist endlich und nichtleer.
λ ∈ A*.
L ⊆ A* heißt Sprache über A.
```

---

## 3. 模块二：Turingmaschine 与 Akzeptor

对应 LNW：Aufgabe 2, 3  
对应课件：DTM、Akzeptor-TM、Konfiguration、Entscheidbarkeit

### 必须掌握

```text
DTM: T = (E, B, S, δ, s0)
Akzeptor-TM: T = (E, B, S, δ, s0, F)
Konfiguration: (v, s, w)
Startkonfiguration bei w ≠ λ: (λ, s0, w)
L(T): Menge aller von T akzeptierten Wörter
```

### 接受、停机、判定要分清

| 概念 | 德语 | 判断标准 |
|---|---|---|
| 接受 | akzeptieren | 机器停在 `F` 中的状态 |
| 不接受 | nicht akzeptieren | 可能停在非终态，也可能不停机 |
| 判定 | entscheiden | 对每个输入都停机并给出 Ja/Nein |
| 语言 | `L(T)` | 所有被接受的词 |

### LNW 会怎么设陷阱

| 错误选项类型 | 为什么错 |
|---|---|
| Nicht akzeptieren bedeutet immer halten | Akzeptor 可能永远不停机 |
| Akzeptieren = Entscheiden | Entscheiden 更强 |
| Startkonfiguration 是 `(s0,λ,w)` | TM 配置顺序是 `(v,s,w)` |
| `L(T)` 是所有让机器停机的词 | `L(T)` 是所有被接受的词 |

---

## 4. 模块三：LBA

对应 LNW：Aufgabe 4  
对应课件：Linear beschränkter Automat

### 必须掌握

```text
Ein LBA ist eine Turingmaschine mit linear beschränktem Band.
Für eine Eingabe w dürfen höchstens k·|w|+c Bandfelder verwendet werden.
k und c sind feste natürliche Zahlen.
```

### LNW 判断重点

| 说法 | 判断 |
|---|---|
| `k,c` hängen nicht von der konkreten Eingabe ab | 对 |
| `k,c` dürfen nachträglich passend gewählt werden | 错 |
| `k,c` können negativ sein | 错 |
| `|w|` beeinflusst den erlaubten Platz nicht | 错 |

### 复习方法

记住一句话即可应对多数 LBA 选择题：

```text
Der Speicherplatz ist linear in der Eingabelänge, aber die Konstanten k und c sind fest.
```

---

## 5. 模块四：DEA

对应 LNW：Aufgabe 5, 6, 10  
对应课件：DEA、DEA Beispiel、Minimierung

### 必须掌握

```text
DEA: A = (E, S, δ, s0, F)
δ : S × E → S
δ*: S × E* → S
w ∈ L(A) ⇔ δ*(s0,w) ∈ F
```

### 图题怎么准备

看到 DEA 图时按这个顺序：

1. 找 Startzustand。
2. 找 Endzustände。
3. 看每个输入符号对状态的作用。
4. 总结语言，例如“奇数个 d”、“包含 aa”、“以 b 结尾”。
5. 再判断每个给出的 Wort。

LNW 图题常见陷阱：

| 错误方式 | 正确方式 |
|---|---|
| 只看最后一个符号 | 要看整个状态变化 |
| 忽略 Startzustand | 必须从 `s0` 开始 |
| 忽略 Endzustand 双圈 | 只有终态结束才接受 |
| 把 `δ` 当成能读整个词 | 读整个词要用 `δ*` |

### DEA-Minimierung 必须掌握

```text
1. Nicht erreichbare Zustände entfernen.
2. Paare markieren, bei denen genau ein Zustand in F liegt.
3. Weitere Paare markieren, wenn sie auf ein bereits markiertes Paar führen.
4. Am Ende unmarkierte Paare verschmelzen.
```

选择题核心：

```text
markiert = unterscheidbar = nicht verschmelzen
unmarkiert = äquivalent = verschmelzen
```

---

## 6. 模块五：NEA 与 Potenzmenge

对应 LNW：Aufgabe 7  
对应课件：NEA、Potenzmengenkonstruktion、NTM/NKA 的非确定思想

### 必须掌握

```text
NEA: δ : S × E → P(S)
NEA mit λ-Übergängen: δ : S × (E ∪ {λ}) → P(S)
P(S): Potenzmenge von S, also Menge aller Teilmengen von S
```

### 接受条件

```text
Ein NEA akzeptiert ein Wort, wenn mindestens ein Rechenpfad nach dem vollständigen Lesen des Wortes in einem Endzustand endet.
```

### LNW 会怎么设陷阱

| 错误选项类型 | 为什么错 |
|---|---|
| `δ:S×E→S` | 这是 DEA，不是 NEA |
| jeder Rechenpfad muss akzeptieren | NEA 只需要至少一条路径接受 |
| λ-Übergang verbraucht ein Zeichen | λ-Übergang 不消耗输入 |
| `P(S)` 是状态中的一个元素 | `P(S)` 是所有状态子集的集合 |

### 关联复习

NTM 和 NKA 也常用类似思想：

```text
nichtdeterministisch = mehrere mögliche nächste Schritte
akzeptiert = mindestens ein akzeptierender Rechenpfad existiert
```

---

## 7. 模块六：Kellerautomat

对应 LNW：Aufgabe 8, 9  
对应课件：KA 定义、KA 操作、Konfiguration、NKA

### 必须掌握

```text
KA: A = (E, K, S, δ, s0, F)
δ : S × (E ∪ {λ}) × K → S × K*
Konfiguration: (s, w, v)
Startkonfiguration: (s0, w, k0)
```

### `δ` 的每个位置怎么理解

```text
δ(s, e, k) = (s', v)
```

| 符号 | 含义 |
|---|---|
| `s` | 当前状态 |
| `e` | 输入符号，或 `λ` 表示不读输入 |
| `k` | 当前栈顶符号 |
| `s'` | 新状态 |
| `v∈K*` | 替换栈顶的 Kellerwort |

### LNW 会怎么设陷阱

| 错误公式 | 错因 |
|---|---|
| `S×(E∪{λ})×K → S×K` | 右边应是 `K*`，因为可能写入多个符号或 `λ` |
| `S×(K∪{λ})×K → S×K*` | 第二个位置应是输入字母表 `E`，不是 Kelleralphabet |
| `S×(E∪{λ})×K* → S×K*` | 左边只看栈顶一个符号 `K`，不是整个栈 |
| 栈清空就一定接受 | 课件中按终态接受 |

### 接受条件

这门课的 LNW 要按课件定义：

```text
vollständig gelesen + hält in einem Zustand aus F
```

不要自动套用“leerer Keller”。

---

## 8. 模块七：Moore 和 Mealy Automaten

对应 LNW：图片中未出现，但属于同类选择题高风险内容  
对应课件：Endliche Automaten mit Ausgabe

### 必须掌握

| 类型 | 输出在哪里 | Ausgabefunktion |
|---|---|---|
| Moore | 状态上 | `γ:S→A` |
| Mealy | 边/转移上 | `γ:S×E→A` |

### LNW 可能问法

| 说法 | 判断 |
|---|---|
| Beim Moore-Automaten hängt die Ausgabe nur vom Zustand ab | 对 |
| Beim Mealy-Automaten hängt die Ausgabe vom Zustand und Eingabezeichen ab | 对 |
| Beim Moore-Automaten steht die Ausgabe an der Kante | 错 |
| Beim Mealy-Automaten hat `γ` die Form `S→A` | 错 |

一句话背诵：

```text
Moore: Ausgabe im Zustand. Mealy: Ausgabe an der Kante.
```

---

## 9. 模块八：Äquivalenzrelation 与 Quotientenmenge

对应 LNW：Aufgabe 11  
对应课件：Äquivalenzrelationen、DEA-Minimierung 的等价思想

### 必须掌握

等价关系必须同时满足：

```text
reflexiv: a ~ a
symmetrisch: a ~ b ⇒ b ~ a
transitiv: a ~ b und b ~ c ⇒ a ~ c
```

商集：

```text
X/~ = {[a]~ | a ∈ X}
```

### LNW 会怎么设陷阱

| 错误选项类型 | 为什么错 |
|---|---|
| “größer als / grüner als” 是等价关系 | 通常不是 reflexiv，也不是 symmetrisch |
| 只满足一个性质就是等价关系 | 必须三个都满足 |
| `X/~ = {[a]~ | [a]~ ∈ X}` | `[a]~` 是等价类，不是 `X` 中的元素 |

---

## 10. 模块九：Formale Grammatik

对应 LNW：Aufgabe 12  
对应课件：Deutsche Grammatik、Phrasentypen、Formale Grammatik、Ableitung、Chomsky-Hierarchie

### 必须掌握

```text
G = (N, T, R, S)
N: Nichtterminale
T: Terminale
R: Regeln / Produktionen
S: Startsymbol
N ∩ T = ∅
S ∈ N
L(G) = { w ∈ T* | S ⇒*_G w }
```

### 产生式判断

普通形式语法中：

```text
linke Seite einer Produktion muss mindestens ein Nichtterminal enthalten
```

所以“左边只由 Terminalsymbolen 组成”是错的。

### Chomsky-Hierarchie 也要准备

| Typ | 语言 | 对应自动机 | 多选题关键词 |
|---|---|---|---|
| Typ 0 | rekursiv aufzählbar | Turingmaschine | 无限制 |
| Typ 1 | kontextsensitiv | LBA | 长度不减少 |
| Typ 2 | kontextfrei | Kellerautomat | 左边一个非终结符 |
| Typ 3 | regulär | endlicher Automat | rechtslinear/linkslinear |

LNW 可能问法：

| 说法 | 判断方向 |
|---|---|
| Jede Typ-3-Sprache ist regulär | 对 |
| Typ-2-Grammatiken entsprechen Kellerautomaten | 对 |
| Typ 1 darf beliebig verkürzen | 错，通常长度不减少 |
| In Typ 2 steht links genau ein Nichtterminal | 对 |

---

## 11. 模块十：Automat ↔ Grammatik

对应课件：Automat ↔ Grammatik  
LNW 可能把它写成规则判断题。

### DEA 到 Typ-3 Grammatik

必须记住：

```text
Zustände werden Nichtterminale.
Eingabealphabet wird Terminalalphabet.
Startzustand wird Startsymbol.
δ(s,e)=s' wird Produktion s → e s'.
Für Endzustände gibt es Produktionen s → λ.
```

常见错误选项：

| 错误说法 | 为什么错 |
|---|---|
| Terminale 是状态集合 | 状态对应 Nichtterminale |
| Startsymbol 是任意状态 | Startsymbol 对应 Startzustand |
| Endzustand 不需要 λ-Regel | 通常需要 `s→λ` 表示词可以结束 |

---

## 12. 模块十一：Entscheidbarkeit 与 Church'sche These

对应课件：Church 论题、Entscheidbarkeit  
图片 LNW 没直接出现，但非常适合多选判断。

### 必须掌握

```text
Ein Problem ist entscheidbar, wenn es eine Turingmaschine gibt,
die für jede Eingabe hält und korrekt Ja/Nein antwortet.
```

```text
Church'sche These:
Alles intuitiv Berechenbare ist Turing-berechenbar.
Sie ist keine mathematisch beweisbare Aussage.
```

LNW 可能问法：

| 说法 | 判断 |
|---|---|
| Entscheidbar bedeutet: TM hält für jede Eingabe | 对 |
| Akzeptierbar bedeutet automatisch entscheidbar | 错 |
| Church'sche These ist ein bewiesener Satz | 错 |
| Eine TM kann als Modell für Berechenbarkeit dienen | 对 |

---

## 13. 考前复习路线

### 第一步：背函数类型

先把下面这些默写出来：

```text
DEA: δ:S×E→S
NEA: δ:S×E→P(S)
NEA mit λ: δ:S×(E∪{λ})→P(S)
KA: δ:S×(E∪{λ})×K→S×K*
NKA: δ:S×(E∪{λ})×K→P(S×K*)
TM-Konfiguration: (v,s,w)
KA-Konfiguration: (s,w,v)
Moore: γ:S→A
Mealy: γ:S×E→A
```

### 第二步：背接受条件

```text
DEA: δ*(s0,w) ∈ F
NEA: mindestens ein akzeptierender Rechenpfad
TM-Akzeptor: hält in einem Zustand aus F
KA in dieser Vorlesung: vollständig gelesen und hält in F
Entscheider: hält auf jeder Eingabe
```

### 第三步：训练真假判断

用下面这个模板检查每个选项：

```text
Ist die Aussage eine Definition?
Ist die Funktion vom richtigen Typ?
Wird ein Wort oder nur ein Zeichen gelesen?
Ist die Aussage zu stark, z.B. "jeder", "stets", "automatisch"?
Passt sie zur Vorlesungskonvention?
```

### 第四步：针对图题训练

对每个 DEA 图都写一句语言描述：

```text
Dieser Automat akzeptiert genau die Wörter, die ...
```

比如：

```text
... eine ungerade Anzahl von d enthalten.
... mit a enden.
... das Teilwort aa enthalten.
```

如果你能把图翻译成一句语言描述，选择题会快很多。

---

## 14. 最小可背清单

如果时间很少，至少背这 12 句：

```text
Ein Alphabet ist endlich und nichtleer.
Das leere Wort λ liegt immer in A*.
Eine Sprache über A ist eine Teilmenge von A*.
Die Startkonfiguration einer TM bei w≠λ ist (λ,s0,w).
Ein Akzeptor muss bei Ablehnung nicht halten.
Entscheiden bedeutet Halten auf jeder Eingabe.
Beim LBA sind k und c feste natürliche Zahlen.
Beim DEA gilt w∈L(A) genau dann, wenn δ*(s0,w)∈F.
Beim NEA genügt mindestens ein akzeptierender Rechenpfad.
Beim KA lautet δ:S×(E∪{λ})×K→S×K*.
Bei der DEA-Minimierung werden am Ende unmarkierte Zustände verschmolzen.
Bei einer Grammatik gilt N∩T=∅, S∈N und L(G)={w∈T* | S⇒*w}.
```

---

## 15. 如何使用这份大纲

建议顺序：

1. 先读本文件，建立 LNW 的出题地图。
2. 再读 `AFS_LNW_Fragen_Review.md`，看图片题 1-12 每个选项为什么对错。
3. 最后回到 `AFS_Wissensbasis.md`，只补本大纲中对应模块的定义和公式。

不要把所有课件逐页重读。LNW 的题型更偏向精确定义和真假判断，所以复习重点应该是：

```text
Definitionen + Funktionssignaturen + Akzeptanzbedingungen + typische falsche Aussagen
```
