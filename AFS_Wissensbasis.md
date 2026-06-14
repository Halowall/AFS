# Automaten und Formale Sprachen — 知识点总结 / Wissensbasis

> **格式说明 / Hinweis zum Format:**
> 每个知识点先写**德语原文**（来自Vorlesung），下方缩进写**中文解释**。
> Jeder Wissenspunkt: zuerst **Deutsch** (aus der Vorlesung), darunter eingerueckt **Chinesisch**.
> 本总结覆盖 VorlesungAFS2.pdf 全部 256 页 + UebungsaufgabenAFS.pdf 练习题知识点。

---

## 1. 理论计算机科学四大领域 / Vier Teilgebiete der Informatik

**Technische Informatik**
  Befasst sich mit der inneren Struktur und dem Bau von Computern und allen damit zusammenhaengenden technischen Fragen.
  技术信息学：研究计算机内部结构、硬件制造及所有相关技术问题。

**Praktische Informatik**
  Umfasst die Prinzipien und Techniken der Programmierung.
  实用信息学：涵盖编程的原理和技术。

**Angewandte Informatik**
  Bildet die Bruecke zwischen den Methoden der Informatik und Anwendungsproblemen.
  应用信息学：在信息学方法与应用问题之间架起桥梁。

**Theoretische Informatik**
  Entwickelt mathematische Modelle von Computern und Hilfsmittel zu ihrer praezisen Beschreibung.
  Ihre Basis ist die Mathematik — insbesondere Logik und Mengenlehre.
  Ein wesentliches Instrument ist die Turingmaschine (TM), die bereits 1936 von Alan Turing eingefuehrt wurde.
  理论信息学：开发计算机的数学模型及其精确描述工具。基础是数学（逻辑和集合论）。
  核心工具是图灵机（TM），1936年由图灵提出——远早于"信息学"这门学科的出现。

---

## 2. 字母表 / Alphabet

**Definition: Ein Alphabet A = {a1, ..., an} ist eine nichtleere Menge von endlich vielen Zeichen (auch Symbole genannt).**
  字母表是一个非空、有限的字符（符号）集合。
  ✓ {b,c,d,e,f}, {0,1,...,9}, {☼,♡,$}, {a}
  ✗ N (无限), ∅ = {} (空集不是字母表)
  Achtung: Es gibt verschiedene Definitionen (Stichworte: Tupel, Ordnung).

---

## 3. 词 / Wort

**Definition: Eine Folge x = x1...xn von n Zeichen heisst Wort (der Laenge n in N).**
  词：由 n 个字符组成的序列，长度为 n。

**Das leere Wort λ (auch ε): Spezialfall mit Laenge 0. Kann ueber jedem Alphabet gebildet werden.**
  空词 λ（也写作 ε）：|λ| = 0。可在任何字母表上构成。
  λ != ⋆ — ⋆ 是带上的空白符号（Blanksymbol），λ 是词，两者完全不同。

**A^n = {x1...xn | xi in A fuer i = 1,...,n}, dabei gilt A^0 = {λ}.**
  A^0 = {λ}（唯一的零长度词）。A^1 = A 本身。A^2 = 所有两字符组合。

**Die Menge aller Woerter ueber A ist A* = Vereinigung ueber n>=0 von A^n (Kleene'sche Huelle / Sternhuelle).**

---

## 4. 克莱尼星号与正闭包 / Sternhuelle und positive Huelle

**A* = {λ, a, b, aa, ab, ba, bb, aaa, ...} (Beispiel A = {a,b})**
  Sternhuelle = 所有可能长度（含0）的词。
  **A+ = A* ohne {λ}** — positive Huelle（不含空词）。
  例: B={0,1}: B*={λ,0,1,00,01,10,11,...}, B+={0,1,00,01,...}

**λ, {λ}, ∅ 三者的区别:**
  λ: das leere Wort (ein Wort)
  {λ}: die Sprache, die nur das leere Wort enthaelt (eine Sprache mit einem Wort)
  ∅: die leere Sprache (eine Sprache ohne Woerter)

---

## 5. 形式语言 / Formale Sprache

**Definition: Jede Teilmenge L ⊆ A* heisst Sprache ueber dem Alphabet A.**
  A* 的任意子集都是 A 上的一个形式语言。∅（空集）也是语言 ✓。
  包含不属于 A 的符号的集合不是该字母表上的语言 ✗。

**Sprachen sind Mengen von Woertern. Entscheidungsproblem → Sprache, Berechnungsproblem → Funktion.**

---

## 6. 两种问题类型 / Zwei Problemarten

**Entscheidungsproblem（判定问题）**
  Die Ausgabe besteht nur aus zwei Moeglichkeiten: Ja oder Nein.
  → Beschreibung durch eine Sprache L: w in L oder w nicht in L.
  例: Ist eine Zahl prim? Enthaelt ein Wort mehr a als b? Gehoert ein Wort zu einer gegebenen Sprache?

**Berechnungsproblem（计算问题）**
  Die Ausgabe ist ein konkretes Wort, eine Zahl oder eine andere kodierte Struktur.
  → Beschreibung durch eine Funktion f: w ↦ f(w).
  例: ggT berechnen, Primfaktorzerlegung, Wortlaenge ausgeben.

**两者互转:**
  判定→计算: f(w) = 1 (falls w in L), 0 (sonst)
  计算→判定: 通过图 Gf = {(w,u) | u = f(w)} → 问 (w,u) in Gf?
  Beide Sichtweisen sind eng verwandt.

---

## 7. 确定型图灵机 / Deterministische Turingmaschine (DTM)

**T = (E, B, S, δ, s0)**

| 符号 | 含义 / Bedeutung |
|------|-----------------|
| **E** | Eingabealphabet — 输入可以含的所有字符（不含 ⋆） |
| **B** | Bandalphabet — 带上可出现的所有字符（含 E 和 ⋆；可含额外字符） |
| **S** | Endliche Zustandsmenge — 有限状态集 (mit s0 in S) |
| **δ** | δ: S × B → S × B × {R, L, N} — **partielle** Zustandsuebergangsfunktion（部分函数） |
| **s0** | Startzustand — 起始状态 |

**δ(s, b) = (s', b', R) 的含义 / Bedeutung:**
  Wenn sich die TM im Zustand s befindet und der Lese-/Schreibkopf das Zeichen b auf dem Band liest:
  - b wird durch b' **ueberschrieben** (改写)
  - Folgezustand ist s' (切换状态)
  - Lese-/Schreibkopf bewegt sich eine Zelle nach **rechts** (R), **links** (L) oder **neutral** (N)
  - Ist δ fuer ein Paar (s,b) **nicht definiert**, haelt T an (停机)

**Turingtafel / Zustandsuebergangstabelle:**
  行 = 所有状态 s in S，列 = 所有可能的带符号 b in B
  格 [s,b] 定义 δ(s,b) 的转移指令

**初始配置 / Start:**
  Band enthaelt Eingabe w in E*, Lese-/Schreibkopf auf erstem Zeichen von w.
  Falls w=λ, steht Kopf auf ⋆.
  图示: ...⋆⋆ e1 e2 ... en ⋆...

---

## 8. 接受器图灵机 / Akzeptor-Turingmaschine

**T = (E, B, S, δ, s0, F) mit F ⊆ S — akzeptierende Endzustaende**
  比基本 TM 多一个接受状态集 F：
  - Haelt in F → **akzeptiert** (接受)
  - Haelt in S\F → **verworfen** (拒绝)
  - Haelt gar nicht → auch nicht akzeptiert (也不接受)

**Akzeptierte Sprache: L(T) = {w in E* | T akzeptiert w}**

| T 的行为 / Verhalten von T auf w | L(T) 含义 | fT(w) |
|----------------------------------|----------|-------|
| T akzeptiert w | w in L(T) | 1 |
| T verwirft w | w nicht in L(T) | 0 |
| T haelt nicht | w nicht in L(T) | undefiniert |

**Wichtig: Akzeptieren != Entscheiden!**
  Eine Akzeptor-TM muss bei nicht akzeptierten Eingaben **nicht unbedingt halten**.
  Entscheiden wuerde zusaetzlich bedeuten: T haelt **fuer jede** Eingabe.

**数字集 → 形式语言需要选择编码:**
  P = {n in N | n prim} 还不是形式语言（元素是数字）。
  需选编码：如单码 (einstellige Darstellung) 用 Alphabet {a}:
  Zahl n → a^n, 则 LP = {a^n | n prim} = {aa, aaa, aaaaa, aaaaaaa, ...}

---

## 9. 格局 / Konfiguration

**Definition: (v, s, w) in B* × S × B* — ein Tripel**
  - **s**: aktueller Zustand (当前状态)
  - **v**: der Teil **links** vom Lese-/Schreibkopf (读写头左侧内容)
  - **w**: der Teil **ab dem Lese-/Schreibkopf** nach rechts (读写头位置起向右)
  - 整条带 = **vw** (die aktuelle Bandinschrift)

**Startkonfiguration:**
  - w != λ: (λ, s0, w)
  - w = λ: (λ, s0, ⋆)

**Veranschaulichung / 图示:**
  ...⋆ 0 0 1 1 0 ⋆...
      ↑ s (Kopf auf der ersten 1)
      v = "00", w = "110"
  ⇒ Konfiguration = (00, s, 110)

**Konfigurationen kodieren die Position des Kopfes implizit — man braucht sie nicht als Zahl zu speichern.**

---

## 10. 格局转移关系 / Uebergangsrelation |-

**|-T Teilmenge von (B* × S × B*) × (B* × S × B*)**
  Fuer δ(s,b) = (s', b', X) mit X in {L,R,N}:

  **X = N** (Neutral / 不动):
  (v, s, bw) |-T (v, s', b'w)

  **X = R** (Rechts / 右移):
  (v, s, bw) |-T (vb', s', w) falls w != λ
  (v, s, bw) |-T (vb', s', ⋆) falls w = λ
  (Dabei: vb'=λ, falls v=λ und b'=⋆)

  **X = L** (Links / 左移):
  四种子情况:
  - v=v'a, b'w!=⋆ → (v', s', ab'w)
  - v=v'a, b'w=⋆ → (v', s', a)
  - v=λ, b'w!=⋆ → (λ, s', ⋆b'w)
  - v=λ, b'w=⋆ → (λ, s', ⋆)

---

## 11. 线性有界自动机 / Linear beschraenkter Automat (LBA)

**Motivation:**
  TMs haben ein unendlich langes Band — keine reale Maschine hat das.
  → linear beschraenkte Turingmaschinen (auch LBAs genannt).

**Prinzip / 原理:**
  → s0 ←
  $L e1 e2 ... en ⋆ ... ⋆ $R
  |w|=n       n        c

  读写头只能在 $L 和 $R 之间移动。
  有固定的自然数 **k** 和 **c**（不依赖具体输入 w）。
  最多可用 **k·|w| + c** 个带格子。
  例: w=baum, |w|=4, k=2, c=3 → 2·4+3=11 格
  w'=baumhaus, |w'|=8 → 2·8+3=19 格 (k,c 不变)

---

## 12. 下推自动机 / Kellerautomat (KA) — 定义

**Motivation / 动机 (Einlass-Auslass-Protokoll):**
  r = eine Person kommt rein (进), g = eine Person geht raus (出).
  读 rrg → 还有一人里面。读 rrrrgg → 还有两人里面。
  Die Anzahl ist bei jedem Wort endlich, aber es gibt **keine feste obere Schranke** fuer alle Woerter.
  → 需要 Automat mit zusaetzlichem Speicher (额外存储)。这就是 Keller / Stack。

**LIFO-Prinzip / 后进先出:**
  Last-In-First-Out = FILO (First-In-Last-Out).
  最后放入的最先被取出。例: 一摞盘子、浏览器后退按钮、函数调用栈。

**Definition: A = (E, K, S, δ, s0, F)**

| 符号 | Bedeutung / 含义 |
|------|-----------------|
| **E** | Eingabealphabet — 输入字母表（不含 k0） |
| **K** | Kelleralphabet — 栈字母表。含 **k0** (Kellerbodensymbol 栈底标记) |
| **S** | Endliche Zustandsmenge — 有限状态集 (s0 in S) |
| **δ** | δ: S × (E∪{λ}) × K → S × K* — partielle Zustandsuebergangsfunktion |
| **s0** | Startzustand — 起始状态 |
| **F** | F ⊆ S — akzeptierende Endzustaende (接受状态集) |

**δ(s, e, k) = (s', v) — Variante 1 (读输入):**
  Zustand s, liest e auf Eingabeband, oberstes Kellerzeichen k →
  k wird durch das ganze Wort v in K* ersetzt (von hinten nach vorne auf den Keller gepackt).
  Folgezustand s', Kopf auf Eingabeband wandert einen Schritt nach rechts.

**δ(s, λ, k) = (s', v) — Variante 2 (λ-Uebergang):**
  Dasselbe, aber das aktuell gelesene Eingabezeichen wird **nicht beachtet**,
  der Lesekopf auf dem Eingabeband bewegt sich **nicht** weiter.
  Bei deterministischen KA: δ(s,λ,k) nur definierbar, wenn δ(s,e,k) **nicht** definiert wurde.

---

## 13. 下推自动机 — 操作、格局、转移关系

**KA 的图示 / Graphische Darstellung:**
  Eingabeband e1 e2 ... en
  s0 → (Lesen, 只读)
  Steuereinheit ←→ Keller (栈) / LIFO / Lesen+Schreiben
  栈底: k0

**KA 的格局 / Konfiguration eines KA:**
  **(s, w, v) in S × E* × K***
  - s: aktueller Zustand
  - w: noch nicht gelesener Teil der Eingabe (剩余输入)
  - v: aktueller Kellerinhalt (当前栈内容)
  - Startkonfiguration: **(s0, w, k0)**

**KA 的转移关系 / Uebergangsrelation |-A:**
  |-A Teilmenge von (S×E*×K*) × (S×E*×K*)

  Fuer δ(s,e,k) = (s',v'), e in E:
  (s, ew, kv) |-A (s', w, v'v)

  Fuer δ(s,λ,k) = (s',v'), λ-Uebergang:
  (s, w, kv) |-A (s', w, v'v)

**栈操作实例 / Kelleroperationen:**
  - δ(s0, a, k0) = (s0, Ak0) — 读 a, 压 A（A 在 k0 上方）
  - δ(s0, a, A) = (s0, AA) — 读 a, 再压 A
  - δ(s0, b, A) = (s1, λ) — 读 b, 弹 A（栈顶 A 被移除 → λ 表示删除）
  - δ(s1, λ, k0) = (se, k0) — λ-Uebergang: 看到栈底就进入接受状态

**Akzeptanz / 接受:**
  Automat haelt nach endlich vielen Schritten, nachdem die Eingabe **vollstaendig gelesen** wurde,
  und befindet sich beim Halten in einem Zustand aus F.
  Der Keller muss dabei **nicht** bis auf k0 geleert sein.
  Ende der Eingabe beendet den Lauf **nicht automatisch**!

**Anwendung / 应用:** Klammerpruefung, a^n b^n, LaTeX-Syntax.

---

## 14. 确定型有限自动机 / Deterministischer Endlicher Automat (DEA)

**Definition: A = (E, S, δ, s0, F)**

| 符号 | Bedeutung |
|------|-----------|
| **E** | Eingabealphabet — 输入字母表 |
| **S** | Endliche Zustandsmenge — 有限状态集 (s0 in S) |
| **δ** | δ: S×E → S — Zustandsuebergangsfunktion (**totale Funktion!** 所有(s,e)必须定义) |
| **s0** | Startzustand |
| **F** | F ⊆ S — akzeptierende Endzustaende |

**Graphische Darstellung / 图形表示:**
  - Kreis = Zustand (圆圈 = 状态)
  - Pfeil mit Symbol = Uebergang (箭头+字符 = 转移)
  - Doppelkreis = Endzustand (双圈 = 接受状态)
  - Eingehender Pfeil = Startzustand (进入箭头 = 起始)

**工作原理 / Funktionsweise:**
  e1 e2 ... en  (Eingabeband)
  s0 → (Lesekopf springt schrittweise nach rechts)
  读完整个词后：若当前状态 in F → 接受；否则拒绝。

**接受的形式化定义:**
  Fuer w = a1...an: δ(...δ(δ(s0,a1),a2)...,an) in F

**Kugelschreiber-Beispiel / 圆珠笔模型:**
  E = {n, d} (n=nichts tun, d=druecken)
  Zustaende: 0 = Miene drinnen, 1 = Miene draussen
  0 --d--> 1 --d--> 0 (druecken wechselt)
  0 --n--> 0, 1 --n--> 1 (nichts tun bleibt)

**λ-Uebergaenge bei DEA:**
  δ(s,λ) = s' — wird aus s nur in s' gewechselt, ohne Lesekopfbewegung.
  δ(s,λ) nur definierbar, wenn δ(s,e) nicht definiert wurde.

---

## 15. DEA 实例与语言分析 / DEA Beispiel

**Beispiel: A mit E={a,b}, S={z0,z1,z2,z3}, F={z3}**

  δ(z0,a)=z1, δ(z0,b)=z3
  δ(z1,a)=z2, δ(z1,b)=z0
  δ(z2,a)=z3, δ(z2,b)=z1
  δ(z3,a)=z0, δ(z3,b)=z2

  **Welche Sprache akzeptiert A?**
  定义 D = #a − #b (a的数量减b的数量)
  z3 对应 D≡3 (mod 4)
  Also: L(A) = {w | D ≡ 3 (mod 4)} = {..., −9, −5, −1, 3, 7, ...}
  x ≡ y (mod m) bedeutet: x−y ist durch m teilbar.

---

## 16. 等价关系 / Aequivalenzrelationen

**Eine Aequivalenzrelation ist eine reflexive, symmetrische und transitive Relation.**
  等价关系 = 自反 + 对称 + 传递。

  **Reflexiv:** ∀a in A (aRa)
  **Symmetrisch:** ∀a,b in A (aRb → bRa)
  **Transitiv:** ∀a,b,c in A (aRb ∧ bRc → aRc)

**Beispiele / 例:**
  - n ~ m :⇔ n−m teilbar durch 2 (或任意 k in N) — 同余关系
  - n ~ m :⇔ (n>0∧m>0)∨(n=m=0)∨(n<0∧m<0) — "gleiches Vorzeichen" (同符号)
  - Gleichheit (=) als "feinste"; Allrelation als "groebste" Aequivalenzrelation

**Aequivalenzklasse / 等价类:**
  [a] := {b in X | b ~ a} = [a]~
  Alle Elemente aus X, die zu a aequivalent sind.

**Quotientenmenge / 商集:**
  X/~ := {[a] | a in X} — die Menge aller Aequivalenzklassen.

**Bedeutung fuer Automaten:**
  Zwei DEA, die die gleiche Sprache akzeptieren, sind aequivalent (A1~A2).
  Oft interessiert uns der "kleinere" (minimierte) Automat.

---

## 17. DEA 最小化 / Minimierung

**Ziel:** Finde aequivalenten DEA mit minimaler Zustandsanzahl.

**方法一 — 分组法 / Grobverfahren:**
  1. Zustandsgruppen bilden: NEZ (Nicht-Endzustaende) und EZ (Endzustaende)
  2. Bei Inkonsistenzen aufteilen: wenn Zustaende derselben Gruppe bei gleicher Eingabe
     in verschiedene Gruppen gehen → trennen
  3. Wiederholen bis keine Inkonsistenzen mehr
  4. Verschmelzen (合并) der Zustaende, die noch in derselben Gruppe liegen → Minimalautomat

**方法二 — 表填充法 / Table-Filling-Algorithmus:**
  1. Erstelle eine Tabelle aller Zustandspaare (s,s') mit s!=s'
  2. Markiere alle Paare mit s in F und s' nicht in F (oder umgekehrt)
  3. Wiederhole: Fuer jedes unmarkierte Paar (s,s') und jedes e in E:
     Wenn (δ(s,e), δ(s',e)) schon markiert ist → markiere (s,s')
  4. Verschmelze unmarkierte Zustandspaare → Minimalautomat

**Beispiel (Passwort-Erkennung mit Gross-/Kleinbuchstaben):**
  Ursprünglicher Automat s0...s4 → minimiert zu s0, s1, s2, s34

**Beispiel (Sprache "enthaelt 00"):**
  Zustaende z0,z1,z2,z3 (NEZ) und z4 (EZ)
  → NEZ aufgeteilt in {z0,z2} und {z1,z3}
  → Minimalautomat: z02, z13, z4

---

## 18. 带输出的有限自动机 / Endliche Automaten mit Ausgabe

**Grundidee:**
  EA mit getrenntem Ausgabeband (beschreibbar, aber nicht lesbar).
  Jedes Eingabezeichen → ein Ausgabezeichen (ohne λ-Uebergaenge).

**Definition: A = (E, A, S, δ, γ, s0)**
  A = Ausgabealphabet (输出字母表)
  γ = Ausgabefunktion (输出函数)

**Mealy-Automat:**
  γ: S × E → A — Ausgabe haengt vom aktuellen Zustand **und** aktuellen Eingabezeichen ab.
  Im Graph: an jeder Kante steht "e/a" (Eingabe/Ausgabe).
  更 kompakt (紧凑), da fuer jede Kombination (s,e) ein Ausgabezeichen.

**Moore-Automat:**
  γ: S → A — Ausgabe haengt **nur** vom aktuellen Zustand ab.
  Im Graph: Ausgabezeichen steht **unter** dem Zustand im Knoten.

**Mealy ↔ Moore 等价:** Beide Modelle sind von ihrer Berechnungsmaechtigkeit her aequivalent.

**Beispiele:**
  - **Flip-Flop (Mealy)**: Zustaende Set/Reset, Eingabe 0/1, Ausgabe = neuer Zustandsindex
  - **Fahrstuhl/Elevator (Moore)**: Zustaende z0(E), z1(1), z2(2) mit Etagenanzeige
  - **Keksautomat (Mealy)**: Eingabe 1€/2€/Taste, Ausgabe 1€/2€/Keks/–, bei 2€ → Keks

---

## 19. 非决定型图灵机 / Nichtdeterministische Turingmaschine (NTM)

**Definition: δ: S × B → P(S × B × {R, L, N})**
  δ bildet auf die **Potenzmenge** (幂集) ab.
  Fuer (s,b) gibt es eine Menge moeglicher Uebergaenge {(s1,b1,X1), (s2,b2,X2), ...}.
  **Jeder** dieser Uebergaenge kann genommen werden.

**Rechenbaum / 计算树:**
  Nichtdeterminismus erzeugt einen Rechenbaum: C0 → mehrere C1 → mehrere C2 → ...
  Es existiert ein akzeptierender Pfad → Eingabe wird akzeptiert.

**Beispiel: L = {ww | w in {0,1}*}**
  Die Maschine **raet** nichtdeterministisch die Mitte, dann:
  - Vergleichsphase: passende Zeichen paarweise suchen, markieren (z.B. mit X)
  - Wenn alle Zeichen links und rechts markiert → akzeptieren

---

## 20. 非决定型下推自动机 / Nichtdeterministischer Kellerautomat (NKA)

**Definition: δ: S × (E∪{λ}) × K → P(S × K*)**
  Wie deterministischer KA, aber δ liefert eine **Menge** von moeglichen Folgepaaren.

**Variante 1:** δ(s,e,k) = {(s1,v1), (s2,v2), ...}
  Eines der Paare (si,vi) wird gewaehlt: k loeschen, vi in Keller schreiben, zu si gehen.

**Variante 2:** δ(s,λ,k) = {(s1,v1), (s2,v2), ...}
  Wie Variante 1, aber Eingabezeichen nicht beachtet, Lesekopf nicht bewegt.
  **Wichtig:** λ-Uebergang darf jetzt auch definiert werden, wenn δ(s,e,k) ebenfalls definiert ist!

**Akzeptanz:** Es muss mindestens einen Rechenpfad geben, der nach vollstaendigem Lesen in F haelt.

**Beispiel: L = {a^n b^n | n >= 0} mit NKA:**
  两阶段策略 / Zwei-Phasen-Strategie:
  - **Phase 1 (a-Phase):** Fuer jedes gelesene a wird A auf den Keller gelegt.
  - **Phase 2 (b-Phase):** Fuer jedes gelesene b wird ein A aus dem Keller entfernt.
  - Die Maschine **weiss nicht**, wann Phase 1 endet — sie **raet** den Umschaltpunkt **nichtdeterministisch**.
  - Bei jedem a darf sie: in Phase 1 bleiben **oder** nichtdeterministisch in Phase 2 wechseln.
  - Alle falschen Umschaltpunkte → Widersprueche im Keller → verwerfen.
  - Genau ein richtiger Umschaltpunkt → Keller am Ende wieder nur k0 → Endzustand → akzeptieren.

**Konkretes Beispiel x=aabb:**
  - Umschalten nach 1. a: Keller zu frueh leer → verwerfen
  - Umschalten nach aa: Keller genau am Ende nur k0 → akzeptierend halten ✓
  - Umschalten nach aab: b kommt aber Keller leer → verwerfen

---

## 21. 非决定型有限自动机 / Nichtdeterministischer Endlicher Automat (NEA)

**Definition: δ: S × E → P(S) — δ(s,e) = {s1, s2, ...}**
  Vom Zustand s beim Lesen von e kann in **einen der Zustaende** aus der Potenzmenge gewechselt werden.
  Die Menge darf auch **leer** sein → Automat kann halten, bevor die Eingabe abgearbeitet wurde.

**Akzeptanz / 接受:**
  Es existiert eine Kantenfolge im Graphen, die nach Abarbeiten der **ganzen** Eingabe
  zu einem Endzustand fuehrt.
  **λ-Beschriftungen (ε-Uebergaenge):** tragen kein Zeichen zum gelesenen Wort bei.

**NEA → DEA:** Jeder NEA kann in einen aequivalenten DEA ueberfuehrt werden (Potenzmengenkonstruktion / 幂集构造法).

**Interpretation des Nichtdeterminismus:**
  a) Der Automat "entscheidet" selbst, welchen Weg er geht.
  b) Kopien des Automaten waehlen jeweils einen anderen Folgezustand.

---

## 22. 德语语法基础 / Deutsche Grammatik (Grundlagen)

**Ein Satz besteht aus: Subjekt + Praedikat + Objekt**
  句子 = 主语 + 谓语 + 宾语

**Subjekt (主语):** Wer? Was? (tut etwas)
**Praedikat (谓语):** Was tut das Subjekt? → Verb (Taetigkeitswort / 动词)
**Objekt (宾语):**
  - Akkusativ: Wen? Was? (直接宾语)
  - Dativ: Wem? (间接宾语)
  - Genitiv: Wessen? (属格宾语)

**Praeposition (介词):**
  Setzen sprachliche Ausdruecke in eine inhaltliche Beziehung.
  例: ueber, fuer, wegen, im, an

**Beispiele:**
  "Luke Skywalker toetet Feinde." → Subjekt Praedikat Akkusativ-Objekt
  "Jana schenkt Jan Blumen." → Jan = Dativ-Objekt
  "Sie hat ihn des Diebstahls beschuldigt." → ihn=Akkusativ, des Diebstahls=Genitiv

---

## 23. 语法短语类型 / Phrasentypen

**Nominalphrase (NP):**
  Eine Phrase, deren Kern ein Nomen (Substantiv) ist.
  例: [Wichtige Entscheidungen]NP, [eine wichtige Entscheidung]NP, [der Burg]NP

**Verbalphrase (VP):**
  Eine Phrase, deren Kern ein Verb ist. Enthaelt auch Ergaenzungen des Verbs.
  例: [schlaeft]VP, [das Licht zu loeschen]VP

**Praepositionalphrase (PP):**
  Phrasen mit einer Praeposition als Kern.
  例: [mit grossem Aufwand]PP, [auf dem Baum]PP

---

## 24. 形式语法 / Formale Grammatik

**G = (N, T, P, S) — ein Quadrupel / 四元组**

| 符号 | Bedeutung / 含义 |
|------|-----------------|
| **N** | Nichtterminale (Variablen) — 非终结符（大写字母） |
| **T** | Terminale — 终结符（小写字母，实际字符） |
| **P** | Produktionen (Regeln) — 产生式规则集 |
| **S** | Startsymbol — 起始符号 (S in N) |

**条件:**
  - N ∩ T = ∅ (N 和 T 不相交)
  - S in N
  - Produktion α → β: α in (N∪T)* \ T* (α 至少含一个非终结符), β in (N∪T)*
  - | (竖线) = Metazeichen (元符号), 表示"或"

**Warum α nicht rein aus T?** Terminalsymbole sollen beenden! 否则可能无法继续推导。

**Beispiel: Deutsche Grammatik-Regeln:**
  NP → N | A N | NP PP
  VP → V | V NP | VP NP
  PP → P P | P NP
  Lexikon: A → der | die | das | dem | ein | einem
  P → mit | in
  N → Hans | Krokodil | Auto | Fernglas
  V → sah

---

## 25. 推导与语法语言 / Ableitung und Sprache einer Grammatik

**Ableitungsschritt / 一步推导:**
  γαφ ⇒ γβφ genau dann, wenn (α,β) in P. 记作 γαφ ⇒1 γβφ.

**Mehrschrittige Ableitung / 多步推导:**
  α1 ⇒ αn bedeutet: α1 ⇒1 α2 ⇒1 ... ⇒1 αn
  α1 ⇒G αn — deutlich machen, dass G verwendet wird.

**Sprache einer Grammatik / 语法的语言:**
  L(G) = {w in T* | S ⇒G w}
  Eine Ableitung endet, wenn nur noch Terminalsymbole auftauchen.

**Beispiel: "Hans sah das Krokodil mit einem Fernglas"**
  S ⇒ NP VP ⇒ N VP PP ⇒ Hans V NP P NP
  ⇒ Hans sah A N mit A N
  ⇒ Hans sah das Krokodil mit einem Fernglas

**Syntaxbaum / 语法树:**
  Jede Verzweigung entspricht der Anwendung einer Regel.
  Zwei verschiedene Syntaxbaeume → strukturelle Ambiguitaet (结构歧义):
  "Hans sah das Krokodil mit einem Fernglas" — hat Hans oder das Krokodil das Fernglas?

---

## 26. 乔姆斯基层级 / Chomsky-Hierarchie

| Typ | Name / 名称 | Einschraenkung / 限制 | Automat / 对应自动机 |
|-----|------------|----------------------|---------------------|
| **Typ 0** | Unbeschraenkt / 无限制 | Keine Einschraenkungen | TM |
| **Typ 1** | Kontextsensitiv / 上下文相关 | |α| ≤ |β| (nicht verkuerzend) | LBA |
| **Typ 2** | Kontextfrei / 上下文无关 | Linke Seite = einzelne Variable | KA |
| **Typ 3** | Regulaer / 正则 | Links einzeln; rechts = Terminal ODER Terminal+Variable | EA/DEA |

**Hierarchie / 层级包含:**
  Typ 3 ⊂ Typ 2 ⊂ Typ 1 ⊂ Typ 0 (每个下级自动是上级的子集)

---

## 27. 各类型详解 / Typen im Detail

**Typ 0:** Jede Grammatik ist zunaechst vom Typ 0. Keine Einschraenkungen.

**Typ 1 (kontextsensitiv):**
  Jede Regel w1→w2 muss |w1| ≤ |w2| erfuellen (Laenge nimmt nicht ab).
  Warum "kontextsensitiv"? 例: aC → aDb
  C darf nur dann durch Db ersetzt werden, wenn es im Kontext "a_" auftritt.
  αVβ → αγβ (mit |γ|≥1): V steht im Kontext von α und β.

**Typ 2 (kontextfrei):**
  Der Kontext faellt weg — linke Seite muss eine einzelne Variable sein. 例: C → aDb ✓

**Typ 3 (regulaer):**
  Linke Seite: einzelne Variable.
  Rechte Seite: **nur** ein Terminal ODER ein Terminal gefolgt von einer Variable.
  允许: S → aA ✓, S → a ✓
  不允许: S → Aa ✗, S → aaA ✗
  → 被称为 rechtslinear (右线性)。

**λ-Sonderregeln:** Je nach Konvention gibt es Sonderregeln fuer das leere Wort λ.

---

## 28. 语法实例 / Grammatik-Beispiele

**例1 (Typ 3 — regulaer):**
  L1 = {w in {a,b}* | in w kommt aa vor} (包含子串 aa)
  Grammatik: S → bS | aA, A → bS | aB | a, B → bB | aB | b | a
  Ableitung: S ⇒ aA ⇒ abS ⇒ abaA ⇒ abaaB ⇒ abaabB ⇒ abaaba

**例2 (Typ 2 — kontextfrei):**
  L2 = {a^n b^n | n >= 1}
  Grammatik: S → aSb | ab

**例3 (Typ 1 — kontextsensitiv):**
  L3 = {a^n b^n c^n | n >= 1}
  Grammatik: S → aSBC | aBC, CB → BC, aB → ab, bB → bb, bC → bc, cC → cc
  （CB → BC是重排规则）

---

## 29. 自动机与语法对应 / Automat ↔ Grammatik

**Chomsky-Typ und zugehoeriger Automat:**
  Typ 0 ↔ TM
  Typ 1 ↔ LBA
  Typ 2 ↔ KA
  Typ 3 ↔ EA

**DEA → Typ 3 Grammatik / 转换规则:**
  - N = S (Nichtterminale = Zustaende)
  - T = E (Terminale = Eingabealphabet)
  - S = s0 (Startsymbol = Startzustand)
  - δ(s, e) = s' ⇒ Produktion s → e s'
  - s in F ⇒ Produktion s → λ
  - Zustaende ohne definierten Uebergang → sFehler mit Selbstschleifen

**Beispiel / 例 (aus Vorlesung Folie 255-256):**
  A: s0 --b--> s1, s0 --a--> s0; s1 --a--> sFehler, s1 --b--> s1; F={s1}
  → G: s0 → a s0 | b s1; s1 → a sFehler | b s1 | λ; sFehler → a sFehler | b sFehler
  Es liegt eine Grammatik vom Typ 3 vor.

**Bedeutung / 意义:**
  Automat: Berechnung endet, wenn gesamte Eingabe gelesen wurde.
  Grammatik: Wortproduktion endet, wenn das letzte Nichtterminal entfernt wurde (→ λ-Produktion).

---

## 30. 重要人物 / Protagonisten

| 人物 / Person | 贡献 / Beitrag |
|---------------|---------------|
| **Kurt Goedel** | Unvollstaendigkeitssaetze / 不完备定理 |
| **Alan Turing** | 1936: Turingmaschine; Entscheidungsproblem |
| **Emil Post** | Postsches Korrespondenzproblem |
| **John von Neumann** | Computer-Architektur (Von-Neumann-Architektur) |
| **Alonzo Church** | λ-Kalkuel; Church'sche These |
| **Noam Chomsky** | Chomsky-Hierarchie der formalen Sprachen |

---

## 31. Church 论题 / Church'sche These

**Inhalt / 内容:**
  Alle intuitiv "berechenbaren" Funktionen koennen durch eine Turingmaschine berechnet werden.
  所有直观上"可计算"的函数都可以被图灵机计算。

  Dies ist **kein mathematischer Satz** — die These kann nicht bewiesen werden, da der Begriff
  "intuitiv berechenbar" nicht formal definiert ist. Sie ist aber allgemein akzeptiert.

---

## 32. 可判定性 / Entscheidbarkeit

**Definition / 定义:**
  Ein Problem heisst **entscheidbar**, wenn es eine Turingmaschine gibt, die fuer **jede** Eingabe
  haelt und die korrekte Antwort (Ja/Nein) liefert.
  一个问题可判定：存在一个 TM，对**每个**输入都停机并给出正确回答。

---

## 33. 常见语言模式与对应自动机 / Haeufige Sprachmuster

| 语言 / Sprache | 最小自动机 / Minimaler Automat | Chomsky-Typ |
|---------------|------------------------------|-------------|
| Woerter, die mit bestimmtem Zeichen enden | EA (DEA) | Typ 3 |
| Woerter, die bestimmtes Teilwort enthalten | EA (DEA) | Typ 3 |
| a^n b^n (gleich viele a und b, sortiert) | KA | Typ 2 |
| w = u$~u (Palindrome mit Trenner) | KA | Typ 2 |
| a^n b^n c^n (drei gleiche Anzahlen) | TM / LBA | Typ 1 |
| ww (Wort doppelt) | NTM | Typ 0 |
| (ab)^n (ba)^n | KA | Typ 2 |
| Geklammerte Ausdruecke / 括号匹配 | KA | Typ 2 |

---

## 34. 考试重点速查 / Klausur-Checkliste

- [ ] Alphabet, Wort, λ, A*, A+, Sprache, {λ} vs ∅ 的定义与区别
- [ ] TM 五元组 (E,B,S,δ,s0)；Turingtafel/Zustandsuebergangstabelle
- [ ] δ(s,b)=(s',b',X) 的精确语义 (R/L/N三种移动)
- [ ] Akzeptor-TM: F 集合；akzeptieren vs. entscheiden 的关键区别
- [ ] 数字集→形式语言：选择编码 (Dezimal/Binaer/einstellig)
- [ ] Konfiguration (v,s,w)：三要素、起始配置、vw=带内容
- [ ] Uebergangsrelation |-：N/R/L 三种情况的精确定义
- [ ] LBA: k·|w|+c；$L/$R 边界；k,c 固定不依赖输入
- [ ] KA: E,K,S,δ,s0,F；LIFO-Prinzip
- [ ] KA δ: S×(E∪{λ})×K → S×K*；Variante 1 vs Variante 2 (λ-Uebergang)
- [ ] λ-Uebergang 的条件和优势；决定型中不可与普通转移共存
- [ ] KA 格局 (s,w,v)；|-A 转移关系；栈操作
- [ ] DEA: (E,S,δ,s0,F)；δ 为 totale Funktion；图形表示
- [ ] DEA 接受：δ(...δ(δ(s0,a1),a2)...,an) in F
- [ ] Aequivalenzrelation: reflexiv+symmetrisch+transitiv；[a]；X/~
- [ ] DEA Minimierung: 分组法 + Table-Filling (表填充法)
- [ ] Moore γ:S→A vs Mealy γ:S×E→A；图形标记方式；互转等价性
- [ ] Flip-Flop (Mealy)；Fahrstuhl (Moore)；Keksautomat (Mealy)
- [ ] NTM: δ→P(S×B×{R,L,N})；Rechenbaum；存在接受路径即接受
- [ ] NKA: δ→P(S×K*)；λ-Uebergang可与普通转移共存
- [ ] NKA a^n b^n: 两阶段非决定猜切换点
- [ ] NEA: δ→P(S)；ε-Uebergaenge；NEA→DEA (Potenzmengenkonstruktion)
- [ ] 德语语法: Subjekt, Praedikat, Objekt, Praeposition, NP, VP, PP
- [ ] 形式语法 G=(N,T,P,S)；N∩T=∅；α in (N∪T)*\T*
- [ ] 推导 ⇒1, ⇒, ⇒G；L(G)={w in T*|S⇒G w}
- [ ] Chomsky-Hierarchie Typ 0–3: 限制条件 + 对应自动机 + 向下兼容
- [ ] Typ 1 为什么叫"上下文相关": aC→aDb；αVβ→αγβ
- [ ] Typ 3: 右侧 = Terminal 或 Terminal+Variable (rechtslinear)
- [ ] DEA → Typ 3 语法: s→e s' 和 s→λ
- [ ] Church'sche These: intuitiv berechenbar = TM-berechenbar
- [ ] Entscheidbarkeit: TM haelt fuer **alle** Eingaben

---

*Erstellt am 19.05.2026 — Letzter Versuch, viel Erfolg! 🍀*
*创建于 2026年5月19日 — 最后一次考试机会，祝顺利通过！*
