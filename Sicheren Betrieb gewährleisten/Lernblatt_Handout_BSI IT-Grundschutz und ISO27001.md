# Lernblatt / Handout: BSI IT-Grundschutz inkl. Vergleich zur ISO/IEC 27001:2022

### Kompaktes Nachschlagewerk für die IHK-Prüfung „Geprüfter Berufsspezialist für Informationssicherheit“

**Stand: 30. August 2026**

---

# ⚡ Schnellcheck vor der Prüfung

## Die wichtigsten Begriffe

- **BSI** = Bundesamt für Sicherheit in der Informationstechnik
- **ISMS** = Informationssicherheitsmanagementsystem
- **IT-Grundschutz** = systematische Methodik zum Aufbau eines ISMS und zur Absicherung eines Informationsverbunds
- **BSI 200-1** = Anforderungen an ein ISMS
- **BSI 200-2** = IT-Grundschutz-Methodik
- **BSI 200-3** = Risikoanalyse
- **BSI 200-4** = Business Continuity Management (BCM)
- **Kompendium** = Bausteine mit konkreten Sicherheitsanforderungen
- **CIA-Schutzziele** = Vertraulichkeit, Integrität, Verfügbarkeit
- **Schutzbedarf** = normal / hoch / sehr hoch

## Drei Vorgehensweisen nach BSI 200-2

- **Basis-Absicherung** → schnelle grundlegende Absicherung des gesamten Informationsverbunds
- **Kern-Absicherung** → zuerst besonders wichtige Geschäftsprozesse und Systeme („Kronjuwelen“)
- **Standard-Absicherung** → vollständige Grundschutz-Methodik für den gesamten Informationsverbund

## Ablauf der Standard-Absicherung

**Strukturanalyse → Schutzbedarfsfeststellung → Modellierung → IT-Grundschutz-Check → ggf. Risikoanalyse → Umsetzung → Aufrechterhaltung/Verbesserung**

## Schutzbedarfsfeststellung

Drei Grundwerte:

- **Vertraulichkeit** → Informationen nur für Berechtigte
- **Integrität** → Informationen/Systeme vollständig und unverändert
- **Verfügbarkeit** → Informationen/Systeme stehen bei Bedarf zur Verfügung

Schutzbedarf:

- **normal**
- **hoch**
- **sehr hoch**

Wichtige Prinzipien:

- **Maximumprinzip** → höchster Schutzbedarf abhängiger Objekte wird übernommen
- **Kumulationseffekt** → viele Objekte zusammen können höheren Schutzbedarf erzeugen
- **Verteilungseffekt** → Redundanz/Verteilung kann Schutzbedarf eines einzelnen Objekts reduzieren

## Wann Risikoanalyse nach BSI 200-3?

Insbesondere wenn:

- Schutzbedarf **hoch oder sehr hoch**
- kein geeigneter Grundschutz-Baustein vorhanden ist
- das Zielobjekt nicht ausreichend modelliert werden kann
- besondere Einsatzszenarien oder zusätzliche Gefährdungen bestehen

Risiko wird grundsätzlich anhand von **Eintrittshäufigkeit und Schadenshöhe** beurteilt.

Mögliche Risikobehandlung:

- Risiko **reduzieren**
- Risiko **vermeiden**
- Risiko **übertragen**
- Risiko **akzeptieren**

## Anforderungen im Kompendium

- **B = Basis-Anforderungen** → grundlegende Erstabsicherung
- **S = Standard-Anforderungen** → angemessene Absicherung bei normalem Schutzbedarf
- **H = Anforderungen bei erhöhtem Schutzbedarf** → zusätzliche Anforderungen, die bei erhöhtem Schutzbedarf betrachtet werden

**Merke:**  
Anforderung = **WAS** erreicht werden soll  
Maßnahme = **WIE** die Anforderung umgesetzt wird

## Zertifizierung

Offizielle Bezeichnung:

**„ISO 27001-Zertifizierung auf der Basis von IT-Grundschutz“**

- Zertifizierungsstelle: **BSI**
- Audit: BSI-lizenzierte Auditoren
- Gültigkeit: **3 Jahre**
- zwei planmäßige Überwachungsaudits
- anschließend Re-Zertifizierung

## ISO 27001:2022

- internationaler ISMS-Standard
- risikobasierter Ansatz
- Annex A: **93 Controls**
- vier Themen:
  - 37 Organizational
  - 8 People
  - 14 Physical
  - 34 Technological
- wichtiges Dokument: **Statement of Applicability (SoA)**

### Prüfungs-Merksatz

> **ISO 27001 sagt überwiegend, WAS ein ISMS leisten muss. IT-Grundschutz liefert eine konkrete Methodik und Anforderungen für die praktische Umsetzung.**

---

# 1. Grundlagen des BSI IT-Grundschutzes

Der **BSI IT-Grundschutz** ist eine vom **Bundesamt für Sicherheit in der Informationstechnik (BSI)** entwickelte Methodik zur systematischen Absicherung von Informationen sowie zum Aufbau, Betrieb und zur kontinuierlichen Verbesserung eines **Informationssicherheitsmanagementsystems (ISMS)**.

Ziel ist es, ein angemessenes Sicherheitsniveau für Informationen, Geschäftsprozesse, Anwendungen, IT-Systeme, Kommunikationsverbindungen und Infrastruktur einer Organisation zu erreichen.

## Hauptmerkmale und Zweck

- **Ganzheitlicher Ansatz:** Betrachtet technische, organisatorische, infrastrukturelle und personelle Aspekte der Informationssicherheit.
- **Systematisches Vorgehen:** Informationsverbünde werden strukturiert erfasst, bewertet und abgesichert.
- **Praxisorientierung:** Das IT-Grundschutz-Kompendium enthält konkrete Sicherheitsanforderungen für typische Zielobjekte.
- **Hilfe zur Selbsthilfe:** Umsetzungshinweise unterstützen Organisationen dabei, geeignete Sicherheitsmaßnahmen abzuleiten.
- **Risikoorientierung:** Typische Gefährdungen sind bereits berücksichtigt; bei besonderen Risiken erfolgt eine zusätzliche Risikoanalyse.
- **Kernkomponenten:** BSI-Standards 200-1 bis 200-4 sowie IT-Grundschutz-Kompendium.

## Für wen ist IT-Grundschutz geeignet?

- **Bundesverwaltung:** BSI-Standards und IT-Grundschutz besitzen eine besondere Bedeutung bei der Umsetzung gesetzlicher Informationssicherheitsanforderungen.
- **KRITIS:** IT-Grundschutz kann zur Umsetzung der erforderlichen Informationssicherheit eingesetzt werden, ist jedoch nicht pauschal die einzig zulässige Methode.
- **Unternehmen und Organisationen:** freiwillig einsetzbare und etablierte Methode zur systematischen Verbesserung der Informationssicherheit.
- **KMU und Kommunen:** können insbesondere über vereinfachte bzw. abgestufte Vorgehensweisen ein angemessenes Sicherheitsniveau aufbauen.
- **Zertifizierung:** Eine „ISO 27001-Zertifizierung auf der Basis von IT-Grundschutz“ ist möglich.

---

# 2. Historie

| Jahr | Meilenstein |
|---|---|
| 1989 | Erste deutsche IT-Sicherheitskriterien |
| 1992 | IT-Sicherheitshandbuch |
| **1994** | Erste Ausgabe des **IT-Grundschutzhandbuchs** |
| 2002 | Einführung der IT-Grundschutz-Zertifizierung |
| 2005 | Weiterentwicklung zu den **IT-Grundschutz-Katalogen** und BSI-Standards der 100-x-Reihe |
| **2017** | Modernisierung durch die **BSI-Standards 200-x** und das **IT-Grundschutz-Kompendium** |
| **2026** | Weiterentwicklung des IT-Grundschutzes durch **Grundschutz++** |
| ab 2026 | Übergangsphase zwischen bestehender Grundschutz-Methodik und Grundschutz++ |

## Ursprünglicher Grundgedanke

Der IT-Grundschutz soll verhindern, dass für jedes einzelne IT-System eine vollständig individuelle Risikoanalyse durchgeführt werden muss.

Typische Gefährdungen und Sicherheitsanforderungen werden bereits durch den IT-Grundschutz berücksichtigt.

Eine zusätzliche individuelle Risikoanalyse wird dort durchgeführt, wo die standardisierte Absicherung nicht ausreicht.

---

# 3. Grundprinzipien

## Ganzheitlichkeit

Informationssicherheit besteht nicht nur aus technischen Schutzmaßnahmen.

Berücksichtigt werden unter anderem:

- Management
- Organisation
- Personal
- IT-Systeme
- Anwendungen
- Netzwerke
- Gebäude und Räume
- Geschäftsprozesse
- Detektion und Reaktion

## Standardisierte Absicherung

Typische Gefährdungen werden durch die IT-Grundschutz-Bausteine bereits berücksichtigt.

Dadurch muss nicht für jedes Zielobjekt eine vollständige individuelle Risikoanalyse durchgeführt werden.

## Angemessenheit und Wirtschaftlichkeit

Sicherheitsmaßnahmen sollen:

- wirksam,
- geeignet,
- praktikabel und
- wirtschaftlich

sein.

Der Aufwand muss in einem angemessenen Verhältnis zum Schutzbedarf stehen.

## Praxisnähe

Die Bausteine definieren Sicherheitsanforderungen für typische Zielobjekte.

Dabei gilt:

> **Anforderung = WAS muss erreicht werden?**  
> **Maßnahme = WIE wird die Anforderung erfüllt?**

Umsetzungshinweise unterstützen bei der Auswahl konkreter Maßnahmen.

## Modularität

Der Informationsverbund wird mithilfe wiederverwendbarer **Bausteine** modelliert.

## Kompatibilität

Die Grundschutz-Methodik ermöglicht die Umsetzung eines ISMS und kann als Grundlage für eine **ISO 27001-Zertifizierung auf der Basis von IT-Grundschutz** dienen.

---

# 4. Die vier BSI-Standards der 200-x-Reihe

| Standard | Inhalt |
|---|---|
| **BSI 200-1** | Anforderungen an ein Informationssicherheitsmanagementsystem (ISMS) |
| **BSI 200-2** | IT-Grundschutz-Methodik einschließlich Basis-, Kern- und Standard-Absicherung |
| **BSI 200-3** | Risikoanalyse auf Basis von IT-Grundschutz |
| **BSI 200-4** | Business Continuity Management (BCM) |

## BSI-Standard 200-1

Definiert grundlegende Anforderungen an ein ISMS.

Dazu gehören insbesondere:

- Verantwortung der Leitung
- Sicherheitsorganisation
- Sicherheitsziele und -strategie
- Ressourcen
- kontinuierliche Verbesserung

## BSI-Standard 200-2

Beschreibt die praktische **IT-Grundschutz-Methodik**.

Dazu gehören insbesondere:

- Strukturanalyse
- Schutzbedarfsfeststellung
- Modellierung
- IT-Grundschutz-Check
- Umsetzungsplanung

## BSI-Standard 200-3

Beschreibt die **Risikoanalyse auf Basis von IT-Grundschutz**.

Sie wird insbesondere benötigt, wenn:

- ein Zielobjekt hohen oder sehr hohen Schutzbedarf besitzt,
- kein geeigneter Baustein existiert,
- das Zielobjekt mit vorhandenen Bausteinen nicht ausreichend modelliert werden kann,
- besondere Einsatzszenarien oder zusätzliche Gefährdungen bestehen.

## BSI-Standard 200-4

Beschreibt das **Business Continuity Management (BCM)**.

Ziel ist es, kritische Geschäftsprozesse auch bei schwerwiegenden Störungen aufrechtzuerhalten oder innerhalb einer definierten Zeit wiederherzustellen.

---

# 5. Das IT-Grundschutz-Kompendium

Das IT-Grundschutz-Kompendium enthält Bausteine mit Sicherheitsanforderungen für typische Prozesse, Anwendungen, IT-Systeme und Infrastrukturen.

## Bausteinschichten

| Kürzel | Schicht |
|---|---|
| **ISMS** | Sicherheitsmanagement |
| **ORP** | Organisation und Personal |
| **CON** | Konzepte und Vorgehensweisen |
| **OPS** | Betrieb |
| **DER** | Detektion und Reaktion |
| **APP** | Anwendungen |
| **SYS** | IT-Systeme |
| **IND** | Industrielle IT |
| **NET** | Netze und Kommunikation |
| **INF** | Infrastruktur |

Die konkrete Anzahl der Bausteine ist abhängig von der jeweiligen Edition des Kompendiums und sollte daher nicht als dauerhaft feste Zahl gelernt werden.

## Aufbau eines Bausteins

Ein typischer Baustein enthält:

1. Beschreibung
2. Gefährdungslage
3. Anforderungen
4. weiterführende Informationen

Ergänzend stellt das BSI für viele Bausteine **Umsetzungshinweise** bereit.

## Anforderungskategorien

### Basis-Anforderungen (B)

Grundlegende Anforderungen für eine schnelle Erstabsicherung.

### Standard-Anforderungen (S)

Zusammen mit den Basis-Anforderungen bilden sie die angemessene Absicherung für den normalen Schutzbedarf.

### Anforderungen bei erhöhtem Schutzbedarf (H)

Zusätzliche Anforderungen, die bei erhöhtem Schutzbedarf betrachtet und im Rahmen der Risikoanalyse berücksichtigt werden können.

---

# 6. Grundschutz++ [2026]

Mit **Grundschutz++** entwickelt das BSI den bisherigen IT-Grundschutz weiter.

Ziel ist eine modernere, stärker digital unterstützte und automatisierbare Anwendung der Grundschutz-Methodik.

## Wesentliche Ziele

- stärkere **Prozessorientierung**
- maschinenlesbare Sicherheitsanforderungen
- strukturierte digitale Bereitstellung von Anforderungen
- stärkere Unterstützung von **Automatisierung**
- kontinuierlichere Bewertung des Sicherheitsniveaus
- flexiblere Berücksichtigung unterschiedlicher Schutzbedarfe
- Weiterentwicklung der Risikoanalyse
- vereinfachte Anwendung des IT-Grundschutzes

Grundschutz++ befindet sich 2026 weiterhin in einer **Einführungs- und Übergangsphase**.

Für Prüfungen sollte deshalb insbesondere die klassische Methodik der BSI-Standards 200-1 bis 200-4 und des IT-Grundschutz-Kompendiums sicher beherrscht werden.

---

# 7. Vorgehensweisen nach BSI-Standard 200-2

Der BSI-Standard 200-2 unterscheidet drei Vorgehensweisen.

| Vorgehensweise | Beschreibung |
|---|---|
| **Basis-Absicherung** | schnelle grundlegende Absicherung des gesamten Informationsverbunds |
| **Kern-Absicherung** | priorisierte Absicherung besonders wichtiger Geschäftsprozesse und Zielobjekte |
| **Standard-Absicherung** | vollständige Anwendung der Grundschutz-Methodik auf den gesamten Informationsverbund |

## Basis-Absicherung

Ziel:

> Möglichst schnell eine grundlegende Absicherung über den gesamten Informationsverbund erreichen.

Geeignet beispielsweise für:

- Einstieg in den IT-Grundschutz
- Organisationen mit begrenzten Ressourcen
- schnelle Verbesserung des Sicherheitsniveaus

## Kern-Absicherung

Ziel:

> Zunächst besonders wichtige Geschäftsprozesse und Zielobjekte schützen.

Im Mittelpunkt stehen die sogenannten **„Kronjuwelen“** der Organisation.

## Standard-Absicherung

Ziel:

> Systematische und vollständige Absicherung des betrachteten Informationsverbunds nach der IT-Grundschutz-Methodik.

---

# 8. Ablauf der Standard-Absicherung

```text
Initiierung und Festlegung des Geltungsbereichs
          ↓
Strukturanalyse
          ↓
Schutzbedarfsfeststellung
          ↓
Modellierung
          ↓
IT-Grundschutz-Check
          ↓
ggf. ergänzende Risikoanalyse
          ↓
Umsetzungs-/Realisierungsplanung
          ↓
Umsetzung der Maßnahmen
          ↓
Aufrechterhaltung und Verbesserung
```

## 8.1 Strukturanalyse

Der Informationsverbund wird erfasst.

Dazu gehören beispielsweise:

- Geschäftsprozesse
- Informationen
- Anwendungen
- IT-Systeme
- Netzwerke
- Kommunikationsverbindungen
- Räume und Gebäude

**Ziel:** Wissen, **was geschützt werden muss**.

## 8.2 Schutzbedarfsfeststellung

Für relevante Zielobjekte wird der Schutzbedarf hinsichtlich der drei Grundwerte bestimmt:

### Vertraulichkeit

> Informationen dürfen nur berechtigten Personen zugänglich sein.

### Integrität

> Informationen und Systeme müssen korrekt, vollständig und vor unbefugter Veränderung geschützt sein.

### Verfügbarkeit

> Informationen und Systeme müssen bei Bedarf verfügbar sein.

## Schutzbedarfskategorien

- **normal**
- **hoch**
- **sehr hoch**

## Wichtige Prinzipien

### Maximumprinzip

Der höchste relevante Schutzbedarf wird auf abhängige Zielobjekte übertragen.

### Kumulationseffekt

Viele einzelne Informationen oder Systeme können zusammen einen höheren Schutzbedarf erzeugen.

**Beispiel:** Ein Server enthält Daten zahlreicher Kunden. Der Ausfall des Servers hätte wesentlich größere Auswirkungen als der Verlust eines einzelnen Datensatzes.

### Verteilungseffekt

Durch Verteilung oder Redundanz kann die Bedeutung eines einzelnen Zielobjekts geringer sein.

**Beispiel:** Ein Dienst läuft redundant auf mehreren Servern. Der Ausfall eines einzelnen Servers führt nicht zum Gesamtausfall.

## 8.3 Modellierung

Passende IT-Grundschutz-Bausteine werden den Zielobjekten des Informationsverbunds zugeordnet.

**Frage:**

> Welche Bausteine gelten für welches Zielobjekt?

## 8.4 IT-Grundschutz-Check

Soll-Ist-Vergleich:

> Welche Anforderungen sind bereits erfüllt und welche noch nicht?

Typische Ergebnisse:

- erfüllt
- teilweise erfüllt
- nicht erfüllt
- nicht relevant

Aus den Abweichungen entsteht eine **Defizit- bzw. Maßnahmenübersicht**.

## 8.5 Risikoanalyse

Eine Risikoanalyse nach BSI-Standard 200-3 ist insbesondere erforderlich, wenn:

- hoher Schutzbedarf vorliegt,
- sehr hoher Schutzbedarf vorliegt,
- kein geeigneter Baustein existiert,
- die vorhandenen Bausteine das Zielobjekt nicht ausreichend abdecken,
- besondere Einsatzszenarien bestehen.

---

# 9. Risikoanalyse nach BSI-Standard 200-3

Grundsätzlich gilt:

> **Risiko ergibt sich aus der Betrachtung von Eintrittshäufigkeit und möglicher Schadenshöhe.**

## Vereinfachter Ablauf

```text
Zielobjekt bestimmen
        ↓
Gefährdungen ermitteln
        ↓
Risiko einschätzen
        ↓
Risiko bewerten
        ↓
Risikobehandlung festlegen
        ↓
Restrisiko bewerten
```

## Möglichkeiten der Risikobehandlung

### Risiko reduzieren

Zusätzliche Sicherheitsmaßnahmen einführen.

### Risiko vermeiden

Risikobehaftete Tätigkeit oder Technologie nicht einsetzen.

### Risiko übertragen

Risiko teilweise auf Dritte übertragen.

**Beispiele:** Versicherung oder Outsourcing.

### Risiko akzeptieren

Ein verbleibendes Risiko wird bewusst akzeptiert.

Die Risikoakzeptanz muss durch eine **entsprechend verantwortliche Stelle** erfolgen.

---

# 10. Sensibilisierung und Schulung – ORP.3

Der Baustein **ORP.3 „Sensibilisierung und Schulung zur Informationssicherheit“** gehört zur Schicht **Organisation und Personal (ORP)**.

## Warum ist Sensibilisierung wichtig?

Fehlhandlungen, mangelndes Sicherheitsbewusstsein und Social Engineering stellen wesentliche Informationssicherheitsrisiken dar.

Technische Sicherheitsmaßnahmen müssen deshalb durch organisatorische und personelle Maßnahmen ergänzt werden.

## Typische Maßnahmen

- regelmäßige Schulungen
- zielgruppenspezifische Schulungen
- Schulung neuer Mitarbeitender
- Phishing-Simulationen
- Awareness-Kampagnen
- Newsletter und Informationsmaterial
- Schulungen für Administratoren
- Schulungen für Führungskräfte
- Wirksamkeitskontrollen

## Zielgruppen

### Mitarbeitende

Grundlegendes Sicherheitsbewusstsein.

### Führungskräfte

- Vorbildfunktion
- Verantwortungsübernahme
- Bereitstellung von Ressourcen

### Administratoren

Vertiefte technische Sicherheitskenntnisse.

### Besonders exponierte Gruppen

Beispiele:

- Buchhaltung → CEO-Fraud
- Personalabteilung → Bewerbungs-Phishing
- Geschäftsführung → Spear-Phishing
- IT-Administratoren → privilegierte Zugriffe

## Awareness vs. Schulung

**Awareness:**

> Sicherheitsbewusstsein und sicherheitsgerechtes Verhalten fördern.

**Schulung:**

> Konkretes Wissen und Fähigkeiten vermitteln.

---

# 11. Zertifizierung

Das BSI bietet die:

> **„ISO 27001-Zertifizierung auf der Basis von IT-Grundschutz“**

an.

Dabei wird geprüft, ob der betrachtete Informationsverbund die entsprechenden Anforderungen unter Anwendung der IT-Grundschutz-Methodik erfüllt.

## Vereinfachter Ablauf

```text
Vorbereitung des Informationsverbunds
        ↓
Zertifizierungsantrag
        ↓
BSI-lizenziertes Auditteam
        ↓
Prüfung der Referenzdokumente
        ↓
Auditierung
        ↓
Auditbericht
        ↓
Prüfung durch das BSI
        ↓
Zertifizierungsentscheidung
```

## Eckdaten

- **Zertifizierungsstelle:** BSI
- **Auditoren:** vom BSI lizenzierte unabhängige Auditoren
- **Gültigkeit:** 3 Jahre
- **Überwachung:** zwei planmäßige Überwachungsaudits während der Zertifikatslaufzeit
- **danach:** Re-Zertifizierung erforderlich

---

# 12. IT-Grundschutz vs. ISO/IEC 27001:2022

Sowohl der **BSI IT-Grundschutz** als auch die **ISO/IEC 27001:2022** unterstützen Organisationen beim Aufbau, Betrieb und der kontinuierlichen Verbesserung eines ISMS.

Die Ansätze unterscheiden sich jedoch hinsichtlich Methodik, Konkretisierungsgrad und Risikobetrachtung.

| Aspekt | BSI IT-Grundschutz | ISO/IEC 27001:2022 |
|---|---|---|
| **Ansatz** | strukturierte Methodik mit konkreten Sicherheitsanforderungen | internationaler, managementsystem- und risikobasierter Standard |
| **Risikobetrachtung** | typische Gefährdungen bereits berücksichtigt; zusätzliche Risikoanalyse in definierten Fällen | systematische Identifikation, Analyse, Bewertung und Behandlung von Informationssicherheitsrisiken |
| **Konkretheit** | hoher Konkretisierungsgrad durch Bausteine und Anforderungen | ISO 27001 definiert primär ISMS-Anforderungen und Referenz-Controls |
| **Umsetzungshilfe** | IT-Grundschutz-Kompendium und Umsetzungshinweise | insbesondere ISO/IEC 27002 |
| **Struktur** | Bausteine in zehn Schichten | Annex A mit 93 Controls in vier Themenbereichen |
| **Dokumentation** | u. a. Strukturanalyse, Schutzbedarfsfeststellung, Modellierung und Grundschutz-Check | u. a. Risikobewertung, Risikobehandlung und Statement of Applicability |
| **Verbreitung** | insbesondere Deutschland | international |
| **Zertifizierung** | ISO 27001 auf der Basis von IT-Grundschutz | ISO/IEC-27001-Zertifizierung |
| **Umsetzung** | stark methodisch geführt | größere organisatorische Freiheit bei der Umsetzung |

### Merksatz

> **ISO 27001 beschreibt primär, welche Anforderungen ein ISMS erfüllen muss. Der IT-Grundschutz bietet eine detaillierte Methodik und konkrete Sicherheitsanforderungen für die praktische Umsetzung.**

---

# 13. ISO/IEC 27001:2022 Annex A

Mit ISO/IEC 27001:2022 wurde Annex A gegenüber der vorherigen Version neu strukturiert.

| Version | Controls | Struktur |
|---|---:|---|
| ISO/IEC 27001:2013 | 114 | 14 Kategorien |
| **ISO/IEC 27001:2022** | **93** | **4 Themenbereiche** |

## Die vier Themenbereiche

| Kategorie | Controls |
|---|---:|
| **Organizational Controls** | 37 |
| **People Controls** | 8 |
| **Physical Controls** | 14 |
| **Technological Controls** | 34 |
| **Gesamt** | **93** |

Die Reduzierung von 114 auf 93 bedeutet nicht, dass 21 Sicherheitsmaßnahmen ersatzlos gestrichen wurden.

Zahlreiche Controls wurden:

- zusammengeführt,
- überarbeitet,
- neu strukturiert oder
- ergänzt.

## 11 neue Controls der Version 2022

1. Threat Intelligence
2. Information Security for Use of Cloud Services
3. ICT Readiness for Business Continuity
4. Physical Security Monitoring
5. Configuration Management
6. Information Deletion
7. Data Masking
8. Data Leakage Prevention
9. Monitoring Activities
10. Web Filtering
11. Secure Coding

---

# 14. Statement of Applicability (SoA)

Das **Statement of Applicability (SoA)** ist ein zentrales Dokument im Rahmen der ISO/IEC 27001.

Es dokumentiert insbesondere:

- welche notwendigen Controls angewendet werden,
- den Umsetzungsstatus und
- warum bestimmte Annex-A-Controls gegebenenfalls nicht erforderlich sind.

Wichtig:

> Die ISO 27001 verlangt **nicht**, dass einfach alle 93 Annex-A-Controls blind umgesetzt werden.

Die Auswahl der erforderlichen Maßnahmen ergibt sich insbesondere aus:

- Informationssicherheitsrisiken,
- Risikobehandlung,
- gesetzlichen Anforderungen,
- vertraglichen Anforderungen,
- organisatorischen Anforderungen.

Annex A dient dabei als Referenz, damit notwendige Controls nicht übersehen werden.

---

# 15. Prüfungsrelevante Begriffsabgrenzungen

## Informationssicherheit vs. IT-Sicherheit

**Informationssicherheit**

schützt Informationen unabhängig davon, ob diese:

- digital,
- auf Papier oder
- mündlich

vorliegen.

**IT-Sicherheit**

konzentriert sich auf technische IT-Systeme und deren Schutz.

> Informationssicherheit ist somit weiter gefasst als reine IT-Sicherheit.

---

## Gefährdung vs. Risiko

**Gefährdung:**

> Potenzielle Ursache eines Schadens.

Beispiel: Feuer.

**Risiko:**

> Bewertung der möglichen Auswirkungen einer Gefährdung unter Berücksichtigung von Eintrittshäufigkeit und Schadenshöhe.

---

## Anforderung vs. Maßnahme

**Anforderung:**

> Beschreibt, WAS erreicht werden soll.

**Maßnahme:**

> Beschreibt, WIE die Anforderung konkret umgesetzt wird.

---

## Schutzbedarf vs. Risiko

**Schutzbedarf:**

> Wie wichtig ist der Schutz eines Zielobjekts?

**Risiko:**

> Welche Gefährdungen bestehen und wie kritisch sind deren mögliche Auswirkungen?

---

## ISMS vs. Sicherheitskonzept

**ISMS:**

> Managementsystem zur systematischen Steuerung und kontinuierlichen Verbesserung der Informationssicherheit.

**Sicherheitskonzept:**

> Dokumentiert konkrete Sicherheitsanforderungen und Maßnahmen für einen definierten Informationsverbund.

---

# 16. Prüfungs-Merksätze

> **BSI 200-1 = WAS braucht ein ISMS?**

> **BSI 200-2 = WIE wende ich IT-Grundschutz an?**

> **BSI 200-3 = WIE behandle ich besondere Risiken?**

> **BSI 200-4 = WIE halte ich kritische Prozesse bei Störungen am Laufen?**

---

> **Strukturanalyse:** Was habe ich?

> **Schutzbedarfsfeststellung:** Wie wichtig ist es?

> **Modellierung:** Welche Bausteine passen dazu?

> **Grundschutz-Check:** Was davon habe ich bereits umgesetzt?

> **Risikoanalyse:** Welche besonderen Risiken bleiben?

> **Umsetzung:** Wie schließe ich die Sicherheitslücken?

---

> **Vertraulichkeit:** Nur Berechtigte dürfen zugreifen.

> **Integrität:** Daten und Systeme müssen korrekt und unverändert sein.

> **Verfügbarkeit:** Daten und Systeme müssen rechtzeitig verfügbar sein.

---

> **Basis-Anforderung:** grundlegende Erstabsicherung.

> **Standard-Anforderung:** angemessene Absicherung bei normalem Schutzbedarf.

> **Erhöhter Schutzbedarf:** zusätzliche Betrachtung und gegebenenfalls Risikoanalyse.

---

> **ISO 27001:** international, risikobasiert und managementsystemorientiert.

> **IT-Grundschutz:** detaillierte Methodik mit konkreten Sicherheitsanforderungen.

---

# Quellen / weiterführende Literatur

- Bundesamt für Sicherheit in der Informationstechnik (BSI): IT-Grundschutz
- BSI-Standard 200-1: Managementsysteme für Informationssicherheit
- BSI-Standard 200-2: IT-Grundschutz-Methodik
- BSI-Standard 200-3: Risikoanalyse auf der Basis von IT-Grundschutz
- BSI-Standard 200-4: Business Continuity Management
- BSI IT-Grundschutz-Kompendium
- ISO/IEC 27001:2022
- ISO/IEC 27002:2022