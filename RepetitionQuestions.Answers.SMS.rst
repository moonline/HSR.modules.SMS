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







