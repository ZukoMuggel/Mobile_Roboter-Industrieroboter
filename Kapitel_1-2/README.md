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
-  Vorabmodellierung der Umgebung (schon vorhanden, als Datei abgelegt)
- Selbstandige Konstruktion(robot selbst erkundt)
- Interaktive Erkundung (Teach-in) (Menschen sie beibring)

**3 Abstraktionsstufen von Formen von Weltmodellen**

- Semantische Weltmodelle(verbal beschrieben) -> Aufgabenplanung.
- Topologische Weltmodelle(Raumstruktur) -> globale  Wegeplanung
- Geometrische Modelle ( konkreten Abmessungen
der Umgebung und der in ihr enthaltenen Objekte) -> lokalen Wegeplanung.

**Die selbstandige Konstruktion eines Weltmodells**

- 1.Messdatenaggregation
   -  Aus Messdaten werden
Merkmale, wie Kanten von Hindernissen etc. extrahiert.
- Geometrische Weltmodellierung:
  - Integration verschiedener Situationen bzw.
Aufnahmen unterschiedlicher Sensortypen ->Erstellen einer geometrischen Karte
- Topologische Weltmodellierung
  - Identifikation von Objekten und Raumstrukturen->
   topologischen Karte
