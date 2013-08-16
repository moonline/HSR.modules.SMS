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

Was ist das Dualitätsprinzip bei der Simulations- und Modelluhr?
----------------------------------------------------------------
