# Lernblatt / Handout: Datenspeicherung & Datensicherung

### Kompaktes Nachschlagewerk für die IHK-Prüfung „Geprüfter Berufsspezialist für Informationssicherheit“

**Stand: 31. August 2026**  
**Grundlagen:** BSI IT-Grundschutz, BSI-Standard 200-2/200-4, DSGVO sowie Herstellerdokumentationen zu Cloud- und Speichertechnologien

---

# ⚡ Schnellcheck vor der Prüfung

## Grundbegriffe

- **Datenspeicherung** = Daten für die laufende Verarbeitung dauerhaft oder temporär ablegen
- **Datensicherung (Backup)** = zusätzliche Kopie zur Wiederherstellung nach Verlust oder Beschädigung
- **Archivierung** = langfristige, regelgebundene und häufig unveränderbare Aufbewahrung
- **Replikation** = Daten auf ein weiteres System kopieren, meist für Verfügbarkeit
- **Snapshot** = zeitpunktbezogener Zustand eines Systems oder Volumes
- **RAID** = erhöht je nach Level Verfügbarkeit und/oder Performance, ersetzt aber **kein Backup**
- **NAS** = dateibasierter Zugriff, typischerweise über SMB/NFS
- **SAN** = blockbasierter Zugriff, z. B. über Fibre Channel, iSCSI oder NVMe-oF
- **Object Storage** = objektbasierter Speicher mit Metadaten, typischerweise über HTTP-APIs
- **RPO** = maximal akzeptabler Datenverlust in Zeit
- **RTO** = Zielzeit für die Wiederaufnahme eines Dienstes bzw. einer BC-Lösung
- **MTPD/MTA** = maximal tolerierbare Ausfallzeit; nicht mit RTO verwechseln
- **3-2-1-Regel** = 3 Datenkopien, 2 unterschiedliche Speicherarten/-medien, 1 Kopie extern
- **Immutable/WORM** = Daten können innerhalb einer Aufbewahrungsfrist nicht verändert oder gelöscht werden
- **Air Gap** = logische oder physische Trennung vom Produktivsystem
- **Shared Responsibility** = Cloudanbieter und Kunde tragen unterschiedliche Sicherheitsverantwortung
- **Schutzbedarf nach BSI** = normal – hoch – sehr hoch
- **Availability Zone** = voneinander getrennte Ausfall-/Bereitstellungsdomäne innerhalb einer Cloud-Region
- **Verfügbarkeit ≠ Backup** → Replikation schützt nicht automatisch vor Löschung, Fehlkonfiguration oder Ransomware

## RAID schnell merken

| RAID | Mindestanzahl | Prinzip | Ausfalltoleranz |
|---|---:|---|---|
| **RAID 0** | 2 | Striping | keine |
| **RAID 1** | 2 | Mirroring | bei 2 Platten 1 |
| **RAID 5** | 3 | Striping + 1 Parität | 1 Platte |
| **RAID 6** | 4 | Striping + 2 Paritäten | 2 Platten |
| **RAID 10** | 4 | Mirroring + Striping | abhängig davon, welche Spiegel betroffen sind |

### Merksätze

> **RAID schützt die Verfügbarkeit – Backup schützt die Wiederherstellbarkeit.**

> **Snapshot ist nicht automatisch Backup.**

> **Replikation kopiert auch Fehler und Löschungen, wenn keine zusätzlichen Schutzmechanismen existieren.**

> **RPO = Wie viel Datenverlust ist tolerierbar?**

> **RTO = Wie schnell muss der Dienst wieder bereitstehen?**

---

# 1. Grundlagen der Datenspeicherung

Datenspeicherung umfasst technische und organisatorische Verfahren, mit denen Daten:

- erzeugt,
- gespeichert,
- verarbeitet,
- übertragen,
- gesichert,
- archiviert,
- wiederhergestellt und
- sicher gelöscht

werden.

Für die Informationssicherheit sind insbesondere die drei Grundwerte relevant:

- **Vertraulichkeit** → nur Berechtigte dürfen Daten lesen
- **Integrität** → Daten dürfen nicht unbemerkt oder unbefugt verändert werden
- **Verfügbarkeit** → Daten müssen bei Bedarf verfügbar sein

Je nach Anwendungsfall kommen weitere Ziele hinzu:

- Authentizität
- Nachvollziehbarkeit
- Nichtabstreitbarkeit
- Datenschutz
- Resilienz

## Wichtige Abgrenzungen

| Begriff | Zweck |
|---|---|
| **Primärspeicher** | produktive Verarbeitung |
| **Sekundärspeicher** | dauerhafte Speicherung |
| **Backup** | Wiederherstellung nach Datenverlust |
| **Replikation** | Verfügbarkeit und Redundanz |
| **Snapshot** | schneller Wiederherstellungspunkt |
| **Archiv** | langfristige Aufbewahrung |
| **Cache** | Beschleunigung von Zugriffen |

**Prüfungswichtig:**

> Eine Kopie auf einem zweiten produktiven System ist nicht automatisch ein Backup.

Wenn eine Fehlkonfiguration, Löschung oder Schadsoftware synchron repliziert wird, kann auch die Kopie betroffen sein.

---

# 2. Speichermedien

## Magnetische Speichermedien

### HDD – Hard Disk Drive

Eigenschaften:

- magnetische Speicherung
- hohe Kapazität
- günstiger Preis pro TB
- mechanische Bauteile
- höhere Zugriffszeiten als SSD
- geeignet für große Datenmengen, Backups und Kapazitätsspeicher

### Magnetband / Tape

Eigenschaften:

- sequenzieller Zugriff
- sehr hohe Kapazität
- niedrige Kosten pro TB
- besonders für Backup und Archivierung geeignet
- offline bzw. Air-Gap-fähig
- Zugriff langsamer als bei Festplatten oder SSDs

---

## Flash-Speicher

Beispiele:

- SSD
- NVMe-SSD
- USB-Flash
- Speicherkarten

Eigenschaften:

- keine beweglichen Teile
- niedrige Latenz
- hohe IOPS
- begrenzte Schreibzyklen
- je nach Speicherzellentyp unterschiedliche Lebensdauer und Performance

### SATA/SAS SSD vs. NVMe

**SATA/SAS** verwenden klassische Storage-Schnittstellen.

**NVMe** wurde speziell für nichtflüchtigen Flash-Speicher entwickelt und ermöglicht hohe Parallelität sowie geringe Latenzen.

---

## Optische Speichermedien

Beispiele:

- CD
- DVD
- Blu-ray

Vorteile:

- physisch transportierbar
- offline lagerbar
- teilweise WORM-ähnliche Eigenschaften

Nachteile:

- vergleichsweise geringe Kapazität
- langsamer Zugriff
- heute in Unternehmensumgebungen nur noch für spezielle Szenarien relevant

---

## In-Memory-Speicherung

Daten liegen überwiegend im Arbeitsspeicher.

Beispiele:

- Redis
- In-Memory-Datenbanken
- Caches

Vorteil:

> sehr niedrige Zugriffszeiten

Nachteil:

> RAM ist grundsätzlich flüchtig; Persistenz muss zusätzlich sichergestellt werden.

---

# 3. Zukunftstechnologien

## DNA-Speicherung

Bei DNA-Speicherung werden digitale Informationen in Basensequenzen wie:

```text
A – C – G – T
```

codiert.

Potenziale:

- extrem hohe Speicherdichte
- sehr lange theoretische Haltbarkeit

Aktuelle Einschränkungen:

- hohe Kosten
- langsames Schreiben und Lesen
- komplexe Verarbeitung

**Prüfungsrelevanz:** eher Zukunftstechnologie als produktiver Unternehmensspeicher.

## Quantenspeicher

Quantenspeicher dienen dem Erhalt von Quantenzuständen für Quantenkommunikation und Quantencomputing.

Sie sind **kein heutiger Ersatz für Massenspeicher wie SSD, HDD oder Tape**.

---

# 4. Speicherzugriffsmodelle: Block, File und Object

Diese drei Modelle gehören zu den wichtigsten Grundlagen moderner Datenspeicherung.

## Block Storage

Daten werden als adressierbare Blöcke bereitgestellt.

Typische Verwendung:

- Betriebssystem-Volumes
- Datenbanken
- Virtualisierung
- hochperformante Anwendungen

Beispiele:

- SAN-LUN
- iSCSI-Volume
- Cloud-Block-Volume

Vorteil:

> hohe Flexibilität und gute Performance.

---

## File Storage

Daten werden als Dateien und Verzeichnisse bereitgestellt.

Typische Protokolle:

- SMB
- NFS

Typische Verwendung:

- Netzlaufwerke
- Homeverzeichnisse
- Teamfreigaben
- Dateiablagen

NAS ist ein typischer Vertreter von File Storage.

---

## Object Storage

Daten werden als **Objekte** gespeichert.

Ein Objekt besteht typischerweise aus:

- Daten
- Metadaten
- eindeutiger Objekt-ID

Typische Verwendung:

- Cloud Storage
- Bilder und Videos
- Backups
- Data Lakes
- statische Webinhalte
- große unstrukturierte Datenmengen

Eigenschaften:

- sehr hohe Skalierbarkeit
- Zugriff häufig über HTTP-/REST-APIs
- kein klassisches hierarchisches Dateisystem erforderlich
- Lifecycle- und Retention-Regeln gut automatisierbar

### Schnellvergleich

| Merkmal | Block | File | Object |
|---|---|---|---|
| Zugriff | Block | Datei/Verzeichnis | Objekt/API |
| Beispiele | SAN, Cloud Volumes | NAS | S3-/Blob-artiger Storage |
| Protokolle | FC, iSCSI, NVMe-oF | SMB, NFS | HTTP/REST |
| Stärke | Performance/Flexibilität | Benutzerfreundliche Freigaben | Skalierbarkeit/Metadaten |

---

# 5. On-Premises-Speicherung

Bei **On-Premises** befinden sich Speicher und Infrastruktur im eigenen Verantwortungsbereich bzw. im eigenen Rechenzentrum.

## Vorteile

- hohe Kontrolle über Infrastruktur und Daten
- eigene Sicherheitsarchitektur
- lokale Zugriffe ohne öffentliche Internetverbindung möglich
- gut kalkulierbare lokale Latenzen
- individuelle Hardwareauswahl

## Nachteile

- Investitionskosten
- eigener Wartungs- und Personalaufwand
- begrenzte kurzfristige Skalierbarkeit
- Verantwortung für Redundanz und Ausfallsicherheit
- Verantwortung für physische Sicherheit
- eigenes Backup- und Disaster-Recovery-Konzept erforderlich

**Wichtig:**

> On-Premises ist nicht automatisch sicherer als Cloud und Cloud ist nicht automatisch sicherer als On-Premises.

Entscheidend sind Architektur, Konfiguration, Schutzbedarf, Prozesse und Betriebsqualität.

---

# 6. Network Attached Storage – NAS

Ein **Network Attached Storage (NAS)** stellt Speicher auf Dateiebene über ein Netzwerk bereit.

Typische Protokolle:

- SMB
- NFS

Typische Einsatzgebiete:

- Dateiablagen
- Teamfreigaben
- Homeverzeichnisse
- Backup-Ziele
- Multimedia
- kleinere Virtualisierungsumgebungen

## Sicherheitsmaßnahmen für NAS

- starke Authentisierung
- MFA, sofern unterstützt
- rollenbasierte Berechtigungen
- Least Privilege
- getrennte Administrationskonten
- regelmäßige Updates
- Deaktivieren unnötiger Dienste
- Netzwerksegmentierung
- sichere Protokolle
- Verschlüsselung
- Protokollierung und Monitoring
- Backup des NAS
- physischer Schutz

**Fernzugriff:**

Direktes Port-Forwarding auf Verwaltungsoberflächen sollte vermieden werden. Besser sind beispielsweise:

- VPN
- Zero-Trust-Zugänge
- abgesicherte Reverse-Proxies bzw. Access Gateways

---

# 7. RAID – Redundant Array of Independent Disks

RAID kombiniert mehrere Datenträger, um je nach RAID-Level:

- Performance,
- Verfügbarkeit,
- Ausfallsicherheit

zu erhöhen.

## RAID 0 – Striping

Daten werden über mehrere Laufwerke verteilt.

**Vorteile:**

- hohe Performance
- volle Nutzkapazität

**Nachteile:**

- keine Redundanz
- Ausfall eines Datenträgers zerstört den Verbund

Typischer Einsatz:

> temporäre oder leicht rekonstruierbare Daten mit hohem Performancebedarf.

---

## RAID 1 – Mirroring

Daten werden gespiegelt.

Bei zwei Laufwerken:

```text
Disk 1: A B C D
Disk 2: A B C D
```

Vorteile:

- einfacher Aufbau
- gute Leseleistung möglich
- Ausfall eines Laufwerks bei einem 2-Disk-Mirror tolerierbar

Nachteil:

- typischerweise nur etwa 50 % der Rohkapazität nutzbar

---

## RAID 5

RAID 5 verwendet:

- Striping
- verteilte Parität

Mindestanzahl:

> **3 Laufwerke**

Nutzkapazität bei gleich großen Laufwerken:

```text
(n - 1) × kleinste Laufwerkskapazität
```

Ausfalltoleranz:

> **1 Laufwerk**

Vorteile:

- gute Speichereffizienz
- gute Leseleistung

Nachteile:

- Schreibaufwand durch Paritätsberechnung
- Rebuild kann lange dauern
- während des Rebuilds erhöhtes Risiko

**Korrektur gegenüber den Ausgangsfolien:**

> RAID 5 ist nicht grundsätzlich „ungeeignet für SSDs“. Die Eignung hängt von Workload, Controller, SSD-Typ, Write-Endurance und gewünschter Ausfallsicherheit ab.

---

## RAID 6

RAID 6 verwendet doppelte verteilte Parität.

Mindestanzahl:

> **4 Laufwerke**

Nutzkapazität:

```text
(n - 2) × kleinste Laufwerkskapazität
```

Ausfalltoleranz:

> **2 Laufwerke**

Vorteil:

- höhere Ausfallsicherheit als RAID 5

Nachteil:

- zusätzlicher Schreib- und Paritätsaufwand

Typische Verwendung:

> größere Arrays mit höherem Verfügbarkeitsbedarf.

---

## RAID 10 – RAID 1+0

RAID 10 kombiniert:

1. Spiegelung
2. Striping

Mindestanzahl:

> **4 Laufwerke**

Typische Nutzkapazität:

> etwa 50 %

Vorteile:

- hohe Performance
- gute Ausfallsicherheit
- häufig schnellere Rebuilds als Paritäts-RAIDs

Ausfalltoleranz:

> Mehrere Laufwerke können ausfallen, **sofern nicht beide Laufwerke desselben Spiegelpaares betroffen sind**.

**Hinweis zu den Originalfolien:**  
Eine Folie ist als „RAID 6“ beschriftet, zeigt grafisch jedoch RAID 10. Das wurde hier fachlich korrigiert.

---

## RAID-Vergleich

| RAID | Min. Laufwerke | Nutzkapazität | Ausfalltoleranz | Typischer Schwerpunkt |
|---|---:|---|---|---|
| RAID 0 | 2 | 100 % | keine | Performance |
| RAID 1 | 2 | ca. 50 % | 1 bei 2 Platten | einfache Redundanz |
| RAID 5 | 3 | n−1 | 1 | Kapazität + Redundanz |
| RAID 6 | 4 | n−2 | 2 | höhere Redundanz |
| RAID 10 | 4 | ca. 50 % | abhängig von Spiegelpaaren | Performance + Redundanz |

### Wichtigster Merksatz

> **RAID ist kein Backup.**

RAID schützt nicht ausreichend gegen:

- versehentliches Löschen
- Ransomware
- Dateikorruption
- Fehlkonfiguration
- Diebstahl
- Feuer
- Wasser
- Überspannung
- Administratorfehler

---

# 8. Storage Area Network – SAN

Ein **Storage Area Network (SAN)** ist ein spezialisiertes Netzwerk, das Servern blockbasierten Speicher zur Verfügung stellt.

## Typische Komponenten

- Hosts/Server
- Host Bus Adapter (HBA)
- Converged Network Adapter (CNA)
- SAN-Switches
- Directors
- Storage Arrays
- Controller
- Kabel und Transceiver
- Managementsysteme

## Typische Protokolle

- Fibre Channel (FC)
- iSCSI
- NVMe over Fabrics (NVMe-oF)

## SAN-Fabric

Eine **Fabric** beschreibt die verbundene SAN-Infrastruktur aus Switches, Hosts und Storage.

Für hohe Verfügbarkeit werden häufig zwei voneinander unabhängige Fabrics eingesetzt:

```text
Host
 ├── Fabric A ── Storage
 └── Fabric B ── Storage
```

Dadurch können Single Points of Failure reduziert werden.

## Zoning und LUN Masking

**Zoning**

> steuert, welche SAN-Teilnehmer miteinander kommunizieren dürfen.

**LUN Masking**

> steuert, welche Hosts auf bestimmte logische Storage-Volumes zugreifen dürfen.

Beides dient der Segmentierung und Zugriffskontrolle.

---

# 9. SAN vs. NAS

| Merkmal | SAN | NAS |
|---|---|---|
| Zugriff | Block-Level | File-Level |
| Protokolle | FC, iSCSI, NVMe-oF | SMB, NFS |
| Sicht für Host | lokales Blockgerät | Netzwerkfreigabe |
| Typischer Einsatz | Datenbanken, Virtualisierung | Dateiablagen, Benutzerfreigaben |
| Komplexität | höher | meist geringer |

### Merksatz

> **SAN liefert Blöcke – NAS liefert Dateien.**

---

# 10. Cloud-Speicherung

Cloud-Speicher wird als Dienst über die Infrastruktur eines Cloudanbieters bereitgestellt.

Wichtige Eigenschaften können sein:

- elastische Skalierung
- nutzungsabhängige Abrechnung
- API-basierte Verwaltung
- automatisierbare Lifecycle-Regeln
- regionale oder zonale Redundanz
- Verschlüsselungsfunktionen
- Versionierung
- zentrale IAM-Integration

**Wichtig:**

> Cloud-Speicher bedeutet nicht automatisch Backup, Hochverfügbarkeit oder vollständige Sicherheit.

Diese Eigenschaften hängen vom gewählten Dienst und seiner Konfiguration ab.

---

# 11. Shared Responsibility Model

In der Cloud teilen sich Anbieter und Kunde die Sicherheitsverantwortung.

Vereinfacht:

## Cloudanbieter

verantwortet insbesondere:

- physische Rechenzentren
- physische Hardware
- Basisnetzwerk
- Hypervisor bzw. Plattformkomponenten entsprechend dem Servicemodell

## Kunde

bleibt insbesondere verantwortlich für:

- Datenklassifizierung
- Benutzer und Identitäten
- Berechtigungen
- Konfigurationen
- Aufbewahrung
- Backup-Anforderungen
- Verschlüsselungsentscheidungen
- Compliance
- sichere Nutzung des Dienstes

Der genaue Umfang hängt vom Modell ab:

```text
On-Premises → Kunde trägt nahezu alles
IaaS        → Verantwortung geteilt
PaaS        → mehr Verantwortung beim Provider
SaaS        → Provider übernimmt mehr Plattformanteile,
              Kunde bleibt u. a. für Daten, Identitäten
              und Konfiguration verantwortlich
```

### Merksatz

> **Der Cloudanbieter sichert die Cloud – der Kunde muss seine Nutzung der Cloud sicher konfigurieren.**

---

# 12. Auswahl eines Cloud-Speichers

Vor der Auslagerung von Unternehmensdaten sollte mindestens geprüft werden:

1. Datenklassifizierung
2. Schutzbedarf
3. Rechtsgrundlage und Datenschutz
4. Speicherregion und Datenresidenz
5. Anbieter und Vertragsbedingungen
6. Verfügbarkeit und SLA
7. Backup und Wiederherstellung
8. Verschlüsselung
9. Schlüsselmanagement
10. IAM und Rollenmodell
11. Logging und Monitoring
12. Exit-Strategie
13. Portabilität
14. Löschkonzept
15. Subdienstleister
16. Incident- und Notfallprozesse

---

# 13. Schutzbedarf nach BSI

Das BSI betrachtet den Schutzbedarf hinsichtlich:

- Vertraulichkeit
- Integrität
- Verfügbarkeit

Die Schutzbedarfskategorien lauten:

| Schutzbedarf | Bedeutung |
|---|---|
| **normal** | Schadensauswirkungen sind begrenzt und überschaubar |
| **hoch** | Schadensauswirkungen können beträchtlich sein |
| **sehr hoch** | Schadensauswirkungen können existenziell bzw. katastrophal sein |

---

# 14. Vererbung des Schutzbedarfs

Der Schutzbedarf wird von Informationen und Geschäftsprozessen auf Anwendungen und technische Zielobjekte übertragen.

Dabei sind insbesondere drei Prinzipien wichtig.

## Maximumprinzip

Der höchste relevante Schutzbedarf setzt sich grundsätzlich durch.

Beispiel:

```text
Anwendung A → normal
Anwendung B → hoch
Server      → mindestens hoch
```

## Kumulationseffekt

Mehrere einzeln weniger kritische Anwendungen können gemeinsam einen höheren Schutzbedarf verursachen.

Beispiel:

> Ein Server hostet 20 Anwendungen mit jeweils normalem Verfügbarkeitsbedarf. Der gleichzeitige Ausfall aller Anwendungen kann einen hohen Gesamtschaden verursachen.

## Verteilungseffekt

Wenn eine kritische Anwendung redundant auf mehrere unabhängige Systeme verteilt ist, kann der Schutzbedarf eines einzelnen Systems geringer sein als der Schutzbedarf der gesamten Anwendung.

### Wichtig

> Der Schutzbedarf eines Systems wird nicht einfach „automatisch immer erhöht“, nur weil darauf schützenswerte Daten liegen. Maximum-, Kumulations- und Verteilungseffekt müssen fachlich betrachtet und begründet werden.

---

# 15. Personenbezogene Daten und DSGVO

## Besondere Kategorien personenbezogener Daten

Art. 9 DSGVO nennt unter anderem Daten über:

- rassische oder ethnische Herkunft
- politische Meinungen
- religiöse oder weltanschauliche Überzeugungen
- Gewerkschaftszugehörigkeit
- genetische Daten
- biometrische Daten zur eindeutigen Identifizierung
- Gesundheitsdaten
- Sexualleben
- sexuelle Orientierung

Für deren Verarbeitung gelten besonders strenge Voraussetzungen.

## Datensicherheit nach Art. 32 DSGVO

Geeignete technische und organisatorische Maßnahmen können unter anderem umfassen:

- Verschlüsselung
- Pseudonymisierung
- Sicherstellung von Vertraulichkeit, Integrität und Verfügbarkeit
- Fähigkeit zur zeitnahen Wiederherstellung der Verfügbarkeit und des Zugangs
- regelmäßige Überprüfung der Wirksamkeit von Schutzmaßnahmen

Für Cloud-Dienste sind zusätzlich relevant:

- Auftragsverarbeitung nach Art. 28 DSGVO
- Prüfung von Unterauftragnehmern
- Drittlandübermittlungen nach Kapitel V DSGVO
- Datenstandort und Vertragsgestaltung

---

# 16. Verschlüsselung von gespeicherten Daten

## Data at Rest

Daten befinden sich auf einem Speichermedium.

Schutzmöglichkeiten:

- Full Disk Encryption
- Volume Encryption
- Datenbankverschlüsselung
- Object-/Storage-Service-Verschlüsselung

## Data in Transit

Daten werden übertragen.

Beispiele:

- TLS
- IPsec
- SSH

## Data in Use

Daten werden verarbeitet und liegen typischerweise entschlüsselt im Arbeitsspeicher vor.

Für besonders hohe Schutzanforderungen können Technologien wie:

- Confidential Computing
- Trusted Execution Environments

relevant sein.

---

# 17. Schlüsselmanagement

Verschlüsselung ist nur so sicher wie das Schlüsselmanagement.

Zu berücksichtigen sind:

- Schlüsselerzeugung
- sichere Speicherung
- Zugriffskontrolle
- Rotation
- Backup von Schlüsseln
- Widerruf
- Löschung
- Trennung von Rollen

Mögliche Systeme:

- KMS – Key Management Service/System
- HSM – Hardware Security Module

### Merksatz

> **Verschlüsselte Daten ohne verfügbaren Schlüssel sind ebenfalls ein Verfügbarkeitsproblem.**

---

# 18. Availability Zones und Regionen

Cloudanbieter teilen ihre Infrastruktur typischerweise in:

- **Regionen**
- **Zonen**

auf.

## Region

Eine geografisch abgegrenzte Cloud-Region.

Beispiel:

```text
Frankfurt
```

## Availability Zone

Eine innerhalb einer Region getrennte Bereitstellungs- bzw. Ausfalldomäne.

Ziel:

> Ein einzelner Infrastrukturfehler soll nicht alle Zonen gleichzeitig betreffen.

Je nach Anbieter bestehen Zonen aus einem oder mehreren Rechenzentren bzw. logisch getrennten Infrastrukturstandorten.

## Zonales Deployment

Ressource ist an eine Zone gebunden.

Nachteil:

> Ausfall der Zone kann den Dienst beeinträchtigen.

## Zonenredundantes Deployment

Ressourcen bzw. Daten werden über mehrere Zonen verteilt.

Vorteil:

> höhere Widerstandsfähigkeit gegen Zonenausfälle.

## Multi-Region

Ressourcen werden über unterschiedliche Regionen verteilt.

Vorteil:

> Schutz gegen größere regionale Ausfälle.

Nachteile:

- höhere Kosten
- höhere Komplexität
- Replikationslatenz
- mögliche Datenresidenz-/Compliance-Fragen

---

# 19. Azure Availability Sets vs. Availability Zones

## Availability Set

Azure verteilt VMs innerhalb eines Availability Sets über:

- **Fault Domains**
- **Update Domains**

Dadurch werden Auswirkungen von:

- Hardwarefehlern
- Strom-/Netzwerkproblemen innerhalb gemeinsamer Domänen
- geplanten Wartungen

reduziert.

Availability Sets schützen jedoch nicht vollständig gegen einen Ausfall auf Rechenzentrumsebene.

## Availability Zones

Availability Zones bieten eine stärkere physische Trennung innerhalb einer Region.

### Merksatz

> **Availability Set = Fehler-/Updatedomänen.**

> **Availability Zone = stärkere räumliche Infrastrukturtrennung.**

---

# 20. AWS und Google Cloud – Benennung von Zonen

## AWS

Beispiel:

```text
eu-central-1a
```

Wichtig:

Bei bestimmten älteren Regionen bzw. älteren Accounts kann der Buchstabe einer Zone zwischen Accounts unterschiedlich auf denselben physischen Standort abgebildet sein.

Für eine accountübergreifend eindeutige Zuordnung verwendet AWS **AZ IDs**.

Beispiel:

```text
euc1-az1
```

## Google Cloud

Beispiel:

```text
europe-west3-a
```

Die Region lautet:

```text
europe-west3
```

die Zone:

```text
a
```

Google unterscheidet:

- globale Ressourcen
- regionale Ressourcen
- zonale Ressourcen

---

# 21. Replikation und Redundanz

## Synchrone Replikation

Ein Schreibvorgang gilt erst als erfolgreich, wenn er auf mehreren Zielen bestätigt wurde.

Vorteile:

- sehr geringer möglicher Datenverlust

Nachteile:

- höhere Latenz
- Distanz begrenzt praktische Einsatzmöglichkeiten

## Asynchrone Replikation

Änderungen werden zeitversetzt übertragen.

Vorteile:

- größere geografische Entfernungen möglich
- geringere Latenzauswirkung auf Primärsystem

Nachteil:

> Bei einem Ausfall können noch nicht replizierte Daten verloren gehen.

---

# 22. Replikation ist kein Backup

Beispiel:

```text
Produktivdaten
     │
     ├── synchrone Replikation ──► Zweitsystem
     │
     └── Benutzer löscht Datei
                 ↓
         Löschung wird repliziert
```

Ohne:

- Versionierung
- Snapshots
- Immutable Backup
- getrennte Backup-Kopie

kann die Löschung auch auf dem Replikat übernommen werden.

### Merksatz

> **Redundanz erhöht Verfügbarkeit. Backup ermöglicht Wiederherstellung eines früheren Datenstands.**

---

# 23. Snapshots

Ein Snapshot bildet den Zustand eines Systems oder Volumes zu einem Zeitpunkt ab.

Arten können sein:

- Copy-on-Write
- Redirect-on-Write
- vollständige Snapshot-Kopie

Vorteile:

- schnell
- häufig platzsparend
- gut für kurzfristige Wiederherstellung

Risiken:

- Abhängigkeit vom zugrunde liegenden Storage
- möglicherweise keine physische Trennung
- bei kompromittiertem Administrationskonto ggf. löschbar

### Wichtig

> Ein Snapshot wird erst dann Teil einer belastbaren Backupstrategie, wenn Unabhängigkeit, Aufbewahrung, Schutz und Wiederherstellbarkeit ausreichend sichergestellt sind.

---

# 24. Storage-Tiering

Storage-Tiering ordnet Daten abhängig von:

- Zugriffshäufigkeit
- Performancebedarf
- Alter
- Schutzbedarf
- Kosten

unterschiedlichen Speicherklassen zu.

Beispiel:

```text
Tier 0 → höchste Performance / sehr aktive Daten
Tier 1 → Hot Data
Tier 2 → Warm Data
Tier 3 → Cold / Archive
```

**Hinweis:**

Die genaue Nummerierung ist **nicht universell standardisiert**. Anbieter können andere Tiermodelle verwenden.

## Grundprinzip

```text
höhere Performance
      ↑
      │   höhere Kosten
      │
      ↓
niedrigere Performance
      ↓
günstigere Archivierung
```

Aufgrund stark schwankender Marktpreise sollte ein prüfungsorientiertes Handout **keine festen Euro-pro-GB-Werte** als allgemeingültige Aussage verwenden.

---

# 25. HSM, ILM und Automated Tiering

## HSM – Hierarchical Storage Management

Daten werden automatisiert zwischen unterschiedlichen Speicherklassen verschoben.

Beispiel:

```text
SSD → HDD → Tape
```

## ILM – Information Lifecycle Management

Steuert Daten während ihres gesamten Lebenszyklus.

Beispiel:

```text
Erstellung
   ↓
aktive Nutzung
   ↓
seltene Nutzung
   ↓
Archivierung
   ↓
Löschung
```

## Automated Tiering

Storage-Systeme analysieren beispielsweise:

- Zugriffshäufigkeit
- I/O-Muster
- Datenalter

und verschieben Daten automatisiert in geeignete Tiers.

---

# 26. Datenlebenszyklus

Ein vollständiges Speicher- und Sicherheitskonzept betrachtet nicht nur die Speicherung.

```text
Erzeugen
   ↓
Klassifizieren
   ↓
Speichern
   ↓
Nutzen
   ↓
Weitergeben
   ↓
Sichern
   ↓
Archivieren
   ↓
Löschen
```

Zu jedem Schritt müssen passende Sicherheitsmaßnahmen existieren.

---

# 27. Sichere Datenlöschung

Normales Löschen entfernt häufig nur Referenzen auf Daten.

Je nach Speichermedium und Schutzbedarf können erforderlich sein:

- Überschreiben
- Secure Erase
- Crypto Erase
- physische Zerstörung

## Crypto Erase

Daten werden verschlüsselt gespeichert und der relevante Schlüssel anschließend sicher vernichtet.

Voraussetzung:

> Das Schlüsselmanagement muss zuverlässig sicherstellen, dass keine nutzbare Schlüsselkopie verbleibt.

Bei SSDs sind herstellerspezifische Secure-Erase-Verfahren oft sinnvoller als klassisches mehrfaches Überschreiben.

---

# 28. Tape Libraries

Eine **Tape Library** verwaltet Magnetbandkassetten automatisiert.

Typische Komponenten:

- Tape Drives
- Slots
- Robotik
- Barcode-System
- Library Controller
- Managementsoftware

## Autoloader

Kleine automatisierte Bandlösung mit:

- wenigen Laufwerken
- kleinerer Slot-Anzahl

## Tape Library

Größere Systeme können:

- viele Laufwerke
- hunderte oder tausende Medien

verwalten.

## Vorteile

- hohe Kapazität
- niedrige Kosten pro TB
- lange Aufbewahrung
- physischer Air Gap möglich
- WORM-Unterstützung
- gut für Backup und Archiv

## Nachteile

- sequenzieller Zugriff
- höhere Restore-Zeit
- Robotik und Laufwerke müssen gewartet werden
- Medienrotation und Lagerung müssen organisiert werden

---

# 29. LTO – Linear Tape-Open

LTO ist ein verbreitetes Magnetbandformat.

Aktuelle Größenordnungen:

| Generation | Native Kapazität | Komprimiert* |
|---|---:|---:|
| **LTO-9** | 18 TB | 45 TB |
| **LTO-10** | 30 TB bzw. bei aktuellen Varianten bis 40 TB | 75 TB bzw. bis 100 TB |

\* Herstellerangaben zur Kompression basieren auf einem angenommenen Kompressionsverhältnis. Reale Ergebnisse hängen stark von den Daten ab; bereits komprimierte oder verschlüsselte Daten lassen sich oft kaum weiter komprimieren.

Typische Sicherheitsfunktionen:

- AES-256-Verschlüsselung
- WORM-Medien
- physischer Air Gap

**LTFS – Linear Tape File System**

ermöglicht einen dateisystemähnlichen Zugriff auf LTO-Medien.

---

# 30. Backup – Grundlagen

Ein Backup ist eine zusätzliche Datenkopie, die zur Wiederherstellung nach Datenverlust dient.

Typische Ursachen für Datenverlust:

- Hardwaredefekt
- Fehlbedienung
- Softwarefehler
- Ransomware
- Sabotage
- Naturereignisse
- Diebstahl
- fehlerhaftes Update
- Datenkorruption

Ein Backupkonzept muss festlegen:

- Was wird gesichert?
- Wie häufig?
- Wohin?
- Wie lange?
- Wer darf zugreifen?
- Wie wird verschlüsselt?
- Wie wird die Wiederherstellung getestet?
- Welche RPO/RTO-Anforderungen bestehen?

---

# 31. 3-2-1-Regel

Die klassische Regel lautet:

> **3 Datenkopien**

> **2 unterschiedliche Speicherarten bzw. Medien**

> **1 Kopie an einem getrennten Standort**

Vereinfacht:

```text
Produktivdaten
     +
lokales Backup
     +
externes/offsite Backup
```

## Erweiterte 3-2-1-1-0-Regel

Eine verbreitete Erweiterung lautet:

- **3** Kopien
- **2** unterschiedliche Medien/Speichertypen
- **1** Kopie offsite
- **1** Kopie offline oder immutable
- **0** ungeprüfte Backupfehler nach Verifikation

**Hinweis:**

> 3-2-1-1-0 ist eine Best-Practice-Erweiterung und keine universell verbindliche Norm.

---

# 32. Backup-Arten

## Vollbackup / Full Backup

Sichert alle ausgewählten Daten.

Vorteile:

- einfacher Restore
- nur ein Sicherungssatz notwendig

Nachteile:

- hoher Speicherbedarf
- längere Backupzeit

---

## Inkrementelles Backup

Sichert Änderungen seit der **letzten Sicherung**, unabhängig davon, ob diese vollständig oder inkrementell war.

Beispiel:

```text
Sonntag:  Full
Montag:   Änderungen seit Sonntag
Dienstag: Änderungen seit Montag
Mittwoch: Änderungen seit Dienstag
```

Vorteil:

- geringer Speicherbedarf
- kurze Sicherungsdauer

Nachteil:

- Restore benötigt typischerweise mehrere Sicherungssätze

---

## Differenzielles Backup

Sichert Änderungen seit dem **letzten Vollbackup**.

Beispiel:

```text
Sonntag: Full
Montag:  Änderung seit Sonntag
Dienstag: alle Änderungen seit Sonntag
Mittwoch: alle Änderungen seit Sonntag
```

Vorteil:

- Restore benötigt Full + letztes Differential

Nachteil:

- Differentialsicherung wächst bis zum nächsten Full Backup

---

# 33. Backup-Vergleich

| Verfahren | Backupaufwand | Speicherbedarf | Restore-Aufwand |
|---|---|---|---|
| Full | hoch | hoch | niedrig |
| Inkrementell | niedrig | niedrig | höher |
| Differenziell | zunehmend | mittel | mittel |

---

# 34. Backup-Konsistenz

Ein technisch vorhandenes Backup muss auch **konsistent** sein.

## Crash-Consistent

Entspricht ungefähr dem Zustand nach einem plötzlichen Stromausfall.

## File-System-Consistent

Dateisystemstrukturen befinden sich in einem konsistenten Zustand.

## Application-Consistent

Anwendungen und Transaktionen werden vor dem Snapshot/Backup koordiniert.

Besonders wichtig bei:

- Datenbanken
- Verzeichnisdiensten
- Transaktionssystemen

### Merksatz

> **Ein erfolgreich kopiertes Backup ist nicht automatisch ein erfolgreich wiederherstellbares Backup.**

---

# 35. RPO und RTO

## RPO – Recovery Point Objective

Das RPO beschreibt:

> **den maximal tolerierbaren Datenverlust gemessen als Zeitspanne.**

Beispiel:

```text
RPO = 1 Stunde
```

Bei einem Ausfall um 14:00 Uhr müssen mindestens Daten bis 13:00 Uhr wiederherstellbar sein.

---

## RTO – Recovery Time Objective

Das RTO beschreibt:

> **die geforderte Zielzeit für den Wiederanlauf bzw. die Bereitstellung der vorgesehenen Wiederherstellungs-/BC-Lösung.**

**Korrektur gegenüber der ursprünglichen Fassung:**

> RTO ist **nicht** identisch mit der maximal tolerierbaren Ausfallzeit.

Im BCM wird die absolute Toleranzgrenze über **MTPD/MTA** beschrieben.

Grundsätzlich:

```text
RTO < MTPD
```

---

# 36. Einfluss des RPO auf die Backupstrategie

Je kleiner das RPO, desto häufiger müssen Daten:

- gesichert,
- repliziert oder
- kontinuierlich geschützt

werden.

Beispiel:

| RPO | Möglicher Ansatz |
|---|---|
| 24 Stunden | tägliches Backup |
| 4 Stunden | mehrere Backups/Snapshots pro Tag |
| 15 Minuten | häufige Snapshots/Replikation |
| nahe 0 | synchrone bzw. sehr engmaschige Replikation/CDP |

Dies sind Architekturbeispiele und keine allgemeingültigen Garantiewerte.

---

# 37. Backup vs. Snapshot vs. Replikation

| Verfahren | Hauptziel | Historische Stände | Schutz bei Standortverlust |
|---|---|---|---|
| Backup | Wiederherstellung | ja | bei externer Kopie ja |
| Snapshot | schneller Point-in-Time-Zustand | ja, abhängig von Retention | häufig nein |
| Replikation | Verfügbarkeit | nicht zwingend | bei geografischer Trennung möglich |

### Prüfungsfalle

> **Hochverfügbarkeit ersetzt keine Datensicherung.**

---

# 38. Immutable Backups und WORM

**Immutable** bedeutet:

> Daten können für einen definierten Zeitraum nicht verändert oder gelöscht werden.

**WORM** bedeutet:

> Write Once, Read Many.

Einsatz:

- Ransomware-Schutz
- Compliance
- revisionsnahe Aufbewahrung
- Schutz vor kompromittierten Administratorkonten

Cloud-Beispiele:

- S3 Object Lock
- Azure Immutable Vault bzw. WORM-Funktionen
- entsprechende Retention-/Lock-Funktionen anderer Anbieter

---

# 39. Air Gap

Ein Air Gap trennt Backupdaten vom Produktivsystem.

## Physischer Air Gap

Beispiel:

> Tape wird aus der Library entnommen und extern gelagert.

## Logischer Air Gap

Beispiele:

- getrenntes Backup-Konto
- getrennte Zugangsdaten
- immutable Backup
- isolierte Recovery-Umgebung

### Merksatz

> Je weniger ein Angreifer vom kompromittierten Produktivkonto aus auf das Backup zugreifen kann, desto höher die Cyber-Resilienz.

---

# 40. Sicherheit von Backups

Ein belastbares Backupkonzept sollte mindestens berücksichtigen:

- Verschlüsselung at rest
- Verschlüsselung in transit
- separates Schlüsselmanagement
- Least Privilege
- MFA für Administratoren
- getrennte Backup-Administratoren
- getrennte Konten/Tenants, wenn sinnvoll
- Immutable/WORM
- Offline-/Offsite-Kopie
- Monitoring
- Alarmierung
- Audit Logs
- Schutz vor Löschung
- regelmäßige Restore-Tests

---

# 41. Restore-Tests

Backups müssen regelmäßig wiederhergestellt werden.

Zu prüfen sind:

- Lesbarkeit der Sicherung
- Vollständigkeit
- Datenintegrität
- Applikationskonsistenz
- Schlüsselverfügbarkeit
- Zugangsdaten
- Restore-Reihenfolge
- Abhängigkeiten
- RTO
- erreichbares RPO
- Dokumentation

### Merksatz

> **Ein ungetestetes Backup ist nur eine Hoffnung auf Wiederherstellung.**

---

# 42. Backup-Monitoring

Zu überwachen sind beispielsweise:

- Backup erfolgreich/fehlgeschlagen
- Sicherungsdauer
- Datenmenge
- Kapazität
- ungewöhnliche Löschungen
- Retention-Fehler
- Replikationsfehler
- Laufwerks-/Medienzustand
- Restore-Test-Ergebnisse

Fehler müssen:

1. erkannt,
2. alarmiert,
3. bearbeitet,
4. dokumentiert

werden.

---

# 43. Aufbewahrung und Retention

Retention legt fest:

> Wie lange Daten bzw. Backupstände aufbewahrt werden.

Zu berücksichtigen sind:

- fachliche Anforderungen
- Wiederherstellungsbedarf
- gesetzliche Aufbewahrung
- Datenschutz
- Kosten
- Speicherbedarf
- Löschpflichten

Mögliche Generationen:

```text
täglich
wöchentlich
monatlich
jährlich
```

Eine verbreitete Methode ist die **Grandfather-Father-Son-Strategie (GFS)**.

---

# 44. Backup und Datenschutz

Bei Backups personenbezogener Daten gelten Datenschutzanforderungen weiter.

Wichtige Punkte:

- Zugriff beschränken
- Backup verschlüsseln
- Aufbewahrungsfristen definieren
- Löschkonzept berücksichtigen
- Wiederherstellungen dokumentieren
- Drittanbieter vertraglich einbinden
- Datenstandort prüfen

**Problem:**

Einzelne Datensätze lassen sich in klassischen Backups oft nicht unmittelbar physisch löschen.

Deshalb müssen Datenschutz- und Löschkonzepte definieren, wie mit:

- abgelaufenen Backups
- Wiederherstellungen
- erneut auftauchenden gelöschten Daten

umgegangen wird.

---

# 45. Cloud-Backup

Cloudplattformen bieten unterschiedliche Funktionen für:

- Snapshots
- Backup
- Replikation
- Versionierung
- Retention
- WORM
- Cross-Region-Kopien

Ein sinnvolles Konzept kann umfassen:

```text
Produktivkonto
     │
     ├── lokaler/zonaler Snapshot
     │
     ├── Backup in getrennten Vault
     │
     └── Kopie in getrenntes Konto/Region
                    ↓
               immutable
```

---

# 46. Providerübergreifende DR-Grundmuster

Anstatt produktspezifische Marketingbegriffe auswendig zu lernen, sind die Architekturprinzipien prüfungsrelevanter.

## Backup & Restore

- geringe laufende Kosten
- längeres RTO
- höheres RPO abhängig vom Sicherungsintervall

## Pilot Light

Kernkomponenten laufen bereits am Ausweichstandort.

Im Notfall werden weitere Komponenten gestartet.

## Warm Standby

Verkleinerte, funktionsfähige Umgebung läuft dauerhaft.

Vorteil:

> schnellerer Wiederanlauf.

## Active/Active bzw. Multi-Site

Mehrere Standorte bedienen gleichzeitig produktiven Traffic.

Vorteile:

- sehr hohe Verfügbarkeit
- geringe Umschaltzeit

Nachteile:

- hohe Kosten
- hohe Komplexität
- Datenkonsistenz muss beherrscht werden

---

# 47. Beispiele für Cloud-Werkzeuge

## AWS

Beispiele:

- AWS Backup
- S3 Object Lock
- AWS Elastic Disaster Recovery
- AWS Resilience Hub
- AWS Fault Injection Service
- CloudFormation

## Microsoft Azure

Beispiele:

- Azure Backup
- Azure Site Recovery
- Azure Storage
- Immutable Vault
- Azure Monitor
- Service Health
- Azure Chaos Studio

## Google Cloud

Beispiele:

- Cloud Storage
- Backup and DR Service
- regionale/multiregionale Speicheroptionen
- Cloud Monitoring
- Cloud Load Balancing

**Korrektur gegenüber den Ausgangsfolien:**

- **Chaos Monkey** stammt aus dem Netflix-Umfeld und ist kein AWS-Dienst.
- **AzERE** ist kein typisches kundenbezogenes Standardwerkzeug, das für eine IHK-Prüfung auswendig gelernt werden sollte.
- Herstellerzertifizierungen und konkrete SLA-/RPO-/RTO-Werte sollten nur dienst- und vertragsbezogen angegeben werden.

---

# 48. Warum pauschale Cloud-RPO/RTO-Werte problematisch sind

Die ursprünglichen Folien nennen sehr konkrete Werte wie:

```text
RPO < 1 Sekunde
RTO < 60 Sekunden
```

für bestimmte Dienste.

Solche Angaben können sich ändern und hängen unter anderem ab von:

- Dienst
- Architektur
- Region
- Replikationsmodus
- Tarif
- Konfiguration
- Anwendung
- Failoververfahren
- SLA-Version

Daher gilt für die Prüfung:

> **RPO und RTO werden aus den Geschäftsanforderungen festgelegt. Die technische Lösung muss anschließend nachweisen, dass sie diese Ziele erfüllen kann.**

Nicht umgekehrt.

---

# 49. Storage-Tiering On-Premises vs. Cloud

| Merkmal | On-Premises | Cloud |
|---|---|---|
| Tiers | SSD, HDD, Tape | Hot, Cool, Cold, Archive o. ä. |
| Migration | Storage-System/HSM | Lifecycle Policies |
| Kosten | Hardware + Betrieb | Nutzung + Zugriffe + Transfer |
| Skalierung | Hardwareabhängig | elastischer |
| Kontrolle | hoch | geteilt |
| Automatisierung | herstellerabhängig | häufig API-/Policy-basiert |

---

# 50. Lokale Speicherung vs. Cloud

| Kriterium | On-Premises | Cloud |
|---|---|---|
| Kontrolle | sehr hoch | Shared Responsibility |
| Skalierbarkeit | hardwareabhängig | meist elastisch |
| Investition | CAPEX-lastig | häufig OPEX/Pay-as-you-go |
| Wartung | eigene Verantwortung | teilweise Provider |
| Internetabhängigkeit | lokale Dienste können offline funktionieren | externer Zugriff oft netzabhängig |
| Redundanz | selbst aufbauen | Dienste bieten verschiedene Optionen |
| Datenresidenz | physisch selbst steuerbar | Region/Vertrag prüfen |
| Exit | Hardware/Daten selbst | Export und Portabilität planen |

### Prüfungsfalle

> Cloud bedeutet nicht „ohne Internet niemals Zugriff“. Hybrid- und Edge-Lösungen, lokale Caches oder private Verbindungen können andere Architekturen ermöglichen.

---

# 51. Single Points of Failure bei Storage

Mögliche SPoFs:

- einzelner Storage Controller
- einzelner SAN-Switch
- einzelne Stromversorgung
- einzelner Backupserver
- einziges Administratorkonto
- einzelner KMS/HSM-Pfad
- nur eine Netzwerkverbindung
- nur ein Standort

Gegenmaßnahmen:

- redundante Controller
- Dual Fabric
- Multipathing
- redundante Netzteile
- USV/Notstrom
- geografische Redundanz
- getrennte Administrationswege
- Wiederherstellungstests

---

# 52. Multipathing

Bei SAN- und Block-Storage-Systemen können mehrere Pfade zwischen Host und Storage existieren.

```text
Host
 ├── Pfad A ──► Storage
 └── Pfad B ──► Storage
```

Multipathing ermöglicht:

- Failover bei Pfadausfall
- teilweise Lastverteilung
- höhere Verfügbarkeit

---

# 53. Deduplizierung und Kompression

## Deduplizierung

Identische Datenblöcke werden nur einmal gespeichert.

Vorteil:

> geringerer Speicherbedarf.

## Kompression

Daten werden platzsparender codiert.

### Sicherheits-/Betriebshinweis

Bereits:

- komprimierte,
- verschlüsselte

Daten lassen sich häufig nur wenig weiter komprimieren oder deduplizieren.

---

# 54. Erasure Coding

Erasure Coding verteilt Daten und Prüfinformationen über mehrere Speicherorte.

Ziel:

> Daten können trotz Ausfall einzelner Fragmente rekonstruiert werden.

Es wird häufig in:

- Object Storage
- verteilten Storage-Systemen
- großen Cloud-Speicherplattformen

eingesetzt.

Vergleich zu klassischem RAID:

> Beide nutzen Redundanz, Erasure Coding ist jedoch besonders für verteilte Systeme und große Skalierung geeignet.

---

# 55. Datenintegrität

Speicherfehler können Daten unbemerkt verändern.

Schutzmechanismen können sein:

- Checksums
- Hashwerte
- Prüfsummen auf Blockebene
- Scrubbing
- ECC
- redundante Kopien
- Integritätsprüfungen im Backup

### Merksatz

> **Verfügbarkeit allein reicht nicht – verfügbare, aber beschädigte Daten sind nicht brauchbar.**

---

# 56. Storage-Monitoring

Wichtige Kennzahlen:

- Kapazitätsauslastung
- IOPS
- Throughput
- Latenz
- Queue Depth
- Fehlerraten
- Disk Health
- Controllerstatus
- Rebuildstatus
- Replikationsverzug
- Backupstatus

Ziel:

> Probleme erkennen, bevor daraus Ausfälle oder Datenverluste entstehen.

---

# 57. Typischer sicherer Storage-Aufbau

```text
                 Benutzer / Anwendungen
                          │
                          ▼
                   Zugriffskontrolle
                     IAM / RBAC / MFA
                          │
                          ▼
                Produktivspeicher
                ┌─────────┴─────────┐
                │                   │
           Redundanz            Monitoring
         RAID/Replication       Logging/Alerting
                │
                ▼
             Backup
       ┌────────┼─────────┐
       │        │         │
    lokal    offsite   immutable/
                       offline
       │
       ▼
 regelmäßiger Restore-Test
```

---

# 58. Typischer Prüfungsablauf bei einer Storage-Aufgabe

Wenn die Aufgabe lautet:

> „Planen Sie eine sichere Datenspeicherung für ein Unternehmen.“

kannst du strukturiert vorgehen:

```text
Daten identifizieren
      ↓
Schutzbedarf bestimmen
      ↓
RPO/RTO aus Geschäftsanforderungen ableiten
      ↓
Storage-Typ auswählen
      ↓
Redundanz planen
      ↓
Zugriff absichern
      ↓
Verschlüsselung planen
      ↓
Backupstrategie festlegen
      ↓
Offsite/Immutable/Air Gap
      ↓
Monitoring
      ↓
Restore testen
      ↓
Dokumentieren und verbessern
```

---

# 59. Typische IHK-Prüfungsfragen

## „Erläutern Sie den Unterschied zwischen RAID und Backup.“

> RAID erhöht je nach Level die Verfügbarkeit eines Speichers, indem Daten gespiegelt oder mit Paritätsinformationen verteilt werden. Ein Backup stellt dagegen eine unabhängige Kopie für die Wiederherstellung früherer Datenstände bereit. RAID schützt beispielsweise nicht gegen versehentliches Löschen oder Ransomware und ersetzt daher kein Backup.

---

## „Erläutern Sie die 3-2-1-Regel.“

> Es sollen mindestens drei Datenkopien vorhanden sein. Diese sollen auf mindestens zwei unterschiedlichen Speicherarten bzw. Medien liegen, wobei mindestens eine Kopie an einem getrennten Standort aufbewahrt wird. Dadurch werden technische und standortbezogene Ausfallrisiken reduziert.

---

## „Unterscheiden Sie inkrementelles und differenzielles Backup.“

> Ein inkrementelles Backup sichert Änderungen seit der letzten Sicherung. Ein differenzielles Backup sichert dagegen alle Änderungen seit dem letzten Vollbackup. Inkrementelle Backups benötigen meist weniger Speicher, während differenzielle Backups häufig schneller wiederhergestellt werden können.

---

## „Unterscheiden Sie SAN und NAS.“

> Ein SAN stellt blockbasierten Speicher bereit und wird typischerweise für Datenbanken und Virtualisierung verwendet. Ein NAS stellt Dateien über Netzwerkprotokolle wie SMB oder NFS bereit und eignet sich insbesondere für gemeinsame Dateiablagen.

---

## „Warum reicht Replikation allein nicht als Backup?“

> Replikation dient primär der Verfügbarkeit und übernimmt Änderungen häufig automatisch auf ein Zweitsystem. Dadurch können auch Löschungen, Datenkorruption oder Ransomware-Aktivitäten repliziert werden. Ein Backup benötigt daher unabhängige Wiederherstellungspunkte, geeignete Aufbewahrung und Schutz vor Manipulation.

---

## „Nennen und erläutern Sie Maßnahmen gegen Ransomware-Angriffe auf Backups.“

Mögliche Maßnahmen:

- Immutable/WORM-Backups
- Offline-/Air-Gap-Kopie
- getrennte Administrationskonten
- MFA
- Least Privilege
- getrennte Backup-Accounts
- Monitoring
- regelmäßige Restore-Tests

---

## „Erläutern Sie RPO und RTO.“

> Das RPO legt fest, wie viel Datenverlust zeitlich maximal akzeptiert wird. Das RTO legt fest, innerhalb welcher Zielzeit eine ausgefallene Funktion bzw. Wiederherstellungslösung wieder bereitstehen muss. Beide Werte werden aus den Anforderungen der Geschäftsprozesse abgeleitet und bestimmen maßgeblich die Backup- und Disaster-Recovery-Architektur.

---

# 60. Häufige Prüfungsfallen

- **RAID = Backup** → falsch
- **Snapshot = automatisch Backup** → falsch
- **Replikation = Backup** → falsch
- **Cloudanbieter macht automatisch alle Backups** → falsch
- **Cloud ist automatisch sicherer** → falsch
- **On-Premises ist automatisch sicherer** → falsch
- **RTO = maximal tolerierbare Ausfallzeit** → zu ungenau/falsch; MTPD/MTA ist die Toleranzgrenze
- **RAID 10 toleriert immer zwei beliebige Plattenausfälle** → falsch
- **RAID 5 ist grundsätzlich ungeeignet für SSDs** → falsch
- **BSI-Schutzbedarf „kein/gering – hoch – sehr hoch“** → falsch; richtig: normal – hoch – sehr hoch
- **Availability Zone = Backup** → falsch
- **Hochverfügbarkeit = Disaster Recovery** → nicht automatisch
- **100 TB „komprimiert“ bei Tape bedeutet garantiert 100 TB reale Daten** → falsch; abhängig von Komprimierbarkeit

---

# ⚡ Schnellcheck – 60 Sekunden vor der Prüfung

- **Storage ≠ Backup ≠ Archiv**
- **Block** → SAN/Volumes
- **File** → NAS/SMB/NFS
- **Object** → API-basierter Objektspeicher
- **RAID 0** → keine Redundanz
- **RAID 1** → Spiegelung
- **RAID 5** → 1 Parität / 1 Ausfall
- **RAID 6** → 2 Paritäten / 2 Ausfälle
- **RAID 10** → Mirror + Stripe
- **RAID ersetzt kein Backup**
- **SAN = Block-Level**
- **NAS = File-Level**
- **Multipathing** → mehrere Wege zum Storage
- **3-2-1** → 3 Kopien / 2 Medien bzw. Speicherarten / 1 offsite
- **3-2-1-1-0** → zusätzlich offline/immutable + verifizierte Backups
- **Full** → alles
- **Incremental** → seit letzter Sicherung
- **Differential** → seit letztem Full
- **Snapshot** → Zeitpunktzustand, nicht automatisch unabhängiges Backup
- **Replikation** → Verfügbarkeit, nicht automatisch historische Wiederherstellung
- **RPO** → tolerierbarer Datenverlust
- **RTO** → Wiederanlaufziel
- **MTPD/MTA** → maximal tolerierbare Ausfallzeit
- **Immutable/WORM** → nicht veränderbar/löschbar innerhalb Retention
- **Air Gap** → logische oder physische Trennung
- **Schutzbedarf BSI** → normal / hoch / sehr hoch
- **Maximumprinzip** → höchster Schutzbedarf setzt sich durch
- **Kumulationseffekt** → viele kleine Schäden ergeben großen Schaden
- **Verteilungseffekt** → Verteilung kann Einzelobjekt entlasten
- **Shared Responsibility** → Provider + Kunde
- **Availability Zones** → getrennte Ausfalldomänen
- **Multi-Region** → zusätzliche geografische Resilienz
- **Verschlüsselung** → at rest + in transit
- **KMS/HSM** → Schlüsselmanagement
- **Restore-Test** → zwingend für belastbare Wiederherstellbarkeit

---

# Prüfungs-Merksätze

> **RAID hält Systeme am Laufen – Backup bringt Daten zurück.**

> **Redundanz schützt vor Ausfall, Versionierung schützt vor Änderungen, Backup schützt vor Datenverlust.**

> **RPO blickt auf den letzten noch akzeptablen Datenstand zurück.**

> **RTO blickt auf die geforderte Wiederanlaufzeit nach vorn.**

> **Ein Backup ist erst dann wertvoll, wenn es erfolgreich wiederhergestellt werden kann.**

> **Cloud entlastet von Infrastrukturaufgaben, nicht von der Verantwortung für die eigenen Daten.**

> **Erst Schutzbedarf und Geschäftsanforderungen bestimmen – danach die Speichertechnik auswählen.**

---

# Quellen und weiterführende Referenzen

## BSI

- Bundesamt für Sicherheit in der Informationstechnik: BSI-Standard 200-2 – IT-Grundschutz-Methodik
- BSI IT-Grundschutz-Kompendium
- BSI-Veröffentlichungen zu Datensicherung, Cloud Computing und Schutzbedarfsfeststellung

## Datenschutz

- Verordnung (EU) 2016/679 – Datenschutz-Grundverordnung (DSGVO), insbesondere Art. 9, Art. 28 und Art. 32

## Cloud

- AWS: Shared Responsibility Model
- AWS: Availability Zones / AZ IDs
- AWS: S3 Object Lock
- Microsoft Learn: Shared Responsibility in the Cloud
- Microsoft Learn: Availability Sets und Availability Zones
- Microsoft Learn: Azure Backup / Immutable Vault
- Google Cloud: Regions and Zones
- Google Cloud Architecture Center: Disaster Recovery

## Tape

- IBM: LTO Ultrium Tape Data Cartridges

---

# Hinweis

Dieses Handout ist als **Lern- und Prüfungshilfe** aufgebaut. Herstellerpreise, Produktnamen, SLAs, Kapazitäten und Cloudfunktionen können sich ändern. Für produktive Architekturentscheidungen, Audits oder rechtlich verbindliche Bewertungen sind immer die jeweils aktuellen Originalstandards, Verträge und Herstellerdokumentationen heranzuziehen.
