# AFS Zusatztraining: 6 Klausur-Saetze mit je 30 Aufgaben

> Form: unbestimmte Multiple-Choice-Aufgaben.  
> Pro Aufgabe koennen 0 bis 4 Antworten richtig sein.  
> Empfehlung: 30 Aufgaben in 60 Minuten bearbeiten.

---

## Satz A

### 1. Aufgabe

Welche Aussagen ueber Alphabete, Woerter und Sprachen sind richtig?

- [ ] A. Ein Alphabet ist eine nichtleere, endliche Menge von Zeichen.
- [ ] B. Die leere Menge ist ein Alphabet.
- [ ] C. Ein Wort ist eine endliche Folge von Zeichen.
- [ ] D. Eine Sprache ueber `A` ist eine Teilmenge von `A*`.

### 2. Aufgabe

Sei `A` ein Alphabet. Welche Aussagen sind richtig?

- [ ] A. `λ∈A*`.
- [ ] B. `λ∈A+`.
- [ ] C. `A^0={λ}`.
- [ ] D. `A+=A*\{λ}`.

### 3. Aufgabe

Welche Aussagen ueber die Symbole `∈`, `⊆` und `⊂` sind richtig?

- [ ] A. `x∈M` bedeutet: `x` ist ein Element von `M`.
- [ ] B. `L⊆A*` bedeutet: `L` ist eine Teilmenge von `A*`.
- [ ] C. `B⊂A` bedeutet ueblicherweise: `B` ist eine echte Teilmenge von `A`.
- [ ] D. Fuer eine Sprache `L` ueber `A` schreibt man normalerweise `L∈A*`.

### 4. Aufgabe

Sei `M={p,q}`. Welche Aussagen sind richtig?

- [ ] A. `P(M)` ist die Menge aller Teilmengen von `M`.
- [ ] B. `{p}∈P(M)`.
- [ ] C. `p∈P(M)`.
- [ ] D. `∅∈P(M)`.

### 5. Aufgabe

Sei `A=(E,S,δ,s0,F)` ein DEA. Welche Aussagen sind richtig?

- [ ] A. `δ:S×E→S`.
- [ ] B. `δ*:S×E*→S`.
- [ ] C. `δ` liest direkt ganze Woerter aus `E*`.
- [ ] D. `δ*` beschreibt die wiederholte Anwendung von `δ` auf ein Wort.

### 6. Aufgabe

Welche Aussagen ueber die Akzeptanz eines DEA sind richtig?

- [ ] A. `w∈L(A)` gilt genau dann, wenn `δ*(s0,w)∈F`.
- [ ] B. `δ(s0,w)∈F` ist fuer jedes Wort `w∈E*` die normale Akzeptanzbedingung.
- [ ] C. Nach dem Lesen des ganzen Wortes muss der erreichte Zustand in `F` liegen.
- [ ] D. Jeder Zustand eines DEA ist automatisch ein Endzustand.

### 7. Aufgabe

Ein DEA hat die Zustaende `0` und `1`. `0` ist Startzustand, `1` ist Endzustand. Das Zeichen `n` laesst den Zustand unveraendert, das Zeichen `d` wechselt zwischen `0` und `1`. Welche Woerter werden akzeptiert?

- [ ] A. `d`
- [ ] B. `ndd`
- [ ] C. `ndndd`
- [ ] D. `nn`

### 8. Aufgabe

Welche Aussagen ueber NEA sind richtig?

- [ ] A. Die Uebergangsfunktion eines NEA kann die Form `δ:S×E→P(S)` haben.
- [ ] B. Der Folgezustand eines NEA ist immer genau ein Zustand.
- [ ] C. Ein Wort wird akzeptiert, wenn mindestens ein Rechenpfad akzeptierend endet.
- [ ] D. Ein Wort wird nur akzeptiert, wenn jeder Rechenpfad akzeptierend endet.

### 9. Aufgabe

Welche Aussagen ueber `λ`-Uebergaenge sind richtig?

- [ ] A. Ein `λ`-Uebergang verbraucht kein Eingabezeichen.
- [ ] B. Ein `λ`-Uebergang liest das Eingabezeichen `λ` aus dem Eingabewort.
- [ ] C. Bei einem deterministischen Automaten darf ein `λ`-Uebergang nicht zu Nichtdeterminismus fuehren.
- [ ] D. Bei einem NEA koennen `λ`-Uebergaenge fuer alternative Wege benutzt werden.

### 10. Aufgabe

Welche Aussagen ueber Turingmaschinen sind richtig?

- [ ] A. Eine deterministische Turingmaschine kann als `T=(E,B,S,δ,s0)` angegeben werden.
- [ ] B. Eine Akzeptor-Turingmaschine besitzt zusaetzlich eine Endzustandsmenge `F`.
- [ ] C. Fuer eine Turingmaschine hat `δ` dieselbe Form wie beim DEA, also `δ:S×E→S`.
- [ ] D. Die Uebergangsfunktion einer Turingmaschine kann partiell sein.

### 11. Aufgabe

Welche Aussagen ueber Konfigurationen einer Turingmaschine sind richtig?

- [ ] A. Eine Konfiguration hat die Form `(v,s,w)`.
- [ ] B. `s` ist der aktuelle Zustand.
- [ ] C. `v` beschreibt den Bandteil links vom Kopf.
- [ ] D. `w` ist immer das urspruengliche Eingabewort.

### 12. Aufgabe

Welche Aussagen ueber Akzeptor-Turingmaschinen sind richtig?

- [ ] A. Haelt die Maschine in einem Zustand aus `F`, so akzeptiert sie.
- [ ] B. Bei nicht akzeptierten Eingaben muss eine Akzeptor-Turingmaschine nicht unbedingt halten.
- [ ] C. `L(T)` ist die Menge aller von `T` akzeptierten Woerter.
- [ ] D. Nicht akzeptieren bedeutet immer, dass die Maschine in einem Nicht-Endzustand haelt.

### 13. Aufgabe

Welche Aussagen ueber Entscheider sind richtig?

- [ ] A. Ein Entscheider haelt fuer jede Eingabe.
- [ ] B. Ein Entscheider liefert eine korrekte Ja/Nein-Antwort.
- [ ] C. Jeder Akzeptor ist automatisch ein Entscheider.
- [ ] D. Jede entscheidbare Sprache ist auch akzeptierbar.

### 14. Aufgabe

Welche Aussagen ueber LBA sind richtig?

- [ ] A. Bei einem LBA sind `k` und `c` feste natuerliche Zahlen.
- [ ] B. `k` und `c` duerfen nach der konkreten Eingabe gewaehlt werden.
- [ ] C. Der erlaubte Speicherplatz ist linear in der Eingabelaenge.
- [ ] D. Ein LBA ist maechtiger als eine allgemeine Turingmaschine.

### 15. Aufgabe

Welche Aussagen ueber die Uebergangsfunktion eines KA im Sinne der Vorlesung sind richtig?

- [ ] A. `δ:S×(E∪{λ})×K→S×K*`.
- [ ] B. Links steht der ganze Kellerinhalt `K*`.
- [ ] C. Rechts darf ein Wort aus `K*` stehen.
- [ ] D. An der Eingabeposition darf `λ` stehen.

### 16. Aufgabe

Welche Aussagen ueber `λ` beim Kellerautomaten sind richtig?

- [ ] A. In `δ(s,λ,k)` bedeutet `λ`, dass kein Eingabezeichen gelesen wird.
- [ ] B. In `δ(s,e,k)=(s',λ)` bedeutet `λ`, dass das oberste Kellersymbol geloescht wird.
- [ ] C. Rechts `λ` bedeutet, dass kein Eingabezeichen gelesen wird.
- [ ] D. Soll der Keller unveraendert bleiben, schreibt man das alte Kellersymbol wieder hin.

### 17. Aufgabe

Welche Aussagen ueber KA-Konfigurationen sind richtig?

- [ ] A. Eine KA-Konfiguration hat die Form `(s,w,v)`.
- [ ] B. Die Startkonfiguration ist `(s0,w,k0)`.
- [ ] C. `w` ist der noch nicht gelesene Teil der Eingabe.
- [ ] D. `v` ist der aktuelle Zustand.

### 18. Aufgabe

Welche Aussagen ueber Akzeptanz bei KA im Sinne der Vorlesung sind richtig?

- [ ] A. Die Eingabe muss vollstaendig gelesen sein.
- [ ] B. Der Automat muss in einem Zustand aus `F` halten.
- [ ] C. Der Keller muss immer bis auf `k0` geleert sein.
- [ ] D. Das Ende der Eingabe beendet den Lauf automatisch.

### 19. Aufgabe

Welche Aussagen ueber nichtdeterministische Kellerautomaten sind richtig?

- [ ] A. `δ:S×(E∪{λ})×K→P(S×K*)`.
- [ ] B. `δ` liefert eine Menge moeglicher Folgepaare.
- [ ] C. Akzeptanz bedeutet: Es gibt mindestens einen akzeptierenden Rechenpfad.
- [ ] D. Bei einem NKA darf ein `λ`-Uebergang nie gleichzeitig mit einem normalen Uebergang moeglich sein.

### 20. Aufgabe

Welche Aussagen ueber die Sprache `{a^n b^n | n≥0}` sind richtig?

- [ ] A. Ein KA kann fuer jedes gelesene `a` ein Symbol auf den Keller legen.
- [ ] B. Ein KA kann fuer jedes gelesene `b` ein Symbol vom Keller entfernen.
- [ ] C. Ein DEA ohne Zusatzspeicher reicht fuer diese Sprache aus.
- [ ] D. Zustaende koennen die Reihenfolge der `a`-Phase und `b`-Phase kontrollieren.

### 21. Aufgabe

Welche Aussagen ueber die Sprache `{u$ũ | u∈{a,b}*}` sind richtig?

- [ ] A. `$` dient als Trennzeichen in der Eingabe.
- [ ] B. Vor dem `$` koennen Zeichen auf dem Keller gespeichert werden.
- [ ] C. Nach dem `$` wird in umgekehrter Reihenfolge mit dem Keller verglichen.
- [ ] D. Ein Kellersymbol `A` muss immer fuer das ganze Wort `ab` stehen.

### 22. Aufgabe

Welche Aussagen ueber DEA-Minimierung sind richtig?

- [ ] A. Nicht erreichbare Zustaende koennen entfernt werden.
- [ ] B. Paare mit genau einem Endzustand werden markiert.
- [ ] C. Ein unmarkiertes Paar wird markiert, wenn es auf ein bereits markiertes Paar fuehrt.
- [ ] D. Am Ende werden die markierten Paare verschmolzen.

### 23. Aufgabe

Welche Aussagen ueber Aequivalenzrelationen sind richtig?

- [ ] A. Eine Aequivalenzrelation ist reflexiv, symmetrisch und transitiv.
- [ ] B. Die Relation "`x` ist groesser als `y`" ist eine Aequivalenzrelation.
- [ ] C. Die Relation "`x` ist gruener als `y`" ist bei strenger Bedeutung nicht reflexiv.
- [ ] D. Die Relation "zwei Woerter haben dieselbe Laenge" ist eine Aequivalenzrelation.

### 24. Aufgabe

Welche Aussagen ueber Aequivalenzklassen und Quotientenmengen sind richtig?

- [ ] A. `X/~ = {[a]~ | a∈X}`.
- [ ] B. `[a]~` ist eine Teilmenge von `X`.
- [ ] C. `[a]~` ist normalerweise ein einzelnes Element von `X`.
- [ ] D. Die Quotientenmenge enthaelt Aequivalenzklassen.

### 25. Aufgabe

Welche Aussagen ueber Moore-Automaten sind richtig?

- [ ] A. `γ:S→A`.
- [ ] B. Die Ausgabe haengt nur vom Zustand ab.
- [ ] C. Die Ausgabe steht an den Kanten.
- [ ] D. Die Ausgabe haengt direkt vom aktuellen Eingabezeichen ab.

### 26. Aufgabe

Welche Aussagen ueber Mealy-Automaten sind richtig?

- [ ] A. `γ:S×E→A`.
- [ ] B. Die Ausgabe kann an den Kanten notiert werden.
- [ ] C. Die Ausgabe haengt nur vom Zustand ab.
- [ ] D. Die Ausgabe kann vom aktuellen Eingabezeichen abhaengen.

### 27. Aufgabe

Sei `G=(N,T,P,S)` eine formale Grammatik. Welche Aussagen sind richtig?

- [ ] A. `N∩T=∅`.
- [ ] B. `S∈N`.
- [ ] C. `L(G)⊆T*`.
- [ ] D. Auf der linken Seite einer Produktion darf nur ein Wort aus Terminalsymbolen stehen.

### 28. Aufgabe

Welche Aussagen ueber Ableitungen in Grammatiken sind richtig?

- [ ] A. `S⇒*_G w` bedeutet, dass `w` aus `S` ableitbar ist.
- [ ] B. Eine fertige Ableitung enthaelt nur noch Terminale.
- [ ] C. Fuer `w∈L(G)` gilt `w∈T*`.
- [ ] D. Nichtterminale muessen in fertigen Woertern erhalten bleiben.

### 29. Aufgabe

Welche Aussagen ueber die Chomsky-Hierarchie sind richtig?

- [ ] A. Typ 0 steht in Beziehung zu Turingmaschinen.
- [ ] B. Typ 1 steht in Beziehung zu LBA.
- [ ] C. Typ 2 steht in Beziehung zu Kellerautomaten.
- [ ] D. Typ 3 steht ausschliesslich in Beziehung zu Turingmaschinen.

### 30. Aufgabe

Welche Aussagen ueber die Konstruktion einer Typ-3-Grammatik aus einem DEA sind richtig?

- [ ] A. Zustaende werden zu Nichtterminalen.
- [ ] B. Eingabezeichen werden zu Terminalen.
- [ ] C. Aus `δ(s,e)=s'` wird eine Regel `s→e s'`.
- [ ] D. Fuer Endzustaende kann eine Regel `s→λ` eingefuehrt werden.

---

## Satz B

### 1. Aufgabe

Sei `A={a,b,c}`. Welche Aussagen sind richtig?

- [ ] A. `abc∈A*`.
- [ ] B. `λ∈A+`.
- [ ] C. `{a,bb,λ}⊆A*`.
- [ ] D. `d∈A*`.

### 2. Aufgabe

Welche Aussagen ueber Sprachen sind richtig?

- [ ] A. `∅` ist eine Sprache ueber jedem Alphabet.
- [ ] B. `{λ}` ist eine Sprache.
- [ ] C. `∅={λ}`.
- [ ] D. Eine Sprache kann unendlich viele Woerter enthalten.

### 3. Aufgabe

Sei `A=(E,S,δ,s0,F)` ein DEA. Welche Aussagen sind richtig?

- [ ] A. `F⊆S`.
- [ ] B. `s0∈S`.
- [ ] C. `δ` ist bei einem vollstaendigen DEA fuer alle Paare `(s,e)` definiert.
- [ ] D. `E` ist die Menge der Endzustaende.

### 4. Aufgabe

Ein DEA akzeptiert genau die Woerter ueber `{0,1}`, die mit `1` enden. Welche Woerter werden akzeptiert?

- [ ] A. `1`
- [ ] B. `101`
- [ ] C. `100`
- [ ] D. `λ`

### 5. Aufgabe

Ein DEA akzeptiert genau die Woerter ueber `{a,b}`, die das Teilwort `aa` enthalten. Welche Woerter werden akzeptiert?

- [ ] A. `aa`
- [ ] B. `baab`
- [ ] C. `abab`
- [ ] D. `bbaa`

### 6. Aufgabe

Welche Aussagen ueber `δ*` sind richtig?

- [ ] A. `δ*(s,λ)=s`.
- [ ] B. `δ*(s,xe)=δ(δ*(s,x),e)` fuer `x∈E*` und `e∈E`.
- [ ] C. `δ*` liest nur ein Zeichen.
- [ ] D. `δ*` wird zur Formulierung der Akzeptanz ganzer Woerter benutzt.

### 7. Aufgabe

Welche Aussagen ueber NEA und DEA sind richtig?

- [ ] A. Jeder DEA ist auch als spezieller NEA auffassbar.
- [ ] B. Jeder NEA kann in einen aequivalenten DEA ueberfuehrt werden.
- [ ] C. NEA erkennen genau die regulaeren Sprachen.
- [ ] D. NEA sind immer maechtiger als Turingmaschinen.

### 8. Aufgabe

Welche Aussagen ueber die Potenzmengenkonstruktion sind richtig?

- [ ] A. Zustaende des neuen DEA koennen Teilmengen der alten NEA-Zustandsmenge sein.
- [ ] B. Der Name kommt daher, dass mit `P(S)` gearbeitet wird.
- [ ] C. Sie zeigt, dass NEA und DEA gleich maechtig fuer regulaere Sprachen sind.
- [ ] D. Sie entfernt alle Endzustaende.

### 9. Aufgabe

Welche Aussagen ueber TM-Konfigurationen sind richtig?

- [ ] A. `(v,s,w)` kodiert auch die Kopfposition implizit.
- [ ] B. `vw` beschreibt die aktuelle Bandinschrift im relevanten Bereich.
- [ ] C. Der Zustand steht in der Mitte.
- [ ] D. Die Kopfposition muss immer zusaetzlich als Zahl angegeben werden.

### 10. Aufgabe

Welche Aussagen ueber Turingmaschinen-Uebergaenge sind richtig?

- [ ] A. Bei `δ(s,b)=(s',b',L)` wird `b` durch `b'` ersetzt.
- [ ] B. `L` bedeutet Bewegung nach links.
- [ ] C. `N` bedeutet keine Kopfbewegung.
- [ ] D. `R` bedeutet, dass das Wort sofort akzeptiert wird.

### 11. Aufgabe

Welche Aussagen ueber Akzeptor-Turingmaschinen sind richtig?

- [ ] A. Die Bandinschrift am Ende ist fuer reine Akzeptanz nicht entscheidend.
- [ ] B. Entscheidend ist, ob die Maschine in einem akzeptierenden Endzustand haelt.
- [ ] C. `L(T)` enthaelt alle Eingaben, bei denen `T` akzeptiert.
- [ ] D. Eine Akzeptor-TM muss immer auf jeder Eingabe halten.

### 12. Aufgabe

Welche Aussagen ueber LBA sind richtig?

- [ ] A. LBA sind Turingmaschinen mit beschraenktem Bandbereich.
- [ ] B. Der erlaubte Bereich ist linear durch `k·|w|+c` beschraenkt.
- [ ] C. `k` und `c` duerfen negative ganze Zahlen sein.
- [ ] D. `|w|` darf den erlaubten Platz beeinflussen.

### 13. Aufgabe

Welche Aussagen ueber KA-Kelleroperationen sind richtig?

- [ ] A. `δ(s,a,k0)=(s,Ak0)` kann bedeuten, dass `A` auf den Keller gelegt wird.
- [ ] B. `δ(s,b,A)=(s',λ)` kann bedeuten, dass `A` entfernt wird.
- [ ] C. Der Keller arbeitet nach FIFO.
- [ ] D. Nur das oberste Kellersymbol ist direkt sichtbar.

### 14. Aufgabe

Welche Aussagen ueber den Kellerinhalt sind richtig?

- [ ] A. Das Kellerbodensymbol wird haeufig mit `k0` bezeichnet.
- [ ] B. `K` ist das Kelleralphabet.
- [ ] C. `K*` ist die Menge der Kellerwoerter.
- [ ] D. `K` ist immer identisch mit dem Eingabealphabet `E`.

### 15. Aufgabe

Welche Aussagen ueber KA-Akzeptanz sind im Sinne der Vorlesung richtig?

- [ ] A. Der Automat muss nach endlich vielen Schritten halten.
- [ ] B. Die Eingabe muss vollstaendig gelesen sein.
- [ ] C. Der Haltezustand muss in `F` liegen.
- [ ] D. Der Keller muss zwingend leer sein.

### 16. Aufgabe

Welche Aussagen ueber NKA sind richtig?

- [ ] A. Ein NKA kann mehrere moegliche Folgepaare besitzen.
- [ ] B. Akzeptanz ist existenziell: mindestens ein Pfad reicht.
- [ ] C. `δ` bildet auf `P(S×K*)` ab.
- [ ] D. Ein NKA darf keine `λ`-Uebergaenge haben.

### 17. Aufgabe

Welche Aussagen ueber `a^n b^n` und `a^n b^n c^n` sind richtig?

- [ ] A. `a^n b^n` ist typisch kontextfrei.
- [ ] B. `a^n b^n` kann mit einem KA erkannt werden.
- [ ] C. `a^n b^n c^n` ist typisch kontextsensitiv.
- [ ] D. `a^n b^n c^n` ist typisch regulaer.

### 18. Aufgabe

Welche Aussagen ueber DEA-Minimierung sind richtig?

- [ ] A. Zwei Zustaende sind unterscheidbar, wenn es ein Wort gibt, das von einem Zustand zur Akzeptanz und vom anderen zur Nichtakzeptanz fuehrt.
- [ ] B. Aequivalente Zustaende koennen verschmolzen werden.
- [ ] C. Nicht erreichbare Zustaende muessen fuer die erkannte Sprache beachtet werden.
- [ ] D. Ziel ist ein aequivalenter Automat mit weniger oder minimalen Zustaenden.

### 19. Aufgabe

Welche Aussagen ueber Relationen sind richtig?

- [ ] A. Reflexiv bedeutet: fuer alle `a` gilt `aRa`.
- [ ] B. Symmetrisch bedeutet: aus `aRb` folgt `bRa`.
- [ ] C. Transitiv bedeutet: aus `aRb` und `bRc` folgt `aRc`.
- [ ] D. Jede Relation ist automatisch eine Aequivalenzrelation.

### 20. Aufgabe

Sei `~` auf Woertern definiert durch: `u~v` genau dann, wenn `|u|=|v|`. Welche Aussagen sind richtig?

- [ ] A. `~` ist reflexiv.
- [ ] B. `~` ist symmetrisch.
- [ ] C. `~` ist transitiv.
- [ ] D. `~` ist keine Aequivalenzrelation.

### 21. Aufgabe

Welche Aussagen ueber Moore/Mealy sind richtig?

- [ ] A. Moore: Ausgabe im Zustand.
- [ ] B. Mealy: Ausgabe an der Kante.
- [ ] C. Moore: `γ:S×E→A`.
- [ ] D. Mealy: `γ:S×E→A`.

### 22. Aufgabe

Welche Aussagen ueber formale Grammatiken sind richtig?

- [ ] A. Eine Grammatik ist ein Tupel `G=(N,T,P,S)`.
- [ ] B. `P` ist die Menge der Produktionen.
- [ ] C. `S` ist ein Terminalsymbol.
- [ ] D. Terminale und Nichtterminale sind disjunkt.

### 23. Aufgabe

Welche Aussagen ueber Produktionen sind richtig?

- [ ] A. Auf der linken Seite muss mindestens ein Nichtterminal vorkommen.
- [ ] B. `S→aSb` ist eine moegliche kontextfreie Regel.
- [ ] C. `S→ab` kann eine Basisregel sein.
- [ ] D. Links duerfen in jeder Grammatik ausschliesslich Terminale stehen.

### 24. Aufgabe

Welche Aussagen ueber Typ 1 sind richtig?

- [ ] A. Typ 1 heisst kontextsensitiv.
- [ ] B. Typ 1 steht in Beziehung zu LBA.
- [ ] C. Typ-1-Regeln sind im Normalfall nicht verkuerzend.
- [ ] D. Typ 1 ist dasselbe wie regulaer.

### 25. Aufgabe

Welche Aussagen ueber Typ 2 sind richtig?

- [ ] A. Typ 2 heisst kontextfrei.
- [ ] B. Links steht genau ein Nichtterminal.
- [ ] C. Typ 2 steht in Beziehung zu Kellerautomaten.
- [ ] D. Typ 2 ist staerker eingeschraenkt als Typ 3.

### 26. Aufgabe

Welche Aussagen ueber Typ 3 sind richtig?

- [ ] A. Typ 3 heisst regulaer.
- [ ] B. Typ 3 steht in Beziehung zu endlichen Automaten.
- [ ] C. Rechtslineare Regeln sind typisch fuer Typ 3.
- [ ] D. Typ 3 enthaelt alle Typ-0-Sprachen.

### 27. Aufgabe

Welche Aussagen ueber DEA zu Grammatik sind richtig?

- [ ] A. Der Startzustand wird zum Startsymbol.
- [ ] B. Endzustaende koennen `λ`-Produktionen erhalten.
- [ ] C. Fehlerzustaende koennen bei fehlenden Uebergaengen ergaenzt werden.
- [ ] D. Eingabezeichen werden zu Nichtterminalen.

### 28. Aufgabe

Welche Aussagen ueber die Church'sche These sind richtig?

- [ ] A. Sie verbindet intuitive Berechenbarkeit mit Turing-Berechenbarkeit.
- [ ] B. Sie ist eine Definition eines DEA.
- [ ] C. Sie ist kein normaler mathematisch beweisbarer Satz.
- [ ] D. Sie ist fuer Berechenbarkeitstheorie relevant.

### 29. Aufgabe

Welche Aussagen ueber Entscheidbarkeit sind richtig?

- [ ] A. Entscheidbar bedeutet Halten auf jeder Eingabe.
- [ ] B. Die Antwort muss korrekt Ja/Nein sein.
- [ ] C. Eine Maschine, die nur akzeptierte Woerter haelt, ist automatisch ein Entscheider.
- [ ] D. Entscheidbarkeit ist staerker als blosse Akzeptierbarkeit.

### 30. Aufgabe

Welche Aussagen ueber typische Sprachmuster sind richtig?

- [ ] A. Woerter, die mit einem bestimmten Zeichen enden, sind regulaer.
- [ ] B. Woerter, die ein festes Teilwort enthalten, sind regulaer.
- [ ] C. Klammerpruefung ist typisch fuer Kellerautomaten.
- [ ] D. Jede Sprache mit gleicher Anzahl von Symbolen ist regulaer.

---

## Satz C

### 1. Aufgabe

Welche Aussagen ueber Mengen und Teilmengen sind richtig?

- [ ] A. Aus `x∈M` folgt nicht, dass `x⊆M` sinnvoll sein muss.
- [ ] B. Aus `B⊆A` folgt, dass jedes Element von `B` auch Element von `A` ist.
- [ ] C. `A⊆A` ist immer wahr.
- [ ] D. `A⊂A` ist bei strenger Bedeutung wahr.

### 2. Aufgabe

Sei `A={a}`. Welche Aussagen sind richtig?

- [ ] A. `A*={λ,a,aa,aaa,...}`.
- [ ] B. `A+={a,aa,aaa,...}`.
- [ ] C. `λ∈A+`.
- [ ] D. `{aa,aaa}⊆A*`.

### 3. Aufgabe

Welche Aussagen ueber Eingabealphabete und Bandalphabete sind richtig?

- [ ] A. Bei einer TM ist `E` das Eingabealphabet.
- [ ] B. Bei einer TM ist `B` das Bandalphabet.
- [ ] C. Das Bandalphabet kann mehr Zeichen enthalten als das Eingabealphabet.
- [ ] D. Das Eingabealphabet enthaelt immer das Blanksymbol.

### 4. Aufgabe

Welche Aussagen ueber TM-Halten sind richtig?

- [ ] A. Ist `δ` fuer eine aktuelle Situation nicht definiert, kann die TM halten.
- [ ] B. Halten in `F` bedeutet Akzeptanz bei einer Akzeptor-TM.
- [ ] C. Halten ausserhalb von `F` bedeutet nicht akzeptieren.
- [ ] D. Nicht halten kann ebenfalls nicht akzeptieren bedeuten.

### 5. Aufgabe

Welche Aussagen ueber Startkonfigurationen sind richtig?

- [ ] A. TM bei `w≠λ`: `(λ,s0,w)`.
- [ ] B. KA bei Eingabe `w`: `(s0,w,k0)`.
- [ ] C. DEA beginnt in `s0`.
- [ ] D. NEA beginnt ohne Startzustand.

### 6. Aufgabe

Welche Aussagen ueber DEA mit `λ`-Uebergaengen im deterministischen Sinn der Vorlesung sind richtig?

- [ ] A. Ein `λ`-Uebergang wechselt den Zustand ohne Lesekopfbewegung.
- [ ] B. Wenn gleichzeitig normale Uebergaenge moeglich sind, kann Nichtdeterminismus entstehen.
- [ ] C. `λ` ist ein normales Zeichen des Eingabewortes.
- [ ] D. Ohne `λ`-Uebergaenge ist `δ` beim DEA fuer alle `(s,e)` definiert.

### 7. Aufgabe

Welche Aussagen ueber NEA-Akzeptanz sind richtig?

- [ ] A. Es existiert ein Weg vom Startzustand zu einem Endzustand.
- [ ] B. Die Kantenbeschriftungen ergeben zusammen das gelesene Wort.
- [ ] C. `λ`-Beschriftungen tragen kein Zeichen bei.
- [ ] D. Alle Wege muessen in Endzustaenden enden.

### 8. Aufgabe

Welche Aussagen ueber einen Rechenbaum sind richtig?

- [ ] A. Er kann bei nichtdeterministischen Maschinen entstehen.
- [ ] B. Verzweigungen stehen fuer verschiedene moegliche Folgeschritte.
- [ ] C. Ein akzeptierender Pfad reicht bei nichtdeterministischer Akzeptanz.
- [ ] D. Ein Rechenbaum tritt nur bei DEA auf.

### 9. Aufgabe

Welche Aussagen ueber KA-Uebergaenge sind richtig?

- [ ] A. Bei `δ(s,e,k)=(s',v)` wird `k` durch `v` ersetzt.
- [ ] B. Der Rest des Kellers unterhalb von `k` bleibt erhalten.
- [ ] C. `v` darf `λ` sein.
- [ ] D. `v` muss immer genau ein Zeichen lang sein.

### 10. Aufgabe

Welche Aussagen ueber `δ(s0,a,k0)=(s0,Ak0)` sind richtig?

- [ ] A. Das Eingabezeichen `a` wird gelesen.
- [ ] B. `k0` wird durch `Ak0` ersetzt.
- [ ] C. Anschaulich wird `A` ueber `k0` gelegt.
- [ ] D. Der Automat wechselt zwingend in einen Endzustand.

### 11. Aufgabe

Welche Aussagen ueber `δ(s1,λ,k0)=(se,k0)` sind richtig?

- [ ] A. Es wird kein Eingabezeichen gelesen.
- [ ] B. Der Zustand wechselt nach `se`.
- [ ] C. Das Kellerbodensymbol bleibt erhalten.
- [ ] D. Das Eingabewort muss ein Zeichen `λ` enthalten.

### 12. Aufgabe

Welche Aussagen ueber die Sprache `{ww | w∈{0,1}*}` sind richtig?

- [ ] A. Eine NTM kann die Mitte nichtdeterministisch raten.
- [ ] B. Die Sprache steht in der Vorlesung im Zusammenhang mit Nichtdeterminismus.
- [ ] C. Ein einfacher DEA erkennt diese Sprache ohne Zusatzidee fuer beliebige `w`.
- [ ] D. Es muss ein Vergleich zweier Worthaelften erfolgen.

### 13. Aufgabe

Welche Aussagen ueber Moore/Mealy-Graphen sind richtig?

- [ ] A. Bei Mealy steht oft `Eingabe/Ausgabe` an Kanten.
- [ ] B. Bei Moore steht die Ausgabe oft im Zustand.
- [ ] C. Bei Moore ist die Ausgabe unabhaengig davon, ueber welche Kante der Zustand erreicht wurde.
- [ ] D. Bei Mealy ist die Ausgabe immer unabhaengig vom Eingabezeichen.

### 14. Aufgabe

Welche Aussagen ueber DEA-Minimierung mit Gruppenverfahren sind richtig?

- [ ] A. Man kann zunaechst Endzustaende und Nicht-Endzustaende trennen.
- [ ] B. Gruppen werden weiter aufgeteilt, wenn Zustaende bei gleicher Eingabe in verschiedene Gruppen gehen.
- [ ] C. Der Prozess wird wiederholt, bis keine Inkonsistenzen mehr auftreten.
- [ ] D. Am Ende werden alle Endzustaende mit allen Nicht-Endzustaenden verschmolzen.

### 15. Aufgabe

Welche Aussagen ueber Aequivalenz von DEA sind richtig?

- [ ] A. Zwei DEA sind aequivalent, wenn sie dieselbe Sprache akzeptieren.
- [ ] B. Ein minimierter DEA soll zur Ausgangsmaschine aequivalent sein.
- [ ] C. Aequivalenz bedeutet immer gleiche Anzahl von Zustaenden.
- [ ] D. Aequivalente Zustaende koennen in der Minimierung zusammengelegt werden.

### 16. Aufgabe

Welche Aussagen ueber Quotientenmengen sind richtig?

- [ ] A. Die Elemente von `X/~` sind Aequivalenzklassen.
- [ ] B. Jede Aequivalenzklasse ist eine Teilmenge von `X`.
- [ ] C. Jede Aequivalenzklasse enthaelt mindestens einen Vertreter.
- [ ] D. `X/~` ist immer leer.

### 17. Aufgabe

Welche Aussagen ueber deutsche Grammatikbegriffe aus der Vorlesung sind richtig?

- [ ] A. Ein Subjekt beantwortet oft die Frage "Wer oder was?".
- [ ] B. Ein Praedikat enthaelt typischerweise ein Verb.
- [ ] C. Ein Objekt kann eine Ergaenzung zum Verb sein.
- [ ] D. Ein Subjekt ist immer ein Kellersymbol.

### 18. Aufgabe

Welche Aussagen ueber Phrasentypen sind richtig?

- [ ] A. `NP` steht fuer Nominalphrase.
- [ ] B. `VP` steht fuer Verbalphrase.
- [ ] C. `PP` steht fuer Praepositionalphrase.
- [ ] D. `NP` steht fuer nichtdeterministische Potenzmenge.

### 19. Aufgabe

Welche Aussagen ueber rekursive Grammatikregeln sind richtig?

- [ ] A. Eine Regel wie `NP→NP PP` ist rekursiv.
- [ ] B. Rekursion kann wiederholte Erweiterungen modellieren.
- [ ] C. Eine rekursive Regel braucht fuer endliche Ableitungen passende Basisregeln.
- [ ] D. Rekursive Regeln sind in Grammatiken grundsaetzlich verboten.

### 20. Aufgabe

Welche Aussagen ueber `L(G)` sind richtig?

- [ ] A. `L(G)` enthaelt die Terminalwoerter, die aus `S` ableitbar sind.
- [ ] B. `L(G)={w∈T* | S⇒*_G w}`.
- [ ] C. Woerter mit verbleibenden Nichtterminalen gehoeren normalerweise nicht zu `L(G)`.
- [ ] D. `L(G)` ist immer leer.

### 21. Aufgabe

Welche Aussagen ueber Chomsky-Typen sind richtig?

- [ ] A. Typ 3 ist in Typ 2 enthalten.
- [ ] B. Typ 2 ist in Typ 1 enthalten.
- [ ] C. Typ 1 ist in Typ 0 enthalten.
- [ ] D. Typ 0 ist in Typ 3 enthalten.

### 22. Aufgabe

Welche Aussagen ueber regulaere Sprachen sind richtig?

- [ ] A. Sie koennen durch endliche Automaten erkannt werden.
- [ ] B. Sie koennen durch Typ-3-Grammatiken beschrieben werden.
- [ ] C. Jede regulaere Sprache ist auch kontextfrei.
- [ ] D. Keine regulaere Sprache enthaelt mehr als drei Woerter.

### 23. Aufgabe

Welche Aussagen ueber kontextfreie Sprachen sind richtig?

- [ ] A. Sie stehen in Beziehung zu Kellerautomaten.
- [ ] B. `a^n b^n` ist ein typisches Beispiel.
- [ ] C. Jede kontextfreie Sprache ist regulaer.
- [ ] D. Typ 2 ist die zugehoerige Chomsky-Klasse.

### 24. Aufgabe

Welche Aussagen ueber kontextsensitive Sprachen sind richtig?

- [ ] A. Sie stehen in Beziehung zu LBA.
- [ ] B. `a^n b^n c^n` ist ein typisches Beispiel.
- [ ] C. Typ 1 ist die zugehoerige Chomsky-Klasse.
- [ ] D. Sie sind weniger maechtig als regulaere Sprachen.

### 25. Aufgabe

Welche Aussagen ueber unbeschraenkte Grammatiken sind richtig?

- [ ] A. Sie gehoeren zu Typ 0.
- [ ] B. Sie stehen in Beziehung zu Turingmaschinen.
- [ ] C. Sie haben keine Einschraenkungen wie Typ 3.
- [ ] D. Sie sind identisch mit endlichen Automaten.

### 26. Aufgabe

Welche Aussagen ueber typische falsche LNW-Formulierungen sind richtig?

- [ ] A. "jeder Rechenpfad muss akzeptieren" ist bei NEA meist zu stark.
- [ ] B. "automatisch" ist bei Haltebedingungen oft verdaechtig.
- [ ] C. "mindestens ein Rechenpfad" passt zu Nichtdeterminismus.
- [ ] D. "δ liest ein ganzes Wort" ist beim DEA die normale Aussage.

### 27. Aufgabe

Welche Aussagen ueber `S×(E∪{λ})×K→S×K*` sind richtig?

- [ ] A. Die Form passt zu deterministischen Kellerautomaten im Sinne der Vorlesung.
- [ ] B. `E∪{λ}` erlaubt normale Eingabezeichen oder keinen Eingabeverbrauch.
- [ ] C. Rechts `K*` erlaubt auch das leere Wort.
- [ ] D. Links `K` bedeutet, dass der Automat den ganzen Keller gleichzeitig liest.

### 28. Aufgabe

Welche Aussagen ueber Sprachen und Entscheidungsprobleme sind richtig?

- [ ] A. Entscheidungsprobleme koennen als Sprachen modelliert werden.
- [ ] B. Ein Wort gehoert zur Sprache, wenn die Antwort "Ja" ist.
- [ ] C. Akzeptor-Turingmaschinen koennen zur Modellierung von Entscheidungsproblemen genutzt werden.
- [ ] D. Eine Sprache ist immer eine Funktion mit Zahlenwerten.

### 29. Aufgabe

Welche Aussagen ueber Klausur-Merksaetze sind richtig?

- [ ] A. `δ` liest ein Zeichen, `δ*` liest ein Wort.
- [ ] B. Beim KA steht links `K`, rechts `K*`.
- [ ] C. Moore: Ausgabe im Zustand.
- [ ] D. Bei der DEA-Minimierung werden markierte Paare verschmolzen.

### 30. Aufgabe

Welche Aussagen ueber sichere Pruefstrategien sind richtig?

- [ ] A. Jede Antwortoption sollte einzeln beurteilt werden.
- [ ] B. Die Anzahl richtiger Antworten kann zwischen 0 und 4 liegen.
- [ ] C. Starke Woerter wie "jeder", "stets" und "automatisch" sollte man besonders pruefen.
- [ ] D. Wenn eine Option lang formuliert ist, ist sie automatisch richtig.

---

## Satz D

### 1. Aufgabe

Ein DEA hat die Zustaende `s0` und `s1`. `s0` ist Startzustand und zugleich Endzustand. Das Zeichen `b` laesst den Zustand unveraendert, das Zeichen `a` wechselt zwischen `s0` und `s1`. Welche Woerter werden akzeptiert?

- [ ] A. `aa`
- [ ] B. `bb`
- [ ] C. `ab`
- [ ] D. `abba`

### 2. Aufgabe

Betrachten Sie denselben DEA wie in Aufgabe 1. Welche Aussagen sind richtig?

- [ ] A. `λ` wird akzeptiert.
- [ ] B. `a` wird akzeptiert.
- [ ] C. Der Automat akzeptiert genau die Woerter mit gerader Anzahl von `a`.
- [ ] D. Das Zeichen `b` aendert den Zustand nicht.

### 3. Aufgabe

Ein Mealy-Automat mit Startzustand `z0` sei durch folgende Tabelle gegeben: In Zustand `z0` gilt bei Eingabe `0`: `z0/0`, bei Eingabe `1`: `z1/1`. In Zustand `z1` gilt bei Eingabe `0`: `z1/1`, bei Eingabe `1`: `z0/0`. Welche Aussagen sind richtig?

- [ ] A. Bei Eingabe `11` ist die Ausgabe `10`.
- [ ] B. Bei Eingabe `00` ist die Ausgabe `00`.
- [ ] C. Bei Eingabe `1` ist die Ausgabe `0`.
- [ ] D. Die Ausgabe hat fuer jede Eingabe dieselbe Laenge wie die Eingabe.

### 4. Aufgabe

Betrachten Sie den Mealy-Automaten aus Aufgabe 3. Welche Aussagen sind richtig?

- [ ] A. Bei Eingabe `01` ist die Ausgabe `01`.
- [ ] B. Bei Eingabe `10` ist die Ausgabe `11`.
- [ ] C. Bei Eingabe `101` ist die Ausgabe `110`.
- [ ] D. Nach Eingabe `11` befindet sich der Automat wieder in `z0`.

### 5. Aufgabe

Sei `A=(E,S,δ,s0,F)` ein DEA. Welche Aussagen ueber `δ` und `δ*` sind richtig?

- [ ] A. `δ*(s,λ)=s`.
- [ ] B. `δ*(s,ab)=δ(δ(s,a),b)`, falls `a,b∈E`.
- [ ] C. `δ(s,ab)` ist die normale Anwendung von `δ` auf ein Wort der Laenge 2.
- [ ] D. `w∈L(A)` gilt genau dann, wenn `δ*(s0,w)∈F`.

### 6. Aufgabe

Welche Aussagen ueber DEA sind richtig?

- [ ] A. Bei einem vollstaendigen DEA ist `δ` fuer jedes Paar `(s,e)` definiert.
- [ ] B. Ein DEA hat fuer ein Paar `(s,e)` genau einen Folgezustand.
- [ ] C. Wenn ein Lauf unterwegs einen Endzustand besucht, wird das Wort sofort akzeptiert, auch wenn noch Eingabe uebrig ist.
- [ ] D. Entscheidend ist der Zustand nach dem Lesen des ganzen Wortes.

### 7. Aufgabe

Welche Aussagen ueber NEA sind richtig?

- [ ] A. Die Uebergangsfunktion kann auf `P(S)` abbilden.
- [ ] B. Die leere Menge als Menge von Folgezustaenden ist moeglich.
- [ ] C. Ein Wort wird akzeptiert, wenn alle Rechenpfade akzeptierend enden.
- [ ] D. Ein Wort wird akzeptiert, wenn mindestens ein akzeptierender Rechenpfad existiert.

### 8. Aufgabe

Welche Aussagen ueber die Potenzmengenkonstruktion sind richtig?

- [ ] A. Zustaende des konstruierten DEA koennen Teilmengen der NEA-Zustandsmenge sein.
- [ ] B. Die Konstruktion zeigt, dass NEA und DEA dieselben regulaeren Sprachen erkennen.
- [ ] C. Bei der Konstruktion werden niemals Endzustaende benoetigt.
- [ ] D. Der Startzustand des DEA haengt vom Startzustand und gegebenenfalls von `λ`-Erreichbarkeit ab.

### 9. Aufgabe

Welche Aussagen ueber die Table-Filling-Minimierung eines DEA sind richtig?

- [ ] A. Paare mit genau einem Endzustand werden markiert.
- [ ] B. Ein markiertes Paar gilt als unterscheidbar.
- [ ] C. Ein unmarkiertes Paar kann markiert werden, wenn es unter einem Eingabezeichen auf ein markiertes Paar fuehrt.
- [ ] D. Am Ende werden markierte Paare verschmolzen.

### 10. Aufgabe

Welche Aussagen ueber das Gruppenverfahren bei der DEA-Minimierung sind richtig?

- [ ] A. Man kann zunaechst Endzustaende und Nicht-Endzustaende trennen.
- [ ] B. Gruppen werden weiter aufgeteilt, wenn Zustaende bei gleicher Eingabe in verschiedene Gruppen fuehren.
- [ ] C. Der Prozess wird wiederholt, bis keine Inkonsistenzen mehr auftreten.
- [ ] D. Nicht erreichbare Zustaende muessen zwingend im Minimalautomaten erhalten bleiben.

### 11. Aufgabe

Welche Aussagen ueber Moore- und Mealy-Automaten sind richtig?

- [ ] A. Beim Moore-Automaten hat `γ` die Form `S→A`.
- [ ] B. Beim Mealy-Automaten hat `γ` die Form `S×E→A`.
- [ ] C. Beim Moore-Automaten haengt die Ausgabe direkt vom aktuell gelesenen Eingabezeichen ab.
- [ ] D. Beim Mealy-Automaten kann die Ausgabe an Kanten notiert werden.

### 12. Aufgabe

Welche Aussagen ueber Ausgabeautomaten sind richtig?

- [ ] A. Bei einem Mealy-Automaten steht im Graphen oft `Eingabe/Ausgabe` an einer Kante.
- [ ] B. Bei einem Moore-Automaten steht die Ausgabe typischerweise am Zustand.
- [ ] C. Moore und Mealy unterscheiden sich darin, wovon die Ausgabe abhaengt.
- [ ] D. Ein Ausgabeautomat besitzt keine Zustandsmenge.

### 13. Aufgabe

Welche Aussagen ueber Konfigurationen einer Turingmaschine sind richtig?

- [ ] A. Eine Konfiguration hat die Form `(v,s,w)`.
- [ ] B. `v` ist der Bandinhalt links vom Kopf.
- [ ] C. `s` ist der aktuelle Zustand.
- [ ] D. `w` ist immer das vollstaendige urspruengliche Eingabewort.

### 14. Aufgabe

Gelte bei einer Turingmaschine `δ(s,b)=(s',b',L)`. Welche Aussagen sind richtig?

- [ ] A. `b` wird durch `b'` ersetzt.
- [ ] B. Der Folgezustand ist `s'`.
- [ ] C. Der Kopf bewegt sich nach links.
- [ ] D. Der Lauf akzeptiert automatisch.

### 15. Aufgabe

Welche Aussagen ueber Akzeptor-Turingmaschinen sind richtig?

- [ ] A. Haelt die Maschine in einem Zustand aus `F`, so akzeptiert sie.
- [ ] B. Haelt die Maschine in `S\F`, so akzeptiert sie nicht.
- [ ] C. Haelt die Maschine gar nicht, so akzeptiert sie ebenfalls nicht.
- [ ] D. Nicht akzeptieren bedeutet immer, dass die Maschine haelt.

### 16. Aufgabe

Welche Aussagen ueber Entscheidbarkeit sind richtig?

- [ ] A. Ein Entscheider muss fuer jede Eingabe halten.
- [ ] B. Ein Entscheider gibt eine korrekte Ja/Nein-Antwort.
- [ ] C. Jeder Akzeptor ist automatisch ein Entscheider.
- [ ] D. Entscheidbarkeit ist staerker als blosse Akzeptierbarkeit.

### 17. Aufgabe

Welche Aussagen ueber LBA sind richtig?

- [ ] A. Ein LBA besitzt eine lineare Platzbeschraenkung.
- [ ] B. Die Konstanten `k` und `c` sind fest.
- [ ] C. `k` und `c` werden nach dem Lesen der Eingabe frei gewaehlt.
- [ ] D. Der erlaubte Platz darf von `|w|` abhaengen.

### 18. Aufgabe

Welche Aussagen ueber die Uebergangsfunktion eines KA sind richtig?

- [ ] A. `δ:S×(E∪{λ})×K→S×K*`.
- [ ] B. Links wird nur ein oberstes Kellersymbol betrachtet.
- [ ] C. Rechts kann ein Wort aus `K*` stehen.
- [ ] D. Links steht immer der ganze Kellerinhalt.

### 19. Aufgabe

Welche Aussagen ueber `λ` beim Kellerautomaten sind richtig?

- [ ] A. In `δ(s,λ,k)` wird kein Eingabezeichen gelesen.
- [ ] B. In `δ(s,e,k)=(s',λ)` wird das oberste Kellersymbol geloescht.
- [ ] C. Rechts `λ` bedeutet, dass die Eingabe nicht weitergelesen wird.
- [ ] D. Wenn der Keller unveraendert bleiben soll, wird das alte Kellersymbol wieder hingeschrieben.

### 20. Aufgabe

Welche Aussagen ueber Akzeptanz bei KA im Sinne der Vorlesung sind richtig?

- [ ] A. Die Eingabe muss vollstaendig gelesen sein.
- [ ] B. Der Automat muss in einem Zustand aus `F` halten.
- [ ] C. Der Keller muss zwingend leer sein.
- [ ] D. Das Ende der Eingabe beendet den Lauf automatisch.

### 21. Aufgabe

Welche Aussagen ueber NKA sind richtig?

- [ ] A. `δ:S×(E∪{λ})×K→P(S×K*)`.
- [ ] B. Es kann mehrere moegliche Folgepaare geben.
- [ ] C. Mindestens ein akzeptierender Rechenpfad reicht.
- [ ] D. Ein NKA besitzt keinen Keller.

### 22. Aufgabe

Welche Aussagen ueber `L={a^n b^n | n≥0}` sind richtig?

- [ ] A. Ein KA kann fuer jedes `a` ein Symbol auf den Keller legen.
- [ ] B. Ein KA kann fuer jedes `b` ein Symbol entfernen.
- [ ] C. Ein DEA ohne Zusatzspeicher erkennt diese Sprache.
- [ ] D. Zustaende koennen die `a`-Phase und die `b`-Phase trennen.

### 23. Aufgabe

Welche Aussagen ueber `L={u$ũ | u∈{a,b}*}` sind richtig?

- [ ] A. Vor dem `$` kann der KA Zeichen speichern.
- [ ] B. Nach dem `$` wird mit dem Keller in umgekehrter Reihenfolge verglichen.
- [ ] C. `$` ist ein Trennzeichen in der Eingabe.
- [ ] D. `$` muss zwingend ein Kellersymbol sein.

### 24. Aufgabe

Welche Aussagen ueber `P(S)` sind richtig?

- [ ] A. `P(S)` ist die Menge aller Teilmengen von `S`.
- [ ] B. `∅∈P(S)`.
- [ ] C. `S∈P(S)`.
- [ ] D. Aus `s∈S` folgt immer `s∈P(S)`.

### 25. Aufgabe

Welche Aussagen ueber Relationen sind richtig?

- [ ] A. Eine Aequivalenzrelation ist reflexiv, symmetrisch und transitiv.
- [ ] B. "`x` ist groesser als `y`" ist reflexiv.
- [ ] C. "`x` hat dieselbe Laenge wie `y`" ist eine Aequivalenzrelation auf Woertern.
- [ ] D. "`x` ist gruener als `y`" ist bei strenger Bedeutung nicht reflexiv.

### 26. Aufgabe

Welche Aussagen ueber Quotientenmengen sind richtig?

- [ ] A. `X/~ = {[a]~ | a∈X}`.
- [ ] B. Die Elemente von `X/~` sind Aequivalenzklassen.
- [ ] C. `[a]~` ist eine Teilmenge von `X`.
- [ ] D. `[a]~` ist normalerweise ein einzelnes Element von `X`.

### 27. Aufgabe

Sei `G=(N,T,P,S)` eine formale Grammatik. Welche Aussagen sind richtig?

- [ ] A. `N∩T=∅`.
- [ ] B. `S∈N`.
- [ ] C. `L(G)={w∈T* | S⇒*_G w}`.
- [ ] D. Auf der linken Seite einer Produktion darf nur ein Wort aus Terminalsymbolen stehen.

### 28. Aufgabe

Welche Aussagen ueber die Chomsky-Hierarchie sind richtig?

- [ ] A. Typ 0 steht in Beziehung zu Turingmaschinen.
- [ ] B. Typ 1 steht in Beziehung zu LBA.
- [ ] C. Typ 2 steht in Beziehung zu Kellerautomaten.
- [ ] D. Typ 3 steht in Beziehung zu endlichen Automaten.

### 29. Aufgabe

Welche Aussagen ueber die Konstruktion einer Typ-3-Grammatik aus einem DEA sind richtig?

- [ ] A. Zustaende werden zu Nichtterminalen.
- [ ] B. Eingabezeichen werden zu Terminalen.
- [ ] C. Aus `δ(s,e)=s'` wird eine Produktion `s→e s'`.
- [ ] D. Fuer Endzustaende kann eine Produktion `s→λ` eingefuehrt werden.

### 30. Aufgabe

Welche Aussagen ueber die Church'sche These und Entscheidbarkeit sind richtig?

- [ ] A. Die Church'sche These verbindet intuitive Berechenbarkeit mit Turing-Berechenbarkeit.
- [ ] B. Sie ist ein normaler mathematisch beweisbarer Satz.
- [ ] C. Entscheidbar bedeutet Halten auf jeder Eingabe mit korrekter Ja/Nein-Antwort.
- [ ] D. Eine entscheidbare Sprache ist auch akzeptierbar.

---

## Satz E

### 1. Aufgabe

Welche Aussagen ueber `A*` und `A+` sind richtig?

- [ ] A. `A*` enthaelt Woerter beliebiger endlicher Laenge.
- [ ] B. `A+` enthaelt nur nichtleere Woerter.
- [ ] C. `A^0={λ}`.
- [ ] D. `A+` enthaelt immer das leere Wort.

### 2. Aufgabe

Welche Aussagen ueber Sprachen sind richtig?

- [ ] A. Eine Sprache ueber `A` ist eine Teilmenge von `A*`.
- [ ] B. `∅` ist eine Sprache ueber `A`.
- [ ] C. `{λ}` ist dieselbe Sprache wie `∅`.
- [ ] D. Eine Sprache kann unendlich viele Woerter enthalten.

### 3. Aufgabe

Welche Aussagen ueber `∈` und `⊆` sind richtig?

- [ ] A. Bei `x∈M` ist `x` ein Element von `M`.
- [ ] B. Bei `L⊆A*` ist `L` eine Menge von Woertern.
- [ ] C. Eine Sprache `L` ueber `A` schreibt man normalerweise als `L⊆A*`.
- [ ] D. Eine Sprache `L` ueber `A` schreibt man normalerweise als `L∈A*`.

### 4. Aufgabe

Welche Aussagen ueber DEA-Graphen sind richtig?

- [ ] A. Ein eingehender Pfeil ohne Herkunft markiert den Startzustand.
- [ ] B. Ein Doppelkreis markiert einen Endzustand.
- [ ] C. Kanten sind mit Eingabezeichen beschriftet.
- [ ] D. Der Startzustand darf nie Endzustand sein.

### 5. Aufgabe

Ein DEA akzeptiert genau Woerter ueber `{0,1}`, die eine gerade Anzahl von `1` enthalten. Welche Woerter werden akzeptiert?

- [ ] A. `λ`
- [ ] B. `11`
- [ ] C. `101`
- [ ] D. `111`

### 6. Aufgabe

Ein DEA akzeptiert genau Woerter ueber `{a,b}`, die mit `b` enden. Welche Woerter werden akzeptiert?

- [ ] A. `b`
- [ ] B. `ab`
- [ ] C. `ba`
- [ ] D. `λ`

### 7. Aufgabe

Welche Aussagen ueber `δ*` sind richtig?

- [ ] A. `δ*` ist nuetzlich, um ganze Woerter zu verarbeiten.
- [ ] B. `δ*(s,λ)=s`.
- [ ] C. `δ*(s,xe)=δ(δ*(s,x),e)` fuer `x∈E*` und `e∈E`.
- [ ] D. `δ*` ersetzt beim DEA die Zustandsmenge `S`.

### 8. Aufgabe

Welche Aussagen ueber nichtdeterministische Automaten sind richtig?

- [ ] A. Nichtdeterminismus kann als mehrere moegliche Folgeschritte verstanden werden.
- [ ] B. Akzeptiert wird, wenn mindestens ein erfolgreicher Pfad existiert.
- [ ] C. Alle Pfade muessen erfolgreich sein.
- [ ] D. Potenzmengen treten in Definitionen nichtdeterministischer Modelle auf.

### 9. Aufgabe

Welche Aussagen ueber NEA mit `λ`-Uebergaengen sind richtig?

- [ ] A. `λ`-Kanten tragen kein Zeichen zum gelesenen Wort bei.
- [ ] B. Die Uebergangsfunktion kann `E∪{λ}` verwenden.
- [ ] C. Ein `λ`-Uebergang verbraucht ein Eingabezeichen.
- [ ] D. Ein NEA mit `λ`-Uebergaengen kann regulaere Sprachen erkennen.

### 10. Aufgabe

Welche Aussagen ueber Turingmaschinen sind richtig?

- [ ] A. Das Bandalphabet kann mehr Zeichen enthalten als das Eingabealphabet.
- [ ] B. Das Blanksymbol gehoert typischerweise nicht zum Eingabealphabet.
- [ ] C. Eine Turingmaschine kann das Band beschreiben.
- [ ] D. Eine Turingmaschine hat keinen Zustand.

### 11. Aufgabe

Welche Aussagen ueber die Startkonfiguration einer TM sind richtig?

- [ ] A. Fuer `w≠λ` ist sie `(λ,s0,w)`.
- [ ] B. Der Kopf steht anfangs auf dem ersten Zeichen von `w`.
- [ ] C. Fuer `w=λ` steht der Kopf auf einem Blank.
- [ ] D. Der Zustand steht in der Konfiguration nie in der Mitte.

### 12. Aufgabe

Welche Aussagen ueber Akzeptor-TM und Entscheider sind richtig?

- [ ] A. Eine Akzeptor-TM muss bei nicht akzeptierten Eingaben nicht unbedingt halten.
- [ ] B. Ein Entscheider muss fuer jede Eingabe halten.
- [ ] C. Akzeptieren ist im Allgemeinen schwaecher als Entscheiden.
- [ ] D. Akzeptieren und Entscheiden bedeuten immer dasselbe.

### 13. Aufgabe

Welche Aussagen ueber LBA sind richtig?

- [ ] A. Ein LBA ist linear beschraenkt.
- [ ] B. `k` und `c` sind Konstanten der Maschine.
- [ ] C. `k` und `c` koennen nachtraeglich passend zur Eingabe gewaehlt werden.
- [ ] D. Der Speicher ist durch `k·|w|+c` beschraenkt.

### 14. Aufgabe

Welche Aussagen ueber KA-Konfigurationen sind richtig?

- [ ] A. Eine KA-Konfiguration hat die Form `(s,w,v)`.
- [ ] B. `w` ist der noch nicht gelesene Eingabeteil.
- [ ] C. `v` ist der Kellerinhalt.
- [ ] D. Die Startkonfiguration ist `(λ,s0,w)`.

### 15. Aufgabe

Welche Aussagen ueber KA-Uebergaenge sind richtig?

- [ ] A. In `δ(s,e,k)=(s',v)` wird `k` durch `v` ersetzt.
- [ ] B. Der Kellerrest unterhalb von `k` bleibt erhalten.
- [ ] C. `v` darf `λ` sein.
- [ ] D. `v` muss immer ein einzelnes Kellersymbol sein.

### 16. Aufgabe

Welche Aussagen ueber `δ(z0,b,A)=(z1,λ)` sind richtig?

- [ ] A. Das Zeichen `b` wird gelesen.
- [ ] B. Der Zustand wechselt nach `z1`.
- [ ] C. Das oberste Kellerzeichen `A` wird entfernt.
- [ ] D. Der gesamte Keller wird geloescht.

### 17. Aufgabe

Welche Aussagen ueber einen KA fuer `a^n b^n` sind richtig?

- [ ] A. Fuer jedes `a` kann ein Symbol gespeichert werden.
- [ ] B. Fuer jedes `b` kann ein gespeichertes Symbol entfernt werden.
- [ ] C. Ein Zustand kann die Umschaltung von der `a`-Phase zur `b`-Phase markieren.
- [ ] D. Die Sprache ist regulaer.

### 18. Aufgabe

Welche Aussagen ueber einen KA fuer Palindrome mit Trenner `$` sind richtig?

- [ ] A. Vor `$` werden Zeichen gespeichert.
- [ ] B. Nach `$` wird mit dem Keller verglichen.
- [ ] C. Der Vergleich geschieht in umgekehrter Reihenfolge.
- [ ] D. `$` muss als Kellerbodensymbol verwendet werden.

### 19. Aufgabe

Welche Aussagen ueber Moore-Automaten sind richtig?

- [ ] A. Die Ausgabe haengt nur vom Zustand ab.
- [ ] B. `γ:S→A`.
- [ ] C. Die Ausgabe wird typischerweise an Kanten notiert.
- [ ] D. Moore-Automaten haben keine Zustaende.

### 20. Aufgabe

Welche Aussagen ueber Mealy-Automaten sind richtig?

- [ ] A. Die Ausgabe haengt vom Zustand und Eingabezeichen ab.
- [ ] B. `γ:S×E→A`.
- [ ] C. Im Graphen steht oft `e/a` an einer Kante.
- [ ] D. Die Ausgabe ist immer unabhaengig vom Eingabezeichen.

### 21. Aufgabe

Welche Aussagen ueber `G=(N,T,P,S)` sind richtig?

- [ ] A. `N` ist die Menge der Nichtterminale.
- [ ] B. `T` ist die Menge der Terminale.
- [ ] C. `P` ist die Menge der Produktionen.
- [ ] D. `S` ist ein Terminalsymbol.

### 22. Aufgabe

Welche Aussagen ueber Produktionen sind richtig?

- [ ] A. Links muss mindestens ein Nichtterminal vorkommen.
- [ ] B. `S→aSb` kann eine kontextfreie Regel sein.
- [ ] C. `S→ab` kann eine Basisregel sein.
- [ ] D. Links duerfen nur Terminale stehen.

### 23. Aufgabe

Welche Aussagen ueber `L(G)` sind richtig?

- [ ] A. `L(G)` enthaelt terminale Woerter.
- [ ] B. `L(G)={w∈T* | S⇒*_G w}`.
- [ ] C. Woerter mit verbleibenden Nichtterminalen gehoeren nicht zu `L(G)`.
- [ ] D. `L(G)` ist immer endlich.

### 24. Aufgabe

Welche Aussagen ueber Chomsky-Typen sind richtig?

- [ ] A. Typ 3 ist regulaer.
- [ ] B. Typ 2 ist kontextfrei.
- [ ] C. Typ 1 ist kontextsensitiv.
- [ ] D. Typ 0 ist unbeschraenkt.

### 25. Aufgabe

Welche Aussagen ueber die Zuordnung von Typen und Automaten sind richtig?

- [ ] A. Typ 3 gehoert zu endlichen Automaten.
- [ ] B. Typ 2 gehoert zu Kellerautomaten.
- [ ] C. Typ 1 gehoert zu LBA.
- [ ] D. Typ 0 gehoert zu Turingmaschinen.

### 26. Aufgabe

Welche Aussagen ueber Typ-3-Grammatiken sind richtig?

- [ ] A. Rechtslineare Regeln sind typisch.
- [ ] B. Typ-3-Sprachen sind regulaer.
- [ ] C. Typ-3-Sprachen koennen von DEA erkannt werden.
- [ ] D. Typ 3 ist maechtiger als Typ 0.

### 27. Aufgabe

Welche Aussagen ueber Typ-2-Grammatiken sind richtig?

- [ ] A. Links steht genau ein Nichtterminal.
- [ ] B. Sie beschreiben kontextfreie Sprachen.
- [ ] C. Sie stehen in Beziehung zu Kellerautomaten.
- [ ] D. Jede Typ-2-Sprache ist regulaer.

### 28. Aufgabe

Welche Aussagen ueber die Church'sche These sind richtig?

- [ ] A. Sie betrifft den Begriff der Berechenbarkeit.
- [ ] B. Sie verbindet intuitive Berechenbarkeit mit Turing-Berechenbarkeit.
- [ ] C. Sie ist kein normal beweisbarer mathematischer Satz.
- [ ] D. Sie besagt, dass DEA alle Funktionen berechnen.

### 29. Aufgabe

Welche Aussagen ueber typische Sprachmuster sind richtig?

- [ ] A. Woerter mit festem Endzeichen sind regulaer.
- [ ] B. Woerter mit festem Teilwort sind regulaer.
- [ ] C. Klammerpruefung passt zu Kellerautomaten.
- [ ] D. `a^n b^n c^n` ist typisch regulaer.

### 30. Aufgabe

Welche Aussagen ueber LNW-typische Fallen sind richtig?

- [ ] A. Das Wort `jeder` ist bei NEA-Akzeptanz oft zu stark.
- [ ] B. Das Wort `automatisch` ist bei Haltebedingungen oft verdaechtig.
- [ ] C. `mindestens ein Rechenpfad` passt zu Nichtdeterminismus.
- [ ] D. Eine lange Antwortoption ist automatisch richtig.

---

## Satz F

### 1. Aufgabe

Welche Aussagen ueber `λ`, `{λ}` und `∅` sind richtig?

- [ ] A. `λ` ist ein Wort.
- [ ] B. `{λ}` ist eine Sprache mit genau einem Wort.
- [ ] C. `∅` ist eine Sprache ohne Woerter.
- [ ] D. `λ=∅`.

### 2. Aufgabe

Sei `A={0,1}`. Welche Aussagen sind richtig?

- [ ] A. `0101∈A*`.
- [ ] B. `2∈A*`.
- [ ] C. `{0,11,λ}⊆A*`.
- [ ] D. `A⊆A*`.

### 3. Aufgabe

Welche Aussagen ueber Potenzmengen sind richtig?

- [ ] A. Fuer jede Menge `M` gilt `∅∈P(M)`.
- [ ] B. Fuer jede Menge `M` gilt `M∈P(M)`.
- [ ] C. Ist `x∈M`, dann gilt immer `{x}∈P(M)`.
- [ ] D. Ist `x∈M`, dann gilt immer `x∈P(M)`.

### 4. Aufgabe

Welche Aussagen ueber den DEA aus Satz D, Aufgabe 1, sind richtig?

- [ ] A. Das Wort `bbbb` wird akzeptiert.
- [ ] B. Das Wort `baab` wird akzeptiert.
- [ ] C. Das Wort `aba` wird akzeptiert.
- [ ] D. Das Wort `aaa` wird akzeptiert.

### 5. Aufgabe

Welche Aussagen ueber den Mealy-Automaten aus Satz D, Aufgabe 3, sind richtig?

- [ ] A. Bei Eingabe `0` ist die Ausgabe `0`.
- [ ] B. Bei Eingabe `1` ist die Ausgabe `1`.
- [ ] C. Bei Eingabe `01` ist die Ausgabe `01`.
- [ ] D. Bei Eingabe `111` ist die Ausgabe `101`.

### 6. Aufgabe

Welche Aussagen ueber DEA und NEA sind richtig?

- [ ] A. Jeder DEA kann als spezieller NEA betrachtet werden.
- [ ] B. Jeder NEA kann in einen aequivalenten DEA ueberfuehrt werden.
- [ ] C. NEA erkennen mehr Sprachen als Turingmaschinen.
- [ ] D. NEA und DEA erkennen regulaere Sprachen.

### 7. Aufgabe

Welche Aussagen ueber `δ:S×E→S` sind richtig?

- [ ] A. Diese Form passt zu einem DEA.
- [ ] B. `δ` liest ein Eingabezeichen.
- [ ] C. `δ` liefert einen Folgezustand.
- [ ] D. Diese Form passt direkt zu einem NKA.

### 8. Aufgabe

Welche Aussagen ueber `δ:S×(E∪{λ})×K→S×K*` sind richtig?

- [ ] A. Diese Form passt zu einem KA im Sinne der Vorlesung.
- [ ] B. Links wird ein Kellersymbol betrachtet.
- [ ] C. Rechts wird ein Kellerwort geschrieben.
- [ ] D. Diese Form ist die Standardform eines DEA.

### 9. Aufgabe

Welche Aussagen ueber `δ:S×(E∪{λ})×K→P(S×K*)` sind richtig?

- [ ] A. Diese Form passt zu einem NKA.
- [ ] B. Das Ergebnis ist eine Menge moeglicher Folgepaare.
- [ ] C. `P` zeigt Nichtdeterminismus an.
- [ ] D. Der Automat hat keinen Keller.

### 10. Aufgabe

Welche Aussagen ueber `δ:S×B→P(S×B×{R,L,N})` sind richtig?

- [ ] A. Diese Form passt zu einer NTM.
- [ ] B. Das Ergebnis kann mehrere moegliche TM-Schritte enthalten.
- [ ] C. `R,L,N` beschreiben Kopfbewegungen.
- [ ] D. Diese Form passt zu einem Moore-Automaten.

### 11. Aufgabe

Welche Aussagen ueber Startzustaende und Endzustaende sind richtig?

- [ ] A. `s0∈S`.
- [ ] B. `F⊆S`.
- [ ] C. Ein Startzustand kann zugleich Endzustand sein.
- [ ] D. Ein Endzustand darf nie Startzustand sein.

### 12. Aufgabe

Welche Aussagen ueber das leere Wort in Automaten sind richtig?

- [ ] A. Ein DEA akzeptiert `λ`, wenn `s0∈F`.
- [ ] B. Bei `λ` wird kein Eingabezeichen gelesen.
- [ ] C. `δ*(s0,λ)=s0`.
- [ ] D. `λ` kann niemals akzeptiert werden.

### 13. Aufgabe

Welche Aussagen ueber `a^n b^n` sind richtig?

- [ ] A. Die Anzahl der `a` muss zur Anzahl der `b` passen.
- [ ] B. Die Reihenfolge ist sortiert: erst `a`, dann `b`.
- [ ] C. Ein Keller kann die Anzahl der `a` speichern.
- [ ] D. Ein DEA reicht fuer beliebiges `n`.

### 14. Aufgabe

Welche Aussagen ueber `u$ũ` sind richtig?

- [ ] A. `ũ` bezeichnet die Umkehrung von `u`.
- [ ] B. Der Keller hilft beim Vergleich in umgekehrter Reihenfolge.
- [ ] C. `$` trennt die beiden Teile.
- [ ] D. Nach `$` wird in derselben Reihenfolge wie vor `$` gelesen und verglichen.

### 15. Aufgabe

Welche Aussagen ueber `a^n b^n c^n` sind richtig?

- [ ] A. Die Sprache verlangt drei gleich grosse Bloecke.
- [ ] B. Sie ist ein typisches Beispiel fuer Typ 1.
- [ ] C. Sie steht in Beziehung zu LBA.
- [ ] D. Sie ist ein typisches Beispiel fuer Typ 3.

### 16. Aufgabe

Welche Aussagen ueber Aequivalenz von Zustaenden im DEA sind richtig?

- [ ] A. Aequivalente Zustaende koennen in der Minimierung zusammengelegt werden.
- [ ] B. Markierte Paare sind unterscheidbar.
- [ ] C. Unmarkierte Paare sind Kandidaten fuer das Verschmelzen.
- [ ] D. Ein Endzustand und ein Nicht-Endzustand sind immer direkt aequivalent.

### 17. Aufgabe

Welche Aussagen ueber Aequivalenzrelationen sind richtig?

- [ ] A. Reflexivitaet allein reicht nicht fuer eine Aequivalenzrelation.
- [ ] B. Symmetrie allein reicht nicht fuer eine Aequivalenzrelation.
- [ ] C. Transitivitaet allein reicht nicht fuer eine Aequivalenzrelation.
- [ ] D. Alle drei Eigenschaften zusammen reichen fuer eine Aequivalenzrelation.

### 18. Aufgabe

Welche Aussagen ueber die Relation `u~v ⇔ |u|=|v|` sind richtig?

- [ ] A. Sie ist reflexiv.
- [ ] B. Sie ist symmetrisch.
- [ ] C. Sie ist transitiv.
- [ ] D. Sie ist eine Aequivalenzrelation.

### 19. Aufgabe

Welche Aussagen ueber `G=(N,T,P,S)` sind richtig?

- [ ] A. `N` und `T` sind disjunkt.
- [ ] B. `S` ist ein Nichtterminal.
- [ ] C. `P` enthaelt Produktionen.
- [ ] D. `T` enthaelt ausschliesslich Zustaende eines DEA.

### 20. Aufgabe

Welche Aussagen ueber Ableitungen sind richtig?

- [ ] A. `⇒*` erlaubt mehrere Ableitungsschritte.
- [ ] B. `⇒*` erlaubt auch null Schritte.
- [ ] C. Ein terminales Wort enthaelt keine Nichtterminale.
- [ ] D. `L(G)` enthaelt auch unfertige Satzformen mit Nichtterminalen.

### 21. Aufgabe

Welche Aussagen ueber die Regel `VP→VP NP` sind richtig?

- [ ] A. Die Regel ist rekursiv.
- [ ] B. Sie kann eine bestehende Verbalphrase erweitern.
- [ ] C. Ohne passende Basisregel kann sie allein keine endliche Terminalableitung liefern.
- [ ] D. Sie ist keine Grammatikregel, weil rechts zwei Symbole stehen.

### 22. Aufgabe

Welche Aussagen ueber `NP`, `VP` und `PP` sind richtig?

- [ ] A. `NP` steht fuer Nominalphrase.
- [ ] B. `VP` steht fuer Verbalphrase.
- [ ] C. `PP` steht fuer Praepositionalphrase.
- [ ] D. Diese Begriffe sind Namen fuer Kelleralphabete.

### 23. Aufgabe

Welche Aussagen ueber Typ-3-Grammatiken sind richtig?

- [ ] A. Sie sind regulaer.
- [ ] B. Sie koennen durch endliche Automaten beschrieben werden.
- [ ] C. Regeln sind typischerweise links- oder rechtslinear.
- [ ] D. Sie koennen jede Typ-0-Sprache beschreiben.

### 24. Aufgabe

Welche Aussagen ueber Typ-2-Grammatiken sind richtig?

- [ ] A. Sie sind kontextfrei.
- [ ] B. Links steht eine einzelne Variable.
- [ ] C. Sie stehen in Beziehung zu Kellerautomaten.
- [ ] D. Sie sind weniger maechtig als Typ 3.

### 25. Aufgabe

Welche Aussagen ueber Typ-1-Grammatiken sind richtig?

- [ ] A. Sie sind kontextsensitiv.
- [ ] B. Sie sind im Normalfall nicht verkuerzend.
- [ ] C. Sie stehen in Beziehung zu LBA.
- [ ] D. Sie sind identisch mit Typ 3.

### 26. Aufgabe

Welche Aussagen ueber Typ-0-Grammatiken sind richtig?

- [ ] A. Sie sind unbeschraenkt.
- [ ] B. Sie stehen in Beziehung zu Turingmaschinen.
- [ ] C. Sie sind die allgemeinste Klasse in der Chomsky-Hierarchie.
- [ ] D. Sie sind weniger maechtig als Typ 3.

### 27. Aufgabe

Welche Aussagen ueber die Umwandlung DEA zu Grammatik sind richtig?

- [ ] A. Ein Uebergang `s --e--> s'` wird zu `s→e s'`.
- [ ] B. Endzustaende koennen `λ`-Produktionen erhalten.
- [ ] C. Der Startzustand wird zum Startsymbol.
- [ ] D. Eingabezeichen werden zu Terminalen.

### 28. Aufgabe

Welche Aussagen ueber Entscheidungsprobleme und Sprachen sind richtig?

- [ ] A. Ein Entscheidungsproblem kann als Sprache der Ja-Instanzen modelliert werden.
- [ ] B. Akzeptor-TM koennen zur Modellierung von Entscheidungsproblemen genutzt werden.
- [ ] C. Entscheiden verlangt Halten auf jeder Eingabe.
- [ ] D. Akzeptieren verlangt immer Halten auf jeder Eingabe.

### 29. Aufgabe

Welche Aussagen ueber Klausurstrategien sind richtig?

- [ ] A. Jede Option muss einzeln beurteilt werden.
- [ ] B. Es kann 0 bis 4 richtige Antworten geben.
- [ ] C. Formulierungen mit `stets`, `jeder` und `automatisch` sollte man besonders pruefen.
- [ ] D. Wenn zwei Antworten richtig klingen, muss genau eine davon falsch sein.

### 30. Aufgabe

Welche Aussagen sind als Merksaetze korrekt?

- [ ] A. `δ` liest ein Zeichen, `δ*` liest ein Wort.
- [ ] B. Beim KA steht links `K`, rechts `K*`.
- [ ] C. Moore: Ausgabe im Zustand; Mealy: Ausgabe an der Kante.
- [ ] D. Beim NEA reicht mindestens ein akzeptierender Pfad.
