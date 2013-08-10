=======================================
SMS FS13 Repetitionsfragen Antworten
=======================================

Dieses Dokument wird vorzu erweitert. Ergänzungen und Antworten sind herzlich willkommen.
Repetitionsfragen: https://github.com/moonline/SMS/blob/master/RepetitionQuestions.Sms.tex


Simulation
==========

1
-
* Erkenntnisse erlangen über Variabilitäten in einem System / Projekt
* Erkenntnisse erlangen über Abhängigkeiten in einem System

2
-
* Es kann nicht ausprobiert werden, weil es das System noch nicht gibt
* Es kann nicht ausprobiert werden, weil es zu teuer wäre
* Es kann nicht ausprobiert werden, weil es zu gefährlich wäre
* BestimmteVorgänge sind zu komplex um sie zu berechnen -> grosse Variabilität

3
-
* Abbildung der Realität in ein Modell. -> Realität enthält immer Variabilität
* Optimierung der variablen Parameter durch Experimentieren

4
-
Modell
	Abstraktion der Realität
Experimente
	Abspielen eines Ablaufes im Modell, variieren von Parametern. Zur Simulation von Streuungen werden Zufallszahlen oder empirische Daten verwendet.

5
-
Physkalisches Modell
	Existiert greifbar, z.B. Windkanal
Logisches Modell
	Existiert nur als Konzept, bzw. als Abstraktionsmodell der Realität

6
-
dynamische Simulation
	* Die Zustände innerhalb der Simulation wechseln kontinuierlich. Die Reale Welt ist kontinuierlich.
	* Das Interesse liegt beim Zustandsübergang
	* Beispiel Crashsimulation

diskrete Simulation
	* Die Zustandswechsel innerhalb der Simulation wechseln in bestimmten Abständen (intervallen) und sind Eventbasiert.
	* Simulation am Rechner ist immer intervallbasiert, weil digital keine stufenlosess Vorgehen möglich ist. Durch unendlich kleine Schritte kann dynamische Simulation angenähert werden.
	* Das Interesse liegt bei den Zuständen und nicht bei den Übergängen

stochastische Simulation
	* Simulation von in der Zeit ablaufende Zufalls abhängige Vorgänge

7
-
Die Ereignisse laufen nicht nach einem festen Schema ab, sondern sondern der Ablauf ist abhängig von Ereignissen (Events). Die Realität ist event driven.

8
-
diskrete
	Zustandsübergänge finden sprunghaft statt, Interesse liegt bei Zuständen
kontinuierlich
	Zustandsübergänge finden kontinuierlich statt. Interesse liegt bei Übergängen

9
-
statisch
	Simulation eines oder mehreren statischen Zustandes. z.B. Spreadsheetsimulation
dynamisch
	Die Simulation verändert sich über der Zeit

10
--
Sämmtliche Systemübergänge fallen in ein Zeitdelta der diskreten Simulation und sind somit nicht sichtbar -> Systemprünge

11
--
* Wie viel Infrastruktur benötigen wir für ein optimales Kosten/Nutzen verhältnis (Maschinen, Lagerhallen, Transportsysteme, ...) für die neue Anlage?
* Wie viele Mitarbeiter benötigen wir für ein optimal ausgelastetes System für die neue Anlage?
* Welche Transportabläufe führen zu den kürzesten Totaltransportzeiten bei der bestehenden Anlage?
* Wo liegen die Engpässe im bestehenden System?

12
--
* Kosten
* Durchlaufzeit
* Wartezeit in Schlangen, Anzahl in Schlangen
* Output (Menge/Zeit)
* Komplette Zykluszeit

13
--
* Animationen
* Live-Diagramme mit aktueller Statistikdaten
* Anpassungen der Simulation während dem Laufen

14
--
Ein reales System wird als abstraktes mathematisches Modell formuliert. Die Simulation basiert auf diesem Modell. Mit der Simulation wird das Modell verifiziert, indem die Reaktion auf Veränderungen im Modell mit Reaktionen auf ähnliche Veränderungen in der Realität abgeglichen werden.

15
--
* In einem realen System werden empirisch Daten gesammelt oder hypothetische Daten zusammengestellt.
* Aus diesen Daten werden formale Daten (Daten, die einer Verteilfunktion folgen) definiert.
* Das reale System wird beschrieben und über eine formale Beschreibung zusammen mit den formalen Daten in ein formales Modell überführt.
* Diese Formale Modell wird nun für die Simulation benutzt.
* Das Resultat der Simulation wird mit der Realität verglichen und anhand der Ergebnisse werden die Beschreibung und damit auch das Modell angepasst.


Event Driven Architecture
=========================

16
--
* Sind unabhängig
* Tauschen Nachrichten ausgelastetes
* Reagieren auf Ereignisse
* Aktivitäten werden durch Ereignisse ausgelöst

17
--
::

	Ereignis = Type + Eigenschaften

18
--
* Ein Ereignis (z.B. Senser meldet 30°) wird von einem Gerät oder andern Prozess ausgelöst
* Der betreffende Prozess empfängt das Ereignis und verarbeitet es (z.B. berechnen, ob die Temperatur über der Soll Grenze liegt)
* Der Prozess reagiert auf das Ereignis, indem er eine Aktion auslöst (z.B. die Klimaanlage einschaltet)

19
--
Ereignisquelle
	* Erzeugt Ereignisse

Ereignisobjekt
	* Weis selbst nicht, wohin es soll

Ereignissenke
	* Empfängt Ereignisse
	* Kann auch gleichzeitig Quelle sein

20
--
synchron
	* Sender und Empfänger sind blockiert, bis Nachricht überliefert wurde
	* Nachricht wird sofort übertragen

asynchron
	* Sender und Emfänger arbeiten, während im Hintergrund die Nachricht in einer Queue landet -> blockiert nicht
	* Ereignis getriebene Architektur ist immer asynchron
	* Lässt sich zu synchroner Kommunikation umbauen

21
--
::

	Observer Observer Observer
	  |  ^     |  ^     |  ^
	  |  !     |  !     |  !
	  v  !     v  !     v  !
	+------------------------+
	|                        | Public / Subscribe Middleware
	+------------------------+
	           ^
	           !
	        Observable
	
	| subscribe

	! notify


22
--
CEP
	* Events werden inklusive Abhängigkeiten und Seiteneffekts verarbeitet
	* Gleichzeitige, dynamische Eventverarbeitung
ESP
	* Verabeitung kontinuierlicher Ereignisströme
	* In einem Ereignisstrom werden Muster erkannt, um daraus Erkenntnisse ableiten zu können

23
--
Die Daten von verschienen Sensoren laufen in der Ereignisverarbeitung zusammen und werden durch mehrere Analyseprozesse analysiert. Daraus resultierende Ereignisse lösen wiederum Prozesse aus, die auch wieder einen Einfluss auf die Eingabeereignisse haben.

24
--
* Schwierig Testbar
* Lokalisierung von Fehlern aufgrund der hohen Freiheitsgrade und Komplexität aufwändig
* Redundanzen und Inkonsistenzen
* Nachverfolgung des Ereignisflusses schwierig

25
--
Reale Uhr
	Physikalische Zeit, Zeiteinheiten die verstreichen
Modelluhr
	* Zeit, die im Modell verstreicht. Rechnet die Simulation eine Ereignisverarbeitung aus, im Modell passiert jedoch nichts, so bleibt die Zeit stehen.
	* Die Modellzeit kann beschleunigt oder verlangsamt werden, um in kurzer Zeit viele Vorgänge durchzusimulieren oder um eine Simulation ganz genau anzusehen
	* Läuft nicht kontinuierlich sondern springt von Ereignis zu Ereignis

26
--
* Parallele Ereignisse werden sequentiell abgearbeitet. Die Modelluhr läuft in dieser Zeit jedoch nicht, sodass die Ereignisse in der Simulation parallel stattfinden.
* Parallele unabhängige Prozesse können sich gegenseitig beeinflussen -> es bracht eine zentrale Kontrollinstanz oder ein Konflikterkennungsverfahren mit Backtracking

27
--

28
--
Wenn das Interesse vor allem an den Zuständen und den Zustandsänderungen und nicht bei den Zustandsübergängen liegt.

29
--
Rechenzeit
	* Zeit, die für die Berechnung eines oder mehreren Ereignissen gebraucht wird
	* Reale Zeit, die verbraucht wird

Realer Zeit
	* Läuft Kontinuierlich, unumkehrbar

Modellzeit
	* Läuft Sprunghaft
	* Von Event zu Event
	* Läuft während Berechnungen nicht

Simulationszeit
	* Zeit, die in der Simulation vergeht
	* Parallelität bezieht sich immer auf die Simulationsuhr und nicht auf die Rechenzeit
30
--
Optimistisches Verfahren
	* Annahme: Wenig Beeinflussung
	* Überwachung, Backtracking falls gegenseitige Beeinflussung stattgefunden

Pessimistisches Verfahren
	* Kontrollinstanz, die kontinuierlich die gegenseitige Beeinflussung von Prozessen überwacht


Warteschlangen
==============

31
--
* M
* M
* n: Anzahl parallele Abarbeitungsprozesse

**Besispiele**
*2 M/M/1: Twincenter mit zwei einzelnen Prozessen, die jeweils eine eigene Warteschlange besitzen
* M/M/2: Dual Server mit zwei einzelnen Prozessen, die eine gemeinsame Warteschlange besitzen.

32
--
* Ankommende Tokens werden in die Warteschlange eingereiht.
* Nach dem Fifo Prinzip werden Tokens aus der Queue entnommen und durch den Prozess abgearbeitet.
* Mittlere Aufenthaltszeit:
	::

		Mittlere Wartezeit + Mittlere Servicezeit:
		R = W + S
		Servicezeit: Total busy Time B/# abgefertigte Tokens C
		R = W + B/C
		Wartezeit: Aufenthaltszeit * Servicezeit * Ankunftsrate
		R = S + l*S*R
		R = S/(1-l*S)


33
--
Das Little's Gesetz besagt, dass die ein System stabil ist, wenn die Ankunftsrate der Durchsatzrate entspricht. Es gehen somit keine Tokens verloren oder kommen neue hinzu.

34
--
Die Residenztime wächst ins unendliche. U = l*S, somit geht bei der Gleichung R = S/(1-l*S) der Ausdruck unter dem Bruchstrich mit der Annäherung an 100% gegen 0, was zu einer unendlich grossen Residenztime führt:

::

	^ Residenztime
	|                 °
	|                °
	|            .-°
	|         .-°
	|   .--°°         100%
	+------------------+----> Utilisation


35
--
Zwei parallele Warteschlangensysteme mit jeweils eigener Warteschlange arbeiten Tokens ab

::

	R = S/(1-XS/2), weil sich die Tokens auf zwei Systeme verteilen


36
--
Zwei parallele Prozesse erhalten Tokens aus einer gemeinsamen Warteschlange.

::

	R = S / (1-p^2), weil die Residenztime vor allem von der Wartewahrscheinlichkeit p abhängigt.


37
--
	^ Residenztime
	|                 °
	|                °°
	|            .-° °
	|         .-°   °
	|   .--°° ..-°   100%
	+------------------+----> Utilisation
	
	Utilization = BusyTime / TotalTime


Die untere Kurve stellt das TwinCenter dar, weil das TwinCenter durch die einzelnen Warteschlangen eine tiefer Auslastung besitzt. Es können Tokens am Warten sein, obwohl der eine Prozess frei wäre, weil die Tokens sich in die Warteschlange des andern Prozesses eingereiht haben.

38
--
Tokens durchlaufen mit einer bestimmten Wahrscheinlichkeit das System am Ende nochmal.

::

	D = ServiceTime S * Prozessdurchsatz V = S*1/(1-p)
	R = D/(1-l*D)


Die Mittlere Aufenthaltszeit im System ist somit abhängig von der Effektiven Anzahl Tokens, die durch den Prozess laufen, und nicht der Anzahl Tokens, die in das System eintreten.

39
--
In einem Closed Queueing Center gibt es eine feste Anzahl Tokens.

::

	R = N/X(N) - Z
	
	X(N): Durchsatz von N Tokens
	Z: Denkzeit, die die Tokens im Tokenspeicher verbringen


Input Datenanalyse
==================

40
--
Zufallsvariable
	Abbildungsfunktion, die den Elementen einer Ergebnismenge reelle Zahlen zuordnet.
Verteilungsdichtefunktion
	Wahrscheinlichkeit des Auftretens von Zufallswerten

41
--
diskrete Verteilfunktion
	gestuft, kennt nur zu bestimmten Werten eine Auftrittswahrscheinlichkeit. Die Summe aller (rechteckiger) Balken ist 1.
kontinuierliche Verteilfunktion
	Gaus Glockenkurve, Fläche 1.

42
--
Verteilungsfunktion
	Zeigt die Verteilung von Werten
Summenfunktion
	Ist die Aufsummierung der Verteilungsfunktion -> steigt daher zwangsmässig von links nach rechts an.

43
--
Verteilungsfunktion
	Zeigt die Verteilung der Werte auf dem Zahlenstrahl
Dichtefunktion
	Zeigt die Häufung (gleicher) Werte auf dem Zahlenstrahl

44
--
Erwartungswert
	Wird als Mittelwert der Experimentresultate erwartet
Standardabweichung
	Range, in dem sich ein bestimmter Teil der Ergebnisse befindet.
Varianz
	Spanne, in der die Ergebnisse schwanken

45
--
* Ereignisse werden zu zufällgen Zeiten erzeugt und vernichtet
* Resourcen, Mengen schwanken
* Bearbeitungszeiten schwanken zufällig
* Entscheidungen im Eventfluss sind zufällig

46
--

47
--

48
--
Siehe 40.

49
--
diskret
	Würfel
stetig
	Temperatur

50
--
Siehe 43.

51
--
Eingabewert, von dem der Zufallszahlen Generator ausgeht. Gleiche Seeds erzeugen gleiche Serien an Zufallszahlen. Dadurch werden Eperimente wiederholbar und nachvollziehbar.

52
--
Die Sequenzlänge bezeichnet den Range, indem Zufallszahlen erzeugt werden. Für die Simulation muss die Sequenzlänge so gewählt werden, dass der Zufallszahlengenerator Zufallszahlen im benötigten Bereich generiert. Für einen Würfel z.B. 1-6, für Wahrscheinlichkeiten 0-1, Für eine Fahrzeugplatzbesetzung 1-5.

53
--
Über eine Umkehrfunktion.

54
--
Weil es je nach Anwendunggebiet eine andere Häufung braucht. z.B. Würfel: Alle Zahlen müssen gleich häufig vorkommen. Bei 2 Würfeln: 6 und 8 kommen am häufigsten vor.

55
--
Sie ist absolut entscheidend. Sollen Würfe mit 2 Würfeln simuliert werden und es wird eine Exponentialverteilung verwendet, so sind die Ergebnisse wertlos.

57
--
Sie müssen wiederholbar sein, damit die Simulation wiederholt und nachvollzogen werden kann. Es dürfen somit keine echten Zufallszahlen sein, sondern Zahlen, die einer Funktion folgen aber verteilt sind wie Zufallszahlen.

58
--
Weil bei jedem Simulationsdurchgang andere Resultate herauskommen würden und das Ergebnis nicht nachvollzogen werden kann.

59
--
Zufallszahlengenerator, Random Number Generator.

60
--

61
--













