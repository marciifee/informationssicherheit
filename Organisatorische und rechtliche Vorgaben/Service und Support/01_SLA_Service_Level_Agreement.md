# Lernblatt / Handout: Service Level Agreement (SLA) & Service Level Management

### Kompaktes Nachschlagewerk für die IHK-Prüfung „Geprüfter Berufsspezialist für Informationssicherheit“

**Stand: 31. August 2026**  
**Schwerpunkt:** SLA-Aufbau, Servicequalität, Verfügbarkeit, Incident-Priorisierung, Reporting, Eskalation, ITIL-Bezug und IT-Sicherheit

> **Hinweis:** Dieses Handout dient der Weiterbildung und Prüfungsvorbereitung. Konkrete SLA-Klauseln müssen für reale Verträge rechtlich und technisch geprüft werden.

---

# ⚡ Schnellcheck vor der Prüfung

- **SLA** = Service Level Agreement: Vereinbarung über messbare Qualität eines IT-Service.
- Ein SLA muss den **Service eindeutig beschreiben**.
- Typische Inhalte: Servicezeiten, Verfügbarkeit, Reaktionszeit, Wiederherstellungs-/Lösungszeit, Prioritäten, Wartungsfenster, Eskalation, Reporting, Verantwortlichkeiten und Rechtsfolgen.
- **SLI** = gemessener Indikator.
- **SLO** = Zielwert für einen Indikator.
- **SLA** = vertragliche Vereinbarung, die Serviceziele und weitere Regelungen enthält.
- **KPI** = Leistungskennzahl zur Steuerung; nicht jeder KPI ist automatisch ein SLA-Ziel.
- **Reaktionszeit** ≠ **Lösungszeit**.
- **MTTR** ist ohne Definition mehrdeutig: Repair, Restore, Resolve oder Recovery können gemeint sein.
- **Verfügbarkeit** braucht Messperiode, Messpunkt, Berechnungsformel und Ausschlüsse.
- **Wartungsfenster** müssen definiert werden.
- **Incident-Priorität** wird sinnvollerweise aus **Impact × Urgency** abgeleitet.
- **OLA** = interne Vereinbarung zwischen beteiligten Organisationseinheiten.
- **Underpinning Contract (UC)** = unterstützender Vertrag mit externem Lieferanten.
- **Service Credits** sind vertragliche Gutschriften bei Zielverfehlung; sie sind nicht automatisch Schadensersatz.
- Ein SLA ersetzt kein BCM- oder Sicherheitskonzept.
- **RTO/RPO** aus BCM sind von Support-Reaktionszeiten zu unterscheiden.

---

# 1. Was ist ein SLA?

Ein Service Level Agreement beschreibt die zwischen Service Provider und Kunde vereinbarte Servicequalität.

Ein gutes SLA beantwortet mindestens:

```text
Welcher Service?
      ↓
Für wen?
      ↓
Wann?
      ↓
In welcher Qualität?
      ↓
Wie wird gemessen?
      ↓
Was passiert bei Abweichungen?
```

Ziel ist, Erwartungen messbar und überprüfbar zu machen.

---

# 2. SLA und Service Level Management

**Service Level Management (SLM)** ist die Managementpraxis, mit der Serviceziele:

- vereinbart,
- dokumentiert,
- überwacht,
- gemessen,
- berichtet,
- überprüft und
- verbessert

werden.

Das SLA ist also ein **Ergebnis bzw. Werkzeug** des Service Level Managements.

---

# 3. SLA, SLI, SLO und KPI

| Begriff | Bedeutung | Beispiel |
|---|---|---|
| **SLI** | gemessener Serviceindikator | gemessene Verfügbarkeit 99,96 % |
| **SLO** | Zielwert | ≥ 99,9 % |
| **SLA** | vertragliche Vereinbarung | 99,9 % Monatsverfügbarkeit |
| **KPI** | Steuerungskennzahl | First Contact Resolution 80 % |

### Merksatz

> **SLI misst – SLO setzt das Ziel – SLA vereinbart – KPI steuert.**

---

# 4. Typische Bestandteile eines SLA

Ein SLA sollte abhängig vom Service enthalten:

1. Parteien und Ansprechpartner
2. Servicebezeichnung
3. Leistungsbeschreibung und Scope
4. Servicezeiten
5. Supportzeiten
6. Verfügbarkeit
7. Performance
8. Incident-Prioritäten
9. Reaktionszeiten
10. Wiederherstellungs-/Lösungszeiten
11. Wartungsfenster
12. Monitoring und Messverfahren
13. Reporting
14. Eskalation
15. Mitwirkungspflichten
16. Informationssicherheitsanforderungen
17. BCM-/Notfallanforderungen
18. Ausnahmen und Ausschlüsse
19. Service Credits / Vertragsfolgen
20. Laufzeit, Änderung und Kündigung

---

# 5. Scope – was ist abgedeckt?

Der SLA-Scope muss klar beschreiben:

- Anwendungen
- Infrastruktur
- Standorte
- Nutzergruppen
- Schnittstellen
- Servicekomponenten
- Supportleistungen

Ebenso wichtig:

## Out of Scope

Beispiele:

- neue Funktionen
- Projektleistungen
- kundenseitig verursachte Änderungen
- nicht vereinbarte Drittprodukte

### Prüfungsmerksatz

> **Eine Funktionsänderung ist nicht automatisch ein Incident.**

---

# 6. Servicezeit und Supportzeit

## Servicezeit

Zeit, in der der IT-Service vereinbarungsgemäß bereitstehen soll.

Beispiel:

> 24×7

## Supportzeit

Zeit, in der Supportpersonal mit garantierten Reaktionszeiten erreichbar ist.

Beispiel:

> Mo–Fr 08:00–18:00 Uhr

### Wichtig

Ein Dienst kann 24×7 verfügbar sein, obwohl der Support nur 8×5 garantiert ist.

---

# 7. Verfügbarkeit

Allgemeine Berechnung:

```text
Verfügbarkeit =
(Servicezeit - anrechenbare Ausfallzeit)
----------------------------------------
              Servicezeit
× 100 %
```

Beispiel:

Servicezeit pro Monat: 720 h  
anrechenbare Ausfallzeit: 43 min = 0,7167 h

```text
(720 - 0,7167) / 720 × 100 ≈ 99,9005 %
```

---

# 8. Zulässige Ausfallzeit

Theoretische maximale Ausfallzeit bei kontinuierlicher Messung:

| Ziel | ca. pro 30 Tage |
|---|---:|
| 99 % | 7 h 12 min |
| 99,9 % | 43 min 12 s |
| 99,95 % | 21 min 36 s |
| 99,99 % | 4 min 19 s |
| 99,999 % | 26 s |

### Wichtig

Diese Werte gelten nur unter der vereinfachten Annahme einer 24×7-Messperiode ohne vertragliche Ausschlüsse.

---

# 9. Messperiode

Verfügbarkeit muss auf eine definierte Periode bezogen werden.

Beispiele:

- Kalendermonat
- Quartal
- Jahr

### Prüfungsfalle

> **99,9 % pro Monat ist nicht dasselbe wie 99,9 % pro Jahr.**

---

# 10. Messpunkt

Der Vertrag muss definieren, **wo** Verfügbarkeit gemessen wird.

Beispiele:

- Provider-Rechenzentrum
- Load Balancer
- API-Endpunkt
- Kundenzugang
- End-to-End aus Nutzersicht

Unterschiedliche Messpunkte können zu unterschiedlichen Ergebnissen führen.

---

# 11. Geplante und ungeplante Nichtverfügbarkeit

## Geplant

- Wartungsfenster
- angekündigte Changes
- Releases

## Ungeplant

- Incident
- Hardwareausfall
- Netzwerkstörung

Im SLA muss stehen, welche Downtime in die Verfügbarkeitsberechnung einfließt.

---

# 12. Wartungsfenster

Regeln sollten enthalten:

- Zeitpunkt
- Dauer
- Ankündigungsfrist
- maximale Häufigkeit
- Notfallwartung
- Kommunikation
- Einfluss auf Verfügbarkeit

---

# 13. Ausschluss- und Suspendierungszeiten

Mögliche vertragliche Ausschlüsse:

- vereinbarte Wartung
- kundenseitig verursachte Verzögerung
- fehlender Zutritt/Zugang
- fehlende Mitwirkung
- höhere Gewalt
- bestimmte Drittanbieterereignisse

### Prüfungsfalle

> Je mehr Zeiten ausgeschlossen werden, desto weniger aussagekräftig kann die nominelle Verfügbarkeit werden.

---

# 14. Incident

Ein Incident ist eine ungeplante Unterbrechung oder Qualitätsminderung eines Service bzw. ein Ausfall eines Configuration Item, der den Service noch nicht beeinträchtigt hat.

Ziel des Incident Managements:

> normalen Servicebetrieb möglichst schnell wiederherstellen und negative Auswirkungen minimieren.

---

# 15. Incident vs. Service Request vs. Problem

| Begriff | Beispiel |
|---|---|
| **Incident** | E-Mail-Service ausgefallen |
| **Service Request** | neues Benutzerkonto |
| **Problem** | unbekannte Ursache wiederholter Mail-Ausfälle |

### Merksatz

> **Incident = Service wiederherstellen. Problem = Ursache verstehen und nachhaltig behandeln.**

---

# 16. Impact und Urgency

## Impact

Wie groß sind die Auswirkungen?

Beispiele:

- Anzahl Nutzer
- Umsatz
- kritischer Geschäftsprozess
- regulatorische Auswirkung

## Urgency

Wie schnell muss gehandelt werden?

Aus Impact und Urgency wird häufig die Priorität abgeleitet.

---

# 17. Beispiel Prioritätsmatrix

| Impact \ Urgency | hoch | mittel | niedrig |
|---|---:|---:|---:|
| **hoch** | P1 | P1/P2 | P2 |
| **mittel** | P2 | P2/P3 | P3 |
| **niedrig** | P3 | P3/P4 | P4 |

Die konkrete Matrix ist organisationsabhängig.

---

# 18. Beispiel Prioritäten

## P1 – kritisch

- zentraler Service ausgefallen
- viele Nutzer
- kein Workaround

## P2 – hoch

- erhebliche Einschränkung
- wichtiger Prozess betroffen
- ggf. eingeschränkter Workaround

## P3 – mittel

- Teilfunktion betroffen
- akzeptabler Workaround

## P4 – niedrig

- geringe Beeinträchtigung

---

# 19. Reaktionszeit

Zeit von einem definierten Startpunkt bis zur qualifizierten Reaktion bzw. Arbeitsaufnahme.

Mögliche Definition:

```text
Ticket registriert
      ↓
Reaktionszeit
      ↓
Bearbeitung qualifiziert aufgenommen
```

### Wichtig

Start- und Endereignis müssen vertraglich exakt festgelegt werden.

---

# 20. Interventionszeit

In manchen SLAs:

> Zeit bis ein Techniker aktiv mit der Störungsbearbeitung beginnt oder vor Ort eingreift.

Der Begriff ist nicht überall identisch definiert.

Deshalb:

> SLA-Glossar verwenden.

---

# 21. Lösungszeit / Resolution Time

Zeit bis der Incident vollständig gelöst ist.

Kann sich unterscheiden von:

- Reaktionszeit
- Wiederherstellungszeit
- Workaround-Zeit

---

# 22. Wiederherstellungszeit / Restore Time

Zeit bis der Service wieder nutzbar ist.

Ein Workaround kann den Service wiederherstellen, obwohl die Root Cause noch nicht beseitigt ist.

```text
Incident
  ↓
Workaround
  ↓
Service restored
  ↓
Root Cause Fix
  ↓
vollständige Lösung
```

---

# 23. MTTR – Vorsicht mit der Abkürzung

MTTR wird unterschiedlich verwendet:

- Mean Time to Repair
- Mean Time to Restore
- Mean Time to Resolve
- Mean Time to Recovery

### Prüfungsmerksatz

> **MTTR nie ohne ausgeschriebene Definition verwenden.**

Außerdem ist ein **Mittelwert** nicht dasselbe wie eine garantierte maximale Lösungszeit.

---

# 24. Weitere Kennzahlen

- MTTA – Mean Time to Acknowledge
- MTTD – Mean Time to Detect
- MTBF – Mean Time Between Failures
- First Contact Resolution
- Ticket Backlog
- Incident Rate
- Customer Satisfaction

---

# 25. RTO und RPO sind keine normalen SLA-Reaktionszeiten

## RTO

geforderte Wiederanlaufzeit aus BCM/Disaster Recovery.

## RPO

maximal tolerierbarer Datenverlust in Zeit.

### Unterschied

> SLA-Reaktionszeit misst Supportverhalten.  
> RTO/RPO beschreiben Kontinuitäts- bzw. Wiederherstellungsziele.

Sie können vertraglich in einem SLA oder einer Serviceanlage festgelegt werden, sind aber fachlich andere Größen.

---

# 26. Service Desk

Der Service Desk ist der zentrale Kommunikationspunkt zwischen Service Provider und Nutzern.

Aufgaben:

- Incidents aufnehmen
- Service Requests bearbeiten
- kommunizieren
- Tickets koordinieren
- Statusinformationen bereitstellen

### Begriff

**SPOC = Single Point of Contact**

---

# 27. Eskalation

## Funktionale Eskalation

Weitergabe an spezialisierte technische Ebene.

```text
1st Level
   ↓
2nd Level
   ↓
3rd Level / Hersteller
```

## Hierarchische Eskalation

Management wird wegen Bedeutung, Risiko oder Zeitüberschreitung eingebunden.

---

# 28. OLA – Operational Level Agreement

Interne Vereinbarung zur Unterstützung eines Kunden-SLA.

Beispiel:

```text
Kunden-SLA:
P1 Restore ≤ 4 h

internes OLA:
Netzwerkteam Diagnose ≤ 30 min
DB-Team Analyse ≤ 30 min
```

---

# 29. Underpinning Contract (UC)

Vertrag mit externem Lieferanten, der einen eigenen Service unterstützt.

Beispiel:

```text
Kunden-SLA
    ↓
eigener IT-Service
    ↓
Carrier-UC
```

### Wichtig

Der Lieferantenvertrag sollte nicht schwächer sein als das, was für das eigene SLA benötigt wird.

---

# 30. Service Level Reporting

Ein Report kann enthalten:

- Verfügbarkeit
- Anzahl Incidents
- SLA-Verletzungen
- Reaktionszeiten
- Restore-/Resolution-Zeiten
- Trends
- Problemfälle
- Service Credits
- Maßnahmen

---

# 31. Service Review

Regelmäßiges Meeting zwischen Provider und Kunde.

Themen:

- SLA-Erfüllung
- wiederkehrende Incidents
- Kapazität
- Risiken
- geplante Änderungen
- Verbesserungen

---

# 32. Messqualität

Messung muss:

- nachvollziehbar
- reproduzierbar
- manipulationsgeschützt
- zeitlich synchronisiert

sein.

Regeln:

- Quelle
- Tool
- Zeitzone
- Messintervall
- Rundung
- Datenaufbewahrung

---

# 33. Service Credits

Vertragliche Gutschrift, wenn Serviceziele verfehlt werden.

Beispiel:

| Monatsverfügbarkeit | Gutschrift |
|---|---:|
| ≥ 99,9 % | 0 % |
| 99,0–99,899 % | 5 % |
| < 99,0 % | 10 % |

Das ist nur ein Beispiel.

---

# 34. Vertragsstrafe vs. Service Credit vs. Schadensersatz

| Instrument | Zweck |
|---|---|
| Service Credit | vereinbarte Gutschrift |
| Vertragsstrafe | pauschalierte Sanktion bei vereinbartem Pflichtverstoß |
| Schadensersatz | Ausgleich eines ersatzfähigen Schadens |

Die Rechtsfolgen hängen vom Vertrag und geltendem Recht ab.

---

# 35. Mitwirkungspflichten des Kunden

Beispiele:

- vollständige Störungsmeldung
- Ansprechpartner erreichbar
- Remote-/Vor-Ort-Zugang
- Freigaben
- Testdaten
- Änderungen kommunizieren

Fehlende Mitwirkung kann SLA-Zeiten beeinflussen, wenn das vertraglich sauber geregelt ist.

---

# 36. Informationssicherheit im SLA

Mögliche Security Service Levels:

- Patchfrist
- Reaktionszeit auf Security Incidents
- Log-Retention
- Backup-Erfolg
- Restore-Test
- Schwachstellenbehebung
- MFA
- Verschlüsselung
- Security Reporting

---

# 37. Beispiel Patch-SLA

| Kritikalität | Ziel |
|---|---|
| Kritisch / aktiv ausgenutzt | z. B. ≤ 24–72 h |
| Hoch | z. B. ≤ 7 Tage |
| Mittel | z. B. ≤ 30 Tage |
| Niedrig | planmäßig |

Werte sind **organisations- und risikobasiert**, keine universellen gesetzlichen Standardfristen.

---

# 38. Datenschutz im SLA

Bei personenbezogenen Daten zusätzlich beachten:

- AVV/DPA
- TOM
- Data-Breach-Meldung
- Unterauftragnehmer
- Löschung
- Drittlandtransfer

SLA und AVV erfüllen unterschiedliche Zwecke.

---

# 39. SLA und BCM

Mögliche Kontinuitätsanforderungen:

- RTO
- RPO
- Notbetriebsniveau
- DR-Test
- Backup
- Ersatzstandort
- Wiederanlauf

---

# 40. SLA und ITIL 4

Service Level Management soll Serviceziele geschäftsorientiert vereinbaren und tatsächliche Serviceerfahrung laufend betrachten.

Wichtig:

> Nicht nur technische Messwerte betrachten, sondern auch, ob der Kunde den benötigten Wert erhält.

---

# 41. SLA und ISO/IEC 20000

ISO/IEC 20000-1 ist eine Managementsystemnorm für Service Management.

Sie fordert einen systematischen Ansatz zur:

- Planung
- Gestaltung
- Transition
- Bereitstellung
- Überwachung
- Verbesserung

von Services.

ITIL kann als Best-Practice-Framework bei der Umsetzung unterstützen.

---

# 42. Typische IHK-Prüfungsfrage

## „Nennen Sie fünf Inhalte eines SLA.“

Mögliche Antwort:

1. Leistungsbeschreibung
2. Service-/Supportzeiten
3. Verfügbarkeit
4. Reaktions- und Wiederherstellungszeiten
5. Priorisierung
6. Wartungsfenster
7. Reporting
8. Eskalation
9. Verantwortlichkeiten

---

# 43. Typische IHK-Prüfungsfrage

## „Erläutern Sie Reaktionszeit und Lösungszeit.“

> Die Reaktionszeit beschreibt die Zeit bis zur vereinbarten qualifizierten Reaktion bzw. Aufnahme der Bearbeitung. Die Lösungszeit beschreibt die Zeit bis zur vollständigen Behebung. Ein Anbieter kann daher die Reaktionszeit einhalten, obwohl der Incident noch lange nicht gelöst ist.

---

# 44. Typische IHK-Prüfungsfrage

## „Warum müssen Wartungsfenster definiert werden?“

> Damit eindeutig geregelt ist, wann geplante Unterbrechungen erlaubt sind, wie früh sie angekündigt werden müssen und ob diese Zeiten in die Verfügbarkeitsberechnung einfließen.

---

# 45. Typische Prüfungsfallen

- SLA = nur Verfügbarkeitszahl → falsch
- Supportzeit = Servicezeit → nicht zwingend
- Reaktionszeit = Lösungszeit → falsch
- MTTR = garantiertes Maximum → falsch
- MTTR immer Repair → falsch
- 99,9 % ohne Messperiode → unvollständig
- hohe Verfügbarkeit = Backup → falsch
- SLA = BCM → falsch
- SLA = AVV → falsch
- P1 nur technisch definieren → Geschäftsimpact berücksichtigen
- Service Credit = automatisch Schadensersatz → falsch
- OLA = Kundenvertrag → falsch
- UC = interne Vereinbarung → falsch

---

# ⚡ 60-Sekunden-Schnellcheck

- SLA = vertragliche Servicequalität
- SLI = Messwert
- SLO = Ziel
- KPI = Steuerungskennzahl
- Scope / Out of Scope
- Servicezeit ≠ Supportzeit
- Availability braucht Messperiode
- Impact × Urgency → Priority
- Incident ≠ Problem
- Reaktion ≠ Restore ≠ Resolution
- MTTR ausschreiben
- OLA = intern
- UC = Lieferant
- Service Desk = SPOC
- funktionale + hierarchische Eskalation
- Reporting + Review
- Service Credits
- Security SLA
- RTO/RPO ≠ normale Supportzeiten
- ITIL SLM ↔ SLA

---

# Quellen

- Kursunterlagen „Inhalte SLA“
- Kursunterlage „Beispiel SLA“
- ITIL-4-Kursunterlagen
- ISO/IEC 20000-1:2018 + Amendment 1:2024
