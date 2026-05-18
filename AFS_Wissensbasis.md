# Automaten und Formale Sprachen — 知识点总结 / Wissensbasis

> **格式说明 / Hinweis zum Format:**
> 每个知识点先写德语（**fett**），下方缩进写中文解释。
> Jeder Wissenspunkt: zuerst Deutsch (**fett**), darunter eingerückt Chinesisch.

---

## 1. 理论计算机科学四大领域 / Vier Teilgebiete der Informatik

**Technische Informatik**
  技术信息学：研究计算机内部结构和硬件制造。
  Befasst sich mit der inneren Struktur und dem Bau von Computern.

**Praktische Informatik**
  实用信息学：编程原理和技术。
  Umfasst die Prinzipien und Techniken der Programmierung.

**Angewandte Informatik**
  应用信息学：信息学方法与应用问题之间的桥梁。
  Bildet die Brücke zwischen Informatik-Methoden und Anwendungsproblemen.

**Theoretische Informatik**
  理论信息学：开发计算机的数学模型及其精确描述工具。基础是数学（逻辑和集合论）。核心工具是图灵机。
  Entwickelt mathematische Modelle von Computern. Basis: Mathematik (Logik, Mengenlehre). Kerninstrument: Turingmaschine (TM).

---

## 2. 字母表 / Alphabet

**Definition: Ein Alphabet A = {a₁, …, aₙ} ist eine nichtleere, endliche Menge von Zeichen (Symbolen).**
  定义：字母表 A 是一个非空的、有限的字符（符号）集合。
  - 例：A = {a, b}、A = {0, 1} ✓
  - N（自然数集）不是字母表（无限集）✗
  - ∅ = {} 不是字母表（空集）✗
  - 单元素集 {a} 是字母表 ✓

**Achtung: Es gibt verschiedene Definitionen (z. B. Tupel vs. Menge).**
  注意：不同文献对字母表的定义有差异。

---

## 3. 词 / Wort

**Definition: Ein Wort x = x₁…xₙ ist eine Folge von n Zeichen (Länge n ∈ ℕ).**
  定义：词是由 n 个字符组成的序列（长度为 n）。

**Leeres Wort λ (auch ε): Spezialfall mit Länge 0. Kann über jedem Alphabet gebildet werden.**
  空词 λ（也写作 ε）：长度为 0 的特殊情况。可以在任何字母表上构成。
  - |λ| = 0
  - λ ≠ ⋆（⋆ 是带上的空白符号，λ 是词）

**Aⁿ = {x₁…xₙ | xᵢ ∈ A}，其中 A⁰ = {λ}**
  A 的 n 次幂：所有由 A 中符号组成的长度为 n 的词的集合。0 次幂 = {λ}。

---

## 4. 克莱尼星号 / Kleene'sche Hülle (Sternhülle)

**A* = ⋃ₙ≥₀ Aⁿ —— 所有由 A 中符号组成的词的集合（包括 λ）**
  A 的星号闭包 = 所有可能长度的词的并集。包含空词。

**Beispiel: A = {a, b}**
  - A⁰ = {λ}
  - A¹ = {a, b}
  - A² = {aa, ab, ba, bb}
  - A³ = {aaa, aab, aba, abb, baa, bab, bba, bbb}
  - A* = {λ, a, b, aa, ab, ba, bb, aaa, …}

---

## 5. 形式语言 / Formale Sprache

**Definition: Jede Teilmenge L ⊆ A* heißt Sprache über dem Alphabet A.**
  定义：A* 的任意子集都是 A 上的一个形式语言。
  - L = {λ, a, bb, aab} 是 {a, b} 上的语言 ✓
  - ∅（空集）是语言 ✓
  - 包含不属于 A 的符号的集合不是该字母表上的语言 ✗

---

## 6. 两种问题类型 / Zwei Problemarten

**Entscheidungsproblem（判定问题）**
  Ausgabe: nur Ja oder Nein（输出：只有是/否）
  - 例：这个数是质数吗？这个词属于某个语言吗？
  - 用语言 L 描述：w ∈ L 或 w ∉ L

**Berechnungsproblem（计算问题）**
  Ausgabe: konkretes Wort / Zahl / Struktur（输出：具体的词/数/结构）
  - 例：计算最大公约数、质因数分解、求词的长度
  - 用函数 f 描述：w ↦ f(w)

**两者可以互相转换 / Beide sind ineinander überführbar:**
  - 判定 → 计算：f(w) = 1 (Ja) 或 0 (Nein)
  - 计算 → 判定：问 f(w) = u? 或第 i 个字符是什么？
  - 函数的图 Gf = {(w, u) | u = f(w)} 将计算转为判定

---

## 7. 确定型图灵机 / Deterministische Turingmaschine (DTM)

**Definition: T = (E, B, S, δ, s₀)**
  五元组定义：

| 符号 | 德语 | 中文 | 含义 |
|------|------|------|------|
| **E** | Eingabealphabet | 输入字母表 | 输入可以包含的所有字符（不含 ⋆） |
| **B** | Bandalphabet | 带字母表 | 带上可以出现的所有字符（含 E 和 ⋆） |
| **S** | Zustandsmenge | 状态集 | 有限状态集合 |
| **δ** | Zustandsübergangsfunktion | 状态转移函数 | δ: S × B → S × B × {R, L, N}（部分函数） |
| **s₀** | Startzustand | 起始状态 | s₀ ∈ S |

**δ(s, b) = (s', b', R) 的含义：**
  在状态 s，读到带上的符号 b 时：
  - 将 b 改写为 b'
  - 切换到状态 s'
  - 读写头向右移动一格（R = rechts）
  - 也可选 L（links，向左）或 N（neutral，不动）
  - 若 δ 对 (s, b) 无定义，则 TM 停机

**Turingtafel（图灵表）：**
  行 = 状态 s ∈ S，列 = 带符号 b ∈ B
  单元格 [s, b] = δ(s, b) 的转移指令

**初始状态 / Start:**
  带上写有输入 w ∈ E*，读写头在 w 的第一个字符上。
  若 w = λ，读写头在 ⋆ 上。

---

## 8. 图灵机作为接受器 / Akzeptor-Turingmaschine

**Definition: T = (E, B, S, δ, s₀, F)**
  比基本 TM 多了 F：
  - **F ⊆ S** = 接受终止状态集（akzeptierende Endzustände）
  - 在 F 中停机 = 接受（akzeptiert）
  - 在 S \ F 中停机 = 拒绝（verworfen）
  - 不停机 = 也视为不接受

**Akzeptierte Sprache L(T) = {w ∈ E* | T akzeptiert w}**
  T 接受的語言 = 所有被 T 接受的词的集合。

**重要区别 / Wichtiger Unterschied:**
  - **Akzeptieren（接受）** ≠ **Entscheiden（判定）**
  - 判定要求对每种输入都停机（要么接受、要么拒绝）
  - 接受器可能在非接受的输入上永远运行

| T 的行为 | L(T) 中的含义 | fT(w) |
|----------|--------------|-------|
| 接受 w | w ∈ L(T) | 1 |
| 拒绝 w | w ∉ L(T) | 0 |
| 不停机 | w ∉ L(T) | 未定义 |

---

## 9. 格局 / Konfiguration

**Definition: (v, s, w) ∈ B* × S × B***
  三元组描述 TM 的完整快照：
  - **s** = 当前状态
  - **v** = 读写头左侧的带内容
  - **w** = 从读写头位置开始向右的带内容
  - 整条带的内容 = vw

**Startkonfiguration / 初始格局:**
  - 输入 w ≠ λ：(λ, s₀, w)
  - 输入 w = λ：(λ, s₀, ⋆)

**Übergangsrelation ⊢（转移关系）:**
  描述格局之间的一步转移。
  例：(λ, s₀, 00110) ⊢ (0, s₀, 0110) ⊢ (00, s₀, 110) ⊢ …
  读写头逐步向右移动，状态可能改变。

---

## 10. 线性有界自动机 / Linear beschränkter Automat (LBA)

**为什么需要 LBA / Warum LBA?**
  TM 有无限长的带 → 现实中不存在。LBA 限制了可用空间。

**原理 / Prinzip:**
  → s₀ ←
  $L e₁ e₂ … eₙ ⋆ … ⋆ $R
  读写头只能在 $L 和 $R 之间移动。

**空间限制 / Platzschranke:**
  最多可用 **k · |w| + c** 个带格子
  - k, c 是固定的自然数（不依赖具体输入）
  - |w| = 输入长度
  - 例：w = baum, |w|=4, k=2, c=3 → 最多 2×4+3 = 11 格

**LBA 的优点:**
  - 比 TM 更贴近实际计算机
  - 仍然足够强大解决很多问题

---

## 11. 下推自动机 / Kellerautomat (KA)

**直观理解 / Intuition:**
  需要一个自动机，不仅有状态，还能在读入过程中「记住」信息。
  例如：读入 r 时存一层，读入 g 时消一层 → 这就是栈（Keller/Stack）。

**原理：LIFO (Last-In-First-Out) / 后进先出**
  最后放进去的东西最先被取出。
  例：一摞盘子、浏览器的后退按钮、函数调用栈。

**FILO (First-In-Last-Out) = LIFO**：同一个原理，只是叫法不同。

**Definition: A = (E, K, S, δ, s₀, F)**

| 符号 | 德语 | 中文 |
|------|------|------|
| **E** | Eingabealphabet | 输入字母表 |
| **K** | Kelleralphabet | 栈字母表（含 k₀ = 栈底标记） |
| **S** | Zustandsmenge | 有限状态集 |
| **δ** | Zustandsübergangsfunktion | 转移函数 |
| **s₀** | Startzustand | 起始状态 |
| **F** | akzeptierende Endzustände | 接受状态集 |

**转移函数 δ: S × (E ∪ {λ}) × K → S × K***
  δ(s, e, k) = (s', v) 的含义：
  - 当前状态 s
  - 读入字符 e ∈ E（或 λ）
  - 栈顶符号 k
  - → 新状态 s'，栈顶 k 被替换为 v ∈ K*（一个词）

**两种转移类型 / Zwei Varianten:**
  1. δ(s, e, k) = (s', v)：读一个输入符号 e，栈顶 k → v
  2. δ(s, λ, k) = (s', v)：**λ-Übergang**，不读输入，只操作栈

**λ-Übergang 的优势：**
  允许自动机在不消耗输入的情况下改变状态或栈内容。
  例如：发现栈底标记 k₀ 时，自动进入接受状态。

**栈操作 / Kelleroperationen:**
  - δ(s, a, k₀) = (s, Ak₀)：读 a，将 A 压入栈（A 在 k₀ 上方）
  - δ(s, a, A) = (s, AA)：读 a，再压一个 A
  - δ(s, b, A) = (s, λ)：读 b，弹出 A（栈顶 A 被移除）
  - δ(s, λ, k₀) = (se, k₀)：不读输入，看到栈底就进入接受状态

**典型应用 / Typisches Beispiel:**
  语言 aⁿbⁿ（n 个 a 后跟 n 个 b）：
  - 读每个 a → 向栈中压入 A
  - 读每个 b → 从栈中弹出一个 A
  - 读完且栈空（只剩 k₀）→ 接受
  - 这不能用有限状态自动机实现，必须用栈！

**KA 的格局 / Konfiguration eines KA:**
  (s, Restwort, Kellerinhalt)
  例：(s₀, abba, k₀) ⊢ (s₁, bba, Ak₀) ⊢ …

**转移关系 ⊢KA** 是 (S × E* × K*) × (S × E* × K*) 的子集。

---

## 12. 有限自动机 / Endlicher Automat (EA)

**Definition: EA = (E, S, δ, s₀, F)**

| 符号 | 含义 |
|------|------|
| E | 输入字母表 |
| S | 有限状态集 |
| δ | 转移函数 δ: S × E → S |
| s₀ | 起始状态 |
| F ⊆ S | 接受状态集 |

**工作原理:**
  - 从头到尾读输入词
  - 每次读一个字符，根据 δ 切换状态
  - 读完整个词后：若当前状态 ∈ F → 接受；否则拒绝

**接受的定义 / Akzeptieren eines Wortes w = x₁…xₙ:**
  存在状态序列 s₀, s₁, …, sₙ 满足 sᵢ = δ(sᵢ₋₁, xᵢ)，且 sₙ ∈ F。

**图形表示 / Graphische Darstellung:**
  - 圆圈 = 状态
  - 箭头 = 转移（标有输入字符）
  - 双圈 = 接受状态
  - 进入箭头 = 起始状态

**接受状态数量 / Anzahl akzeptierender Zustände:**
  可以有多个接受状态（≥ 0）。

**EA 实例 / Beispiel:**
  接受所有偶数值的二进制数（以 0 结尾）：
  - s₀: 读到 1 → s₁，读到 0 → s₀
  - s₁: 读到 1 → s₀，读到 0 → s₁
  - F = {s₀}

---

## 13. 非确定型有限自动机 / Nichtdeterministischer EA (NEA)

**与 DEA 的区别:**
  - δ: S × E → P(S)（映射到状态的幂集，即状态集合）
  - 同一输入下可以有多个可能的下一状态
  - 只要存在一条路径通向接受状态，就接受

**DEA 和 NEA 等价:** 每个 NEA 都可以转化为等价的 DEA（幂集构造法）。

---

## 14. Moore 与 Mealy 自动机

**Moore-Automat:**
  输出只依赖于当前状态。
  每个状态绑定一个输出值。
  例：在读到序列 011 时输出 1，其他输出 0。

**Mealy-Automat:**
  输出依赖于当前状态和当前输入。
  转移边上标有「输入/输出」。
  同样可以实现在读到 011 时输出 1。

---

## 15. 自动机最小化 / Minimierung

**目标:** 找到与给定 EA 等价但状态数最少的 EA。

**基本思路:**
  1. 移除不可达状态
  2. 合并等价状态（无法通过任何输入词区分出来的状态）
  3. 使用表填充算法（Table-Filling-Algorithm）

**等价关系 / Äquivalenzrelation:**
  - 反射性、对称性、传递性
  - n ∼ m ⇔ n−m 可被 k 整除（同余关系）
  - A₁ ∼ A₂ ⇔ A₁ 和 A₂ 接受相同的语言

---

## 16. 形式语法 / Formale Grammatik

**Definition: G = (N, T, S, P)**

| 符号 | 德语 | 中文 |
|------|------|------|
| **N** | Nichtterminale (Variablen) | 非终结符（变量，大写字母） |
| **T** | Terminale | 终结符（小写字母，实际字符） |
| **S** | Startsymbol | 起始符号（S ∈ N） |
| **P** | Produktionen | 产生式规则集 |

**Produktionen 产生式:**
  形式：α → β（α 至少含一个非终结符，β 是任意串）
  例：S → NP VP, NP → N, N → Hans

**推导 / Ableitung:**
  S → NP VP → N VP → Hans VP → Hans V NP → Hans sah NP → Hans sah Krokodil

**为什么恰好需要一个起始符号?**
  确保推导有明确的起点，否则无法确定从哪开始。

**注意:** 产生式 A → aA 会导致无限长词的可能。

---

## 17. 重要人物 / Protagonisten

| 人物 | 贡献 |
|------|------|
| **Kurt Gödel** | 不完备定理 |
| **Alan Turing** | 1936 年提出图灵机；判定问题 |
| **Emil Post** | Post 对应问题 |
| **John von Neumann** | 计算机体系结构 |
| **Alonzo Church** | λ 演算；Church 论题 |
| **Noam Chomsky** | 形式语言层级（Chomsky 层级） |

---

## 18. Church 论题 / Church'sche These

**内容:** 所有直观上「可计算」的函数都可以被图灵机计算。
  换句话说：图灵机精确地刻画了「可计算」的直觉概念。
  （这不是数学定理，而是无法被证明的论题。）

---

## 19. 可判定性 / Entscheidbarkeit

**一个问题称为可判定的 (entscheidbar)，当存在一个图灵机，对每个输入都停机并给出正确回答（Ja/Nein）。**
  关键：对**每个**输入都必须停机。

---

## 20. 常见语言模式 / Häufige Sprachmuster

| 语言 | 需要的最小自动机类型 |
|------|---------------------|
| 以某字符结尾的词 | EA (有限自动机) |
| 包含特定子串的词 | EA |
| aⁿbⁿ（n 个 a + n 个 b） | KA (下推自动机) 或更强 |
| w = u$ũ（回文带分隔符） | KA |
| aⁿbⁿcⁿ | TM / LBA |
| (ab)ⁿ(ba)ⁿ | KA |

---

## 21. 考试重点速查 / Klausur-Checkliste

- [x] Alphabet, Wort, λ, A*, Sprache 的定义
- [x] TM 五元组 (E, B, S, δ, s₀) 和 Turingtafel
- [x] Akzeptor-TM: F 集合，akzeptieren vs. entscheiden
- [x] Konfiguration (v, s, w) 和转移关系 ⊢
- [x] LBA: k·|w|+c 空间限制
- [x] KA 定义：E, K, S, δ, s₀, F + LIFO
- [x] λ-Übergang 的含义和优势
- [x] KA 的转移书写：δ(s, e, k) = (s', v)
- [x] EA 定义和图形表示
- [x] Moore vs Mealy
- [x] EA 最小化
- [x] 语法 G = (N, T, S, P) 和推导
- [x] Church 论题和可判定性
- [x] 判定问题 → 语言，计算问题 → 函数

---

*Erstellt am 18.05.2026 — Letzter Versuch, viel Erfolg! 🍀*
*创建于 2026年5月18日 — 最后一次机会，祝顺利！*
