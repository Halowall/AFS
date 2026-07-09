# AFS Mockaufgaben im LNW-/Klausur-Stil

> Form: Multiple Choice wie im LNW.  
> Pro Aufgabe koennen 0 bis 4 Antworten richtig sein.  
> Bearbeitungszeit: Ein Satz mit 12 Aufgaben entspricht ca. 30 Minuten. Fuer eine 60-Minuten-Klausursimulation bearbeiten Sie zwei Saetze direkt nacheinander.

---

## Satz 1

### 1. Aufgabe

Sei `A` ein Alphabet. Welche Aussagen sind richtig?

- [ ] A. Ein Alphabet ist eine nichtleere, endliche Menge von Zeichen.
- [ ] B. Das leere Wort `λ` ist in `A*` enthalten.
- [ ] C. Jede Teilmenge `L ⊆ A*` heißt Sprache ueber `A`.
- [ ] D. Ein Alphabet darf unendlich viele Zeichen enthalten.

### 2. Aufgabe

Sei `A={a,b}`. Welche Aussagen sind richtig?

- [ ] A. `λ ∈ A*`.
- [ ] B. `λ ∈ A+`.
- [ ] C. `ab ∈ A+`.
- [ ] D. `{a,ab} ⊆ A*`.

### 3. Aufgabe

Sei `A=(E,S,δ,s0,F)` ein deterministischer endlicher Automat. Welche Aussagen sind richtig?

- [ ] A. `δ:S×E→S`.
- [ ] B. `δ*:S×E*→S`.
- [ ] C. Fuer jedes Wort `w∈E*` ist `δ(s0,w)` die richtige Schreibweise der normalen Uebergangsfunktion.
- [ ] D. `w∈L(A)` gilt genau dann, wenn `δ*(s0,w)∈F`.

### 4. Aufgabe

Sei `A` ein nichtdeterministischer endlicher Automat. Welche Aussagen sind richtig?

- [ ] A. Die Uebergangsfunktion hat die Form `δ:S×E→P(S)`.
- [ ] B. Ein Wort wird akzeptiert, wenn mindestens ein Rechenpfad akzeptierend endet.
- [ ] C. Ein Wort wird nur dann akzeptiert, wenn jeder Rechenpfad akzeptierend endet.
- [ ] D. `P(S)` ist die Potenzmenge von `S`.

### 5. Aufgabe

Betrachten Sie die Uebergangsfunktion eines Kellerautomaten im Sinne der Vorlesung. Welche Aussagen sind richtig?

- [ ] A. `δ:S×(E∪{λ})×K→S×K*`.
- [ ] B. Auf der linken Seite wird nur das oberste Kellersymbol gelesen.
- [ ] C. Auf der rechten Seite darf ein Wort aus `K*` stehen.
- [ ] D. Wenn rechts `λ` steht, wird das oberste Kellersymbol geloescht.

### 6. Aufgabe

Sei `T` eine Turingmaschine und `w≠λ` eine Eingabe. Welche Aussagen sind richtig?

- [ ] A. Eine Konfiguration einer Turingmaschine hat die Form `(v,s,w)`.
- [ ] B. Die Startkonfiguration fuer `w≠λ` ist `(λ,s0,w)`.
- [ ] C. In `(v,s,w)` steht `s` fuer den aktuellen Zustand.
- [ ] D. In `(v,s,w)` steht `v` fuer den noch nicht gelesenen Teil der Eingabe.

### 7. Aufgabe

Sei `T` eine deterministische Akzeptor-Turingmaschine mit Endzustandsmenge `F`. Welche Aussagen sind richtig?

- [ ] A. Haelt `T` in einem Zustand aus `F`, so akzeptiert `T` die Eingabe.
- [ ] B. Wenn `T` eine Eingabe nicht akzeptiert, muss `T` bei dieser Eingabe nicht unbedingt halten.
- [ ] C. Akzeptieren bedeutet dasselbe wie Entscheiden.
- [ ] D. `L(T)` ist die Menge aller von `T` akzeptierten Woerter.

### 8. Aufgabe

Zu einem linear beschraenkten Automaten gehoeren feste Zahlen `k` und `c`, und fuer eine Eingabe `w` duerfen hoechstens `k·|w|+c` Bandfelder verwendet werden. Welche Aussagen sind richtig?

- [ ] A. `k` und `c` sind feste natuerliche Zahlen.
- [ ] B. `k` und `c` duerfen nachtraeglich passend zur konkreten Eingabe gewaehlt werden.
- [ ] C. Der erlaubte Speicherplatz ist linear in der Eingabelaenge.
- [ ] D. Ein LBA ist maechtiger als eine unbeschraenkte Turingmaschine.

### 9. Aufgabe

Welche Aussagen ueber die Minimierung eines DEA sind richtig?

- [ ] A. Zunaechst koennen nicht erreichbare Zustaende entfernt werden.
- [ ] B. Zustandspaare, bei denen genau ein Zustand in `F` liegt, werden markiert.
- [ ] C. Am Ende werden die markierten Zustandspaare verschmolzen.
- [ ] D. Am Ende werden die unmarkierten, aequivalenten Zustaende verschmolzen.

### 10. Aufgabe

Welche Aussagen ueber Aequivalenzrelationen sind richtig?

- [ ] A. Eine Aequivalenzrelation ist reflexiv, symmetrisch und transitiv.
- [ ] B. Die Relation "`x` ist groesser als `y`" ist auf den natuerlichen Zahlen reflexiv.
- [ ] C. Fuer eine Aequivalenzrelation `~` gilt `X/~ = {[a]~ | a∈X}`.
- [ ] D. `X/~ = {[a]~ | [a]~∈X}` ist die uebliche Definition der Quotientenmenge.

### 11. Aufgabe

Welche Aussagen ueber Moore- und Mealy-Automaten sind richtig?

- [ ] A. Beim Moore-Automaten hat die Ausgabefunktion die Form `γ:S→A`.
- [ ] B. Beim Mealy-Automaten hat die Ausgabefunktion die Form `γ:S×E→A`.
- [ ] C. Beim Moore-Automaten steht die Ausgabe an den Kanten.
- [ ] D. Beim Mealy-Automaten haengt die Ausgabe nur vom Zustand ab.

### 12. Aufgabe

Sei `G=(N,T,P,S)` eine formale Grammatik. Welche Aussagen sind richtig?

- [ ] A. `N∩T=∅`.
- [ ] B. `S∈N`.
- [ ] C. Auf der linken Seite einer Produktion darf ein Wort stehen, das nur aus Terminalsymbolen besteht.
- [ ] D. `L(G)={w∈T* | S⇒*_G w}`.

---

## Satz 2

### 1. Aufgabe

Welche Aussagen ueber die Potenzmenge sind richtig?

- [ ] A. `P(M)` ist die Menge aller Teilmengen von `M`.
- [ ] B. Fuer `M={p,q}` gilt `{p}∈P(M)`.
- [ ] C. Fuer `M={p,q}` gilt `p∈P(M)`.
- [ ] D. Fuer jede Menge `M` gilt `∅∈P(M)`.

### 2. Aufgabe

Sei `A=(E,S,δ,s0,F)` ein DEA und `w=e1e2...en`. Welche Aussagen sind richtig?

- [ ] A. `δ*(s0,w)` beschreibt den Zustand nach dem Lesen des ganzen Wortes.
- [ ] B. `δ*(s0,e1e2)=δ(δ(s0,e1),e2)`.
- [ ] C. `δ` und `δ*` haben immer denselben Definitionsbereich.
- [ ] D. Ist `δ*(s0,w)∈F`, so wird `w` akzeptiert.

### 3. Aufgabe

Ein DEA hat zwei Zustaende `0` und `1`. `0` ist Startzustand, `1` ist Endzustand. Das Symbol `n` laesst den Zustand unveraendert, das Symbol `d` wechselt zwischen `0` und `1`. Welche Woerter werden akzeptiert?

- [ ] A. `d`
- [ ] B. `nnd`
- [ ] C. `ddn`
- [ ] D. `ndnndd`

### 4. Aufgabe

Welche Aussagen ueber NEA mit `λ`-Uebergaengen sind richtig?

- [ ] A. Ein `λ`-Uebergang verbraucht kein Eingabezeichen.
- [ ] B. Die Uebergangsfunktion kann die Form `δ:S×(E∪{λ})→P(S)` haben.
- [ ] C. Ein NEA akzeptiert nur, wenn alle moeglichen Rechenpfade akzeptieren.
- [ ] D. Jeder NEA kann in einen aequivalenten DEA ueberfuehrt werden.

### 5. Aufgabe

Welche Aussagen ueber nichtdeterministische Turingmaschinen sind richtig?

- [ ] A. Die Uebergangsfunktion kann auf eine Potenzmenge moeglicher Folgeschritte abbilden.
- [ ] B. Nichtdeterminismus erzeugt anschaulich einen Rechenbaum.
- [ ] C. Eine Eingabe wird akzeptiert, wenn mindestens ein akzeptierender Pfad existiert.
- [ ] D. Eine NTM ist per Definition dasselbe wie ein DEA.

### 6. Aufgabe

Welche Aussagen ueber nichtdeterministische Kellerautomaten sind richtig?

- [ ] A. `δ:S×(E∪{λ})×K→P(S×K*)`.
- [ ] B. `δ` liefert eine Menge moeglicher Folgepaare.
- [ ] C. Bei einem NKA darf ein `λ`-Uebergang auch dann moeglich sein, wenn ein normaler Uebergang moeglich ist.
- [ ] D. Ein NKA hat keinen Keller.

### 7. Aufgabe

Betrachten Sie die Sprache `L={a^n b^n | n≥0}`. Welche Aussagen sind richtig?

- [ ] A. Ein Kellerautomat kann fuer jedes gelesene `a` ein Symbol auf den Keller legen.
- [ ] B. Fuer jedes gelesene `b` kann ein Symbol vom Keller entfernt werden.
- [ ] C. Ein endlicher Automat ohne Zusatzspeicher reicht fuer diese Sprache aus.
- [ ] D. Die Reihenfolge der Phasen kann durch Zustaende kontrolliert werden.

### 8. Aufgabe

Betrachten Sie die Sprache `L={u$ũ | u∈{a,b}*}`. Welche Aussagen sind richtig?

- [ ] A. Das Zeichen `$` dient als Trenner in der Eingabe.
- [ ] B. Vor dem `$` koennen die gelesenen Zeichen auf dem Keller gespeichert werden.
- [ ] C. Nach dem `$` wird in umgekehrter Reihenfolge mit dem Keller verglichen.
- [ ] D. Das Zeichen `$` muss zwingend ein Kellersymbol sein.

### 9. Aufgabe

Welche Aussagen ueber Konfigurationen eines Kellerautomaten sind richtig?

- [ ] A. Eine KA-Konfiguration hat die Form `(s,w,v)`.
- [ ] B. `s` ist der aktuelle Zustand.
- [ ] C. `w` ist der noch nicht gelesene Teil der Eingabe.
- [ ] D. Die Startkonfiguration ist `(s0,w,k0)`.

### 10. Aufgabe

Welche Aussagen ueber Akzeptanz bei Kellerautomaten im Sinne der Vorlesung sind richtig?

- [ ] A. Die Eingabe muss vollstaendig gelesen sein.
- [ ] B. Der Automat muss in einem Zustand aus `F` halten.
- [ ] C. Der Keller muss dabei immer bis auf `k0` geleert sein.
- [ ] D. Das Ende der Eingabe beendet den Lauf automatisch.

### 11. Aufgabe

Welche Aussagen ueber die Chomsky-Hierarchie sind richtig?

- [ ] A. Typ 3 entspricht regulaeren Sprachen und endlichen Automaten.
- [ ] B. Typ 2 entspricht kontextfreien Sprachen und Kellerautomaten.
- [ ] C. Typ 1 entspricht kontextsensitiven Sprachen und LBA.
- [ ] D. Typ 0 entspricht nur DEA.

### 12. Aufgabe

Welche Aussagen ueber Entscheidbarkeit sind richtig?

- [ ] A. Ein Problem ist entscheidbar, wenn es eine Turingmaschine gibt, die fuer jede Eingabe haelt und korrekt Ja/Nein antwortet.
- [ ] B. Akzeptierbarkeit ist automatisch dasselbe wie Entscheidbarkeit.
- [ ] C. Ein Entscheider darf bei manchen Eingaben endlos laufen.
- [ ] D. Jede entscheidbare Sprache ist auch akzeptierbar.

---

## Satz 3

### 1. Aufgabe

Welche Aussagen ueber Woerter und Sprachen sind richtig?

- [ ] A. Ein Wort ist eine endliche Folge von Zeichen.
- [ ] B. `|λ|=0`.
- [ ] C. Eine Sprache ist eine Menge von Woertern.
- [ ] D. Jede Sprache muss endlich sein.

### 2. Aufgabe

Welche Aussagen ueber `∈`, `⊆` und `⊂` sind richtig?

- [ ] A. `x∈M` bedeutet: `x` ist ein Element von `M`.
- [ ] B. `L⊆A*` bedeutet: `L` ist eine Teilmenge von `A*`.
- [ ] C. `B⊂A` bedeutet ueblicherweise: `B` ist eine echte Teilmenge von `A`.
- [ ] D. Fuer eine Sprache `L` ueber `A` schreibt man normalerweise `L∈A*`.

### 3. Aufgabe

Sei `T=(E,B,S,δ,s0)` eine deterministische Turingmaschine. Welche Aussagen sind richtig?

- [ ] A. `E` ist das Eingabealphabet.
- [ ] B. `B` ist das Bandalphabet.
- [ ] C. `δ:S×B→S×B×{R,L,N}` ist eine moegliche Form der Uebergangsfunktion.
- [ ] D. Eine Turingmaschine besitzt niemals einen Zustand.

### 4. Aufgabe

Gelte `δ(s,b)=(s',b',R)` fuer eine Turingmaschine. Welche Aussagen sind richtig?

- [ ] A. Das gelesene Bandzeichen `b` wird durch `b'` ueberschrieben.
- [ ] B. Der Folgezustand ist `s'`.
- [ ] C. Der Kopf bewegt sich nach rechts.
- [ ] D. Die Eingabe wird automatisch akzeptiert.

### 5. Aufgabe

Welche Aussagen ueber Startkonfigurationen sind richtig?

- [ ] A. Bei einer TM und `w≠λ` ist die Startkonfiguration `(λ,s0,w)`.
- [ ] B. Bei einem KA ist die Startkonfiguration `(s0,w,k0)`.
- [ ] C. Bei einem DEA beginnt die Berechnung im Startzustand `s0`.
- [ ] D. Der Startzustand muss immer ein Endzustand sein.

### 6. Aufgabe

Welche Aussagen ueber Relationen sind richtig?

- [ ] A. Eine Relation auf `X` kann als Teilmenge von `X×X` verstanden werden.
- [ ] B. `aRb` bedeutet, dass `a` in Relation `R` zu `b` steht.
- [ ] C. Eine symmetrische Relation muss automatisch reflexiv sein.
- [ ] D. Eine transitive Relation muss automatisch symmetrisch sein.

### 7. Aufgabe

Sei `k1 R k2 ⇔ k1 ist gruener als k2`. Welche Aussagen sind richtig?

- [ ] A. `R` ist reflexiv.
- [ ] B. `R` ist nicht reflexiv.
- [ ] C. `R` ist eine Aequivalenzrelation.
- [ ] D. Kein Objekt ist gruener als es selbst, wenn "gruener" streng gemeint ist.

### 8. Aufgabe

Welche Aussagen ueber Grammatiken sind richtig?

- [ ] A. `N` ist die Menge der Nichtterminale.
- [ ] B. `T` ist die Menge der Terminale.
- [ ] C. `S` ist das Startsymbol.
- [ ] D. `N` und `T` duerfen beliebig viele gemeinsame Elemente haben.

### 9. Aufgabe

Welche Aussagen ueber Ableitungen sind richtig?

- [ ] A. `S⇒*_G w` bedeutet, dass `w` in mehreren oder auch null Schritten aus `S` ableitbar ist.
- [ ] B. In `L(G)` stehen nur Woerter ueber dem Terminalalphabet `T`.
- [ ] C. Eine Ableitung ist beendet, wenn nur noch Terminale vorkommen.
- [ ] D. Nichtterminale und Terminale haben in einer Grammatik genau dieselbe Rolle.

### 10. Aufgabe

Welche Aussagen ueber Typ-3-Grammatiken sind richtig?

- [ ] A. Typ-3-Grammatiken beschreiben regulaere Sprachen.
- [ ] B. Typ-3-Sprachen koennen durch endliche Automaten erkannt werden.
- [ ] C. Rechtslineare Regeln haben typischerweise die Form `A→aB` oder `A→a`.
- [ ] D. Typ-3-Grammatiken sind maechtiger als Turingmaschinen.

### 11. Aufgabe

Welche Aussagen ueber die Konstruktion einer Grammatik aus einem DEA sind richtig?

- [ ] A. Zustaende des Automaten werden zu Nichtterminalen.
- [ ] B. Das Eingabealphabet wird zum Terminalalphabet.
- [ ] C. Aus `δ(s,e)=s'` wird eine Produktion `s→e s'`.
- [ ] D. Fuer Endzustaende kann eine Produktion `s→λ` eingefuehrt werden.

### 12. Aufgabe

Welche Aussagen ueber die Church'sche These sind richtig?

- [ ] A. Sie besagt, dass intuitiv berechenbare Funktionen durch Turingmaschinen berechnet werden koennen.
- [ ] B. Sie ist kein mathematischer Satz im ueblichen beweisbaren Sinn.
- [ ] C. Sie behauptet, dass endliche Automaten alle berechenbaren Funktionen berechnen.
- [ ] D. Sie steht im Zusammenhang mit dem Begriff der Berechenbarkeit.

---

## Satz 4

### 1. Aufgabe

Welche Aussagen ueber DEA-Graphen sind richtig?

- [ ] A. Ein eingehender Pfeil ohne Herkunft markiert den Startzustand.
- [ ] B. Ein Doppelkreis markiert einen Endzustand.
- [ ] C. Eine Kante ist mit einem Eingabezeichen beschriftet.
- [ ] D. Ein DEA darf keine Zustaende besitzen.

### 2. Aufgabe

Ein DEA akzeptiert genau die Woerter ueber `{a,b}`, die mit `a` enden. Welche Woerter werden akzeptiert?

- [ ] A. `a`
- [ ] B. `ba`
- [ ] C. `abb`
- [ ] D. `λ`

### 3. Aufgabe

Ein DEA akzeptiert genau die Woerter ueber `{0,1}`, die das Teilwort `00` enthalten. Welche Woerter werden akzeptiert?

- [ ] A. `00`
- [ ] B. `1001`
- [ ] C. `10101`
- [ ] D. `1100`

### 4. Aufgabe

Welche Aussagen ueber Mealy-Automaten sind richtig?

- [ ] A. Die Ausgabe kann vom aktuellen Zustand und vom aktuellen Eingabezeichen abhaengen.
- [ ] B. Im Graphen steht oft `e/a` an einer Kante.
- [ ] C. Die Ausgabefunktion hat die Form `γ:S×E→A`.
- [ ] D. Die Ausgabe steht zwingend nur in den Knoten.

### 5. Aufgabe

Welche Aussagen ueber Moore-Automaten sind richtig?

- [ ] A. Die Ausgabe haengt nur vom Zustand ab.
- [ ] B. Die Ausgabefunktion hat die Form `γ:S→A`.
- [ ] C. Im Graphen wird die Ausgabe oft am Zustand notiert.
- [ ] D. Die Ausgabe haengt direkt vom aktuell gelesenen Zeichen ab.

### 6. Aufgabe

Welche Aussagen ueber die Sprache `L={w∈{0,1}* | w enthaelt 011}` sind richtig?

- [ ] A. Ein DEA kann diese Sprache erkennen.
- [ ] B. Ein Moore-Automat kann bei Erreichen eines passenden Zustands eine Ausgabe erzeugen.
- [ ] C. Ein Mealy-Automat kann die Ausgabe auf dem Uebergang erzeugen, der das Muster vervollstaendigt.
- [ ] D. Kein endlicher Automat kann Teilwoerter erkennen.

### 7. Aufgabe

Welche Aussagen ueber `λ`-Uebergaenge sind richtig?

- [ ] A. Ein `λ`-Uebergang bewegt den Lesekopf auf dem Eingabeband nicht weiter.
- [ ] B. Bei einem deterministischen Automaten darf ein `λ`-Uebergang nicht zu Nichtdeterminismus fuehren.
- [ ] C. Bei einem NEA koennen `λ`-Uebergaenge fuer alternative Wege benutzt werden.
- [ ] D. Ein `λ`-Uebergang liest immer das Zeichen `λ` aus der Eingabe.

### 8. Aufgabe

Welche Aussagen ueber den Keller eines KA sind richtig?

- [ ] A. Der Keller arbeitet nach dem Last-In-First-Out-Prinzip.
- [ ] B. Das Kellerbodensymbol ist haeufig `k0`.
- [ ] C. Der Automat kann nur das oberste Kellersymbol direkt sehen.
- [ ] D. Ein Kellerautomat hat keinen Zustand.

### 9. Aufgabe

Gelte `δ(z0,b,A)=(z1,λ)` in einem KA. Welche Aussagen sind richtig?

- [ ] A. Das Eingabezeichen `b` wird gelesen.
- [ ] B. Der Zustand wechselt nach `z1`.
- [ ] C. Das oberste Kellersymbol `A` wird geloescht.
- [ ] D. Der gesamte Keller wird automatisch geloescht.

### 10. Aufgabe

Welche Aussagen ueber die Sprache `L={a^n b^n c^n | n≥1}` sind richtig?

- [ ] A. Sie ist ein typisches Beispiel fuer eine kontextsensitive Sprache.
- [ ] B. Sie kann mit einem LBA in Verbindung gebracht werden.
- [ ] C. Sie ist ein typisches Beispiel fuer eine regulaere Sprache.
- [ ] D. Sie verlangt den Vergleich dreier gleich grosser Bloecke.

### 11. Aufgabe

Welche Aussagen ueber Phrasentypen sind richtig?

- [ ] A. Eine Nominalphrase hat typischerweise ein Nomen als Kern.
- [ ] B. Eine Verbalphrase enthaelt typischerweise ein Verb.
- [ ] C. Eine Praepositionalphrase enthaelt typischerweise eine Praeposition.
- [ ] D. `NP`, `VP` und `PP` sind Namen fuer Turingmaschinen.

### 12. Aufgabe

Welche Aussagen ueber die Regeln `VP→V NP` und `VP→VP NP` sind richtig?

- [ ] A. `VP→V NP` kann eine Basisregel fuer eine Verbalphrase sein.
- [ ] B. `VP→VP NP` ist rekursiv, weil links und rechts wieder `VP` vorkommt.
- [ ] C. Beide Regeln sind kontextfrei, wenn links jeweils genau ein Nichtterminal steht.
- [ ] D. `VP→VP NP` kann ohne jede Basisregel keine endliche Ableitung liefern.

---

## Satz 5

### 1. Aufgabe

Welche Aussagen ueber `A*` und `A+` sind richtig?

- [ ] A. `A*` enthaelt `λ`.
- [ ] B. `A+` enthaelt `λ` immer.
- [ ] C. `A+` enthaelt alle nichtleeren Woerter ueber `A`.
- [ ] D. `A* = A+ ∪ {λ}`.

### 2. Aufgabe

Welche Aussagen ueber formale Sprachen sind richtig?

- [ ] A. Eine Sprache ueber `A` ist eine Teilmenge von `A*`.
- [ ] B. `∅` ist eine Sprache ueber jedem Alphabet `A`.
- [ ] C. `{λ}` ist dasselbe wie `∅`.
- [ ] D. Eine Sprache besteht aus Woertern, nicht aus Uebergaengen.

### 3. Aufgabe

Welche Aussagen ueber DEA und NEA sind richtig?

- [ ] A. Ein DEA hat fuer jede Kombination aus Zustand und Eingabezeichen genau einen Folgezustand.
- [ ] B. Ein NEA kann fuer eine Kombination mehrere Folgezustaende haben.
- [ ] C. Jeder NEA kann in einen aequivalenten DEA umgewandelt werden.
- [ ] D. DEA und NEA erkennen voellig verschiedene Klassen von Sprachen.

### 4. Aufgabe

Welche Aussagen ueber Table-Filling bei der DEA-Minimierung sind richtig?

- [ ] A. Man betrachtet Zustandspaare.
- [ ] B. Paare mit genau einem Endzustand sind unterscheidbar.
- [ ] C. Ein Paar kann spaeter markiert werden, wenn es unter einem Eingabezeichen auf ein markiertes Paar fuehrt.
- [ ] D. Markierte Paare sind die Paare, die am Ende verschmolzen werden.

### 5. Aufgabe

Welche Aussagen ueber Typ 1 der Chomsky-Hierarchie sind richtig?

- [ ] A. Typ 1 heißt kontextsensitiv.
- [ ] B. Typ 1 steht in Beziehung zu linear beschraenkten Automaten.
- [ ] C. Typ-1-Regeln sind im Normalfall nicht verkuerzend.
- [ ] D. Typ 1 ist dasselbe wie Typ 3.

### 6. Aufgabe

Welche Aussagen ueber Typ 2 der Chomsky-Hierarchie sind richtig?

- [ ] A. Typ 2 heißt kontextfrei.
- [ ] B. Bei Typ 2 steht links eine einzelne Variable.
- [ ] C. Typ 2 steht in Beziehung zu Kellerautomaten.
- [ ] D. Typ 2 ist weniger maechtig als Typ 3.

### 7. Aufgabe

Welche Aussagen ueber Typ 0 der Chomsky-Hierarchie sind richtig?

- [ ] A. Typ 0 ist unbeschraenkt.
- [ ] B. Typ 0 steht in Beziehung zu Turingmaschinen.
- [ ] C. Typ 0 hat strengere Regeln als Typ 3.
- [ ] D. Jede Grammatik ist zunaechst mindestens vom Typ 0.

### 8. Aufgabe

Welche Aussagen ueber Typ 3 der Chomsky-Hierarchie sind richtig?

- [ ] A. Typ 3 beschreibt regulaere Sprachen.
- [ ] B. Typ 3 steht in Beziehung zu endlichen Automaten.
- [ ] C. Rechtslineare Regeln sind typisch fuer Typ 3.
- [ ] D. Typ 3 ist maechtiger als Typ 0.

### 9. Aufgabe

Welche Aussagen ueber die Akzeptanz eines NEA sind richtig?

- [ ] A. Es reicht ein Weg vom Startzustand zu einem Endzustand, dessen Kantenbeschriftungen das Wort ergeben.
- [ ] B. `λ`-Beschriftungen tragen kein Zeichen zum gelesenen Wort bei.
- [ ] C. Jeder moegliche Weg muss erfolgreich sein.
- [ ] D. Der akzeptierende Weg muss nach dem ganzen Wort in einem Endzustand enden.

### 10. Aufgabe

Welche Aussagen ueber Endzustaende sind richtig?

- [ ] A. Bei Akzeptoren spielen Endzustaende eine zentrale Rolle.
- [ ] B. Bei DEA wird ein Wort akzeptiert, wenn der Zustand nach dem Lesen des Wortes in `F` liegt.
- [ ] C. Bei einer Akzeptor-TM wird akzeptiert, wenn die Maschine in einem Zustand aus `F` haelt.
- [ ] D. Jeder Zustand ist automatisch ein Endzustand.

### 11. Aufgabe

Welche Aussagen ueber die Bandinschrift bei Akzeptor-Turingmaschinen sind richtig?

- [ ] A. Fuer Akzeptanz ist entscheidend, ob die Maschine in einem akzeptierenden Endzustand haelt.
- [ ] B. Die Bandinschrift am Ende ist fuer die reine Akzeptanz nicht das entscheidende Kriterium.
- [ ] C. Eine Akzeptor-TM wird zur Modellierung von Entscheidungsproblemen benutzt.
- [ ] D. Eine Eingabe wird nur akzeptiert, wenn am Ende das Eingabewort unveraendert auf dem Band steht.

### 12. Aufgabe

Welche Aussagen ueber Protagonisten und Begriffe sind richtig?

- [ ] A. Alan Turing steht in Verbindung mit der Turingmaschine.
- [ ] B. Noam Chomsky steht in Verbindung mit der Chomsky-Hierarchie.
- [ ] C. Die Church'sche These steht in Verbindung mit Berechenbarkeit.
- [ ] D. Der Begriff "Turingmaschine" bezeichnet einen Kellerautomaten ohne Keller.

---

## Satz 6

### 1. Aufgabe

Welche Aussagen sind richtig?

- [ ] A. `λ` ist ein Wort.
- [ ] B. `λ` ist dasselbe wie `∅`.
- [ ] C. `{λ}` ist eine Sprache.
- [ ] D. `∅` ist eine Sprache.

### 2. Aufgabe

Sei `A={0,1}`. Welche Aussagen sind richtig?

- [ ] A. `010∈A*`.
- [ ] B. `2∈A*`.
- [ ] C. `{0,11}⊆A*`.
- [ ] D. `A⊆A*`.

### 3. Aufgabe

Welche Aussagen ueber totale und partielle Funktionen sind im Kontext der Vorlesung richtig?

- [ ] A. Beim DEA ohne `λ`-Uebergaenge ist `δ` fuer alle Kombinationen `(s,e)` definiert.
- [ ] B. Bei einer Turingmaschine kann `δ` partiell sein.
- [ ] C. Ist `δ` bei einer TM fuer eine Situation nicht definiert, kann die Maschine halten.
- [ ] D. Ein DEA ohne `λ`-Uebergaenge darf bei einem gelesenen Zeichen zwei verschiedene Folgezustaende haben.

### 4. Aufgabe

Welche Aussagen ueber Akzeptieren und Entscheiden sind richtig?

- [ ] A. Ein Entscheider muss fuer jede Eingabe halten.
- [ ] B. Ein Akzeptor muss bei jeder nicht akzeptierten Eingabe halten.
- [ ] C. Wenn eine Maschine in `F` haelt, akzeptiert sie.
- [ ] D. Akzeptieren ist im Allgemeinen schwaecher als Entscheiden.

### 5. Aufgabe

Welche Aussagen ueber einen LBA sind richtig?

- [ ] A. Ein LBA besitzt eine lineare Platzbeschraenkung.
- [ ] B. Die Konstanten `k` und `c` werden fuer jedes Wort neu geraten.
- [ ] C. Reale Rechner motivieren die Betrachtung beschraenkten Speichers.
- [ ] D. Der erlaubte Platz kann von `|w|` abhaengen.

### 6. Aufgabe

Welche Aussagen ueber Kelleroperationen sind richtig?

- [ ] A. Rechts `λ` in `δ(s,e,k)=(s',λ)` bedeutet, dass `k` entfernt wird.
- [ ] B. Links `λ` in `δ(s,λ,k)` bedeutet, dass kein Eingabezeichen gelesen wird.
- [ ] C. Wenn der Keller unveraendert bleiben soll, schreibt man rechts normalerweise das alte Kellersymbol wieder hin.
- [ ] D. `δ(s,e,k)=(s',λ)` bedeutet, dass das Eingabezeichen `e` nicht gelesen wird.

### 7. Aufgabe

Welche Aussagen ueber die Sprache `L={w∈{a,b,$}* | w=u$ũ, u∈{a,b}*}` sind richtig?

- [ ] A. Vor dem `$` kann ein KA Zeichen auf den Keller legen.
- [ ] B. Nach dem `$` kann ein KA passende Kellerzeichen entfernen.
- [ ] C. `$` trennt die beiden Wortteile.
- [ ] D. Die Sprache verlangt keinen Vergleich mit umgekehrter Reihenfolge.

### 8. Aufgabe

Welche Aussagen ueber Minimierung und Aequivalenz von DEA sind richtig?

- [ ] A. Zwei DEA sind aequivalent, wenn sie dieselbe Sprache akzeptieren.
- [ ] B. Ziel der Minimierung ist ein aequivalenter DEA mit minimaler Zustandsanzahl.
- [ ] C. Nicht erreichbare Zustaende koennen fuer die akzeptierte Sprache irrelevant sein.
- [ ] D. Markierte Zustandspaare gelten als aequivalent.

### 9. Aufgabe

Welche Aussagen ueber Grammatiken und Sprachen sind richtig?

- [ ] A. `L(G)` enthaelt nur Woerter aus `T*`.
- [ ] B. `S` ist das Startsymbol.
- [ ] C. Terminale sind Symbole, die am Ende in den erzeugten Woertern stehen koennen.
- [ ] D. Nichtterminale muessen in einem fertigen Wort erhalten bleiben.

### 10. Aufgabe

Welche Aussagen ueber Phrasenregeln sind richtig?

- [ ] A. `NP→N` kann eine Nominalphrase auf ein Nomen zurueckfuehren.
- [ ] B. `NP→A N` kann Adjektiv plus Nomen modellieren.
- [ ] C. `PP→P NP` kann eine Praepositionalphrase modellieren.
- [ ] D. `VP→V NP` enthaelt kein Verb.

### 11. Aufgabe

Welche Aussagen ueber Nichtdeterminismus sind richtig?

- [ ] A. Bei Nichtdeterminismus kann es mehrere moegliche Folgezustaende geben.
- [ ] B. Bei NEA und NTM ist die Existenz eines akzeptierenden Pfades zentral.
- [ ] C. Nichtdeterminismus bedeutet, dass der Automat gar keine Regeln hat.
- [ ] D. Potenzmengen treten in Definitionen nichtdeterministischer Modelle auf.

### 12. Aufgabe

Welche Aussagen eignen sich als sichere Merksaetze fuer die Klausur?

- [ ] A. `δ` liest ein Zeichen, `δ*` liest ein Wort.
- [ ] B. Beim KA steht links `K`, rechts `K*`.
- [ ] C. Beim NEA reicht mindestens ein akzeptierender Pfad.
- [ ] D. Bei der DEA-Minimierung werden markierte Paare verschmolzen.
