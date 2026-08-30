# Sicheren Betrieb gewährleisten

Dieser Ordner enthält Lernunterlagen und kompakte Handouts zum Themenbereich **„Sicheren Betrieb gewährleisten“** im Rahmen der Vorbereitung auf die IHK-Prüfung zum **Geprüften Berufsspezialisten für Informationssicherheit**.

Die enthaltenen Dokumente behandeln zentrale organisatorische, technische und methodische Aspekte zur Sicherstellung eines stabilen, sicheren und widerstandsfähigen IT-Betriebs.

---

## Enthaltene Lernunterlagen

### 1. BSI IT-Grundschutz und ISO/IEC 27001

📄 **[BSI IT-Grundschutz und ISO27001.md](./BSI%20IT-Grundschutz%20und%20ISO27001.md)**

Dieses Lernblatt behandelt die Grundlagen des **BSI IT-Grundschutzes** sowie die Abgrenzung und Verbindung zur **ISO/IEC 27001:2022**.

Schwerpunkte sind unter anderem:

- Aufbau und Ziele eines Informationssicherheitsmanagementsystems (ISMS)
- BSI-Standards 200-1 bis 200-4
- IT-Grundschutz-Kompendium
- Basis-, Kern- und Standard-Absicherung
- Strukturanalyse und Schutzbedarfsfeststellung
- Modellierung und IT-Grundschutz-Check
- Risikoanalyse nach BSI-Standard 200-3
- Schutzbedarf: normal, hoch und sehr hoch
- Vertraulichkeit, Integrität und Verfügbarkeit
- ISO/IEC 27001:2022 und Annex A
- Statement of Applicability (SoA)
- Vergleich zwischen ISO 27001 und BSI IT-Grundschutz
- ISO-27001-Zertifizierung auf Basis von IT-Grundschutz

---

### 2. Business Continuity Management (BCM)

📄 **[Business Continuity Management (BCM).md](./Business%20Continuity%20Management%20%28BCM%29.md)**

Dieses Dokument behandelt den Aufbau und Betrieb eines **Business Continuity Management Systems (BCMS)** nach dem **BSI-Standard 200-4**.

Schwerpunkte sind:

- Business Continuity, BCM und BCMS
- Abgrenzung zwischen Störung, Notfall und Krise
- Allgemeine und Besondere Aufbauorganisation (AAO / BAO)
- Business Impact Analyse (BIA)
- BCM-Risikoanalyse
- zeitkritische Geschäftsprozesse
- MTPD / MTA
- RTO / WAZ
- RPO
- MBCO
- RTA und RPA
- Business-Continuity-Strategien
- Geschäftsfortführungsplan (GFP)
- Wiederanlaufplan (WAP)
- Wiederherstellungsplan (WHP)
- Notfall- und Krisenkommunikation
- Übungen und Tests
- PDCA-Zyklus
- Reaktiv-, Aufbau- und Standard-BCMS
- Verbindung zur ISO 22301

---

### 3. Testmanagement & Testautomatisierung

📄 **[Testmanagement & Testautomatisierung.md](./Testmanagement%20%26%20Testautomatisierung.md)**

Dieses Lernblatt behandelt die Planung, Durchführung, Steuerung und Automatisierung von Softwaretests auf Grundlage gängiger **ISTQB- und ISO/IEC/IEEE-29119-Konzepte**.

Schwerpunkte sind:

- Grundlagen des Testmanagements
- Testplanung und Teststeuerung
- Testanalyse und Testentwurf
- Testrealisierung und Testdurchführung
- Testabschluss
- Teststrategie und Testkonzept
- Teststufen
- Testarten
- Testtechniken
- statische und dynamische Tests
- funktionale und nicht-funktionale Tests
- Black-Box- und White-Box-Verfahren
- Regressionstests
- Bestätigungstests
- Wiederanlauftests
- Sicherheitstests und Penetrationstests
- Testautomatisierung
- Testpyramide
- Data-Driven und Keyword-Driven Testing
- Behaviour-Driven Development (BDD)
- CI/CD-Integration
- Quality Gates
- Flaky Tests
- Testmetriken und risikobasiertes Testen

---

## Zusammenhang der Themen

Die drei Themenbereiche ergänzen sich bei der Sicherstellung eines stabilen und sicheren IT-Betriebs:

```text
                 Sicherer IT-Betrieb
                        │
        ┌───────────────┼───────────────┐
        │               │               │
        ▼               ▼               ▼
Informations-       Business        Testmanagement
 sicherheit         Continuity          &
        │           Management      Testautomatisierung
        │               │               │
        ▼               ▼               ▼
BSI IT-Grundschutz  Betriebs-       Qualität und
ISO/IEC 27001       kontinuität     Funktionssicherheit
        │               │               │
        └───────────────┼───────────────┘
                        ▼
             Widerstandsfähiger und
               sicherer Betrieb