====================
Exam preparation SMS
====================


Simulation
==========

Was ist Simulation?
-------------------
Simulation ist das Aufbauen eines Modells und das Durchführen von Experimente in diesem Modell.

Wozu dient Simulation?
----------------------
* Erkenntnisse erlangen über Variabilitäten und Abhängigkeiten in einem System

Wann wird Simulation eingesetzt?
--------------------------------
* Rechnen ist nicht möglich weil zu komplex
* Ausprobieren ist nicht möglich weil zu gefährtlich oder zu teuer

Gründe ein Simulationsprojekt zu starten
----------------------------------------
* Finden von Flaschenhälsen in Abläufen
* Finden von Ressourcenverschwendung
* Optimieren des Systems trotz der Komplexität

Grunddefinition von Shannon
---------------------------
Simulation ist die Entwicklung eines Modells eines konkreten Systems und dem Durchführen von Experimenten mit diesem Modell zur Verständnis des Verhaltens des konkreten Systems oder dem Evaluieren von verschiedenen Strategien zur Operation mit dem System.

Was ist ein System?
-------------------
* klar definierte Grenzen
* Schnittstellen
* Subsysteme

Unterschied physikalisches & logisches Modell
---------------------------------------------
physikalisches Modell
	Ist physisch vorhanden, z.B. Windkanal
Logisches Modell
	Gibt es nur als Gedankenexperiment, bzw. als Computersimulation

Warum streuen die Resultate bei mehreren Experimenten?
------------------------------------------------------
Ein konkretes System und auch dessen Modell besitzen Variabilitäten, die zur Streuung der Resultate führt.

Ist Simulation eine analytische oder eine experimentelle Methode?
-----------------------------------------------------------------
Simulation ist ein experimentelles Vorgehen. Es wird ein Modell erstellt, an das anschliessend Fragen (in Form von Experimenten) gestellt werden.

Die Analyse des Datenmaterials ist jedoch eine analytische Vorgehensweise.

Was ist statische Simulation?
-----------------------------
Es wird ein sich nicht verändernder Zustand mit gegebenen Parametern simuliert (Spreadsheet Simulation).

Was ist kontinuierliche Simulation?
-----------------------------------
Das Interesse liegt an den Zustandsübergängen und nicht an der Zustandsanderung. Die Simulation geht fortschreitend und nicht sprunghaft voran.

Wie kann in einer diskreten Ereignissimulation kontinuierliches Verhalten simuliert werden?
-------------------------------------------------------------------------------------------
Die zu betrachtenden Zeitintervalle hinreichend klein machen.

Was sind stochastische Systeme?
-------------------------------
In einem stochastischen System kann nur mit einer bestimmten Wahrscheinlichkeit vorausgesagt werden, was als nächstes passiert. Ein stochastisches System unterliegt gewisser Variabilität (Zufall) und ist daher nicht deterministisch.

Simulationsphasen
-----------------
Wozu dient das formale Modell?
..............................
Das formale Modell dient dazu, das konkrete System abstrakt zu beschreiben und zu formulieren, damit daraus anschliessend ein Simulationsmodell gebaut werden kann.

Wozu dient Modellverifikation?
..............................
Mit den Resultaten der Simulation wird das formale Modell verifiziert und daraufhin angepasst/verbessert.

Wozu dient Modellvalidierung?
.............................
Mit den Resultaten der Simulation wird durch Vergleichen mit dem konkreten System das Modell logische Modell optimiert.

Was ist isolierende Simulation/Abstrakton?
..........................................
Den Eigenschaften von Ergebnissen/Vorgängen wird anhand der Varianz der Input Daten Rechnung getragen.

Ist hypothetisches oder empirisches Datenmaterial geeigneter?
.............................................................
Empirisches, weil dahinter die Realität steckt.


Was ist generalisierende Abstraktion?
.....................................
Das Abbilden von Datenmaterial auf eine Verteilfunktion, um beliebig viele Experimente durchführen zu können.

Wozu können Simulationsergebnisse benutzt werden?
.................................................
Sie denen der Verifikation des Modells.


Event Driven Architecture
=========================

Was sind Ereignisse?
--------------------
* Ereignisse werden definiert durch ihren Typ und ihre Attribute.
* Ereignisse zielen auf eine Zustandsänderung
* Beispiele:
	* Geschäftsereignisse: z.B. Vertragskündigung
	* Systemereignisse: z.B. Paketeingang in einem System
	* Technische Ereignisse: z.B. Statusänderung von Sensor

Wie werden Ereignisse erkannt & Verarbeitet?
--------------------------------------------
Die Ereignisse der verschieden Quellen werden analysiert, aggregiert, aufgesplittet, korelliert, teilweise verworfen und kategorisiert (geclustert).

Simulations- und Modelluhr
--------------------------
Simulationsuhr
	* Zeit, die in der Simulation vergeht.
	* Vergeht sprunghaft (disrekt)
	* Während die Simulation berechnet wird, vergeht keine Simulationszeit

Reale Uhr
	* Läuft kontinuierlich mit immer gleichen Zeitabständen

Was ist das Dualitätsprinzip bei der Simulations- und Modelluhr?
................................................................
* Simulationsuhr und reale Uhr sind unabhängig.
* Das Weiterstellen (verbrauchen) der Simulationszeit benötigt quasi keine Rechenzeit
* Das Abarbeiten der Ereignisroutinen benötigt Rechenzeit aber keine Simulationszeit

Überholvorgänge
...............
Parallel ablaufende Vorgänge werden zwar sequentiell verarbeitet, jedoch im Rahmend der Modelluhr parallel platziert. Sind sie unabhängig (greifen auf keine gemeinsamen Ressourcen zu), so ist ein Überholen des früher gestarteten Vorgangs durch den später gestarteten möglich.

Kann eine parallele Simulation jederzeit auf einer Multicore Machine ausgeführt werden?
.......................................................................................
Nein, wenn die Prozesse auf gemeinsame Ressourcen zugreifen nicht.

Optimistischer Ansatz
	Die Simulation rechnet drauflos und prüft anschliessend, ob sich die Prozesse gegenseitig beeinflusst hätten (Kollision) -> wenn ja, dann Backtracking
Pessimistischer Ansatz
	Die Simulation prüft jederzeit, ob und wie sich die beiden Prozesse gegenseitig beeinflussen. (synchronisation)



Warteschlangen
==============

Welcher Verteilfunktion folgt der Markoffprozess?
-------------------------------------------------
Eine negative Exponentialfunktion, weil Markoff Erinnerungsbehaftet ist.

Rückgekoppeltes Warteschlangensystem
------------------------------------
Annahme: Simple Queue gemeint
::

	Geg:  u = 15s
	Ges:  R
	Annahme:  sigma = 10s
	Annahme: sigma = mittlere Servicezeit D

	u = 1/lamda
	lamda = 1/u = 1/15/s
	R = S/(1-l*S) = 10s/(1-1/15*10) = 10s/3.333 = 3.33s

Verlistwahrscheinlichkeit
-------------------------
::

	v = 1-X/lamda

Utilisation & Wartewahrscheinlichkeit
-------------------------------------
Utilisation = Wartewahrscheinlichkeit


Inputdatenanalyse
=================

Diskrete Wahrscheinlichkeit & kontinuierliche Verteilfunktionen
---------------------------------------------------------------
Bei diskreten Wahrscheinlichkeiten kann der Wert direkt abgelesen werden. Bei Verteilfunktionen muss er abgelesen werden.

Dichtefunktion
--------------
Wahrscheinlichkeit des Auftretens von Zufallswerten (Zeitabstand, in denen Ereignisse ankommen).

Verteilfunktion
---------------
Bildet ab, wie die auftretenden Zufallswerte über den Zahlenstrahl verteilt sind.

Normalverteilung
----------------
* Gaus
* Varianz: sigma = Abstand vom Maximalwert
	.. image:: img/normalverteilung-sigma.gif
* Erwartungswert/median: u = Position des Maximalwertes
	.. image:: img/normalverteilung-u.png
* Veränderungen der Parameter:
	* u wird grösser/kleiner: Kurve wandert horizontal
	* sigma wird grösser: Kurve wird breiter und weniger hoch

Wie werden Zufallszahlen erzeugt?
---------------------------------
Zufallszahlen werden durch eine inverse Funktion erzeugt. -> Die Inversionsmethode ist ein Simulationsverfahren, um aus gleichverteilten Zufallszahlen andere Wahrscheinlichkeitsverteilungen zu erzeugen.


Output Datenanalyse
===================

Stichprobenarten
----------------
Zufallsauswahl
    * Einfache Zufallsstichprobe
    * Systematische Stichprobe
    * Mehrstufige Stichprobe

Bewusste Auswahn
	* Systematische Stichprobenziehung -> Die Auswahl erfolgt anhand von Listen und festgelegten Regeln. 

Willkürliche Auswahl
	* Willkürliche Stichproben -> Die Auswahl liegt im Ermessen des Interviewers – oder auch der Probanden (Selbstselektion).

Varianz
-------


Grundgesammtheit (Hypothesentest)
---------------------------------

