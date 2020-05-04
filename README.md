# Programming Principles

- [SOLID](#solid)
- [Tell, dont ask](#tell-dont-ask)
- [KISS](#kiss)
- [SLAP](#slap)
- [DRY](#dry)
- [YAGNI](#yagni)
- [GRASP](#grasp)
- [Conways Law](#conways-law)


## SOLID

#### **S**ingle Responsibility Principle
- jede Klasse hat nur eine Zuständigkeit

#### **O**pen Closed Principle
- offen für Erweiterungen
- geschlossen für Änderungen

#### **L**iskov Substitution Principle
- Objekte eines abgeleiteten Typs müssen als Ersatz ihres Basistyps funktionieren, ohne die Korrektheit zu ändern.

#### **I**nterface Segregation Principle
- Interfaces aufteilen, sodass Funktionalität getrennt ist
- Fat Interfaces bündeln viel Funktionalität:
    - Anwender abhängig von Änderungen anderer Methoden im Interface
    - Anwender hat Zugriff auf Methoden, die nicht für ihn bestimmt sind

#### **D**ependency Inversion Principle
- High-Level-Module sollten nicht von Low-Level-Modulen abhängen
- Regeln in High-Level-Modul vorgegeben, in Low-Level-Modul implementiert
- ausschließlich von Abstraktionen abhängen\
  &rarr; High-Level-Module können so wiederverwendet werden


## Tell, don't ask
- Objekt selbst etwas ausführen lassen\
  &rarr; hat alle Informationen um Entscheidungen selbst zu treffen
- Kommandos statt Abfragen

&rarr; Führt zu **verteilter Businesslogik**


## KISS
_"Keep it simple, stupid"_
- Komplexität so gering wie möglich halten
- Code nicht unnötig verkomplizieren


## SLAP
_"Single Level of Abstraction Principle"_
- Code innerhalb einer Methode ist auf einem Abstraktionsniveau
  - keine Vermischung von Arbeit und Delegation
  - keine Vermischung aus Technischem und Businesslogik
  
&rarr; **Composed Methods:** Einstiegsmethode delegiert an private Hilfsmethoden


## DRY
_"Don't repeat yourself"_
- Code nur einmal schreiben
- gleicher Code auslagern und von allen anderen Stellen darauf zugreifen
- Änderungen müssen nur an einer Stelle gemacht werden
- Nur eine Quelle der Wahrheit


## YAGNI
_"You ain't gonna need it"_
- nicht benötigte Features nicht implementieren
- unnötige Features erhöhen Komplexität
- bindet unnötig Ressourcen


## GRASP
_"General Responsibility Assignment Software Patterns"_

Ziel: **Low Representational Gap (LRG)** möglichst klein halten\
(LRG = Lücke zwischen gedachtem Domänenmodell und Implementierung)

#### Low Coupling
- geringe Kopplung zwischen Objekten
- Abhängigkeiten so gering wie möglich halten

#### High Cohesion
- starke Kohäsion innerhalb einer Klasse
- semantische Nähe der Elemente einer Klasse

#### Information Expert
- Objekt hält Verantwortung für Informationen die es besitzt
- Objekte sind zuständig für Aufgaben die ihre Informationen betreffen

#### Creator
- Legt fest, wer für die Erzeugung von Objekten zuständig ist
- Objekt kommt als Creator infrage, wenn es zu jedem erstellten Objekt eine Beziehung hat

#### Indirection
- Delegation
- kann Teile des Systems entkoppeln, indem Aufgaben ausgelagert werden

#### Polymorphism
- Behandlung von alternativen abhängig vom Typ
- Umgang mit Variation in der OO-Programmierung
- Methoden je nach Typ andere Implementierung
- Vermeidung von Fallunterscheidungen

#### Controller
- Verarbeitung einkommender Benutzereingaben
- Koordination UI &harr; Logik
- Hauptsächlich Delegation
- Verwalten des Anwendungszustands

#### Pure Fabrication
- reine Verhalten- oder Arbeiterklasse
- keinen Bezug zur Domäne
- Trennung technisch &harr; fachlich

#### Protected Variations
- Kapselung verschiedener Implementierungen hinter einer einheitlichen API
- Variabilität einzelner Komponenten soll nicht Gesamtsystem beeinflussen


## Conways Law
- Kommunikationsstruktur eines Unternehmens bildet sich auf Code bzw. Architektur ab
- Kommunikationsschnittstellen entsprechen Modulschnittstellen im Code
- Besser: Kommunikationsstruktur an Produkt/Kundenbedürfnis ausrichten
