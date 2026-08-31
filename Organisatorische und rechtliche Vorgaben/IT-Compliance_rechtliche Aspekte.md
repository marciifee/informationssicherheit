# Lernblatt / Handout: IT-Compliance – rechtliche Aspekte

### Kompaktes Nachschlagewerk für die IHK-Prüfung „Geprüfter Berufsspezialist für Informationssicherheit“

**Stand: 31. August 2026**  
**Schwerpunkt:** rechtliche und regulatorische Anforderungen an IT-Systeme, IT-Betrieb und Informationssicherheit

> **Hinweis:** Rechtslage, Behördenpraxis und Regulierung ändern sich. Für produktive Entscheidungen sind aktuelle Originalquellen maßgeblich.

---

# ⚡ Schnellcheck vor der Prüfung

- **IT-Compliance** = regelkonformer Einsatz und Betrieb von IT **und** Unterstützung unternehmensweiter Compliance durch IT.
- Rechtsquellen: EU-Verordnungen, Gesetze, Rechtsverordnungen, Verträge, Behördenanforderungen, interne Regeln.
- **DSGVO Art. 28** → Auftragsverarbeitung
- **DSGVO Art. 32** → Sicherheit der Verarbeitung
- **DSGVO Art. 33** → Data-Breach-Meldung grundsätzlich binnen 72 h, soweit meldepflichtig
- **BDSG § 26** → Beschäftigtendaten
- **BetrVG § 87 Abs. 1 Nr. 6** → Mitbestimmung bei Überwachungstechnik
- **HGB/AO** → Buchführung/Aufbewahrung
- **GoBD** → aktuelle Grundsätze für elektronische Bücher, Aufzeichnungen, Unterlagen und Datenzugriff
- **GoBS und GDPdU** sind als eigenständige Regelwerke historisch und durch GoBD abgelöst.
- **E-Rechnung** → seit 1.1.2025 neue B2B-Regeln; Übergangsregelungen beachten.
- **HinSchG** → interne Meldestellen grundsätzlich ab 50 Beschäftigten.
- **BSIG 2025 / NIS-2-Umsetzung** → seit 2025/2026 neuer deutscher Rahmen mit wichtigen und besonders wichtigen Einrichtungen.
- **§ 30 BSIG** → Cyber-Risikomanagementmaßnahmen.
- **§ 32 BSIG** → gestufte Meldung erheblicher Sicherheitsvorfälle: 24 h / 72 h / weitere Abschlussmeldung.
- **§ 38 BSIG** → Geschäftsleitungs-, Überwachungs- und Schulungspflichten.
- **DORA** gilt seit 17.1.2025 für erfasste Finanzunternehmen.
- **AI Act** gilt seit 2.8.2026 grundsätzlich, mit gestaffelten Sonderfristen.
- **EU Data Act** gilt seit 12.9.2025 weitgehend.
- Standards wie **ISO 27001** sind nicht automatisch Gesetz, können aber Stand der Technik/Vertragspflichten konkretisieren.
- **Outsourcing verlagert Aufgaben, nicht automatisch Verantwortung.**
- **IT-Compliance muss nachweisbar sein.**

---

# 1. Begriff IT-Compliance

IT-Compliance hat zwei Perspektiven:

## 1. Regelkonforme IT

IT-Systeme müssen relevante Regeln einhalten.

Beispiele:

- Datenschutz
- Informationssicherheit
- Aufbewahrung
- Mitbestimmung
- Lizenzrecht

## 2. Compliance durch IT

IT unterstützt die Einhaltung anderer Verpflichtungen.

Beispiele:

- Buchhaltung
- Audit Trails
- Vier-Augen-Workflows
- Sanktionslistenprüfung
- Hinweisgebersysteme

---

# 2. IT-Compliance als kontinuierlicher Prozess

```text
Anforderungen identifizieren
        ↓
Betroffenheit prüfen
        ↓
Kontrollen ableiten
        ↓
Umsetzen
        ↓
Nachweise erzeugen
        ↓
Überwachen
        ↓
Änderungen erkennen
        ↓
Verbessern
```

---

# 3. Rechtsquellen-Hierarchie

Mögliche Quellen:

- EU-Verordnungen
- EU-Richtlinien + nationale Umsetzung
- Bundes-/Landesgesetze
- Rechtsverordnungen
- Verwaltungsakte
- Verträge
- interne Richtlinien
- Normen/Standards

### Wichtig

> Eine ISO-Norm ist nicht allein deshalb gesetzlich verbindlich, weil sie existiert.

Verbindlichkeit kann entstehen durch:

- Vertrag
- Gesetzesverweis
- Behördenanforderung
- Stand-der-Technik-Konkretisierung

---

# 4. Veraltete Rechtsgrundlagen aus älteren IT-Compliance-Unterlagen

Historische Folien verwenden häufig:

- § 9 BDSG + Anlage
- § 11 BDSG Auftragsdatenverarbeitung
- GoBS
- GDPdU

Für eine Prüfung 2026 solltest du aktualisieren:

| Alt | Heute zentral |
|---|---|
| § 9 BDSG + Anlage | Art. 32 DSGVO + ergänzendes BDSG |
| § 11 BDSG | Art. 28 DSGVO |
| GoBS | GoBD |
| GDPdU | GoBD |

---

# 5. Datenschutz – DSGVO

Zentrale Prinzipien nach Art. 5 DSGVO:

- Rechtmäßigkeit
- Transparenz
- Zweckbindung
- Datenminimierung
- Richtigkeit
- Speicherbegrenzung
- Integrität/Vertraulichkeit
- Rechenschaftspflicht

---

# 6. Rechenschaftspflicht

Organisationen müssen Datenschutz nicht nur einhalten, sondern nachweisen können.

Nachweise:

- Verzeichnis von Verarbeitungstätigkeiten
- TOM
- Verträge
- Löschkonzept
- DSFA
- Richtlinien
- Schulungen

---

# 7. Auftragsverarbeitung

Art. 28 DSGVO verlangt bei Auftragsverarbeitung einen Vertrag/Rechtsakt.

Der Verantwortliche darf nur Auftragsverarbeiter einsetzen, die hinreichende Garantien bieten.

Praktisch:

- Due Diligence
- AVV
- TOM
- Unterauftragnehmer
- Audit
- Exit

---

# 8. Sicherheit der Verarbeitung

Art. 32 DSGVO:

- Stand der Technik
- Implementierungskosten
- Art/Umfang/Zweck
- Risiko

berücksichtigen.

Beispiele:

- Pseudonymisierung
- Verschlüsselung
- Resilienz
- Wiederherstellung
- regelmäßige Tests

---

# 9. Data Breach

Art. 33 DSGVO:

> meldepflichtige Verletzung grundsätzlich unverzüglich und möglichst binnen **72 Stunden** nach Bekanntwerden.

Art. 34:

> bei hohem Risiko kann Benachrichtigung betroffener Personen erforderlich sein.

---

# 10. Datenschutz-Folgenabschätzung

Art. 35 DSGVO:

Bei voraussichtlich hohem Risiko ist vor Verarbeitung eine DSFA durchzuführen.

---

# 11. Datenschutzbeauftragter

Zusätzlich zu Art. 37 DSGVO bestimmt **§ 38 BDSG** für nichtöffentliche Stellen insbesondere eine nationale Schwelle:

> grundsätzlich ab 20 Personen, die ständig automatisiert personenbezogene Daten verarbeiten.

Weitere Fälle können unabhängig von dieser Zahl eine Benennung erfordern.

---

# 12. Beschäftigtendatenschutz

§ 26 BDSG ergänzt die DSGVO für Beschäftigungsverhältnisse.

IT-relevant:

- HR-Systeme
- Monitoring
- E-Mail
- Zeiterfassung
- Video
- DLP
- Security Logs

---

# 13. Betriebsrat

§ 87 Abs. 1 Nr. 6 BetrVG:

Mitbestimmung bei technischen Einrichtungen zur Überwachung von Verhalten oder Leistung.

### Merksatz

> Technisch mögliche Überwachung kann bereits mitbestimmungsrelevant sein.

---

# 14. TDDDG

Das **Telekommunikation-Digitale-Dienste-Datenschutz-Gesetz (TDDDG)** enthält Datenschutz-/Privatsphärenregeln für Telekommunikation und digitale Dienste.

Besonders bekannt:

**§ 25 TDDDG**

→ Speicherung von oder Zugriff auf Informationen in Endeinrichtungen, z. B. Cookies/ähnliche Technologien.

---

# 15. Buchführung und digitale Unterlagen

Relevante Rechtsgrundlagen:

- HGB
- AO
- UStG
- GoBD

IT-Systeme müssen gewährleisten:

- Nachvollziehbarkeit
- Nachprüfbarkeit
- Vollständigkeit
- Ordnung
- Unveränderbarkeit
- Verfügbarkeit

---

# 16. HGB-Aufbewahrung

§ 257 HGB enthält unterschiedliche Fristen.

Stand 2026:

- bestimmte Bücher/Abschlüsse: **10 Jahre**
- Buchungsbelege: **8 Jahre**
- Handelsbriefe: **6 Jahre**

Sonderregeln können gelten.

---

# 17. AO-Aufbewahrung

§ 147 AO enthält ebenfalls:

- 10 Jahre für bestimmte Unterlagen
- 8 Jahre für Buchungsbelege
- 6 Jahre für sonstige bestimmte Unterlagen

Fristen können länger wirken, wenn sie noch steuerlich relevant sind.

---

# 18. GoBD

Aktuelle Basis:

> BMF-Schreiben zu den „Grundsätzen zur ordnungsmäßigen Führung und Aufbewahrung von Büchern, Aufzeichnungen und Unterlagen in elektronischer Form sowie zum Datenzugriff“.

Die GoBD wurden zuletzt u. a. 2024 und 2025 angepasst.

---

# 19. GoBD – IT-Anforderungen

Praktische Anforderungen:

- Nachvollziehbarkeit
- Verfahrensdokumentation
- Unveränderbarkeit
- Protokollierung
- Zugriffsschutz
- Datenzugriff für Prüfung
- maschinelle Auswertbarkeit
- Aufbewahrung

---

# 20. Verfahrensdokumentation

Beschreibt beispielsweise:

- Prozesse
- Systeme
- Datenflüsse
- Berechtigungen
- Archivierung
- Änderungen
- Kontrollen

---

# 21. E-Rechnung

Seit **1. Januar 2025** gelten neue Regeln für B2B-E-Rechnungen zwischen inländischen Unternehmern.

Seit diesem Zeitpunkt müssen inländische Unternehmer grundsätzlich E-Rechnungen empfangen können.

Übergangsregeln für die Ausstellung laufen teilweise bis Ende 2026 bzw. für bestimmte kleinere Aussteller bis Ende 2027.

---

# 22. E-Rechnung ist nicht einfach PDF

Seit 2025 ist eine E-Rechnung im steuerlichen Sinn grundsätzlich ein **strukturiertes elektronisches Format**, das elektronische Verarbeitung ermöglicht.

Ein einfaches PDF ist nicht automatisch eine E-Rechnung im neuen Sinn.

---

# 23. Unternehmensorganisation

IT-Compliance ist Leitungsaufgabe.

Relevante Grundlagen:

- § 43 GmbHG
- §§ 91, 93 AktG
- § 130 OWiG

Die operative Umsetzung kann delegiert werden, angemessene Organisation und Überwachung bleiben jedoch Leitungsthema.

---

# 24. § 91 AktG

Vorstand muss ein Überwachungssystem einrichten, damit bestandsgefährdende Entwicklungen früh erkannt werden.

Für börsennotierte AG zusätzlich angemessenes und wirksames internes Kontroll- und Risikomanagementsystem.

IT kann dafür kritisch sein.

---

# 25. § 93 AktG

Vorstandsmitglieder müssen die Sorgfalt eines ordentlichen und gewissenhaften Geschäftsleiters anwenden.

IT-/Cyberrisiken können Teil dieser Sorgfaltspflichten sein.

---

# 26. § 43 GmbHG

Geschäftsführer müssen die Sorgfalt eines ordentlichen Geschäftsmannes anwenden.

Pflichtverletzungen können Schadensersatzpflichten gegenüber der Gesellschaft auslösen.

---

# 27. OWiG

## § 130

Verletzung erforderlicher Aufsichtspflichten kann ordnungswidrig sein.

## § 30

Unter Voraussetzungen kann eine Unternehmensgeldbuße verhängt werden.

---

# 28. Hinweisgeberschutzgesetz

Arbeitgeber ab grundsätzlich 50 Beschäftigten müssen eine interne Meldestelle einrichten.

IT-Anforderungen:

- Vertraulichkeit
- Zugriffsbeschränkung
- sichere Kommunikation
- Datenschutz
- Dokumentation

---

# 29. IT-Strafrecht

Beispiele:

- § 202a StGB – Ausspähen von Daten
- § 202b – Abfangen von Daten
- § 202c – Vorbereitung
- § 303a – Datenveränderung
- § 303b – Computersabotage
- § 203 – Verletzung von Privatgeheimnissen in bestimmten Berufs-/Geheimnisträgerkontexten

---

# 30. Geschäftsgeheimnisse

GeschGehG:

Schutz setzt angemessene Geheimhaltungsmaßnahmen voraus.

IT-Maßnahmen:

- Zugriff
- Verschlüsselung
- DLP
- Logging
- Klassifizierung
- NDA

---

# 31. Lizenz-Compliance

Zu überwachen:

- Nutzungsrechte
- Benutzerzahl
- Geräte
- Cores/CPU
- Virtualisierung
- Cloudnutzung
- Open Source
- Auditklauseln

Risiko:

- Unterlizenzierung
- Überlizenzierung
- Lizenzverletzung

---

# 32. NIS-2 in Deutschland – aktueller Stand 2026

Deutschland hat die NIS-2-Vorgaben durch das neue **BSI-Gesetz (BSIG 2025)** umgesetzt.

Das Gesetz unterscheidet unter anderem:

- **besonders wichtige Einrichtungen**
- **wichtige Einrichtungen**

Betroffenheit hängt insbesondere von:

- Sektor
- Einrichtungsart
- Größe

ab.

---

# 33. § 30 BSIG – Risikomanagement

Besonders wichtige und wichtige Einrichtungen müssen geeignete, verhältnismäßige und wirksame technische und organisatorische Maßnahmen ergreifen.

Berücksichtigt werden:

- Risikoexposition
- Größe
- Kosten
- Eintrittswahrscheinlichkeit
- Schwere
- gesellschaftliche/wirtschaftliche Auswirkungen

Stand der Technik soll eingehalten werden.

---

# 34. NIS-2-/BSIG-Maßnahmenbereiche

Typische Themen:

- Risikoanalyse
- Incident Handling
- BCM
- Backup/DR
- Lieferkettensicherheit
- sichere Beschaffung/Entwicklung/Wartung
- Schwachstellen
- Wirksamkeitsprüfung
- Kryptografie
- Zugriffskontrolle
- MFA

---

# 35. § 32 BSIG – Meldepflichten

Bei erheblichem Sicherheitsvorfall:

- **spätestens 24 Stunden** → frühe Erstmeldung
- **spätestens 72 Stunden** → aktualisierte/qualifizierte Meldung
- weitere Zwischen-/Abschlussinformationen nach Gesetz

### Prüfungsfalle

> Die 24-/72-Stunden-Fristen des BSIG sind nicht mit der DSGVO-72-Stunden-Regel gleichzusetzen.

Unterschiedliche Meldepflichten können parallel bestehen.

---

# 36. Registrierung

§ 33 BSIG:

wichtige/besonders wichtige Einrichtungen müssen sich grundsätzlich innerhalb einer gesetzlichen Frist beim BSI registrieren.

---

# 37. Geschäftsleitung nach § 38 BSIG

Geschäftsleitungen müssen:

- Risikomanagementmaßnahmen umsetzen
- Umsetzung überwachen
- regelmäßig Schulungen besuchen

Bei Pflichtverletzung können Haftungsfolgen bestehen.

---

# 38. KRITIS

Betreiber kritischer Anlagen unterliegen zusätzlichen Anforderungen.

### Wichtig

> „KRITIS“ und „wichtige/besonders wichtige Einrichtung“ sind nicht vollständig identische Kategorien.

---

# 39. DORA

**Digital Operational Resilience Act – Verordnung (EU) 2022/2554**

Gilt seit:

> **17. Januar 2025**

für erfasste Finanzunternehmen.

---

# 40. DORA-Kernbereiche

- IKT-Risikomanagement
- IKT-Vorfallsmeldung
- Resilienztests
- Drittparteienrisiko
- Informationsaustausch
- Governance

---

# 41. DORA und Drittanbieter

Finanzunternehmen müssen IKT-Drittparteienrisiken über den gesamten Lebenszyklus steuern.

Vor Vertragsabschluss:

- Risikobewertung
- Due Diligence
- Abhängigkeit
- Konzentrationsrisiko

---

# 42. DORA-Informationsregister

Art. 28 Abs. 3 DORA verpflichtet erfasste Finanzunternehmen zur Führung eines Informationsregisters über Verträge mit IKT-Drittdienstleistern.

---

# 43. BAIT im DORA-Zeitalter

Historische Präsentationen nennen häufig BAIT.

Stand 2026:

- Für viele Institute, die seit 17.1.2025 DORA anwenden, gelten BAIT-Anforderungen nicht mehr.
- Für bestimmte Nicht-CRR-Institute bestehen Übergangs-/Sonderregelungen bis Ende 2026; ab 2027 greifen weitere DORA-Anwendungen.

### Prüfungsfalle

> BAIT 2026 nicht pauschal als zentrale aktuelle IT-Regulierung aller Banken darstellen.

---

# 44. AI Act

**Verordnung (EU) 2024/1689**

Grundsätzlicher Geltungsbeginn:

> **2. August 2026**

Einzelne Regelungen gelten bereits seit 2025, andere erst später.

IT-Compliance muss bei KI-Projekten daher Rollen und Übergangsfristen genau prüfen.

---

# 45. AI Act – Compliance-Dimensionen

Je nach Rolle/Risikoklasse:

- verbotene Praktiken
- AI Literacy
- Transparenz
- GPAI-Anforderungen
- High-Risk-Anforderungen
- technische Dokumentation
- Logging
- Human Oversight
- Risikomanagement

---

# 46. Data Act

**Verordnung (EU) 2023/2854**

Gilt weitgehend seit:

> **12. September 2025**

Relevanz:

- Zugang zu Daten vernetzter Produkte
- Datenweitergabe
- Cloud-/Data-Processing-Switching
- Vertragsbedingungen

---

# 47. Cloud-Compliance

Prüfen:

- DSGVO
- Drittstaaten
- Auftragsverarbeitung
- Datenresidenz
- Verschlüsselung
- Unterauftragnehmer
- Audit
- Exit
- Portabilität
- NIS2
- DORA, soweit Finanzsektor

---

# 48. Drittlandübermittlung

Bei personenbezogenen Daten außerhalb EWR:

- Angemessenheitsbeschluss oder
- geeignete Garantien, z. B. SCC
- zusätzliche Maßnahmen je Risikolage

müssen geprüft werden.

---

# 49. Outsourcing

Outsourcing erfordert:

- Due Diligence
- Vertrag
- SLA
- Security
- Audit
- Exit
- Subunternehmer
- BCM
- Datenschutz

### Merksatz

> **Die Durchführung kann ausgelagert werden, die Steuerungsverantwortung häufig nicht.**

---

# 50. Audit-Rechte

Verträge sollten ggf. ermöglichen:

- Nachweise
- Zertifikate
- Prüfberichte
- Vor-Ort-/Remote-Audits
- Behördenzugriff
- Subunternehmerkontrolle

---

# 51. Standards

Mögliche Referenzen:

- ISO/IEC 27001
- ISO/IEC 27002
- BSI IT-Grundschutz
- ISO 22301
- ISO 37301

Sie können:

- Anforderungen konkretisieren
- Vertragspflichten werden
- als Nachweis dienen

ersetzen aber keine Prüfung des geltenden Rechts.

---

# 52. Nachweisführung

IT-Compliance muss dokumentiert werden.

Beispiele:

- Policies
- Kontrollen
- Logs
- Tickets
- Freigaben
- Risikoanalysen
- Schulungen
- Auditberichte
- Restore-Tests
- Lieferantenprüfungen

---

# 53. Kontrolltypen

## Präventiv

- MFA
- Freigabeprozess
- Firewall

## Detektiv

- SIEM
- Audit
- Monitoring

## Korrektiv

- Incident Response
- Restore
- Patch

---

# 54. Continuous Compliance

Automatisierbare Kontrollen:

- Konfigurationsprüfung
- Cloud Policies
- Vulnerability Scans
- IaC-Checks
- Berechtigungsreview
- Zertifikatsablauf
- Log-Alarmierung

---

# 55. Sanktionen

Mögliche Folgen von Non-Compliance:

- Bußgelder
- Schadensersatz
- Aufsichtsmaßnahmen
- Vertragsstrafen
- Kündigung
- Ausschluss
- Organhaftung
- Reputationsschaden
- Versicherungsauswirkungen

---

# 56. Datenschutzbußgelder

DSGVO sieht abhängig vom Verstoß Bußgeldrahmen bis zu:

- 10 Mio. € bzw. 2 % weltweiter Jahresumsatz oder
- 20 Mio. € bzw. 4 %

vor, jeweils nach den gesetzlichen Voraussetzungen.

---

# 57. IT-Compliance und Versicherung

Cyberversicherungen enthalten:

- Obliegenheiten
- Sicherheitsanforderungen
- Meldepflichten

Fehler können Deckungsfragen auslösen.

---

# 58. Adressaten

IT-Compliance betrifft:

- Geschäftsleitung
- CIO
- CISO
- Datenschutz
- Compliance
- IT-Betrieb
- Entwickler
- Fachbereiche
- Lieferanten
- Aufsichtsorgane

---

# 59. Verantwortungsmatrix

Beispiel:

| Thema | Owner |
|---|---|
| DSGVO | DPO/Fachbereich |
| ISMS | CISO |
| Lizenz | IT Asset Management |
| GoBD | Finance/IT |
| NIS2 | Leitung/CISO |
| DORA | reguliertes Unternehmen |
| Arbeitsrecht | HR/Legal |

---

# 60. IT-Compliance-Prozess

```text
Rechtsmonitoring
      ↓
Betroffenheit
      ↓
Requirement
      ↓
Control
      ↓
Owner
      ↓
Evidence
      ↓
Monitoring
      ↓
Audit
      ↓
Remediation
```

---

# 61. IT-Compliance-Matrix

| Requirement | Control | Evidence |
|---|---|---|
| Art. 32 DSGVO | Verschlüsselung | Config Report |
| § 87 BetrVG | Betriebsvereinbarung | Freigabe |
| GoBD | Unveränderbarkeit | Audit Log |
| BSIG § 30 | Risk Controls | Risikoanalyse |
| DORA | Drittparteienkontrolle | Register |

---

# 62. Typische IHK-Prüfungsfrage

## „Nennen Sie rechtliche Anforderungen an IT-Systeme.“

Mögliche Antworten:

- DSGVO/BDSG
- BetrVG
- HGB/AO/GoBD
- BSIG
- Urheberrecht/Lizenzen
- sektorspezifische Regulierung

---

# 63. Typische IHK-Prüfungsfrage

## „Wie gewährleisten Sie IT-Compliance?“

> Zunächst werden geltende Verpflichtungen identifiziert und auf die IT-Systeme abgebildet. Anschließend werden Verantwortlichkeiten und Kontrollen definiert, technisch und organisatorisch umgesetzt, dokumentiert und regelmäßig überwacht. Änderungen der Rechtslage werden über Rechtsmonitoring aufgenommen und in einen kontinuierlichen Verbesserungsprozess überführt.

---

# 64. Typische Prüfungsfallen

- § 9 BDSG + Anlage → historisch
- § 11 BDSG AV → historisch; heute Art. 28 DSGVO
- GoBS/GDPdU → durch GoBD ersetzt
- PDF = ab 2025 nicht automatisch E-Rechnung
- NIS2 = in Deutschland 2026 über neues BSIG umgesetzt
- DSGVO 72 h ≠ BSIG 24/72 h
- DORA gilt bereits seit 17.1.2025
- BAIT nicht pauschal für alle DORA-Institute weiter anwenden
- ISO 27001 = keine automatische gesetzliche Compliance
- Outsourcing = keine vollständige Verantwortungsübertragung
- Zertifikat = kein Beweis vollständiger Compliance
- AI Act = gestaffelte Anwendung, nicht alles seit einem einzigen Datum

---

# ⚡ 60-Sekunden-Schnellcheck

- IT-Compliance = regelkonforme IT + Compliance durch IT
- DSGVO Art. 28 = AV
- Art. 32 = Sicherheit
- Art. 33 = 72 h
- Art. 35 = DSFA
- § 26 BDSG = Beschäftigte
- § 38 BDSG = DSB nationale Ergänzung
- § 87 BetrVG = Mitbestimmung
- TDDDG § 25 = Endeinrichtungen
- HGB/AO = Aufbewahrung
- GoBD = digitaler Buchführungsrahmen
- E-Rechnung seit 2025
- HinSchG = Meldestellen
- § 130 OWiG = Aufsicht
- BSIG 2025 = NIS2-Umsetzung
- § 30 BSIG = Risikomanagement
- § 32 BSIG = 24/72 h Meldung
- § 38 BSIG = Geschäftsleitung
- DORA seit 17.1.2025
- AI Act grundsätzlich seit 2.8.2026
- Data Act seit 12.9.2025
- Evidence = Compliance nachweisen
- Outsourcing ≠ Verantwortung los

---

# Quellen

- DSGVO (EU) 2016/679
- Bundesdatenschutzgesetz (BDSG)
- Betriebsverfassungsgesetz (BetrVG)
- TDDDG
- Handelsgesetzbuch (HGB)
- Abgabenordnung (AO)
- BMF-GoBD, zuletzt geändert 2025
- BSI-Gesetz (BSIG 2025)
- Verordnung (EU) 2022/2554 (DORA)
- Verordnung (EU) 2024/1689 (AI Act)
- Verordnung (EU) 2023/2854 (Data Act)
- Strafgesetzbuch (StGB)
- GeschGehG
