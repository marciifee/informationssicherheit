# Lernblatt / Handout: Rechtliche Aspekte in IT-Projekten und IT-Verträgen

### Kompaktes Nachschlagewerk für die IHK-Prüfung „Geprüfter Berufsspezialist für Informationssicherheit“

**Stand: 31. August 2026**  
**Schwerpunkt:** deutsches IT-Vertragsrecht, Software- und Cloudverträge, Datenschutz, Haftung, Urheberrecht und Informationssicherheit

> **Hinweis:** Dieses Handout dient der Weiterbildung und Prüfungsvorbereitung. Es ersetzt keine Rechtsberatung im Einzelfall.

---

# ⚡ Schnellcheck vor der Prüfung

- **Entscheidend ist nicht der Vertragsname, sondern die geschuldete Leistung.**
- **Kaufvertrag (§ 433 BGB)** → Sache/Recht wird dauerhaft übertragen; Verkäufer schuldet mangelfreie Leistung.
- **Dienstvertrag (§ 611 BGB)** → Tätigkeit wird geschuldet, nicht zwingend ein bestimmter Erfolg.
- **Werkvertrag (§ 631 BGB)** → bestimmter Erfolg wird geschuldet; Abnahme ist zentral.
- **Mietvertrag (§ 535 BGB)** → zeitlich begrenzte Gebrauchsüberlassung.
- **Softwarevertrag** ist kein eigenständiger gesetzlicher Vertragstyp.
- **Individualsoftware** ist häufig werkvertraglich geprägt, wenn ein konkreter Erfolg geschuldet wird.
- **SaaS/Cloud** ist meist ein typengemischter Vertrag; je nach Leistungsbild können Miet-, Dienst-, Werk- und weitere Elemente zusammentreffen.
- **SLA** konkretisiert messbare Servicequalität, z. B. Verfügbarkeit, Reaktions- und Wiederherstellungszeiten.
- **AV-Vertrag** nach Art. 28 DSGVO, wenn personenbezogene Daten im Auftrag verarbeitet werden.
- **Abnahme (§ 640 BGB)** → besonders wichtig beim Werkvertrag.
- **Mängelrechte beim Werkvertrag (§ 634 BGB)** → Nacherfüllung, Selbstvornahme, Rücktritt/Minderung, Schadensersatz.
- **Verzug (§ 286 BGB)** → Voraussetzung für viele Verzögerungsschäden.
- **AGB** unterliegen Inhaltskontrolle; auch im B2B-Bereich gilt insbesondere § 307 BGB.
- **Software ist urheberrechtlich geschützt** (§§ 69a ff. UrhG).
- **Sicherungskopie** kann unter den Voraussetzungen des § 69d Abs. 2 UrhG zulässig sein.
- **Geschäftsgeheimnisse** benötigen angemessene Geheimhaltungsmaßnahmen, damit Schutz nach GeschGehG greift.
- **IT-Verträge müssen Exit, Datenrückgabe und Löschung regeln.**
- **Cloud-Outsourcing verlagert Verantwortung, beseitigt sie aber nicht.**

---

# 1. Warum rechtliche Aspekte in IT-Projekten wichtig sind

IT-Projekte verbinden Technik mit rechtlichen Verpflichtungen. Fehlerhafte Vertragsgestaltung kann zu:

- Nachforderungen,
- Verzögerungen,
- Haftung,
- Lizenzverstößen,
- Datenschutzverletzungen,
- Sicherheitsrisiken,
- Vendor Lock-in,
- Streit über Abnahme und Vergütung

führen.

Für die Informationssicherheit ist entscheidend, dass Sicherheitsanforderungen **vertraglich konkretisiert** werden.

Beispiele:

- Patchfristen
- Meldefristen für Sicherheitsvorfälle
- Backup-/Restore-Anforderungen
- Verschlüsselung
- MFA
- Berechtigungsmanagement
- Audit- und Kontrollrechte
- Datenstandort
- Subunternehmer
- Exit und Löschung

---

# 2. Vertragsfreiheit und Vertragsauslegung

Grundsätzlich können Parteien Verträge frei gestalten, soweit zwingendes Recht nicht entgegensteht.

Ein IT-Vertrag kann Elemente mehrerer gesetzlicher Vertragstypen enthalten.

### Merksatz

> **Nicht die Überschrift „Lizenzvertrag“, „Cloudvertrag“ oder „IT-Projektvertrag“ entscheidet über die Rechtsfolgen, sondern der tatsächliche Vertragsinhalt.**

Daher muss geprüft werden:

```text
Welche Leistung?
      ↓
Welcher Erfolg geschuldet?
      ↓
Dauerhafte oder zeitweise Überlassung?
      ↓
Welche Mitwirkungspflichten?
      ↓
Welche Rechtsfolgen bei Mängeln?
```

---

# 3. Kaufvertrag

## Rechtsgrundlage

**§ 433 BGB**

Der Verkäufer schuldet insbesondere:

- Übergabe,
- Eigentumsverschaffung bei Sachen,
- Freiheit von Sach- und Rechtsmängeln.

Der Käufer schuldet:

- Kaufpreis,
- Abnahme der Kaufsache.

## Typische IT-Beispiele

- Serverhardware
- Netzwerkkomponenten
- Datenträger
- dauerhafte Überlassung bestimmter Standardsoftware kann kaufrechtlich geprägt sein

Bei Rechten und sonstigen Gegenständen ist zusätzlich **§ 453 BGB** wichtig.

---

# 4. Dienstvertrag

## Rechtsgrundlage

**§ 611 BGB**

Beim Dienstvertrag wird die **Tätigkeit** geschuldet.

Ein bestimmter wirtschaftlicher oder technischer Erfolg ist nicht automatisch geschuldet.

## IT-Beispiele

- Beratung
- Schulungen
- laufende Betriebsunterstützung
- Unterstützungsleistungen
- teilweise Softwarepflege

### Prüfungsmerksatz

> **Dienstvertrag = Tätigwerden geschuldet.**

---

# 5. Werkvertrag

## Rechtsgrundlage

**§ 631 BGB**

Beim Werkvertrag schuldet der Auftragnehmer einen **bestimmten Erfolg**.

## Typische IT-Beispiele

- Entwicklung einer konkret spezifizierten Individualsoftware
- Implementierung einer vereinbarten Schnittstelle
- Migration mit definiertem Abnahmeergebnis
- Erstellung eines technisch festgelegten Systems

### Prüfungsmerksatz

> **Werkvertrag = Erfolg geschuldet.**

---

# 6. Kauf-, Dienst- und Werkvertrag vergleichen

| Merkmal | Kauf | Dienst | Werk |
|---|---|---|---|
| Hauptpflicht | Übergabe/Übertragung | Tätigkeit | Erfolg |
| Abnahme zentral? | Abnahme der Kaufsache, aber andere Funktion | nein | **ja** |
| Erfolg geschuldet? | mangelfreier Kaufgegenstand | grundsätzlich nein | **ja** |
| Typisches IT-Beispiel | Hardware | Beratung | Individualsoftware |
| Mängelrecht | §§ 437 ff. BGB | Pflichtverletzungsrecht | §§ 634 ff. BGB |

---

# 7. Mietvertrag und zeitweise Softwareüberlassung

## Rechtsgrundlage

**§ 535 BGB**

Beim Mietvertrag wird der Gebrauch einer Sache für eine bestimmte Zeit gegen Entgelt gewährt.

Bei **zeitlich begrenzter Softwareüberlassung** können mietrechtliche Elemente einschlägig sein.

Typische Beispiele:

- zeitlich befristete On-Prem-Lizenz
- Hosting-/SaaS-Modelle mit dauernder Nutzbarkeit während der Vertragslaufzeit

### Wichtig

> SaaS ist nicht automatisch ausschließlich Dienstvertrag.

Die rechtliche Einordnung hängt von der konkreten Hauptleistung ab.

---

# 8. Typengemischte IT-Verträge

Viele IT-Verträge enthalten verschiedene Elemente.

Beispiel:

```text
Cloudprojekt
├── Softwareüberlassung
├── Hosting
├── Support
├── Datenmigration
├── Customizing
└── Schulung
```

Daraus können unterschiedliche Rechtsfolgen entstehen.

Deshalb sollten Leistungsbestandteile sauber getrennt beschrieben werden.

---

# 9. Standardsoftware

Bei Standardsoftware sind insbesondere zu regeln:

- Lizenzmodell
- Anzahl Nutzer
- Geräte/CPU/Cores
- Nutzungsdauer
- geografischer Umfang
- Konzernnutzung
- Virtualisierung
- Test-/Entwicklungsinstanzen
- Backupkopien
- Updates/Upgrades
- Audit-/Vermessungsrechte
- Kündigung
- Übertragbarkeit

### Prüfungsfalle

> **„Jeder Softwarelizenzvertrag ist automatisch ein Kaufvertrag“ ist zu pauschal.**

Dauerhafte Überlassung kann kaufrechtlich geprägt sein; zeitweise Überlassung kann mietrechtlich geprägt sein.

---

# 10. Individualsoftware

Bei Individualsoftware sollten Anforderungen möglichst messbar beschrieben werden.

Beispiele:

- Lastenheft
- Pflichtenheft
- User Stories
- Akzeptanzkriterien
- Schnittstellen
- Performancewerte
- Sicherheitsanforderungen

### Wichtig

Unklare Anforderungen führen häufig zu:

- Scope Creep,
- Change Requests,
- Claims,
- Abnahmestreitigkeiten.

---

# 11. Abnahme beim Werkvertrag

## § 640 BGB

Der Besteller muss ein vertragsgemäß hergestelltes Werk grundsätzlich abnehmen.

Wegen **unwesentlicher Mängel** kann die Abnahme nicht verweigert werden.

Abnahme kann erfolgen durch:

- ausdrückliche Erklärung,
- Abnahmeprotokoll,
- unter Voraussetzungen auch fingierte Abnahme.

### Rechtsfolgen

Abnahme ist regelmäßig wichtig für:

- Fälligkeit der Werkvergütung,
- Beginn bestimmter Mängelverjährungsfristen,
- Beweislastfragen,
- Gefahrtragung.

---

# 12. Abnahmeprotokoll

Ein Abnahmeprotokoll sollte enthalten:

- Projekt/Vertrag
- Abnahmegegenstand
- Datum
- Teilnehmer
- Testgrundlage
- Abnahmekriterien
- festgestellte Mängel
- Klassifizierung der Mängel
- offene Restarbeiten
- Vorbehalte
- Fristen
- Unterschriften/Freigaben

### Merksatz

> **Was nicht sauber dokumentiert ist, lässt sich später schwer beweisen.**

---

# 13. Mängelrechte beim Werkvertrag

Nach **§ 634 BGB** kommen insbesondere in Betracht:

1. Nacherfüllung
2. Selbstvornahme und Aufwendungsersatz
3. Rücktritt oder Minderung
4. Schadensersatz bzw. Ersatz vergeblicher Aufwendungen

Bei Nacherfüllung ist **§ 635 BGB** zentral.

### Begriffskorrektur

> Der alte Begriff **„Wandelung“** wird im heutigen BGB regelmäßig durch **Rücktritt** ersetzt.

---

# 14. Verjährung von Mängelansprüchen

Fristen hängen vom Vertragstyp und Gegenstand ab.

Beim Werkvertrag regelt **§ 634a BGB** unterschiedliche Fristen.

Bei Kaufverträgen ist **§ 438 BGB** relevant.

### Prüfungsfalle

> **„Die Gewährleistung beträgt bei Software generell sechs Monate“ ist falsch.**

Im B2B-Bereich können Verträge Fristen verändern, jedoch bestehen Grenzen, insbesondere durch AGB-Recht.

---

# 15. Verzug

## § 286 BGB

Verzug kann insbesondere eintreten, wenn:

- eine fällige Leistung trotz Mahnung nicht erbracht wird,
- ein kalendermäßig bestimmter Termin verstreicht,
- Leistung endgültig verweigert wird.

Mögliche Folgen:

- Verzögerungsschaden
- Verzugszinsen
- weitere vertragliche Ansprüche

Bei Schadensersatz wegen Pflichtverletzung ist **§ 280 BGB** wichtig.

---

# 16. Zahlungsverzug

Bei Entgeltforderungen zwischen Unternehmen gelten nach **§ 288 Abs. 2 BGB** grundsätzlich Verzugszinsen von:

> **9 Prozentpunkten über dem Basiszinssatz**

Zusätzlich kann unter Voraussetzungen eine **40-Euro-Verzugspauschale** nach § 288 Abs. 5 BGB entstehen.

---

# 17. Vertragsstrafe

## §§ 339 ff. BGB

Eine Vertragsstrafe kann vereinbart werden, z. B. für:

- Terminüberschreitungen,
- Verstöße gegen bestimmte Pflichten.

### Prüfungsfalle

> Vertragsstrafen sind nach dem gesetzlichen Grundmodell **nicht pauschal immer verschuldensunabhängig**.

§ 339 BGB knüpft bei Nichterfüllung/nicht gehöriger Erfüllung grundsätzlich an Verzug an. Die konkrete Vertragsregelung ist entscheidend.

---

# 18. Mitwirkungspflichten des Auftraggebers

IT-Projekte scheitern nicht nur am Auftragnehmer.

Mitwirkung kann erforderlich sein bei:

- Anforderungen
- Testdaten
- Zugang zu Systemen
- Ansprechpartnern
- Freigaben
- Entscheidungen
- Infrastruktur

Bei Werkverträgen kann **§ 642 BGB** bei unterlassener erforderlicher Mitwirkung eine Entschädigung des Unternehmers begründen.

---

# 19. Allgemeine Geschäftsbedingungen – AGB

## § 305 BGB

AGB sind vorformulierte Vertragsbedingungen für eine Vielzahl von Verträgen.

Im IT-Bereich regeln sie häufig:

- Leistungsumfang
- Haftung
- Gewährleistung
- Nutzungsrechte
- Vertragsdauer
- Kündigung
- Zahlungsbedingungen

---

# 20. AGB-Kontrolle

## § 307 BGB

AGB-Klauseln können unwirksam sein, wenn sie den Vertragspartner unangemessen benachteiligen.

Auch im B2B-Bereich ist § 307 BGB relevant; § 310 BGB enthält besondere Regeln für Unternehmer.

Besonders kritisch:

- unangemessen weitgehende Haftungsausschlüsse
- unklare Leistungsbeschreibungen
- einseitige Änderungsrechte
- problematische Abnahmeklauseln
- überraschende Preisanpassungen
- unklare Laufzeiten

---

# 21. Haftung

Haftung kann entstehen aus:

- Vertrag
- Delikt
- Datenschutzrecht
- Produkthaftung
- Gesellschaftsrecht
- spezialgesetzlichen Pflichten

Im Vertrag sollten geregelt sein:

- Haftungsumfang
- Haftungshöchstgrenzen
- indirekte Schäden
- Datenverlust
- Wiederherstellungskosten
- Vorsatz/grobe Fahrlässigkeit
- Personenschäden
- Verletzung von Schutzrechten
- Datenschutzverletzungen

### Wichtig

Haftungsbeschränkungen können nicht beliebig formuliert werden.

---

# 22. Service Level Agreements – SLA

Ein SLA beschreibt messbare Servicequalität.

Typische Kennzahlen:

- Verfügbarkeit
- Reaktionszeit
- Wiederherstellungszeit
- Supportzeit
- Lösungszeit
- Wartungsfenster
- Performance
- Backup/Restore

---

# 23. SLA-Verfügbarkeit

Beispiel:

```text
Verfügbarkeit = 99,9 % pro Monat
```

Der Vertrag muss zusätzlich beantworten:

- Was ist „verfügbar“?
- Welche Messstelle zählt?
- Welche Wartungsfenster sind ausgenommen?
- Welche Ausfälle sind ausgeschlossen?
- Welche Kompensation erfolgt?
- Gibt es ein Sonderkündigungsrecht?

### Prüfungsfalle

> Eine hohe Prozentzahl ohne Messmethode ist kein gutes SLA.

---

# 24. Cloud- und SaaS-Verträge

Cloudverträge sollten insbesondere regeln:

- Leistungsgegenstand
- Service Level
- Datenstandort
- Datenschutz
- Auftragsverarbeitung
- Unterauftragnehmer
- Informationssicherheit
- Incident Notification
- Backup
- Portabilität
- Exportformate
- Exit
- Löschung
- Audit
- Haftung
- Laufzeit/Kündigung

---

# 25. Shared Responsibility

Auch bei Cloud-Diensten verbleiben Pflichten beim Kunden.

Beispiel:

```text
Provider:
physische Infrastruktur / Plattformanteile

Kunde:
Daten
Identitäten
Berechtigungen
Konfiguration
fachliche Compliance
```

Der genaue Umfang hängt von IaaS, PaaS und SaaS ab.

---

# 26. Exit-Management und Vendor Lock-in

Bereits beim Vertragsabschluss sollte geregelt werden:

- Datenexport
- Format
- Frist
- Kosten
- Unterstützung bei Migration
- Restdatenlöschung
- Bestätigung der Löschung
- Übergabe von Dokumentationen
- Schlüssel/Zertifikate
- Übergangsservices

### Merksatz

> **Der Exit wird beim Eintritt geplant.**

---

# 27. Datenschutz – DSGVO

Sobald personenbezogene Daten verarbeitet werden, müssen insbesondere geklärt werden:

- Verantwortlicher
- Auftragsverarbeiter
- Rechtsgrundlage
- Zweck
- Datenminimierung
- Speicherfristen
- TOM
- Betroffenenrechte
- Drittlandübermittlung
- Meldepflichten

---

# 28. Auftragsverarbeitung – Art. 28 DSGVO

Wenn ein Dienstleister personenbezogene Daten **im Auftrag** verarbeitet, muss ein Vertrag bzw. Rechtsinstrument nach Art. 28 DSGVO bestehen.

Wichtige Inhalte:

- Gegenstand und Dauer
- Art und Zweck
- Datenarten
- Betroffenengruppen
- Weisungsbindung
- Vertraulichkeit
- TOM
- Unterauftragsverarbeiter
- Unterstützung bei Betroffenenrechten
- Löschung/Rückgabe
- Nachweise/Audits

---

# 29. Sicherheit der Verarbeitung – Art. 32 DSGVO

Art. 32 DSGVO verlangt risikoadäquate technische und organisatorische Maßnahmen.

Beispiele:

- Pseudonymisierung
- Verschlüsselung
- Vertraulichkeit
- Integrität
- Verfügbarkeit
- Resilienz
- Wiederherstellbarkeit
- regelmäßige Wirksamkeitsprüfung

---

# 30. Datenschutzvorfall

Nach Art. 33 DSGVO muss eine meldepflichtige Datenschutzverletzung grundsätzlich:

> **unverzüglich und möglichst binnen 72 Stunden nach Kenntnis**

an die zuständige Aufsichtsbehörde gemeldet werden.

Bei hohem Risiko kann zusätzlich Art. 34 DSGVO die Benachrichtigung betroffener Personen verlangen.

---

# 31. Datenschutz-Folgenabschätzung – DSFA

Nach Art. 35 DSGVO ist eine DSFA erforderlich, wenn eine Verarbeitung voraussichtlich ein **hohes Risiko** für Rechte und Freiheiten natürlicher Personen verursacht.

Beispiele können sein:

- umfangreiche sensible Daten
- systematische Überwachung
- neue risikoreiche Technologien

---

# 32. Beschäftigtendatenschutz

Für Beschäftigtendaten ist in Deutschland insbesondere **§ 26 BDSG** relevant.

Zusätzlich können Mitbestimmungsrechte des Betriebsrats bestehen.

---

# 33. Betriebsrat und IT-Systeme

## § 87 Abs. 1 Nr. 6 BetrVG

Der Betriebsrat hat ein Mitbestimmungsrecht bei Einführung und Anwendung technischer Einrichtungen, die dazu bestimmt sind, Verhalten oder Leistung von Arbeitnehmern zu überwachen.

Praktische Beispiele:

- Monitoring
- Zeiterfassung
- DLP
- Callcenter-Analytics
- E-Mail-/Internetkontrolle
- Endpoint Monitoring

---

# 34. Urheberrecht an Software

Computerprogramme sind nach **§ 69a UrhG** geschützt.

Geschützt ist die Ausdrucksform eines Programms, nicht jede zugrunde liegende Idee oder jedes Prinzip.

---

# 35. Nutzungsrechte

Ein Lizenzvertrag sollte festlegen:

- einfach/ausschließlich
- zeitlich
- räumlich
- sachlich
- Benutzerzahl
- Vervielfältigung
- Bearbeitung
- Weitergabe
- Unterlizenz
- Virtualisierung

---

# 36. Sicherungskopie

Nach **§ 69d Abs. 2 UrhG** darf die Erstellung einer Sicherungskopie durch eine zur Nutzung berechtigte Person nicht vertraglich untersagt werden, wenn sie für die Sicherung künftiger Benutzung erforderlich ist.

---

# 37. Dekompilierung und Interoperabilität

**§ 69e UrhG** erlaubt unter engen Voraussetzungen Dekompilierung, soweit sie unerlässlich ist, um Informationen zur Herstellung der Interoperabilität eines unabhängig geschaffenen Programms zu erhalten.

### Wichtig

> Das ist keine allgemeine Erlaubnis zum Reverse Engineering beliebiger Software.

---

# 38. Open-Source-Software

Open Source bedeutet nicht „rechtsfrei“.

Zu prüfen sind:

- Lizenztyp
- Copyright-Hinweise
- Notice-Pflichten
- Source-Code-Pflichten
- Copyleft
- Weitergabe
- Lizenzkompatibilität

Beispiele:

- MIT
- Apache-2.0
- BSD
- GPL
- LGPL
- AGPL

---

# 39. Geschäftsgeheimnisse

Das **Geschäftsgeheimnisgesetz (GeschGehG)** schützt Informationen nur, wenn unter anderem angemessene Geheimhaltungsmaßnahmen getroffen werden.

Maßnahmen:

- NDA
- Rollen/Berechtigungen
- Klassifizierung
- Verschlüsselung
- Logging
- Need-to-know
- technische Zugriffsbeschränkung

### Prüfungsmerksatz

> **Ein Geheimnis ohne angemessene Schutzmaßnahmen kann seinen gesetzlichen Geschäftsgeheimnisschutz verlieren.**

---

# 40. Geheimhaltungsvereinbarung – NDA

Ein NDA sollte regeln:

- Definition vertraulicher Informationen
- zulässige Nutzung
- Empfängerkreis
- Schutzmaßnahmen
- Ausnahmen
- Dauer
- Rückgabe/Löschung
- Rechtsfolgen

---

# 41. IT-Sicherheitsklauseln im Vertrag

Beispiele:

- Mindeststandards
- ISO-27001-/BSI-Bezug
- Schwachstellenmanagement
- Patchfristen
- Penetrationstests
- Logging
- MFA
- Verschlüsselung
- Incident Response
- Meldefristen
- Forensik-Unterstützung
- Audit
- Business Continuity

---

# 42. Subunternehmer und Lieferkette

Zu klären:

- Genehmigungspflicht
- Transparenz
- Sicherheitsanforderungen
- Datenschutz
- Standort
- Audit
- Haftung
- Wechsel von Subunternehmern

### Merksatz

> **Outsourcing ist keine Auslagerung der eigenen Verantwortung.**

---

# 43. Öffentliche Beschaffung und EVB-IT

Bei IT-Beschaffung der öffentlichen Hand spielen die **EVB-IT** (Ergänzende Vertragsbedingungen für die Beschaffung von IT-Leistungen) eine wichtige Rolle.

Je nach Leistungsgegenstand existieren unterschiedliche Vertragstypen.

Für Prüfungen reicht meist:

> EVB-IT standardisieren Vertragsbedingungen für IT-Beschaffungen der öffentlichen Hand.

---

# 44. IT-Strafrecht – Beispiele

Relevante Tatbestände können sein:

- § 202a StGB – Ausspähen von Daten
- § 202b StGB – Abfangen von Daten
- § 202c StGB – Vorbereiten des Ausspähens/Abfangens
- § 303a StGB – Datenveränderung
- § 303b StGB – Computersabotage

### Wichtig

Penetrationstests benötigen eine eindeutige Autorisierung und einen festgelegten Scope.

---

# 45. Vertragsdokumente in IT-Projekten

Mögliche Dokumente:

```text
Rahmenvertrag
├── Leistungsbeschreibung
├── Preisblatt
├── SLA
├── Datenschutzvereinbarung
├── TOM
├── Sicherheitsanlage
├── Lizenzbedingungen
├── Change-Prozess
└── Exit-Plan
```

Widersprüche und Rangfolgen sollten geregelt werden.

---

# 46. Change Request

Ein Change Request ist zunächst ein Änderungswunsch.

Er sollte enthalten:

- Beschreibung
- Grund
- Auswirkungen
- Kosten
- Termin
- Risiko
- Security-/Compliance-Auswirkungen
- Freigabe

### Merksatz

> **Ein Change Request ist noch nicht automatisch ein durchsetzbarer Claim.**

---

# 47. Typische Vertragsrisiken

- unklare Anforderungen
- fehlende Akzeptanzkriterien
- falscher Vertragstyp
- unklare Mitwirkung
- fehlende Security-Anforderungen
- unbegrenzte Subunternehmer
- fehlender Exit
- Vendor Lock-in
- unklare IP-Rechte
- unklare Datenhoheit
- unbestimmte SLA-Messung
- unangemessene Haftungsregelung

---

# 48. Typische IHK-Prüfungsfrage

## „Unterscheiden Sie Dienst- und Werkvertrag.“

> Beim Dienstvertrag wird die vereinbarte Tätigkeit geschuldet, ohne dass zwingend ein bestimmter Erfolg garantiert werden muss. Beim Werkvertrag schuldet der Auftragnehmer dagegen einen konkret vereinbarten Erfolg. Beim Werkvertrag spielt die Abnahme eine zentrale Rolle.

---

# 49. Typische IHK-Prüfungsfrage

## „Nennen Sie fünf Regelungen eines Cloudvertrags.“

Mögliche Punkte:

1. SLA/Verfügbarkeit
2. Datenschutz und AV-Vertrag
3. Informationssicherheit
4. Unterauftragnehmer
5. Datenstandort
6. Backup/Restore
7. Exit und Datenportabilität
8. Haftung

---

# 50. Typische Prüfungsfallen

- § 433 BGB ist Kaufvertrag – **nicht § 33 BGB**
- Lizenzvertrag ist **nicht immer Kaufvertrag**
- SaaS ist **nicht automatisch reiner Dienstvertrag**
- Gewährleistung bei Software beträgt **nicht generell sechs Monate**
- „Wandelung“ → heute regelmäßig **Rücktritt**
- Abnahme ist nicht zwingend ein körperlicher Vorgang
- SLA-Verfügbarkeit ohne Messdefinition ist unvollständig
- AV-Vertrag ersetzt keine Rechtsgrundlage der Verarbeitung
- ISO-Zertifikat ersetzt keine Vertragsprüfung
- Outsourcing beseitigt keine Verantwortlichkeit
- Penetrationstest ohne Autorisierung kann strafrechtlich relevant sein

---

# ⚡ 60-Sekunden-Schnellcheck

- Kauf → § 433 BGB
- Dienst → § 611 BGB
- Werk → § 631 BGB
- Abnahme → § 640 BGB
- Werkmängel → § 634 BGB
- Mitwirkung → § 642 BGB
- Verzug → § 286 BGB
- Schadensersatz → § 280 BGB
- Vertragsstrafe → §§ 339 ff. BGB
- AGB → §§ 305 ff. BGB
- AGB-Kontrolle → § 307 BGB
- Softwareurheberrecht → §§ 69a ff. UrhG
- Sicherungskopie → § 69d UrhG
- Dekompilierung → § 69e UrhG
- AV-Vertrag → Art. 28 DSGVO
- TOM → Art. 32 DSGVO
- Data Breach → Art. 33/34 DSGVO
- DSFA → Art. 35 DSGVO
- Betriebsrat → § 87 Abs. 1 Nr. 6 BetrVG
- Geschäftsgeheimnis → GeschGehG
- SaaS → Leistungsbild prüfen, oft typengemischt
- Exit → vor Vertragsschluss planen

---

# Quellen

- Bürgerliches Gesetzbuch (BGB), aktuelle Fassung
- Urheberrechtsgesetz (UrhG), insbesondere §§ 69a ff.
- Datenschutz-Grundverordnung (DSGVO)
- Bundesdatenschutzgesetz (BDSG)
- Betriebsverfassungsgesetz (BetrVG)
- Geschäftsgeheimnisgesetz (GeschGehG)
- Strafgesetzbuch (StGB)
- EVB-IT des Bundes
