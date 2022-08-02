## 1.Einführung und Historie

**Roboter**: Ein Roboter ist eine Bewegungen ausführende Maschine,\
 die Eigenschaften besitzt, die denen von Lebewesen nachgebildet sind

zwei **Gesichtspunkte** für den Einsatz von Robotern:
- 1.Die Aufgabe kann oder darf nicht von einem  Menschen ausgeführt werden
- 2.Der Nutzen/Kosten-Quotient ist hoch

## 2.Mobile Roboter
### 2.1 Typen und Anwendungen
**1.**Autonome mobile Roboter sollen sich
**in einer veränderlichen  Umgebung ohne externe Steuerung** frei bewegen

**2.** Ein autonomer mobiler Roboter kann folgende **Eigenschaften** aufweisen:
- Positionsbestimmung,
- selbstandige Planung und Ausfuhrung von Aktionen,
- Kommunikation mit der Umwelt,
- Kollisionsvermeidung.

**3.** Drei Art vom Roboter:**landgestützte, seegestützte und  luftgestützte**

Anwendungsbeispiele:\
Landgestützte : Transport,Uberwachung,Spielzeug
seegestützte :Kabelverlegung,Exploration,Bergung
luftgestützte : Marschflugkorper,Drohnen

**4.Landgestützten Systeme:**\
Transportroboter, Uberwachungsroboter und  Museumsfuhrer mussen uber:
- eine Karte des Operationsgebietes
- eine Wegplanung
- eine Hindernisvermeidung
- Kommunikationsfahigkeiten

verfugen.

Transportroboter werden heute z. B
- in Krankenhausern eingesetzt, um Mahlzeiten, Bettlaken, Medikamente etc. zu transportieren.

Uberwachungsroboter werden z. B.
- in der chemischen Industrie und in militarischen Anlagen eingesetzt.

**5.Flachenabdeckungsaufgabe**

**a) Umweltmodell**
- Quadtree-Modell
- polygonale Modelle (Befahrbare Flachen ist polygonale)
- Topologisches Modell

**b) Positionsbestimmung**
- Interne Sensoren(Koppelnavigation): Gyroskope und Tachometer
- Externe Sensoren: Kameras
  - Positionsbestimmung: kunstlicher
Landmarken
  - naturlicher Umweltobjekte


Bei modernen Systemen kombiniert man die Koppelnavigation mit der relativen Methode.\

Koppelnavigation dient zur Positionsbestimmung\
Relativen Methode hilfe dabei,geschatzte Lage zu\
  stutzen,an bestimmten Zeit/Orten zu eichen

**c) Bahnplanung**

Potentialfeldmethode： bei Potentialfeld liegt \
der  Startpunkt A auf einem Berg und der Zielpunkt B in einem Tal

**d) Hinderniserkennung und -vermeidung**

 Nach dem Abstand eines Hindernisses vom Roboter wird
 \
 vier Zonen unterteilt.Je nachdem in welcher Zone das
 \
  Hindernis dann liegt,wird durch Bahnregler und
\
   Hindernisstrategie steuert

**6.Zusammenfassung**

Druch Sensoren wird Karte der Operationsgebietes erstellt,Mit Hilfe von Umgebungskarte und Karte der Operationsgebietes wird Position bestimmt.\
Position + Hinderniserkennung/-vermeidung + Zielvorgabe = Bahnplanung ->Motorsteuerung

### 2.2 Sensoren
Sensoren fur autonome mobile Robotik zur **Multisensorsystemen**:
- interne Sensoren:
  - Gyroskop
  - Odometrie
- externe Sensoren:
  - beruhrungslos:
    - Laser/Kamera
    - Ultraschall
    - GPS/Radar
  - taktil:
   - Kraftsensor  

**Funf Aufgaben von Sensoren**:
- **Entfernungsmessung** (Ultraschall,Laser-Scanner)
- **Positions- und Richtungsbestimmung** (Gyroskope,Odometrie)
- **taktile Objektdetektion** (Kraftsensoren)
- **beruhrungslose Objektdetektion** (Infrarotsensoren)
- **Objekt- und Situationserkennung** (Kamera)

**Ultraschall-Sensoren** werden zur Entfernungsmessung verwendet:\
Fur Abstand d, Laufzeit t und Schallgeschwindigkeit vc gilt:d=vc*t/2

**Gyroskope** dient der Bestimmung von Beschleunigungen:
- mechanische Gyroskope (Der Kreisel versucht seinen Drehimpuls L, im  kraftefreien Fall beizubehalten)
- Glasfaser-Gyroskope (1 Lichtstrahl wird in zwei geteilt.Die beiden geteilten Strahlen bewegen sich einmal links und einmal rechts herum in einem Kreis. durch Treffpunkt bekommt man winkelgewindigkeit )

**Odometrie** auch Koppelnavigation genannt, dient ebenfalls der Positionsbestimmung\
Die Position des Roboters ist durch die x- und y-Koordinaten  gegeben. Seine Orientierung durch den Winkel Θ.

**Kraftsensoren und Taster** werden fur die Kontakterkennung genutzt.\
Wird eine Kollision oder ein Kontakt des Roboters mit
einem Objekt festgestellt.fuhrt dies zum des Roboters oder zu einem Ruckzugsmanover.\
Kontakterkennung bilden eine Sicherheitseinrichtung,\
 die Schaden beim Fahren gegen ein Objekt vermeiden soll



**Sensorfusion**\
Man kombiniert verschiedene Sensoren,Die aufgenommenen Daten erganzen sich und erlauben so eine moglichst sichere
- Positionsbestimmung und
- Hinderniserkennung.

### 2.3 Umweltkarten und Kartenaufbau
\
**3 Weg zur Weltmodell**
- Vorabmodellierung der Umgebung
- Selbstandige Konstruktion
- Interaktive Erkundung (Teach-in)

**3 Abstraktionsstufen von Formen von Weltmodellen**

- Semantische Weltmodelle(verbal beschrieben) -> Aufgabenplanung.
- Topologische Weltmodelle(Raumstruktur) -> globale  Wegeplanung
- Geometrische Modelle ( konkreten Abmessungen
der Umgebung und der in ihr enthaltenen Objekte) -> lokalen Wegeplanung.

**Die selbstandige Konstruktion eines Weltmodells**

- 1.Messdatenaggregation
   -  Zusammenfassung der Sensordaten zu einer
lokalen Aufnahme.Aus Aufnahme werden
Merkmale, wie Kanten von Hindernissen etc. extrahiert.
- 2.Geometrische Weltmodellierung:
  - Integration verschiedener
Aufnahmen unterschiedlicher Sensortypen ->Erstellen einer geometrischen Karte
- 3.Topologische Weltmodellierung
  - Identifikation von Objekten und Raumstrukturen ->
   topologischen Karte


**Messdatenaggregation**\
Beim Messen von Entfernungen durch den Roboter erhalt man eine Reihe von Messpunkten.Aus ihnen werden nun  Merkmale extrahiert\
z.b Linien Tracking

**Geometrische Weltmodellierung**\
Wird aus den abstrahierten Messdaten – z. B.Linien – eine geometrische Weltkarte aufgebaut.\
indem man lokale Aufnahmen verschiedener Sensortypen aus unterschiedlichen Positionen fusioniert. \
Aus ihnen wird dann ein globales Weltmodell aufgebaut bzw. die Daten werden in ein bestehendes Weltmodell integriert.\

**Laßt sich mj mit einem mi ∈ W zusammenfassen oder ist es ein neues Merkmal, das zu W hinzuzufugen ist?**
- Line Matching:
  - Linienumrahmung miteinader uberlappt Wird ->Fusionieren
  - Steigungswinkeldifferenz und maximaler Abstand(Kriterien)
  - Fusionieren zweier Linien(Methode)

**Topologische Weltmodellierung**\
Hierbei werden die Geometriedaten einer lokal begrenzten\
Umgebung mit bestimmter Objekte verglichen und  identifiziert\
Die globale Wegplanung erfolgt anhand der topologischen Karten\
Die konkrete Wegplanung erfolgt anhand des geometrischen Modells

### 2.4 Bahnplanung

**Bahnplanungsverfahren**
- Roadmap-Verfahren
- Cell-decomposition-Verfahren
- Potential-Verfahren
- Verfahren fur Flachenabdeckungsaufgaben


1.Visibility-Graph: (Roadmap)
- A, B und den Polyederecken von H als Knoten
- allen Verbindungen der Knoten untereinander

das Gebiet aller Hindernisse H \
der Startpunkt A \
der Zielpunkt B

2.Tiefensuche:(Roadmap)\
Such nach einem Weg zwischen A und B:
- markieren die Nachbarknoten von A und so weiter bis zur Ende.Dann von A anfangen,ein Weg zu finden

Wenn ein Weg nicht gefunden ist,geht auf dem bisherig weg zuruck bis man wieder einen neuen Nachbarknoten erreichen kann.

3.Voronoi-Diagramm:(Roadmap)\
Es basiert auf einer polygonale Karte.es ist Wegnetz,auf dessen weiss man den maximalen Freiraum und Abstand zu alle Verhinissen.Es kann Kollision gut vermeiden.\

Definition:
- x ist die Punkt von befahrbaren Freiraum.
- clearance(x)ist Abstand zur Hindernisse
- near (x)ist Menge der Punkte auf den Rand,deren Abstand zu x gleich wie clearance(x)
- voronoi(F),wie viel Element in near(x)

polygonale Hindernisse ist durch Gerade und Parabelteilen zusammengesetzt.\
Voronoi-Diagramm zwischen zwei Gerade-> Gerade
Voronoi-Diagramm zwischen eine Ecke und eine Gerade->
Parabel

4.Exact-cell-decompositionVerfahren
Befahrbare Freiraum wird in Zellen unterteilt.\
Als Weg zwischen Start A und Ziel B werden die Mittelpunkten der Zellenkanten verbunden.

5.Approximate-cell-decomposition-Verfahren
ahlich wie Exact-cell-decompositionVerfahren,aber werden Quadrate verwendet

6.Potential-Verfahren
Umgebung ist Potentialfeld,Zielpunkt ist die globalem Minium.wir versuchen,den Roboter von seinem Startort x in das Minimum zu ziehen.\
Es gibt zwei Kraft:
- eine Kraft,die den Roboter in den Zielpunkt zieht
- eine Kraft,die den Roboter von Hindernissen abstosst.

Gradientensuche:\
Der Roboter bewegt vom Startpunkt in kleinen Schritten entlang des Gradienten.
Nachteil:es kann in localen Minium bleiben kann.

7.Algorithmus von Henrich und Graf(Verfahren fur Flachenabdeckungsaufgaben)

Die Umgebung ist polygonal und druch ein rechteckiges Gitternetz uberzogen.Der Roboter kann 8 Nachbarfeld erreichen.

Regeln zur Bahnplanung(nicht befahrbare und schon befahrene Zellen als "kritische Zellen“):
- Fahre nur in Zellen, die nicht kritisch sind.
- Fahre nach rechts.
- Fahre geradeaus, wenn rechts nicht moglich ist
- Fahre nach links, wenn rechts und geradeaus nicht moglich ist
- keine Weg gefunden? mittels des Potentialfeld-Verfahrens werden nachst nicht kritische Zellen bestimmt

Die zentrale Element ist Speicher,in dem festgehalten wird, welche Zellen kritisch sind und welche nicht.
