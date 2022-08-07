## 3.Industrieroboter
### 3.1 Typen und Anwendungen

Industrieroboter sind mechanische autonome Handhabungsgerate.Computer steurn der so, dass er ein Aufgabe ohne fremde Einfluss erledigt.\
Mechanische Handhabungsgerate ist von Menschen gesteuert als Manipulatoren.\

**1.Gelenktypen**
- 1. Translationsgelenk
- 2. Rotationsgelenk
- 3. Torsionsgelenk
- 4. Revolvergelenk

**2.Stellglieder**
- Elektromotoren
- Hydraulikantribe
- pneumatische Antribe

**pneumatische Antirbe** werden nur bei sehr kleinen Robotern eingesetzt,bei denen geringe Stellkrafte ausreichend sind.\
Vorteil: niedrige Kosten

**Elektromotoren** ist die Standardantriebe fur Industrieroboter.

**Hydraulikantrieben** besitzen nur ein hohere Stellkrafte.

**4.Sensoren bei Industrieroboter**

**Positionssensoren**:
- potentionmeter,eine dem
Drehwinkel ϕ proportionale Spannung
- Drehmelder,
- Kodiereinrichtungen


**Geschwindigkeitssensoren**:Tachogeneratoren

 **5.Sicherheit von Industrierobotern**

**Gefahrliche Situationen**
- Menschen in der Nahe des Robotern arbeiten
- Menschen betreten wo der Roboter bewegen.
- der Roboter gewartet wird
- der Roboter programmiert wird

**passive Sicherheitseinrichtungen**
- Absperrgitter
- Stahlpfosten, die Roboter bei unkontrollierten  Bewegungen zerstoren
- NOT-AUS-Schalter

**aktive Sicherheitsmaßnahmen**
- Sensoren:Lichtvorhange/druckempfingliche Matten


**Sicherheitsstufen**
- Eindringung in die Aussere Umgebung der Roboterzelle
- Eindringung in die Innere der Roboterzelle
- Eindringung in den Arbeitbereich/ in der Nahe von Roboters

**Reaktionen**
- Warnsignal
- Reduktion die Geschwindigkeit auf eine sichere Stufe
- aktive Verhinderung einer Kollision durch Roboter
- Durchfuhrung von Arbeiten in entfernten Bereichen
- Abschaltung der Roboters

Industrieroboter ist eine interdisziplinare Aufgabe:
Mechnik,Antribestechnik,Messtechnik,Rechnertechnik,Regelungstechnik


### 3.2 -3.3
**Matrix**

### 3.4 Regelung von Industrierobotern

Wir versuche ,Robotergreifer entlang der Trajektorie abzufahren.\

1.Steuerung mit inversem Modell\
Nachteil: Storung kann nicht ausgeregelt werden\

2.Achsregelung ohne Vorsteuerung\
Kaskadenregler:
- Positionsregler -- P
- Drehzahlregler -- PI
- Stromsregler -- PI
Schlecht Bahnverfolgung:nichtlineare Verkoppelung der einzelnen Achsen

3.Achsregelung mit Vorsteuerung uber inverses Modell\

4.Entkopplung + Linearisierung\

Aber selten genutzt:
- nicht direkt einsetzt werden
- Modellierungsgenauigkeit verhindert eine optimale Entkopplung
-  hohe Online-Rechenaufwand ber Bewertung des inverse Modells fuhrt zu Verzogung.
