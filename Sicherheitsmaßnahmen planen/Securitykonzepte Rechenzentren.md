# Lernblatt / Handout: Securitykonzepte in Rechenzentren

### Kompaktes Nachschlagewerk für die IHK-Prüfung „Geprüfter Berufsspezialist für Informationssicherheit"

**Stand: 31. August 2026**\
**Grundlagen:** BSI IT-Grundschutz, insbesondere INF.1 / INF.2 / INF.12,
BSI-Standards 200-1 bis 200-4, ISO/IEC 27001:2022, DIN EN 50600, DSGVO
sowie aktuelle BSI-Empfehlungen

------------------------------------------------------------------------

# ⚡ Schnellcheck vor der Prüfung

## Die wichtigsten Begriffe

-   **Rechenzentrum (RZ)** = besonders geschützter IT-Betriebsbereich
    einschließlich notwendiger Support-Infrastruktur
-   **Schutzziele** = Vertraulichkeit, Integrität und Verfügbarkeit;
    ergänzend Authentizität, Nachvollziehbarkeit und Resilienz
-   **Defense in Depth** = mehrere voneinander unabhängige
    Schutzschichten
-   **Security by Design** = Sicherheit bereits bei Planung und
    Architektur berücksichtigen
-   **Least Privilege** = nur die minimal erforderlichen Rechte vergeben
-   **Need-to-know** = Zugriff nur, wenn die Information für die Aufgabe
    benötigt wird
-   **Zero Trust** = keinem Benutzer, Gerät oder Netzsegment allein
    aufgrund seines Standorts automatisch vertrauen
-   **Sicherheitszonen** = Bereiche mit unterschiedlichen
    Schutzanforderungen
-   **Perimeterschutz** = äußere physische Schutzlinie des RZ
-   **Zutrittskontrolle** = Wer darf physisch hinein?
-   **Zugangskontrolle** = Wer darf IT-Systeme benutzen?
-   **Zugriffskontrolle** = Auf welche Daten/Funktionen darf ein
    Benutzer zugreifen?
-   **USV** = unterbrechungsfreie Stromversorgung für kurze
    Unterbrechungen und Überbrückung bis zur Ersatzstromversorgung
-   **NEA** = Netzersatzanlage, häufig Generator, für längere
    Stromausfälle
-   **A/B-Versorgung** = redundante Strompfade bis zu IT-Systemen
-   **N+1** = ein zusätzliches Element über den notwendigen Bedarf
    hinaus
-   **2N** = zwei vollständig dimensionierte, unabhängige
    Versorgungspfade
-   **Brandfrüherkennung** = Rauch-/Branddetektion möglichst vor einem
    Vollbrand
-   **RPO** = maximal tolerierbarer Datenverlust in Zeit
-   **RTO** = Zielzeit für die Wiederaufnahme eines Dienstes
-   **MTPD/MTA** = maximal tolerierbare Ausfallzeit
-   **BCM** = Business Continuity Management
-   **DR** = Disaster Recovery / IT-Wiederanlauf
-   **SIEM** = zentrale Sammlung, Korrelation und Auswertung
    sicherheitsrelevanter Ereignisse
-   **IDS** = erkennt verdächtigen Datenverkehr
-   **IPS** = erkennt und kann automatisiert blockieren
-   **DMZ** = isolierte Netzwerkzone für extern erreichbare Dienste
-   **HSM** = besonders geschütztes System für Schlüssel und
    kryptografische Operationen
-   **PKI** = Infrastruktur zur Verwaltung digitaler Zertifikate und
    Schlüssel
-   **MFA** = Authentisierung mit mindestens zwei unabhängigen Faktoren
-   **Immutable Backup** = Backup, das während einer definierten Frist
    nicht verändert oder gelöscht werden kann

## Prüfungs-Merksatz

> **Ein sicheres Rechenzentrum benötigt physische, technische,
> organisatorische, kryptografische und rechtliche Schutzmaßnahmen --
> nicht nur Firewalls.**

------------------------------------------------------------------------

# 1. Ziel eines Securitykonzeptes im Rechenzentrum

Ein Securitykonzept beschreibt, wie Informationen, IT-Systeme,
Infrastruktur und Geschäftsprozesse eines Rechenzentrums gegen
Gefährdungen geschützt werden.

Die Sicherheitsmaßnahmen müssen sich am:

-   Schutzbedarf,
-   Risiko,
-   Stand der Technik,
-   Geschäftszweck,
-   gesetzlichen Anforderungen und
-   akzeptierten Restrisiko

orientieren.

Ein ganzheitliches Konzept betrachtet mindestens:

``` text
Governance / Organisation
          │
          ├── Physische Sicherheit
          ├── Technische Sicherheit
          ├── Kryptografische Sicherheit
          ├── Netzwerk- und Systemsicherheit
          ├── Betriebs- und Personalsicherheit
          ├── Datensicherung / Resilienz
          ├── Notfallmanagement
          └── Compliance / Datenschutz
```

------------------------------------------------------------------------

# 2. Schutzziele

## Vertraulichkeit

Informationen dürfen nur von berechtigten Personen oder Systemen
eingesehen werden.

Maßnahmen:

-   Zutrittskontrolle
-   IAM/RBAC
-   Verschlüsselung
-   Netzwerksegmentierung
-   Need-to-know

## Integrität

Daten und Systeme dürfen nicht unbemerkt oder unbefugt verändert werden.

Maßnahmen:

-   Hashwerte
-   digitale Signaturen
-   Änderungsmanagement
-   Logging
-   File Integrity Monitoring
-   restriktive Berechtigungen

## Verfügbarkeit

Informationen und Systeme müssen bei Bedarf verfügbar sein.

Maßnahmen:

-   Redundanz
-   USV/NEA
-   redundante Kühlung
-   Cluster
-   Backups
-   Ersatzstandorte
-   BCM/Disaster Recovery

## Ergänzende Sicherheitsziele

-   **Authentizität** → Echtheit von Identitäten und Informationen
-   **Nachvollziehbarkeit** → Aktionen müssen zuordenbar sein
-   **Nichtabstreitbarkeit** → Handlungen/Erklärungen können nicht ohne
    Weiteres abgestritten werden
-   **Resilienz** → Systeme können Störungen widerstehen und sich davon
    erholen

------------------------------------------------------------------------

# 3. Schutzbereiche eines Rechenzentrums

Ein vollständiges Securitykonzept kann in fünf große Schutzbereiche
gegliedert werden:

  -----------------------------------------------------------------------
  Bereich                             Beispiele
  ----------------------------------- -----------------------------------
  **Physische Sicherheit**            Perimeter, Zutritt, Brand, Wasser,
                                      Klima

  **Technische Sicherheit**           Netzwerk, Server, Storage,
                                      Endpunkte

  **Kryptografische Sicherheit**      Verschlüsselung, PKI, HSM,
                                      Schlüssel

  **Organisatorische Sicherheit**     Rollen, Richtlinien, Prozesse,
                                      Personal

  **Rechtliche Sicherheit**           DSGVO, NIS-2/BSIG, KRITIS,
                                      Verträge, Audits
  -----------------------------------------------------------------------

### Wichtig

> Die Bereiche wirken zusammen. Eine hochsichere Firewall hilft
> beispielsweise wenig, wenn Unbefugte direkten physischen Zugriff auf
> die Server erhalten.

------------------------------------------------------------------------

# 4. Defense in Depth

**Defense in Depth** bedeutet, mehrere voneinander unabhängige
Sicherheitsmaßnahmen hintereinander einzusetzen.

Beispiel:

``` text
Grundstück
   ↓
Zaun / Perimeter
   ↓
Gebäudezutritt
   ↓
Personenschleuse
   ↓
RZ-Sicherheitsbereich
   ↓
Serverraum
   ↓
Rack
   ↓
Betriebssystem
   ↓
Anwendung
   ↓
Daten
```

Fällt eine Schutzschicht aus, bestehen weitere Barrieren.

### Merksatz

> **Keine einzelne Sicherheitsmaßnahme darf allein über die Sicherheit
> des gesamten Rechenzentrums entscheiden.**

------------------------------------------------------------------------

# 5. Sicherheitszonen

Bereiche werden abhängig vom Schutzbedarf in Zonen eingeteilt.

Beispiel:

``` text
Zone 0 → öffentlich
Zone 1 → kontrollierter Unternehmensbereich
Zone 2 → technischer Betriebsbereich
Zone 3 → Rechenzentrumsbereich
Zone 4 → besonders kritischer Sicherheitsbereich
```

Je höher die Zone, desto stärker können sein:

-   Identitätsprüfung
-   Zutrittsbeschränkung
-   Protokollierung
-   Überwachung
-   bauliche Sicherung
-   Vier-Augen-Prinzip

Die konkrete Zoneneinteilung ist organisationsabhängig.

------------------------------------------------------------------------

# 6. Physische Sicherheit

Physische Sicherheit schützt:

-   Menschen,
-   Gebäude,
-   IT-Systeme,
-   Datenträger,
-   Energieversorgung,
-   Kühlung,
-   Kommunikationswege

vor physischen Gefährdungen.

Typische Gefährdungen:

-   unbefugter Zutritt
-   Diebstahl
-   Sabotage
-   Feuer
-   Rauch
-   Wasser
-   Überspannung
-   Stromausfall
-   Überhitzung
-   Naturereignisse
-   Bauarbeiten
-   technische Defekte

------------------------------------------------------------------------

# 7. Standortwahl

Die Standortwahl ist eine der wichtigsten präventiven
Sicherheitsentscheidungen.

Zu untersuchen sind unter anderem:

-   Hochwasser- und Starkregenrisiko
-   Erdbeben
-   Sturm
-   Waldbrand
-   industrielle Gefahren
-   Gefahrgut
-   Flughäfen und Verkehrswege
-   kritische Nachbargebäude
-   Stromversorgung
-   Telekommunikationsanbindung
-   Erreichbarkeit
-   politische und rechtliche Rahmenbedingungen

### Wichtig

> Standortentscheidungen werden aus Schutzbedarf und Risikoanalyse
> abgeleitet. Es gibt keinen universell richtigen Mindestabstand für
> jedes Rechenzentrum.

------------------------------------------------------------------------

# 8. Georedundanz

Bei besonders hohen Verfügbarkeitsanforderungen können zwei räumlich
getrennte Rechenzentren eingesetzt werden.

Ziele:

-   Schutz vor großflächigem Stromausfall
-   Schutz vor Naturkatastrophen
-   Schutz vor regionalen Kommunikationsstörungen
-   Fortführung kritischer Dienste

Zu beachten:

-   unabhängige Stromversorgung
-   unabhängige Carrier/Trassen
-   gemeinsame Risikogebiete vermeiden
-   Replikationsverfahren
-   Datenkonsistenz
-   RPO/RTO
-   Umschaltverfahren

------------------------------------------------------------------------

# 9. Perimeterschutz

Der Perimeter bildet die äußere Sicherheitsgrenze.

Mögliche Maßnahmen:

-   Einfriedung
-   Sicherheitszaun
-   Zufahrtskontrolle
-   Poller
-   Schranken
-   Beleuchtung
-   Videoüberwachung
-   Einbruchmeldeanlage
-   Sicherheitsdienst

Ziel:

> Angriffe möglichst erkennen und verzögern, bevor kritische
> Gebäudebereiche erreicht werden.

------------------------------------------------------------------------

# 10. Mehrstufige Zutrittskontrolle

Beispiel:

``` text
1. Perimeter
      ↓
2. Gebäude
      ↓
3. Sicherheitszone
      ↓
4. RZ-Schleuse
      ↓
5. Serverraum
      ↓
6. Rack
```

Nicht jede Person, die das Gebäude betreten darf, darf auch das
Rechenzentrum betreten.

------------------------------------------------------------------------

# 11. Authentisierungsfaktoren beim Zutritt

## Wissen

-   PIN
-   Passwort

## Besitz

-   Chipkarte
-   Smartcard
-   Hardware-Token
-   Mobilgerät

## Inhärenz

-   Fingerabdruck
-   Gesicht
-   Iris

Für besonders kritische Bereiche können mehrere Faktoren kombiniert
werden.

Beispiel:

``` text
Chipkarte + PIN
```

------------------------------------------------------------------------

# 12. Personenschleusen

Eine Personenschleuse verhindert, dass mehrere Personen mit einer
einzigen Berechtigung eintreten.

Ziele:

-   Schutz gegen Tailgating
-   Identitätskontrolle
-   Vereinzelung
-   Protokollierung

Mögliche Ergänzungen:

-   Gewichtssensor
-   Kamera
-   Gegensprechanlage
-   biometrische Prüfung

Flucht- und Arbeitsschutzanforderungen müssen weiterhin eingehalten
werden.

------------------------------------------------------------------------

# 13. Besucherregelung

Besucher sollten nicht dieselben Rechte wie RZ-Mitarbeiter erhalten.

Typischer Prozess:

``` text
Anmeldung
   ↓
Identitätsprüfung
   ↓
Besucherausweis
   ↓
Begleitung
   ↓
Zutrittsprotokollierung
   ↓
Rückgabe des Ausweises
```

Zusätzlich möglich:

-   zeitlich begrenzte Berechtigungen
-   Zugang nur zu definierten Bereichen
-   NDA/Vertraulichkeitsvereinbarung
-   Verbot unbeaufsichtigter Tätigkeiten

------------------------------------------------------------------------

# 14. Zutritt, Zugang und Zugriff unterscheiden

  Begriff       Bedeutung
  ------------- --------------------------------------
  **Zutritt**   physischer Zugang zu Gebäuden/Räumen
  **Zugang**    Nutzung eines IT-Systems
  **Zugriff**   Nutzung bestimmter Daten/Funktionen

### Prüfungsbeispiel

> Chipkarte an der RZ-Tür = Zutrittskontrolle.

> MFA am Administrationssystem = Zugangskontrolle.

> RBAC auf einer Datenbank = Zugriffskontrolle.

------------------------------------------------------------------------

# 15. Videoüberwachung und Alarmanlagen

Videoüberwachung kann:

-   Ereignisse erkennen,
-   abschrecken,
-   Vorfälle rekonstruieren

helfen.

Zu beachten:

-   Kamerapositionen
-   tote Winkel
-   Aufzeichnungsqualität
-   Manipulationsschutz
-   Zeitsynchronisation
-   Aufbewahrungsdauer
-   Zugriffsschutz
-   Datenschutz

Alarmanlagen können überwachen:

-   Türen
-   Fenster
-   Bewegung
-   Glasbruch
-   Manipulation

------------------------------------------------------------------------

# 16. Brandschutz

Brandschutz besteht aus:

1.  **baulichem Brandschutz**
2.  **technischem Brandschutz**
3.  **organisatorischem Brandschutz**

## Baulich

-   Brandabschnitte
-   Brandschutztüren
-   feuerbeständige Wände
-   Kabelabschottungen

## Technisch

-   Rauchmelder
-   Brandfrüherkennung
-   Löschanlagen
-   Alarmierung

## Organisatorisch

-   Brandschutzordnung
-   Unterweisungen
-   Räumungskonzepte
-   Wartung
-   Übungen

------------------------------------------------------------------------

# 17. Brandfrüherkennung

In Rechenzentren ist eine möglichst frühe Erkennung wichtig.

Möglichkeiten:

-   punktförmige Rauchmelder
-   Rauchansaugsysteme / Aspirating Smoke Detection
-   Temperaturüberwachung

Rauchansaugsysteme untersuchen kontinuierlich Luftproben und können sehr
kleine Rauchpartikel früh erkennen.

------------------------------------------------------------------------

# 18. Löschanlagen

Mögliche Systeme:

-   Inertgaslöschung
-   chemische Gaslöschung
-   Wassernebel
-   Sprinkler je nach Gebäudekonzept

Bei Gaslöschanlagen sind insbesondere zu berücksichtigen:

-   Personenschutz
-   Voralarm
-   Evakuierungszeit
-   Druckentlastung
-   Raumdichtigkeit
-   Wartung

### Prüfungsfalle

> **„Im Serverraum darf niemals Wasser eingesetzt werden" ist zu
> pauschal.**

Das geeignete Löschkonzept wird durch Fachplanung, Risiko und bauliche
Anforderungen bestimmt.

------------------------------------------------------------------------

# 19. Schutz vor Wasser

Wasser kann entstehen durch:

-   Rohrbruch
-   Löschwasser
-   Starkregen
-   Hochwasser
-   Kondensat
-   Klimaanlagen

Maßnahmen:

-   wasserführende Leitungen vermeiden bzw. absichern
-   Leckagesensoren
-   geeignete Boden-/Raumplanung
-   Pumpen
-   Entwässerung
-   Hochwasserschutz

------------------------------------------------------------------------

# 20. Stromversorgung

Ein Rechenzentrum benötigt eine stabile und belastbare Stromversorgung.

Typischer Aufbau:

``` text
Stromnetz
   ↓
Hauptverteilung
   ↓
USV
   ↓
Unterverteilung
   ↓
PDU
   ↓
Server / Storage / Netzwerk
```

Bei hoher Verfügbarkeit kommen redundante Pfade hinzu.

------------------------------------------------------------------------

# 21. USV -- Unterbrechungsfreie Stromversorgung

Die USV schützt unter anderem gegen:

-   kurze Stromausfälle
-   Spannungseinbrüche
-   Spannungsspitzen
-   Netzschwankungen

Sie überbrückt die Zeit bis:

-   die Netzversorgung zurückkehrt oder
-   die Netzersatzanlage übernimmt.

### Wichtig

> Eine USV ist normalerweise **keine Ersatzstromversorgung für einen
> tagelangen Stromausfall**.

------------------------------------------------------------------------

# 22. Netzersatzanlage -- NEA

Eine NEA stellt bei längerem Stromausfall elektrische Energie bereit.

Typisch:

-   Dieselgenerator
-   andere geeignete Generator-/Energiesysteme

Zu planen sind:

-   Startautomatik
-   Kraftstoffvorrat
-   Nachbetankung
-   Wartung
-   Lasttests
-   Abgasführung
-   Ersatzteile
-   Ausfallszenarien

------------------------------------------------------------------------

# 23. Redundanzmodelle

## N

Genau die benötigte Kapazität.

Ausfall eines Elements kann zum Ausfall führen.

## N+1

Ein zusätzliches Element ist vorhanden.

Beispiel:

``` text
3 Klimageräte benötigt
+ 1 Reserve
= 4 Geräte
```

## 2N

Zwei vollständig dimensionierte, möglichst unabhängige Systeme.

## 2N+1

Zwei vollständige Pfade plus zusätzliche Reserve.

### Wichtig

> Mehr Redundanz erhöht die Verfügbarkeit, aber auch Kosten und
> Komplexität.

------------------------------------------------------------------------

# 24. A/B-Stromversorgung

Kritische Systeme können zwei unabhängige Strompfade erhalten.

``` text
Versorgung A ──┐
               ├── Server mit 2 Netzteilen
Versorgung B ──┘
```

Optimalerweise sind getrennt:

-   Einspeisung
-   USV
-   Verteilung
-   PDU
-   Netzteile

Geräte mit nur einem Netzteil können über geeignete Transfer-Switches
eingebunden werden.

------------------------------------------------------------------------

# 25. Klimatisierung

IT-Systeme erzeugen große Wärmemengen.

Zu überwachen sind:

-   Temperatur
-   Luftfeuchtigkeit
-   Luftstrom
-   Kühlleistung

Mögliche Konzepte:

-   Präzisionsklimatisierung
-   Kaltgang-/Warmgangtrennung
-   Einhausung
-   freie Kühlung
-   Flüssigkeitskühlung

------------------------------------------------------------------------

# 26. Kaltgang und Warmgang

Server werden so angeordnet, dass sich kalte und warme Luft möglichst
wenig vermischen.

``` text
Warmgang
↑       ↑
Rack   Rack
→ Kaltgang ←
Rack   Rack
↓       ↓
Warmgang
```

Vorteile:

-   effizientere Kühlung
-   geringere Hotspots
-   bessere Energieeffizienz

------------------------------------------------------------------------

# 27. Umgebungsmonitoring

Sensoren können überwachen:

-   Temperatur
-   Luftfeuchtigkeit
-   Wasser
-   Rauch
-   Türzustände
-   Strom
-   USV
-   Generator
-   Klima
-   Rackzustände

Alarmierung sollte möglichst automatisiert erfolgen.

Beispiele:

-   E-Mail
-   SMS
-   Bereitschaftssystem
-   Leitstelle
-   SIEM/Event-Management

------------------------------------------------------------------------

# 28. Verkabelung

Auch Kommunikations- und Stromverkabelung muss geschützt werden.

Maßnahmen:

-   getrennte Trassen
-   redundante Leitungswege
-   Brandschottung
-   Dokumentation
-   Schutz gegen mechanische Beschädigung
-   Schutz gegen Abhören
-   geeignete Kabelwege
-   klare Kennzeichnung

Bei hoher Verfügbarkeit sollten redundante Carrier nicht unbemerkt
dieselbe physische Trasse nutzen.

------------------------------------------------------------------------

# 29. Organisatorische Sicherheit

Technische Maßnahmen funktionieren nur mit geeigneten Prozessen.

Wichtige Bereiche:

-   Rollen und Verantwortlichkeiten
-   Richtlinien
-   Berechtigungsmanagement
-   Change Management
-   Incident Management
-   Patchmanagement
-   Wartung
-   Dokumentation
-   Awareness
-   Lieferantenmanagement
-   Notfallorganisation

------------------------------------------------------------------------

# 30. Rollen- und Berechtigungskonzept

Prinzipien:

-   Least Privilege
-   Need-to-know
-   Funktionstrennung
-   Vier-Augen-Prinzip
-   regelmäßige Rezertifizierung

Typische Rollen:

-   RZ-Leitung
-   Administrator
-   Netzwerkadministrator
-   Security Administrator
-   Backup Administrator
-   Facility Management
-   Informationssicherheitsbeauftragter
-   Datenschutzbeauftragter
-   Notfallbeauftragter

------------------------------------------------------------------------

# 31. Funktionstrennung

Kritische Aufgaben sollten nicht vollständig von einer einzelnen Person
kontrolliert werden.

Beispiel:

``` text
Administrator A → beantragt Änderung
Administrator B → prüft/genehmigt
System          → protokolliert
```

Ziel:

-   Missbrauch erschweren
-   Fehler reduzieren
-   Nachvollziehbarkeit erhöhen

------------------------------------------------------------------------

# 32. Privileged Access Management -- PAM

Privilegierte Administrationskonten benötigen besonderen Schutz.

Maßnahmen:

-   separate Admin-Konten
-   MFA
-   Just-in-Time-Rechte
-   Just-Enough-Administration
-   Passwort-/Secret-Vault
-   Session Recording
-   Genehmigungsworkflow
-   Jump Hosts / Bastion Hosts

------------------------------------------------------------------------

# 33. Change Management

Änderungen an kritischen Systemen müssen kontrolliert erfolgen.

Typischer Prozess:

``` text
Change Request
     ↓
Risikoanalyse
     ↓
Freigabe
     ↓
Test
     ↓
Implementierung
     ↓
Kontrolle
     ↓
Dokumentation
```

Für Notfälle kann ein definierter Emergency-Change-Prozess bestehen.

------------------------------------------------------------------------

# 34. Patch- und Schwachstellenmanagement

Ein kontinuierlicher Prozess umfasst:

1.  Assets erfassen
2.  Schwachstellen erkennen
3.  Risiko bewerten
4.  priorisieren
5.  Patch/Mitigation testen
6.  ausrollen
7.  Erfolg prüfen
8.  dokumentieren

Priorisierung kann berücksichtigen:

-   CVSS
-   tatsächliche Ausnutzbarkeit
-   Internetexposition
-   Schutzbedarf
-   Kritikalität des Systems
-   vorhandene Exploits

### Prüfungsfalle

> **CVSS allein ist keine vollständige Risikobewertung.**

------------------------------------------------------------------------

# 35. Kryptografische Sicherheit

Kryptografie unterstützt insbesondere:

-   Vertraulichkeit
-   Integrität
-   Authentizität
-   Nichtabstreitbarkeit

Wichtige Bereiche:

-   Verschlüsselung
-   Hashfunktionen
-   MAC
-   digitale Signaturen
-   Zertifikate
-   Schlüsselmanagement

------------------------------------------------------------------------

# 36. Data at Rest, in Transit und in Use

## At Rest

Gespeicherte Daten.

Beispiele:

-   Festplattenverschlüsselung
-   Datenbankverschlüsselung
-   Storage-Verschlüsselung

## In Transit

Übertragene Daten.

Beispiele:

-   TLS
-   IPsec
-   SSH

## In Use

Daten während der Verarbeitung.

Schutzmöglichkeiten können umfassen:

-   Prozessisolation
-   Trusted Execution Environments
-   Confidential Computing

------------------------------------------------------------------------

# 37. Symmetrische Verschlüsselung

Sender und Empfänger verwenden denselben geheimen Schlüssel.

Beispiel:

-   AES

Vorteile:

-   schnell
-   für große Datenmengen geeignet

Nachteil:

-   sicherer Schlüsselaustausch erforderlich

------------------------------------------------------------------------

# 38. AES

AES ist eine symmetrische Blockchiffre.

AES verwendet:

-   Blockgröße: **128 Bit**
-   Schlüssel: **128, 192 oder 256 Bit**

Bezeichnungen:

-   AES-128
-   AES-192
-   AES-256

### Wichtig

> Die Zahl bei AES bezeichnet die **Schlüssellänge**, nicht die
> Blockgröße.

Moderne Anwendungen verwenden AES zusammen mit einem geeigneten
Betriebsmodus, beispielsweise AEAD-Verfahren wie GCM.

------------------------------------------------------------------------

# 39. Asymmetrische Kryptografie

Es existiert ein Schlüsselpaar:

-   Public Key
-   Private Key

Anwendungen:

-   Schlüsselaustausch
-   digitale Signaturen
-   Zertifikate
-   Authentisierung

Beispiele:

-   RSA
-   elliptische Kurvenverfahren

Asymmetrische Kryptografie ist rechenintensiver als symmetrische
Kryptografie.

------------------------------------------------------------------------

# 40. Hybride Verschlüsselung

Moderne Protokolle kombinieren beide Verfahren.

Vereinfacht:

``` text
Asymmetrisches Verfahren
        ↓
sicherer Schlüsselaustausch
        ↓
symmetrischer Sitzungsschlüssel
        ↓
schnelle Datenverschlüsselung
```

Beispiel:

> TLS verwendet hybride kryptografische Mechanismen.

------------------------------------------------------------------------

# 41. One-Time Pad

Ein korrekt verwendetes One-Time Pad ist informationstheoretisch sicher,
wenn:

-   der Schlüssel wirklich zufällig ist,
-   mindestens so lang wie die Nachricht ist,
-   geheim bleibt,
-   exakt einmal verwendet wird.

Praktischer Nachteil:

> Das sichere Verteilen und Verwalten sehr großer Schlüssel macht das
> Verfahren für normale IT-Anwendungen unpraktisch.

------------------------------------------------------------------------

# 42. Hashfunktionen

Hashfunktionen erzeugen aus Daten einen Hashwert fester Länge.

Eigenschaften einer kryptografischen Hashfunktion:

-   Einwegfunktion
-   Kollisionsresistenz
-   Änderungen am Eingang verändern den Hash

Anwendungen:

-   Integritätsprüfung
-   digitale Signaturen
-   Passwortspeicherung als Bestandteil geeigneter
    Password-Hashing-Verfahren

### Wichtig

> Hashing ist **keine Verschlüsselung**, da kein
> Entschlüsselungsschlüssel vorgesehen ist.

------------------------------------------------------------------------

# 43. Digitale Signaturen

Digitale Signaturen schützen insbesondere:

-   Integrität
-   Authentizität
-   je nach Kontext Nichtabstreitbarkeit

Vereinfacht:

``` text
Dokument
   ↓
Hash
   ↓
Signatur mit privatem Schlüssel
   ↓
Empfänger prüft mit öffentlichem Schlüssel
```

### Präzisierung

> Der Hash wird bei modernen Signaturverfahren nicht einfach allgemein
> „mit dem privaten Schlüssel verschlüsselt". Eine digitale Signatur ist
> eine definierte kryptografische Signaturoperation.

------------------------------------------------------------------------

# 44. PKI -- Public Key Infrastructure

Eine PKI verwaltet:

-   Zertifikate
-   Schlüssel
-   Vertrauensketten
-   Sperrinformationen

Typische Komponenten:

-   Root CA
-   Intermediate CA
-   Registration Authority
-   Zertifikatsrepository
-   CRL
-   OCSP

Zertifikatstypen:

-   TLS
-   S/MIME
-   Code Signing
-   Client Authentication

------------------------------------------------------------------------

# 45. Schlüsselmanagement

Der gesamte Lebenszyklus eines Schlüssels muss geschützt werden:

``` text
Erzeugung
   ↓
Speicherung
   ↓
Verteilung
   ↓
Nutzung
   ↓
Rotation
   ↓
Sperrung
   ↓
Archivierung
   ↓
Vernichtung
```

Fehler im Schlüsselmanagement können eine starke Verschlüsselung
wirkungslos machen.

------------------------------------------------------------------------

# 46. HSM -- Hardware Security Module

Ein HSM schützt kryptografische Schlüssel und führt kryptografische
Operationen in einer besonders geschützten Umgebung aus.

Funktionen:

-   Schlüsselgenerierung
-   Schlüsselspeicherung
-   Signieren
-   Entschlüsseln
-   Zugriffskontrolle
-   Auditierung
-   Manipulationsschutz

Einsatz:

-   PKI
-   TLS
-   Code Signing
-   Zahlungsverkehr
-   Cloud Key Management

### Präzisierung zu den Folien

> Ein Cloud Key Vault ist nicht automatisch dasselbe wie ein dediziertes
> HSM. Cloudanbieter bieten sowohl Key-Management-Dienste als auch
> HSM-basierte bzw. dedizierte HSM-Angebote an.

------------------------------------------------------------------------

# 47. BYOK und HYOK

## BYOK -- Bring Your Own Key

Der Kunde erzeugt bzw. kontrolliert Schlüsselmaterial und bringt es in
die Cloud-Schlüsselverwaltung ein.

## HYOK -- Hold Your Own Key

Schlüssel bleiben stärker unter externer bzw. kundeneigener Kontrolle.

Ziele:

-   stärkere Kontrolle
-   Compliance
-   Trennung von Provider und Schlüsselbesitz

Nachteile:

-   höhere Komplexität
-   Verfügbarkeitsrisiken
-   anspruchsvolleres Lifecycle-Management

------------------------------------------------------------------------

# 48. Key Rotation

Schlüssel werden regelmäßig oder ereignisbezogen ersetzt.

Auslöser:

-   Zeitintervall
-   Verdacht auf Kompromittierung
-   Mitarbeiterwechsel
-   Richtlinien
-   kryptografische Migration

Zu beachten:

-   Schlüsselversionen
-   Alt-Daten
-   Anwendungen
-   Trust Chains
-   Secrets
-   IAM
-   Logging

------------------------------------------------------------------------

# 49. Authentisierung

Faktoren:

  Faktor         Beispiele
  -------------- ------------------------------
  **Wissen**     Passwort, PIN
  **Besitz**     Smartcard, Token, Smartphone
  **Inhärenz**   Fingerabdruck, Gesicht

**MFA** kombiniert mindestens zwei unabhängige Faktoren.

Beispiel:

``` text
Passwort + Hardware-Token
```

------------------------------------------------------------------------

# 50. Netzwerksicherheit

Ziele:

-   Vertraulichkeit
-   Integrität
-   Verfügbarkeit
-   Authentizität

Typische Maßnahmen:

-   Firewall
-   IDS/IPS
-   Segmentierung
-   VPN/ZTNA
-   NAC
-   sichere Routingkonfiguration
-   DNS-Sicherheit
-   DDoS-Schutz
-   Monitoring
-   Verschlüsselung

------------------------------------------------------------------------

# 51. Netzwerksegmentierung

Das Netzwerk wird in Sicherheitsbereiche getrennt.

Beispiel:

``` text
Internet
   │
Firewall
   │
  DMZ
   │
Firewall
   │
Applikationszone
   │
Firewall / ACL
   │
Datenbankzone
```

Vorteile:

-   Begrenzung lateraler Bewegung
-   kleinere Angriffsflächen
-   gezieltere Regeln
-   bessere Überwachung

------------------------------------------------------------------------

# 52. Typisches Zonenmodell im RZ

  Zone              Beispiele                          Schutzmaßnahmen
  ----------------- ---------------------------------- ---------------------------------
  **Public/Edge**   Internet-Uplinks                   DDoS-Schutz, Edge-Firewall
  **DMZ**           Web, Reverse Proxy, Mail Gateway   Firewall, IDS/IPS
  **Application**   Applikationsserver                 Segmentierung, ACL
  **Database**      Datenbanken                        strikte Zugriffspfade
  **Management**    Admin, Monitoring                  MFA, Jump Hosts
  **Storage**       SAN/NAS                            Isolation, ACL, Verschlüsselung
  **Backup**        Backupserver/Vault                 Isolation, Immutable Backup

------------------------------------------------------------------------

# 53. Firewall

Eine Firewall kontrolliert Netzwerkkommunikation anhand definierter
Regeln.

Typen:

-   Host-/Personal Firewall
-   Netzwerk-Firewall
-   Next-Generation Firewall
-   virtuelle/Cloud-Firewall
-   Web Application Firewall

### Prüfungsfalle

> AWS Security Groups oder Azure NSGs sind virtuelle Netzwerkfilter bzw.
> verteilte Firewall-Funktionen, aber nicht mit jeder Funktion einer
> klassischen Hardware-/NGFW gleichzusetzen.

------------------------------------------------------------------------

# 54. IDS und IPS

## IDS -- Intrusion Detection System

-   erkennt verdächtige Aktivitäten
-   alarmiert
-   blockiert nicht zwingend

## IPS -- Intrusion Prevention System

-   erkennt Angriffe
-   kann Datenverkehr automatisiert blockieren

### Merksatz

> **IDS erkennt -- IPS kann eingreifen.**

------------------------------------------------------------------------

# 55. VPN und ZTNA

## VPN

Erstellt einen verschlüsselten Tunnel und ermöglicht typischerweise
Netzwerkzugriff.

## ZTNA

Gewährt identitäts- und kontextbezogenen Zugriff auf definierte
Anwendungen oder Ressourcen.

### Wichtig

> ZTNA ist nicht einfach „ein besseres VPN", sondern folgt einem anderen
> Zugriffsmodell. Beide Technologien können je nach Anwendungsfall
> nebeneinander bestehen.

------------------------------------------------------------------------

# 56. Zero Trust

Grundidee:

> **Never trust, always verify** -- Vertrauen wird nicht allein aufgrund
> eines Netzwerkstandorts vergeben.

Zero Trust berücksichtigt:

-   Benutzeridentität
-   Gerät
-   Gerätezustand
-   Anwendung
-   Ressource
-   Kontext
-   Risiko

Maßnahmen:

-   MFA
-   Mikrosegmentierung
-   Conditional Access
-   ZTNA
-   Least Privilege
-   kontinuierliches Monitoring

------------------------------------------------------------------------

# 57. Mikrosegmentierung

Mikrosegmentierung trennt Systeme oder Workloads noch feiner als
klassische VLAN-Segmentierung.

Beispiel:

``` text
Webserver A
   │ nur TCP 443
   ▼
API Server
   │ nur TCP 5432
   ▼
Datenbank
```

Nicht erforderliche Kommunikation wird unterbunden.

------------------------------------------------------------------------

# 58. Network Access Control -- NAC

NAC prüft Geräte vor bzw. beim Netzwerkzugriff.

Mögliche Kriterien:

-   Identität
-   Zertifikat
-   Gerätetyp
-   Patchstand
-   Sicherheitssoftware
-   Compliance-Status

Nicht konforme Geräte können:

-   blockiert,
-   isoliert oder
-   in ein Quarantänenetz verschoben

werden.

------------------------------------------------------------------------

# 59. DNS-Sicherheit

DNS ist eine kritische Infrastrukturkomponente.

Gefährdungen:

-   DNS Spoofing
-   Cache Poisoning
-   DDoS
-   manipulierte Zonen
-   DNS Tunneling

Maßnahmen:

-   DNSSEC für Authentizität/Integrität von DNS-Daten
-   getrennte autoritative und rekursive Resolver
-   Zugriffskontrollen
-   Logging
-   redundante DNS-Server
-   sichere Zonentransfers
-   Monitoring

------------------------------------------------------------------------

# 60. DDoS-Schutz

Distributed-Denial-of-Service-Angriffe versuchen Dienste durch
Überlastung unerreichbar zu machen.

Schutzmaßnahmen:

-   Upstream-/Provider-Schutz
-   Scrubbing
-   Rate Limiting
-   Anycast
-   CDN
-   Load Balancing
-   skalierbare Architektur
-   WAF bei Anwendungsschichtangriffen

------------------------------------------------------------------------

# 61. Serversicherheit

Server sollten gehärtet werden.

Maßnahmen:

-   Minimalinstallation
-   unnötige Dienste deaktivieren
-   sichere Baselines
-   Patchmanagement
-   EDR
-   Host-Firewall
-   MFA für Administration
-   separate Admin-Konten
-   Logging
-   Secure Boot/TPM, wo sinnvoll
-   Konfigurationsmanagement

------------------------------------------------------------------------

# 62. Hardening

Hardening reduziert die Angriffsfläche.

Beispiele:

-   Standardkonten deaktivieren
-   sichere Cipher Suites
-   unnötige Ports schließen
-   Standardpasswörter ändern
-   Dienste entfernen
-   restriktive Dateirechte
-   sichere Registry-/Kernel-Einstellungen

Grundlage können sein:

-   BSI-Anforderungen
-   Herstellerempfehlungen
-   CIS Benchmarks
-   eigene Security Baselines

------------------------------------------------------------------------

# 63. Virtualisierungssicherheit

Zu schützen sind:

-   Hypervisor
-   Managementschnittstelle
-   virtuelle Netzwerke
-   VM-Templates
-   Storage
-   Backups

Maßnahmen:

-   Managementnetz isolieren
-   MFA
-   Hypervisor patchen
-   Rollen trennen
-   sichere Templates
-   keine unnötigen virtuellen Geräte
-   Logging

### Prüfungsfalle

> Eine VM ist nicht automatisch vollständig von anderen VMs isoliert,
> wenn Hypervisor oder Managementebene kompromittiert sind.

------------------------------------------------------------------------

# 64. Containersicherheit

Zu beachten:

-   vertrauenswürdige Images
-   Image Scanning
-   minimale Images
-   Secrets Management
-   Runtime Security
-   Netzwerk-Policies
-   Least Privilege
-   keine unnötig privilegierten Container
-   Patch-/Lifecycle-Management

------------------------------------------------------------------------

# 65. Storage-Sicherheit

Schutzmaßnahmen:

-   Verschlüsselung at rest
-   Zugriffskontrolle
-   getrennte Storage-Netze
-   sichere SAN-Zonen
-   LUN Masking
-   Snapshots
-   Integritätsprüfungen
-   Backup
-   Monitoring

### Merksatz

> **RAID schützt Verfügbarkeit -- Backup schützt
> Wiederherstellbarkeit.**

------------------------------------------------------------------------

# 66. Backup-Sicherheit

Ein belastbares Konzept berücksichtigt:

-   3-2-1 bzw. erweiterte Strategien
-   Offsite-Kopie
-   Immutable/WORM
-   Air Gap
-   Verschlüsselung
-   getrennte Backup-Accounts
-   MFA
-   Restore-Tests
-   Monitoring

### Wichtig

> Replikation allein ist kein Backup, da auch Fehler, Löschungen oder
> Ransomware repliziert werden können.

------------------------------------------------------------------------

# 67. Logging

Sicherheitsrelevante Ereignisse müssen nachvollziehbar sein.

Beispiele:

-   Anmeldungen
-   fehlgeschlagene Anmeldungen
-   Admin-Aktionen
-   Firewall-Ereignisse
-   IDS/IPS
-   Änderungen
-   Zutritte
-   Backupfehler
-   HSM-/PKI-Ereignisse

Logs müssen gegen Manipulation geschützt werden.

------------------------------------------------------------------------

# 68. Zeitsynchronisation

Für die Korrelation von Ereignissen müssen Systeme eine konsistente
Zeitbasis besitzen.

Typisch:

-   NTP
-   abgesicherte interne Zeitquellen

Warum wichtig?

``` text
Firewall: 14:02:13
Server:   14:02:14
IAM:      14:02:15
```

Nur mit konsistenter Zeit lassen sich Vorfälle zuverlässig
rekonstruieren.

------------------------------------------------------------------------

# 69. SIEM

Ein **Security Information and Event Management** sammelt und korreliert
Sicherheitsereignisse.

Ablauf:

``` text
Logquellen
   ↓
zentrale Sammlung
   ↓
Normalisierung
   ↓
Korrelation
   ↓
Alarm
   ↓
Analyse / Response
```

Quellen:

-   Firewall
-   Server
-   IAM
-   EDR
-   IDS/IPS
-   Cloud
-   Anwendungen

------------------------------------------------------------------------

# 70. SOC

Ein **Security Operations Center** überwacht und bearbeitet
Sicherheitsereignisse.

Aufgaben:

-   Monitoring
-   Alert Triage
-   Incident Detection
-   Analyse
-   Threat Hunting
-   Incident Response
-   Reporting

Ein SIEM ist ein Werkzeug -- ein SOC ist eine organisatorische Funktion
bzw. Einheit.

------------------------------------------------------------------------

# 71. Incident Response

Typischer Ablauf:

``` text
Vorbereitung
   ↓
Erkennung
   ↓
Analyse
   ↓
Eindämmung
   ↓
Beseitigung
   ↓
Wiederherstellung
   ↓
Lessons Learned
```

Wichtige Anforderungen:

-   Eskalationswege
-   Verantwortlichkeiten
-   Kommunikationsplan
-   Beweissicherung
-   Meldepflichten
-   Dokumentation

------------------------------------------------------------------------

# 72. Forensik und Beweissicherung

Bei Sicherheitsvorfällen können digitale Beweise erforderlich sein.

Grundsätze:

-   Veränderungen minimieren
-   Chain of Custody
-   Zeitpunkte dokumentieren
-   Hashwerte bilden
-   Originale schützen
-   Zugriffe protokollieren

------------------------------------------------------------------------

# 73. BCM und Disaster Recovery

**BCM** betrachtet die Fortführung kritischer Geschäftsprozesse.

**Disaster Recovery** fokussiert stärker auf die technische
Wiederherstellung.

Wichtige Größen:

-   RPO
-   RTO
-   MTPD/MTA

### Zusammenhang

``` text
Geschäftsprozess
     ↓
BIA
     ↓
RTO / RPO
     ↓
IT-Architektur
     ↓
Backup / Redundanz / DR
```

------------------------------------------------------------------------

# 74. Business Impact Analysis -- BIA

Die BIA ermittelt Auswirkungen von Ausfällen.

Untersucht werden:

-   kritische Prozesse
-   zeitliche Kritikalität
-   Abhängigkeiten
-   Ressourcen
-   Schadensentwicklung
-   Wiederanlaufprioritäten

Die BIA ist eine Grundlage für Notfall- und Wiederanlaufstrategien.

------------------------------------------------------------------------

# 75. Notfallvorsorge

Ein RZ benötigt vorbereitete Pläne für Szenarien wie:

-   Stromausfall
-   Ausfall der Kühlung
-   Brand
-   Wasser
-   Cyberangriff
-   Ransomware
-   Carrier-Ausfall
-   Storage-Ausfall
-   Personalausfall
-   Naturkatastrophe

------------------------------------------------------------------------

# 76. Notfall- und Wiederanlauftests

Pläne müssen getestet werden.

Testformen:

-   Dokumentenreview
-   Walkthrough
-   Tabletop Exercise
-   technische Wiederherstellung
-   Failover-Test
-   Vollübung

### Merksatz

> **Ein nicht getesteter Notfallplan ist nur eine Annahme.**

------------------------------------------------------------------------

# 77. Hochverfügbarkeit vs. Disaster Recovery

## High Availability

Ziel:

> lokale bzw. unmittelbare Ausfälle möglichst ohne längere
> Dienstunterbrechung abfangen.

Beispiele:

-   Cluster
-   redundante Netzteile
-   Dual Fabric
-   Load Balancer

## Disaster Recovery

Ziel:

> Wiederherstellung nach größeren Störungen oder Katastrophen.

Beispiele:

-   zweites Rechenzentrum
-   Wiederherstellung aus Backup
-   DR-Site

### Prüfungsfalle

> Hochverfügbarkeit ersetzt kein Backup und kein vollständiges
> Disaster-Recovery-Konzept.

------------------------------------------------------------------------

# 78. Lieferanten- und Dienstleistermanagement

RZ-Sicherheit hängt häufig von Dritten ab.

Beispiele:

-   Stromversorger
-   Carrier
-   Wartungsfirmen
-   Cloudanbieter
-   Hardwarelieferanten
-   Reinigung
-   Sicherheitsdienst

Zu regeln:

-   Sicherheitsanforderungen
-   SLAs
-   Zutrittsrechte
-   Vertraulichkeit
-   Incident-Meldung
-   Subdienstleister
-   Exit
-   Auditrechte

------------------------------------------------------------------------

# 79. Wartung und Fremdpersonal

Besondere Risiken entstehen bei:

-   Technikern
-   Reinigung
-   Lieferanten
-   externen Administratoren

Maßnahmen:

-   Voranmeldung
-   Identitätsprüfung
-   zeitlich begrenzte Berechtigung
-   Begleitung
-   Protokollierung
-   Vier-Augen-Prinzip
-   Remote-Zugriffe nur kontrolliert

------------------------------------------------------------------------

# 80. Asset Management

Man kann nur schützen, was bekannt ist.

Ein Asset-Inventar sollte umfassen:

-   Server
-   Netzwerkgeräte
-   Storage
-   VMs
-   Anwendungen
-   Lizenzen
-   Datenträger
-   Zertifikate
-   Cloudressourcen
-   Supportsysteme

Zusätzliche Informationen:

-   Eigentümer
-   Standort
-   Kritikalität
-   Schutzbedarf
-   Lifecycle
-   Abhängigkeiten

------------------------------------------------------------------------

# 81. Konfigurationsmanagement

Sichere Konfigurationen sollten:

-   definiert,
-   versioniert,
-   freigegeben,
-   überwacht,
-   regelmäßig geprüft

werden.

Infrastructure as Code kann dabei unterstützen, Änderungen
reproduzierbar und nachvollziehbar umzusetzen.

------------------------------------------------------------------------

# 82. Datenschutz im Rechenzentrum

Personenbezogene Daten unterliegen weiterhin der DSGVO.

Relevant sind unter anderem:

-   Art. 5 -- Grundsätze
-   Art. 25 -- Datenschutz durch Technikgestaltung
-   Art. 28 -- Auftragsverarbeitung
-   Art. 32 -- Sicherheit der Verarbeitung
-   Art. 33/34 -- Datenschutzverletzungen
-   Kapitel V -- Drittlandübermittlungen

Art. 32 verlangt risikoadäquate technische und organisatorische
Maßnahmen.

------------------------------------------------------------------------

# 83. Technische und organisatorische Maßnahmen -- TOM

Beispiele:

-   Zutrittskontrolle
-   Zugangskontrolle
-   Zugriffskontrolle
-   Verschlüsselung
-   Protokollierung
-   Backup
-   Wiederherstellung
-   Verfügbarkeitsmaßnahmen
-   regelmäßige Überprüfung der Wirksamkeit

------------------------------------------------------------------------

# 84. NIS-2 / BSIG und KRITIS

Für betroffene Unternehmen können zusätzliche Anforderungen gelten.

Themen sind insbesondere:

-   Risikomanagementmaßnahmen
-   Incident Handling
-   Business Continuity
-   Lieferkettensicherheit
-   Schwachstellenmanagement
-   Kryptografie
-   Zugriffskontrolle
-   MFA
-   Melde- und Registrierungspflichten

### Wichtig

> Ob ein Unternehmen unter NIS-2/BSIG oder KRITIS-Regelungen fällt,
> hängt von Sektor, Größe, Tätigkeit und gegebenenfalls gesetzlichen
> Schwellenwerten ab.

------------------------------------------------------------------------

# 85. BSI IT-Grundschutz für Rechenzentren

Besonders relevant sind unter anderem:

-   **INF.1 Allgemeines Gebäude**
-   **INF.2 Rechenzentrum sowie Serverraum**
-   **INF.12 Verkabelung**

Je nach Architektur kommen weitere Bausteine hinzu, beispielsweise aus:

-   NET
-   SYS
-   OPS
-   ORP
-   CON
-   DER
-   APP

### Wichtig

> Rechenzentrumssicherheit ist im IT-Grundschutz kein einzelner
> isolierter Baustein, sondern entsteht durch die Modellierung aller
> relevanten Zielobjekte.

------------------------------------------------------------------------

# 86. BSI INF.2 -- Rechenzentrum sowie Serverraum

Der Baustein adressiert den sicheren Betrieb von Rechenzentren und
Serverräumen.

Typische Themen:

-   Planung
-   Zutritt
-   Strom
-   Klima
-   Brand
-   technische Infrastruktur
-   Überwachung
-   Betrieb
-   Dokumentation

Für Gebäude und allgemeine Verkabelung sind zusätzlich entsprechende
Infrastrukturbausteine zu berücksichtigen.

------------------------------------------------------------------------

# 87. DIN EN 50600

Die Normenreihe **DIN EN 50600** behandelt
Rechenzentrumsinfrastrukturen.

Themen umfassen unter anderem:

-   Gebäudekonstruktion
-   Stromversorgung
-   Umgebungsbedingungen
-   Telekommunikationsverkabelung
-   Sicherheitssysteme
-   Betrieb

Sie ist besonders für Planung, Bau und Betrieb professioneller
Rechenzentren relevant.

------------------------------------------------------------------------

# 88. ISO/IEC 27001

ISO/IEC 27001 definiert Anforderungen an ein ISMS.

Für Rechenzentren relevante Themen aus Annex A umfassen beispielsweise:

-   physische Sicherheit
-   Zugriffskontrolle
-   Kryptografie
-   Betriebssicherheit
-   Netzwerksicherheit
-   Lieferanten
-   Incident Management
-   Business Continuity

### Merksatz

> ISO 27001 definiert das Managementsystem; IT-Grundschutz und
> technische Normen können bei der konkreten Umsetzung unterstützen.

------------------------------------------------------------------------

# 89. Security by Design

Sicherheit wird bereits bei Planung und Beschaffung berücksichtigt.

Beispiele:

-   Sicherheitszonen bereits im Gebäudeentwurf
-   redundante Kabelwege
-   A/B-Stromversorgung
-   Managementnetz getrennt planen
-   sichere Standardkonfigurationen
-   Logging von Anfang an
-   Backup und Restore vor Produktivstart planen

------------------------------------------------------------------------

# 90. Security by Default

Systeme werden standardmäßig sicher ausgeliefert bzw. konfiguriert.

Beispiele:

-   unnötige Ports geschlossen
-   MFA aktiviert
-   restriktive Berechtigungen
-   Logging aktiv
-   sichere Protokolle
-   keine Standardpasswörter

------------------------------------------------------------------------

# 91. Least Privilege

Benutzer und Systeme erhalten nur Rechte, die für ihre Aufgabe
erforderlich sind.

Beispiel:

> Ein Backupdienst benötigt Zugriff auf Sicherungsdaten, aber nicht
> automatisch Domain-Admin-Rechte.

Vorteile:

-   kleinere Angriffsfläche
-   geringerer Schaden bei kompromittierten Konten
-   bessere Trennung von Verantwortlichkeiten

------------------------------------------------------------------------

# 92. Need-to-know

Zugriff wird nicht allein aufgrund einer Rolle vergeben, sondern nur,
wenn die konkrete Information benötigt wird.

Beispiel:

> Ein RZ-Techniker darf Hardware warten, benötigt aber nicht automatisch
> Zugriff auf Kundendaten.

------------------------------------------------------------------------

# 93. Vier-Augen-Prinzip

Besonders kritische Vorgänge werden von mindestens zwei autorisierten
Personen kontrolliert.

Beispiele:

-   HSM-Schlüsselzeremonie
-   Löschung kritischer Backups
-   Änderung zentraler Firewallregeln
-   Zugriff auf besonders geschützte Bereiche

------------------------------------------------------------------------

# 94. Sicherheitsmonitoring

Ein ganzheitliches Monitoring umfasst:

## IT

-   CPU/RAM
-   Netzwerk
-   Storage
-   Dienste

## Security

-   SIEM
-   IDS/IPS
-   EDR
-   IAM
-   Schwachstellen

## Facility

-   Strom
-   USV
-   Generator
-   Klima
-   Temperatur
-   Wasser
-   Brand
-   Zutritt

------------------------------------------------------------------------

# 95. Kennzahlen und KPIs

Mögliche Kennzahlen:

-   Verfügbarkeit
-   Anzahl kritischer Schwachstellen
-   Patch Compliance
-   MTTD -- Mean Time to Detect
-   MTTR -- Mean Time to Respond/Repair, je nach Kontext
-   Backup-Erfolgsrate
-   Restore-Erfolgsrate
-   Anzahl unberechtigter Zutrittsversuche
-   USV-/NEA-Testquote
-   Incident-Anzahl

------------------------------------------------------------------------

# 96. Risikoanalyse

Vorgehen:

``` text
Asset / Geschäftsprozess
        ↓
Gefährdung
        ↓
Schwachstelle
        ↓
Eintrittshäufigkeit
        ↓
Schadensauswirkung
        ↓
Risiko
        ↓
Behandlung
```

Möglichkeiten:

-   vermeiden
-   reduzieren
-   übertragen
-   akzeptieren

------------------------------------------------------------------------

# 97. Beispiel Risiko: Stromausfall

**Gefährdung:** Ausfall der öffentlichen Stromversorgung

**Auswirkung:**

-   Serverausfall
-   Datenverlust
-   Geschäftsunterbrechung

**Maßnahmen:**

-   USV
-   NEA
-   redundante Einspeisung
-   A/B-Verteilung
-   Tests
-   Monitoring

**Restrisiko:**

> z.  B. gleichzeitiger Ausfall mehrerer Versorgungskomponenten.

------------------------------------------------------------------------

# 98. Beispiel Risiko: Ransomware

**Gefährdung:** kompromittiertes Administratorkonto

**Mögliche Folgen:**

-   Verschlüsselung von Servern
-   Löschung von Backups
-   Produktionsausfall

**Maßnahmen:**

-   MFA
-   PAM
-   Netzwerksegmentierung
-   EDR
-   Immutable Backup
-   getrennte Backup-Identitäten
-   SIEM
-   Restore-Tests

------------------------------------------------------------------------

# 99. Beispiel Risiko: Kühlungsausfall

**Gefährdung:** Ausfall der Klimatisierung

**Folgen:**

-   Überhitzung
-   Hardwareabschaltung
-   Hardwaredefekt

**Maßnahmen:**

-   N+1-Kühlung
-   Temperatursensoren
-   Alarmierung
-   Wartung
-   definierte Notabschaltung

------------------------------------------------------------------------

# 100. Typischer Aufbau eines sicheren Rechenzentrums

``` text
                         Internet
                            │
                      DDoS-Schutz
                            │
                      Edge-Firewall
                            │
                           DMZ
                            │
                      interne Firewall
                            │
              ┌─────────────┼─────────────┐
              │             │             │
         Web/App-Zone   Management     Monitoring
              │             │             │
              │        PAM / MFA          SIEM
              │             │             │
              └─────── Datenbank ─────────┘
                          │
                        Storage
                          │
                        Backup
                  ┌───────┴────────┐
                  │                │
              Immutable         Offsite
                  │                │
                  └──── Restore-Test
```

Physisch darunter:

``` text
Perimeter
   ↓
Gebäude
   ↓
Sicherheitszone
   ↓
Schleuse
   ↓
RZ
   ↓
Rack

+ redundante Stromversorgung
+ redundante Kühlung
+ Brand-/Wasserschutz
+ Umgebungsmonitoring
```

------------------------------------------------------------------------

# 101. Typischer Ablauf zur Erstellung eines RZ-Securitykonzeptes

``` text
Geschäftsprozesse erfassen
        ↓
Assets und Abhängigkeiten erfassen
        ↓
Schutzbedarf feststellen
        ↓
Gefährdungen identifizieren
        ↓
Risiken bewerten
        ↓
Soll-Sicherheitsarchitektur entwickeln
        ↓
physische Maßnahmen
        ↓
technische Maßnahmen
        ↓
organisatorische Maßnahmen
        ↓
Notfall-/Backupkonzept
        ↓
Umsetzung
        ↓
Tests und Abnahme
        ↓
Monitoring
        ↓
regelmäßige Verbesserung
```

------------------------------------------------------------------------

# 102. Typische IHK-Prüfungsfrage: Zutrittskontrolle

## Aufgabe

> Erläutern Sie vier Stufen eines Zutrittskontrollsystems für ein
> Rechenzentrum.

## Musterantwort

**1. Perimeterschutz**

Zaun, Beleuchtung, Videoüberwachung und kontrollierte Zufahrten
verhindern bzw. erschweren das unbemerkte Erreichen des Gebäudes.

**2. Gebäudeauthentisierung**

Mitarbeiter authentisieren sich beispielsweise mit Chipkarte und PIN.

**3. RZ-Sicherheitszone**

Eine Personenschleuse mit MFA verhindert Tailgating und stellt sicher,
dass nur einzeln autorisierte Personen eintreten.

**4. Rack-/Systembereich**

Besonders kritische Racks oder Bereiche besitzen zusätzliche
Schließsysteme und werden vollständig protokolliert.

------------------------------------------------------------------------

# 103. Typische IHK-Prüfungsfrage: Katastrophenschutz

## Aufgabe

> Erläutern Sie drei Anforderungen an Katastrophenschutz und redundante
> Infrastruktur eines Rechenzentrums.

## Musterantwort

**Redundante Stromversorgung**

USV und Netzersatzanlage stellen den Betrieb auch bei Ausfall der
öffentlichen Versorgung sicher.

**Redundante Klimatisierung**

Eine N+1- oder höher ausgelegte Kühlung verhindert, dass der Ausfall
eines Klimagerätes unmittelbar zur Überhitzung führt.

**Brandschutz**

Brandfrüherkennung, bauliche Brandabschnitte und eine geeignete
Löschanlage reduzieren die Gefahr eines vollständigen RZ-Ausfalls.

------------------------------------------------------------------------

# 104. Typische IHK-Prüfungsfrage: Netzwerksicherheit

## Aufgabe

> Nennen und erläutern Sie fünf Maßnahmen zur Absicherung des
> RZ-Netzwerks.

Mögliche Antwort:

1.  **Firewall** → kontrolliert Kommunikationsbeziehungen.
2.  **Segmentierung** → trennt Sicherheitszonen und begrenzt laterale
    Bewegungen.
3.  **IDS/IPS** → erkennt bzw. blockiert Angriffsversuche.
4.  **MFA/PAM** → schützt administrative Zugänge.
5.  **SIEM** → korreliert Ereignisse und ermöglicht frühzeitige
    Angriffserkennung.

------------------------------------------------------------------------

# 105. Typische IHK-Prüfungsfrage: Verschlüsselung

## Aufgabe

> Unterscheiden Sie symmetrische und asymmetrische Verschlüsselung.

**Symmetrisch:**

-   gleicher geheimer Schlüssel
-   hohe Geschwindigkeit
-   für große Datenmengen
-   Beispiel AES

**Asymmetrisch:**

-   Public-/Private-Key-Paar
-   aufwendiger
-   für Signaturen, Authentisierung und Schlüsselaustausch
-   Beispiele RSA bzw. elliptische Kurvenverfahren

Moderne Systeme kombinieren häufig beide Verfahren.

------------------------------------------------------------------------

# 106. Typische IHK-Prüfungsfrage: Zero Trust

## Musterantwort

> Zero Trust geht davon aus, dass weder Benutzer noch Geräte allein
> aufgrund ihres Netzwerkstandorts automatisch vertrauenswürdig sind.
> Jeder Zugriff wird abhängig von Identität, Gerätezustand,
> Zielressource und Kontext geprüft. Typische Maßnahmen sind MFA, Least
> Privilege, Mikrosegmentierung, Conditional Access, ZTNA und
> kontinuierliches Monitoring.

------------------------------------------------------------------------

# 107. Typische IHK-Prüfungsfrage: USV und NEA

> Eine USV stellt bei einer Unterbrechung unmittelbar Energie bereit und
> stabilisiert die Stromversorgung. Ihre Überbrückungszeit ist jedoch
> begrenzt. Eine Netzersatzanlage übernimmt bei längeren Stromausfällen
> die Energieversorgung. In einem hochverfügbaren Rechenzentrum werden
> beide Systeme kombiniert und regelmäßig getestet.

------------------------------------------------------------------------

# 108. Typische IHK-Prüfungsfrage: IDS und IPS

> Ein IDS erkennt verdächtige Netzwerkaktivitäten und erzeugt Meldungen.
> Ein IPS kann zusätzlich aktiv in den Datenverkehr eingreifen und
> erkannte Angriffe blockieren. Ein IPS birgt daher bei
> Fehlklassifikationen ein höheres Risiko, legitimen Datenverkehr zu
> unterbrechen.

------------------------------------------------------------------------

# 109. Typische IHK-Prüfungsfrage: Sicherheitszonen

> Sicherheitszonen gruppieren Systeme und Bereiche mit ähnlichem
> Schutzbedarf. Übergänge zwischen Zonen werden kontrolliert. Dadurch
> werden Angriffsflächen reduziert und laterale Bewegungen eines
> Angreifers erschwert. Beispiele sind DMZ, Applikationszone,
> Datenbankzone, Managementzone, Storagezone und Backupzone.

------------------------------------------------------------------------

# 110. Typische Prüfungsfallen

-   **Firewall = vollständiges Securitykonzept** → falsch
-   **RAID = Backup** → falsch
-   **Replikation = Backup** → falsch
-   **USV = unbegrenzte Notstromversorgung** → falsch
-   **Hohe Verfügbarkeit = Disaster Recovery** → falsch
-   **VLAN allein = vollständige Sicherheitssegmentierung** → zu kurz
    gegriffen
-   **VPN = automatisch Zero Trust** → falsch
-   **IDS blockiert immer Angriffe** → falsch
-   **IPS erkennt nur, blockiert aber nie** → falsch
-   **Hashing = Verschlüsselung** → falsch
-   **Digitale Signatur = komplette Datei mit Private Key
    verschlüsseln** → fachlich zu vereinfacht
-   **AES-256 besitzt 256-Bit-Blöcke** → falsch; AES hat 128-Bit-Blöcke
-   **Cloud Key Vault = immer dediziertes HSM** → falsch
-   **Biometrie allein ist automatisch MFA** → falsch
-   **Mehr Redundanz = automatisch mehr Sicherheit** → falsch;
    Komplexität und Common-Mode-Fehler beachten
-   **Zutritt, Zugang und Zugriff sind dasselbe** → falsch
-   **Zero Trust bedeutet, niemandem zu vertrauen** → zu ungenau;
    Zugriffe werden explizit und kontinuierlich bewertet
-   **Security by Design = nachträgliches Hardening** → falsch
-   **CVSS = Risiko** → falsch; CVSS ist ein technischer
    Schweregradindikator, Risiko benötigt Kontext
-   **Ein erfolgreiches Backup = garantiert erfolgreicher Restore** →
    falsch
-   **ISO 27001 schreibt konkrete RZ-Hardware vor** → falsch

------------------------------------------------------------------------

# ⚡ Schnellcheck -- 60 Sekunden vor der Prüfung

-   **CIA** → Vertraulichkeit / Integrität / Verfügbarkeit
-   **Defense in Depth** → mehrere Schutzschichten
-   **Security by Design** → Sicherheit von Anfang an
-   **Least Privilege** → minimale Rechte
-   **Need-to-know** → Zugriff nur bei fachlichem Bedarf
-   **Zutritt** → Raum
-   **Zugang** → IT-System
-   **Zugriff** → Daten/Funktionen
-   **Perimeter → Gebäude → Schleuse → RZ → Rack**
-   **MFA** → mindestens zwei unabhängige Faktoren
-   **USV** → sofortige Überbrückung
-   **NEA** → längere Ersatzstromversorgung
-   **N+1** → eine Reserve
-   **2N** → zwei vollständige Pfade
-   **A/B** → redundante Strompfade
-   **Kalt-/Warmgang** → Luftströme trennen
-   **Brandfrüherkennung** → möglichst vor Vollbrand erkennen
-   **Wasser** → Leckageüberwachung
-   **Segmentierung** → laterale Bewegung begrenzen
-   **DMZ** → extern erreichbare Dienste isolieren
-   **IDS** → erkennen
-   **IPS** → erkennen + blockieren
-   **NAC** → Gerätezugang prüfen
-   **ZTNA** → anwendungsbezogener, identitätsbasierter Zugriff
-   **Zero Trust** → explizit prüfen, minimale Rechte, kontinuierlich
    überwachen
-   **PAM** → privilegierte Zugriffe schützen
-   **SIEM** → Logs sammeln und korrelieren
-   **SOC** → Security-Überwachung organisatorisch durchführen
-   **AES** → symmetrisch, 128-Bit-Block, 128/192/256-Bit-Schlüssel
-   **RSA/ECC** → asymmetrische Verfahren
-   **Hash** → Einwegfunktion, keine Verschlüsselung
-   **Signatur** → Integrität + Authentizität
-   **PKI** → Zertifikate und Vertrauensketten
-   **HSM** → Schlüssel besonders schützen
-   **BYOK/HYOK** → unterschiedliche Modelle der Schlüsselhoheit
-   **RPO** → tolerierbarer Datenverlust
-   **RTO** → Wiederanlaufziel
-   **MTPD/MTA** → maximal tolerierbare Ausfallzeit
-   **BCM** → Geschäftsfortführung
-   **DR** → technische Wiederherstellung
-   **Immutable Backup** → gegen Änderung/Löschung geschützt
-   **Restore-Test** → Wiederherstellbarkeit beweisen
-   **INF.2** → Rechenzentrum sowie Serverraum
-   **DIN EN 50600** → RZ-Infrastruktur
-   **ISO 27001** → ISMS
-   **BSI IT-Grundschutz** → konkrete Methodik und Anforderungen

------------------------------------------------------------------------

# Prüfungs-Merksätze

> **Physische Sicherheit beginnt am Grundstück -- nicht an der
> Serverraumtür.**

> **Zutritt schützt Räume, Zugang schützt Systeme, Zugriff schützt
> Daten.**

> **USV überbrückt -- die Netzersatzanlage versorgt länger.**

> **Redundanz reduziert Ausfallrisiken, ersetzt aber weder Backup noch
> Notfallplanung.**

> **IDS erkennt -- IPS kann verhindern.**

> **Segmentierung begrenzt den Blast Radius eines Angriffs.**

> **Zero Trust ersetzt nicht jede andere Sicherheitsmaßnahme, sondern
> verändert das Vertrauens- und Zugriffsmodell.**

> **Starke Kryptografie mit schlechtem Schlüsselmanagement ist keine
> starke Sicherheitslösung.**

> **Ein SIEM ist ein Werkzeug; ein SOC ist eine organisatorische
> Fähigkeit.**

> **Ein Rechenzentrum ist nur so resilient wie seine schwächste
> kritische Abhängigkeit.**

> **Sicherheit muss geplant, umgesetzt, überwacht, getestet und
> kontinuierlich verbessert werden.**

------------------------------------------------------------------------

# Quellen und weiterführende Referenzen

## BSI

-   BSI IT-Grundschutz-Kompendium
-   BSI-Baustein **INF.1 Allgemeines Gebäude**
-   BSI-Baustein **INF.2 Rechenzentrum sowie Serverraum**
-   BSI-Baustein **INF.12 Verkabelung**
-   BSI-Standards 200-1 bis 200-4
-   BSI: Standort-Kriterien für Rechenzentren
-   BSI TR-02102 -- Kryptographische Verfahren: Empfehlungen und
    Schlüssellängen

## Normen

-   ISO/IEC 27001:2022 -- Informationssicherheitsmanagementsysteme
-   ISO/IEC 27002:2022 -- Informationssicherheitsmaßnahmen
-   DIN EN 50600 -- Einrichtungen und Infrastrukturen von Rechenzentren

## Recht

-   Datenschutz-Grundverordnung (DSGVO)
-   BSIG in aktueller Fassung
-   NIS-2-Umsetzung in Deutschland
-   KRITIS-Dachgesetz und einschlägige sektorale Anforderungen, soweit
    anwendbar

------------------------------------------------------------------------

# Hinweis

Dieses Handout ist als **Lern- und Prüfungshilfe** konzipiert. Konkrete
Redundanzklassen, bauliche Vorgaben, kryptografische Schlüssellängen,
gesetzliche Pflichten und technische Detailanforderungen müssen für
reale Rechenzentren anhand des aktuellen Schutzbedarfs, der
Risikoanalyse, der jeweils geltenden Normen und Gesetze sowie der
aktuellen BSI-Empfehlungen festgelegt werden.
