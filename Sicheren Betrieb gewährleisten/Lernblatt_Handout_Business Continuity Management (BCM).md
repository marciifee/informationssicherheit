# Lernblatt / Handout: Business Continuity Management (BCM)

### Kompaktes Nachschlagewerk für die IHK-Prüfung „Geprüfter Berufsspezialist für Informationssicherheit“

**Stand: 30. August 2026**  
**Grundlage:** BSI-Standard 200-4 „Business Continuity Management“, Version 1.0

---

# ⚡ Schnellcheck vor der Prüfung

## Die wichtigsten Begriffe

- **BC** = Business Continuity → angestrebter Zustand der Geschäftskontinuität
- **BCM** = Business Continuity Management → Managementprozess zur Sicherstellung der Geschäftskontinuität
- **BCMS** = Business Continuity Management System → Managementsystem zur systematischen Steuerung des BCM
- **BIA** = Business Impact Analyse → Auswirkungen von Prozessausfällen untersuchen
- **BCB** = Business Continuity Beauftragte
- **AAO** = Allgemeine Aufbauorganisation → normale Organisationsstruktur
- **BAO** = Besondere Aufbauorganisation → temporäre Organisationsstruktur für Notfälle/Krisen
- **GFP** = Geschäftsfortführungsplan
- **WAP** = Wiederanlaufplan
- **WHP** = Wiederherstellungsplan
- **NuK-Kommunikation** = Notfall- und Krisen-Kommunikation

## Störung – Notfall – Krise

- **Störung** → im Normalbetrieb durch die AAO beherrschbar
- **Notfall** → zeitkritischer Geschäftsprozess betroffen; Bewältigung benötigt eine BAO
- **Krise** → außergewöhnliche Lage mit hohem Entscheidungs- und Koordinationsbedarf; vorhandene Pläne reichen gegebenenfalls nicht aus

## Die vier wichtigsten BIA-Kenngrößen

- **MTPD / MTA** → maximal tolerierbare Ausfallzeit
- **RTO / WAZ** → geforderte Wiederanlaufzeit
- **RPO** → maximal zulässiger Datenverlust
- **MBCO** → notwendiges Leistungsniveau des Notbetriebs

### Merksatz

> **MTPD = Wie lange darf der Prozess maximal ausfallen?**  
> **RTO = Wie schnell muss die BC-Lösung funktionieren?**  
> **RPO = Wie viele Daten dürfen maximal verloren gehen?**  
> **MBCO = Wie leistungsfähig muss der Notbetrieb mindestens sein?**

## Wichtigste Beziehung

> **RTO < MTPD**

Zwischen RTO und MTPD muss ausreichend Zeit für Reaktion, Detektion und weitere Unsicherheiten berücksichtigt werden.

## RTA und RPA

- **RTA** = Recovery Time Actual → tatsächlich bzw. zugesichert erreichbare Wiederanlaufzeit
- **RPA** = Recovery Point Actual → tatsächlich bzw. zugesichert erreichbarer maximaler Datenverlust

Soll:

> **RTA ≤ RTO**  
> **RPA ≤ RPO**

## Drei BCMS-Stufen

1. **Reaktiv-BCMS** → schneller rudimentärer Einstieg
2. **Aufbau-BCMS** → schrittweiser Ausbau und Erweiterung des Prozessumfangs
3. **Standard-BCMS** → vollständiges, ISO-22301-kompatibles BCMS

## BCB

- zentrale Ansprechperson für BCM
- koordiniert BCM-Aufgaben
- unterstützt die Institutionsleitung
- **Stabsstelle direkt bei der Leitung wird empfohlen**
- Verortung z. B. innerhalb der IT-Linie sollte wegen möglicher Interessenkonflikte vermieden werden

## PDCA

- **Plan** → planen
- **Do** → umsetzen
- **Check** → überprüfen
- **Act** → verbessern

---

# 1. Grundlagen

**Business Continuity Management (BCM)** ist ein ganzheitlicher Managementprozess, mit dem eine Institution Vorsorge für schwerwiegende Betriebsunterbrechungen trifft und sicherstellt, dass **zeitkritische Geschäftsprozesse bei einem Notfall auf einem festgelegten Niveau fortgeführt bzw. innerhalb definierter Zeiten wieder aufgenommen werden können**.

BCM betrachtet dabei nicht nur IT-Ausfälle, sondern beispielsweise auch:

- Strom- und Versorgungsausfälle
- Cyberangriffe
- Ausfälle von Gebäuden
- Personalausfälle
- Ausfälle von Dienstleistern
- Lieferkettenunterbrechungen
- Naturereignisse
- sonstige schwerwiegende Schadensereignisse

## BC, BCM und BCMS

| Begriff | Bedeutung |
|---|---|
| **BC – Business Continuity** | angestrebter Zustand, in dem zeitkritische Geschäftsprozesse trotz eines Schadensereignisses angemessen fortgeführt werden können |
| **BCM – Business Continuity Management** | Managementprozess zur Herstellung, Aufrechterhaltung und Verbesserung der Business Continuity |
| **BCMS – Business Continuity Management System** | Managementsystem aus Prozessen, Rollen, Verantwortlichkeiten, Methoden, Dokumentationen und Ressourcen zur systematischen Steuerung des BCM |

## BCM und Informationssicherheit

BCM und Informationssicherheit überschneiden sich insbesondere beim Schutzziel **Verfügbarkeit**, sind jedoch nicht identisch.

**Informationssicherheit** schützt insbesondere:

- Vertraulichkeit
- Integrität
- Verfügbarkeit

von Informationen.

**BCM** konzentriert sich dagegen auf die **Fortführung zeitkritischer Geschäftsprozesse** bei schwerwiegenden Unterbrechungen.

Dabei betrachtet BCM neben IT-Ressourcen auch:

- Personal
- Gebäude
- Informationen
- Betriebsmittel
- Dienstleister und Lieferanten

### Merksatz

> **IT-Ausfall kann ein BCM-Szenario sein – BCM ist aber wesentlich mehr als IT-Notfallmanagement.**

Das speziell auf IT-Dienste und IT-Ressourcen ausgerichtete Kontinuitätsmanagement wird als **IT Service Continuity Management (ITSCM)** bezeichnet.

## Ziele des BCM

BCM soll insbesondere:

- zeitkritische Geschäftsprozesse aufrechterhalten oder rechtzeitig wieder aufnehmen,
- Schäden durch Betriebsunterbrechungen begrenzen,
- die Handlungs- und Entscheidungsfähigkeit erhalten,
- gesetzliche, regulatorische und vertragliche Anforderungen unterstützen,
- die Widerstandsfähigkeit der Institution erhöhen,
- Kunden und andere Interessengruppen weiterhin angemessen versorgen.

## Regulatorische Bedeutung

Business Continuity kann Bestandteil gesetzlicher, regulatorischer oder vertraglicher Anforderungen sein.

Beispiele sind:

- Anforderungen an Betreiber kritischer Infrastrukturen,
- Anforderungen im Zusammenhang mit NIS2,
- DORA im Finanzsektor,
- Anforderungen an die Wiederherstellbarkeit und Verfügbarkeit personenbezogener Daten gemäß DSGVO,
- vertraglich vereinbarte Verfügbarkeits- und Wiederanlaufanforderungen.

**Wichtig:** Der BSI-Standard 200-4 selbst ist dadurch nicht automatisch für jedes Unternehmen gesetzlich verpflichtend. Er stellt eine anerkannte Methodik zur Umsetzung eines BCMS dar.

---

# 2. Störung, Notfall und Krise

Der BSI-Standard 200-4 unterscheidet insbesondere zwischen **Störung, Notfall und Krise**.

## Allgemeine Aufbauorganisation – AAO

Die **Allgemeine Aufbauorganisation (AAO)** ist die normale Organisationsstruktur einer Institution.

Sie umfasst beispielsweise:

- reguläre Zuständigkeiten,
- normale Hierarchien,
- etablierte Kommunikationswege,
- Incident- und Störungsmanagement.

## Besondere Aufbauorganisation – BAO

Die **Besondere Aufbauorganisation (BAO)** ist eine zeitlich begrenzte Organisationsstruktur für außergewöhnliche Situationen.

Sie kann vom Normalbetrieb abweichende:

- Verantwortlichkeiten,
- Entscheidungsbefugnisse,
- Hierarchien,
- Kommunikationswege

besitzen.

## Störung

Eine **Störung** liegt vor, wenn Prozesse oder Ressourcen nicht wie vorgesehen zur Verfügung stehen.

Sie kann normalerweise durch die bestehende **AAO** und die normalen Störungs- bzw. Incident-Management-Prozesse behoben werden.

Beispiel:

> Ein Server fällt aus und wird innerhalb der vereinbarten Zeit durch den IT-Betrieb wiederhergestellt.

## Notfall

Ein **Notfall** liegt insbesondere vor, wenn mindestens ein zeitkritischer Geschäftsprozess betroffen ist und die Situation nicht mehr angemessen durch den normalen Geschäftsbetrieb beherrscht werden kann.

Zur Bewältigung wird eine **BAO** benötigt.

Für einen Notfall existieren üblicherweise vorbereitete Pläne oder vorhandene Pläne können an die Situation angepasst werden.

## Krise

Eine **Krise** ist eine außergewöhnliche Situation mit erheblichem Entscheidungs- und Koordinationsbedarf.

Sie unterscheidet sich vom klassischen Notfall insbesondere dadurch, dass die Situation nicht vollständig anhand vorbereiteter Notfallpläne bewältigt werden kann und verstärkte strategische Entscheidungen notwendig sind.

### Vereinfachte Eskalation

```text
Normalbetrieb
     ↓
   Störung
     ↓
   Notfall
     ↓
    Krise
```

**Merke:** Nicht jede Störung wird zum Notfall und nicht jeder Notfall entwickelt sich zu einer Krise.

---

# 3. Business Impact Analyse (BIA)

Die **Business Impact Analyse (BIA)** gehört zu den zentralen Bestandteilen des BCM.

## Ziel der BIA

Mit der BIA wird untersucht:

> Welche Auswirkungen entstehen, wenn ein Geschäftsprozess für eine bestimmte Zeit ausfällt?

Dadurch werden insbesondere:

- zeitkritische Geschäftsprozesse identifiziert,
- Auswirkungen von Ausfällen untersucht,
- zeitliche Anforderungen ermittelt,
- Abhängigkeiten identifiziert,
- Wiederanlaufprioritäten festgelegt.

## Typischer Ablauf

```text
Geltungsbereich festlegen
        ↓
Geschäftsprozesse erfassen
        ↓
Ausfallauswirkungen untersuchen
        ↓
Schadensentwicklung über die Zeit bewerten
        ↓
MTPD / MTA bestimmen
        ↓
RTO / WAZ festlegen
        ↓
RPO und MBCO bestimmen
        ↓
Abhängigkeiten und Ressourcen analysieren
        ↓
zeitkritische Geschäftsprozesse priorisieren
```

## Schadenskategorien

Die konkreten Kategorien werden institutionsspezifisch festgelegt.

Mögliche Auswirkungen sind:

### Finanzielle Schäden

- Umsatzausfall
- Produktionsausfall
- Vertragsstrafen
- zusätzliche Kosten

### Rechtliche und regulatorische Schäden

- Gesetzesverstöße
- Vertragsverletzungen
- aufsichtsrechtliche Konsequenzen

### Reputationsschäden

- Vertrauensverlust
- negative Öffentlichkeit
- Kundenverlust

### Personenschäden

- Gefährdung von Mitarbeitenden
- Gefährdung von Kunden
- Gefährdung Dritter

### Beeinträchtigung der Aufgabenerfüllung

Insbesondere bei Behörden oder kritischen Dienstleistungen kann die Fähigkeit zur Erfüllung der institutionellen Aufgaben beeinträchtigt werden.

---

# 4. Zentrale BIA-Kenngrößen

Die vier wichtigsten Kenngrößen sind:

- MTPD
- RTO
- RPO
- MBCO

---

## 4.1 MTPD / MTA

**MTPD = Maximum Tolerable Period of Disruption**

Deutsch:

**MTA = maximal tolerierbare Ausfallzeit**

Sie beschreibt:

> Wie lange darf ein Geschäftsprozess maximal ausfallen, bevor nicht mehr tolerierbare Auswirkungen für die Institution entstehen?

Beispiel:

Ein Bestellsystem darf maximal **8 Stunden** ausfallen.

```text
MTPD = 8 Stunden
```

---

## 4.2 RTO / WAZ

**RTO = Recovery Time Objective**

Deutsch:

**WAZ = geforderte Wiederanlaufzeit**

Die RTO beschreibt die Zeitspanne vom **Ausrufen des Notfalls bis zur geforderten Inbetriebnahme der vorgesehenen BC-Lösung**.

Beispiel:

```text
MTPD = 8 Stunden
RTO  = 4 Stunden
```

Der Notbetrieb muss somit spätestens innerhalb von vier Stunden bereitstehen.

Grundsätzlich gilt:

> **RTO < MTPD**

Die Differenz dient unter anderem dazu, Reaktionszeiten und zeitliche Unsicherheiten zu berücksichtigen.

---

## 4.3 RPO

**RPO = Recovery Point Objective**

Das RPO beschreibt den:

> **maximal zulässigen Datenverlust**

Es beantwortet die Frage:

> Wie alt dürfen die nach einem Ausfall wiederhergestellten Daten maximal sein?

Beispiel:

```text
RPO = 1 Stunde
```

Bei einem Ausfall um 14:00 Uhr müssen mindestens Daten von 13:00 Uhr wiederhergestellt werden können.

Das RPO beeinflusst beispielsweise:

- Backup-Intervalle
- Replikationsverfahren
- Speicherstrategien

### Merksatz

> **RPO schaut zeitlich zurück.**

---

## 4.4 MBCO

**MBCO = Minimum Business Continuity Objective**

Deutsch:

**Notbetriebsniveau**

Es beschreibt die erforderliche Leistungsfähigkeit eines Geschäftsprozesses während des Notbetriebs.

Beispiel:

Im Normalbetrieb werden:

```text
1.000 Aufträge pro Stunde
```

verarbeitet.

Für den Notbetrieb wird festgelegt:

```text
MBCO = 40 %
```

Die Notfalllösung muss damit mindestens:

```text
400 Aufträge pro Stunde
```

ermöglichen.

---

# 5. Zusammenhang der BIA-Kennzahlen

Vereinfacht:

```text
     Schadensereignis / Störung / Notfall
                      │
                      ▼
            Detektion / Bewertung
                      │
               Notfall ausrufen
                      │ angestrebte Wiederanlaufzeit
                      ├──────────── RTO ────────────►
                      │                             │
                      │                         BC-Lösung /
                      │                         Notbetrieb
                      │								│
Normalbetrieb ────────│─────────────────────────────│───────────────────────│───────► Ausfall-Zeit; Schadenhöhe steigt mit der Ausfall-Zeit.
        			  │
        			  └──────────────── MTPD ───────────────────────────────►
		◄──── RPO ────│  maximal tolerierbar Ausfallzeit
       letzter nutzbarer
       Datenbestand
```

![BIA-Ablauf](https://github.com/marciifee/informationssicherhet/blob/main/assets/BIA_Kennzahlen_DE.png)

Dabei gilt grundsätzlich:

```text
RTO < MTPD
```

und:

```text
RPO = maximal zulässiger Datenverlust
MBCO = erforderliches Leistungsniveau im Notbetrieb
```

---

# 6. RTA und RPA

Neben den geforderten Zielwerten unterscheidet der BSI-Standard auch tatsächlich bzw. zugesichert erreichbare Werte.

## RTA

**Recovery Time Actual**

Deutsch:

> erreichbare Wiederanlaufzeit

Sie beschreibt, welche Wiederanlaufzeit mit einer konkreten BC-Lösung tatsächlich bzw. zugesichert erreicht werden kann.

Ziel:

```text
RTA ≤ RTO
```

## RPA

**Recovery Point Actual**

Deutsch:

> zugesicherter maximaler Datenverlust

Sie beschreibt, welcher Datenverlust mit der tatsächlich eingesetzten Lösung erreicht bzw. zugesichert werden kann.

Ziel:

```text
RPA ≤ RPO
```

### Beispiel

Anforderung:

```text
RTO = 4 Stunden
RPO = 1 Stunde
```

Technische Lösung:

```text
RTA = 2 Stunden
RPA = 30 Minuten
```

Damit erfüllt die Lösung die Anforderungen.

---

# 7. BCM-Risikoanalyse und BC-Strategien

Die **BIA** und die **BCM-Risikoanalyse** beantworten unterschiedliche Fragen.

## BIA

> Welche Auswirkungen entstehen, wenn ein Prozess ausfällt?

## BCM-Risikoanalyse

> Welche Risiken können die für zeitkritische Prozesse benötigten Ressourcen beeinträchtigen?

Betrachtet werden beispielsweise:

- Personal
- Gebäude
- IT
- Informationen
- Betriebsmittel
- Dienstleister
- Lieferketten

## Allgemeine Möglichkeiten der Risikobehandlung

Risiken können grundsätzlich:

- **vermieden**
- **reduziert**
- **transferiert**
- **akzeptiert**

werden.

Diese allgemeine Risikobehandlung ist jedoch von den **BC-Strategien** zu unterscheiden.

## BC-Strategien

BC-Strategien legen fest, wie ein zeitkritischer Geschäftsprozess bzw. seine benötigten Ressourcen nach einem Ausfall fortgeführt oder wieder bereitgestellt werden.

Beispiele:

- redundante Systeme
- Ausweicharbeitsplätze
- Ausweichstandorte
- Ersatzpersonal
- alternative Lieferanten
- manuelle Ersatzverfahren
- Notstromversorgung
- alternative Kommunikationswege
- Datenreplikation
- Ersatzhardware

---

# 8. Single Point of Failure – SPoF

Ein **Single Point of Failure (SPoF)** ist eine einzelne Ressource oder Komponente, deren Ausfall zum Ausfall eines Geschäftsprozesses oder einer wichtigen Funktion führen kann.

Beispiele:

- nur eine Internetleitung
- nur ein Domain Controller
- einzelner Stromanschluss
- nur ein wichtiger Mitarbeiter mit Spezialwissen
- ausschließlich ein Lieferant
- einzelner Produktionsstandort

## Gegenmaßnahmen

- Redundanz
- Ersatzsysteme
- mehrere Lieferanten
- Wissenstransfer
- Vertretungsregelungen
- geografische Verteilung
- alternative Kommunikationswege

**Merke:**

> Ein SPoF kann technisch, organisatorisch, personell oder infrastrukturell sein.

---

# 9. BCM-Organisation

Die Verantwortung für das BCM liegt letztlich bei der **Institutionsleitung**.

## Institutionsleitung

Aufgaben sind insbesondere:

- BCM initiieren
- Rahmenbedingungen festlegen
- Ressourcen bereitstellen
- BCMS unterstützen
- BCM-Leitlinie verabschieden
- Verantwortlichkeiten festlegen

---

## BC-Beauftragte – BCB

Die **Business Continuity Beauftragten (BCB)** sind zentrale Ansprechpersonen für BCM.

Typische Aufgaben:

- Aufbau und Weiterentwicklung des BCMS koordinieren
- BCM-Prozess steuern
- Fachbereiche unterstützen
- BIA koordinieren
- Dokumentationen koordinieren
- Übungen und Tests unterstützen
- an die Institutionsleitung berichten

### Organisatorische Einordnung

Das BSI **empfiehlt**, die Rolle des BCB als **Stabsstelle direkt der Institutionsleitung zuzuordnen**.

Dadurch erhält der BCB:

- direkten Zugang zur Leitung,
- organisatorische Unabhängigkeit,
- bessere Möglichkeiten zur institutionsweiten Koordination.

Von einer Einordnung innerhalb einer Linienorganisation, beispielsweise der IT-Abteilung, wird aufgrund möglicher Interessenkonflikte abgeraten.

**Prüfungs-Merksatz:**

> Der BCB sollte möglichst unabhängig und leitungsnah organisiert sein – BCM ist keine reine IT-Aufgabe.

---

# 10. Besondere Aufbauorganisation – BAO

Bei schwerwiegenden Ereignissen reicht die normale Organisationsstruktur gegebenenfalls nicht aus.

Dann wird eine **Besondere Aufbauorganisation (BAO)** aktiviert.

Mögliche Funktionen innerhalb der BAO sind beispielsweise:

- Stabsleitung
- Lagebearbeitung
- IT/Technik
- Fachbereiche
- interne und externe Kommunikation
- Personal
- Recht/Compliance
- Dokumentation

Die konkrete Zusammensetzung ist **institutionsspezifisch**.

Eine pauschal vorgeschriebene Mindestbesetzung eines Krisenstabs gibt es nicht.

---

# 11. Alarmierung und Eskalation

Damit eine Institution im Ernstfall schnell reagieren kann, müssen Melde-, Alarmierungs- und Eskalationswege vorbereitet werden.

Dazu gehören beispielsweise:

- zentrale Meldestellen
- Meldewege
- Alarmierungspläne
- Kontaktlisten
- Eskalationskriterien
- Vertretungsregelungen
- Erreichbarkeiten
- Entscheidungskompetenzen

Typischer Ablauf:

```text
Schadensereignis
       ↓
Detektion
       ↓
Meldung
       ↓
Bewertung
       ↓
Eskalation
       ↓
Notfall ausrufen
       ↓
BAO aktivieren
       ↓
Notfallbewältigung
```

---

# 12. Notfallplanung

Die im Voraus erstellten Dokumente müssen die Institution in die Lage versetzen, im Ernstfall schnell und strukturiert zu handeln.

## Notfallhandbuch

Das **Notfallhandbuch** enthält die Informationen, die während der Notfallbewältigung benötigt werden.

Dazu können beispielsweise gehören:

- Alarmierungsinformationen
- Geschäftsordnung der BAO bzw. des Stabes
- Kommunikationskonzept
- Geschäftsfortführungspläne
- Wiederanlaufpläne
- Wiederherstellungspläne
- Kontaktinformationen
- Eskalationswege

---

# 13. Geschäftsfortführungs-, Wiederanlauf- und Wiederherstellungspläne

## Geschäftsfortführungsplan – GFP

Ein **Geschäftsfortführungsplan** beschreibt, wie ein zeitkritischer Geschäftsprozess während eines Notfalls fortgeführt werden kann.

Beispiele:

- manuelles Ersatzverfahren
- Ausweicharbeitsplatz
- reduzierte Dienstleistung
- Ersatzlieferant

Ziel:

> einen angemessenen Notbetrieb sicherstellen.

---

## Wiederanlaufplan – WAP

Ein **Wiederanlaufplan** beschreibt die notwendigen Schritte, um ausgefallene Ressourcen oder Funktionen wieder bereitzustellen.

Beispiel:

```text
Serverausfall
    ↓
Ersatzsystem aktivieren
    ↓
Daten wiederherstellen
    ↓
Anwendung starten
    ↓
Funktion prüfen
    ↓
für Notbetrieb freigeben
```

---

## Wiederherstellungsplan – WHP

Ein **Wiederherstellungsplan** beschreibt die Schritte zur vollständigen Wiederherstellung und Rückkehr zum geregelten Normalbetrieb.

### Merkhilfe

> **GFP = Wie arbeiten wir während des Notfalls weiter?**

> **WAP = Wie bekommen wir benötigte Ressourcen/Funktionen wieder zum Laufen?**

> **WHP = Wie kommen wir vollständig zurück in den Normalbetrieb?**

---

# 14. Notfall- und Krisen-Kommunikation

Der BSI-Standard verwendet dafür die Abkürzung:

**NuK-Kommunikation = Notfall- und Krisen-Kommunikation**

Eine vorbereitete Kommunikation soll verhindern:

- widersprüchliche Aussagen
- Informationsverluste
- Verzögerungen
- Gerüchte
- unnötige Reputationsschäden

## Zielgruppen

### Intern

- Mitarbeitende
- Führungskräfte
- BAO
- Fachabteilungen

### Extern

- Kunden
- Dienstleister
- Behörden
- Aufsichtsstellen
- Presse
- Öffentlichkeit

## Wichtige Bestandteile

- Kommunikationswege
- Ansprechpartner
- Freigabeverfahren
- vorbereitete Kommunikationskanäle
- Vertretungsregelungen
- alternative Kommunikationsmittel

---

# 15. Übungen und Tests

Ein BCMS ist nur wirksam, wenn die vorbereiteten Verfahren praktisch funktionieren.

Daher müssen Übungen und Tests regelmäßig durchgeführt und ausgewertet werden.

## Mögliche Übungsarten

### Planbesprechung

Theoretische Überprüfung eines Plans.

### Stabsübung

Übung der Zusammenarbeit innerhalb der BAO bzw. eines Stabes.

### Simulation

Ein Notfallszenario wird realitätsnah durchgespielt.

### Funktionstest

Einzelne technische oder organisatorische Maßnahmen werden getestet.

Beispiel:

> Kann der Ersatzserver tatsächlich innerhalb der RTO bereitgestellt werden?

### Vollübung

Umfangreiche Simulation mit mehreren beteiligten Organisationseinheiten.

## Nachbereitung

Nach jeder relevanten Übung sollten:

- Ergebnisse dokumentiert,
- Probleme analysiert,
- Verbesserungsmöglichkeiten identifiziert,
- Maßnahmen festgelegt,
- Verantwortlichkeiten zugewiesen,
- Pläne aktualisiert

werden.

### Lessons Learned

> Erkenntnisse aus Übungen und realen Ereignissen fließen in die kontinuierliche Verbesserung des BCMS ein.

---

# 16. PDCA-Zyklus

Ein BCMS wird kontinuierlich weiterentwickelt.

Hierfür wird der **PDCA-Zyklus** verwendet:

```text
      ┌─────────┐
      │  PLAN   │
      └────┬────┘
           ↓
      ┌─────────┐
      │   DO    │
      └────┬────┘
           ↓
      ┌─────────┐
      │  CHECK  │
      └────┬────┘
           ↓
      ┌─────────┐
      │   ACT   │
      └────┬────┘
           │
           └────────► PLAN
```

## Plan

Beispielsweise:

- BCM-Leitlinie
- Rahmenbedingungen
- Organisation
- BIA
- BCM-Risikoanalyse
- BC-Strategien

## Do

Beispielsweise:

- BC-Lösungen umsetzen
- BAO aufbauen
- Notfallpläne erstellen
- Mitarbeitende sensibilisieren
- Übungen durchführen

## Check

Beispielsweise:

- Ergebnisse überwachen
- Kennzahlen auswerten
- Übungen analysieren
- interne Überprüfungen
- Managementbewertung

## Act

Beispielsweise:

- Schwachstellen beseitigen
- Pläne verbessern
- Maßnahmen anpassen
- BCMS weiterentwickeln

---

# 17. BCMS-Stufen nach BSI 200-4

Der BSI-Standard 200-4 ermöglicht einen **stufenweisen Einstieg in das BCM**.

## Reaktiv-BCMS

Das **Reaktiv-BCMS** dient als schneller Einstieg.

Ziel ist zunächst eine grundlegende Fähigkeit zur **Notfall- und Krisenbewältigung**.

Merkmale:

- stark vereinfachte Methodik
- schnelle Umsetzbarkeit
- Schwerpunkt auf unmittelbarer Bewältigungsfähigkeit
- keine dauerhaft anzustrebende Endstufe

**Wichtig:**

> Das BSI empfiehlt, nicht dauerhaft beim Reaktiv-BCMS zu verbleiben.

---

## Aufbau-BCMS

Das **Aufbau-BCMS** ermöglicht einen schrittweisen Aufbau.

Zunächst werden besonders zeitkritische Geschäftsprozesse betrachtet.

Danach wird der betrachtete Prozessumfang schrittweise erweitert.

Vorteil:

> Die Institution muss nicht sofort sämtliche Geschäftsprozesse vollständig untersuchen.

---

## Standard-BCMS

Das **Standard-BCMS** stellt die vollständige Ausbaustufe dar.

Merkmale:

- vollständige BCM-Methodik
- alle Geschäftsprozesse werden hinsichtlich ihrer Zeitkritikalität untersucht
- zeitkritische Geschäftsprozesse werden angemessen abgesichert
- vollständiger PDCA-Ansatz
- kompatibel zur **ISO 22301:2019**

### Merksatz

> **Reaktiv = schnell handlungsfähig**

> **Aufbau = schrittweise erweitern**

> **Standard = vollständiges BCMS**

---

# 18. BCM und ISO 22301

Die **ISO 22301** ist der internationale Standard für Business Continuity Management Systeme.

| BSI 200-4 | ISO 22301 |
|---|---|
| deutscher BSI-Standard | internationale ISO-Norm |
| sehr praxisorientierte Methodik | Managementsystemanforderungen |
| detaillierte Umsetzungshilfe | stärker abstrakt |
| Stufenmodell für den Einstieg | vollständiges BCMS als Ziel |
| Standard-BCMS ist ISO-22301-kompatibel | internationale Zertifizierungsgrundlage |

Der BSI-Standard 200-4 kann damit als praxisorientierte Unterstützung beim Aufbau eines zur ISO 22301 kompatiblen BCMS verwendet werden.

---

# 19. BSI 200-4 und BSI 100-4

Der **BSI-Standard 200-4** ersetzt den früheren **BSI-Standard 100-4**.

Wesentliche Weiterentwicklungen sind unter anderem:

- stärkere Orientierung an ISO 22301
- Einführung des BCMS-Stufenmodells
- stärkere Betrachtung organisatorischer Resilienz
- klare Unterscheidung zwischen BC, BCM und BCMS
- stärkere Betrachtung von Schnittstellen zu anderen Managementsystemen
- Berücksichtigung von Outsourcing und Lieferketten
- systematischer PDCA-Ansatz
- modernisierte BIA
- stärkere Verzahnung mit ITSCM, ISMS und Krisenmanagement

---

# 20. BCM – ISMS – ITSCM – Krisenmanagement

Die Bereiche hängen zusammen, haben aber unterschiedliche Schwerpunkte.

| Bereich | Schwerpunkt |
|---|---|
| **ISMS** | Schutz von Informationen und Informationswerten |
| **BCM** | Fortführung zeitkritischer Geschäftsprozesse |
| **ITSCM** | Kontinuität von IT-Services und IT-Ressourcen |
| **Krisenmanagement** | strategische Bewältigung außergewöhnlicher und komplexer Krisensituationen |

### Beispiel Ransomware

Ein Ransomware-Angriff kann gleichzeitig mehrere Bereiche betreffen:

**ISMS:**

> Angriff erkennen, eindämmen und Informationswerte schützen.

**ITSCM:**

> IT-Systeme und IT-Services wieder bereitstellen.

**BCM:**

> zeitkritische Geschäftsprozesse trotz IT-Ausfall fortführen.

**Krisenmanagement:**

> strategische Entscheidungen, Kommunikation und institutionsweite Koordination übernehmen.

---

# 21. Prüfungsrelevante Begriffsabgrenzungen

## BIA vs. Risikoanalyse

**BIA:**

> Welche Auswirkungen hat ein Ausfall?

**Risikoanalyse:**

> Welche Gefahren bzw. Risiken können zu einem Ausfall führen?

---

## Prävention vs. Business Continuity

**Prävention:**

> Eintritt eines Schadensereignisses möglichst verhindern.

**Business Continuity:**

> Trotz eingetretenem Schadensereignis weiterarbeiten bzw. zeitkritische Prozesse rechtzeitig wieder aufnehmen.

---

## RTO vs. RPO

**RTO:**

> Wie schnell muss eine Funktion wieder bereitstehen?

**RPO:**

> Wie viele Daten dürfen maximal verloren gehen?

---

## MTPD vs. RTO

**MTPD:**

> Wie lange ist ein Ausfall maximal tolerierbar?

**RTO:**

> Innerhalb welcher Zeit muss die BC-Lösung bereitstehen?

Deshalb:

> **RTO < MTPD**

---

## Notbetrieb vs. Normalbetrieb

**Notbetrieb:**

> eingeschränkter Geschäftsbetrieb, der mindestens die erforderlichen zeitkritischen Funktionen sicherstellt.

**Normalbetrieb:**

> regulärer planmäßiger Geschäftsbetrieb.

---

# 22. Typische IHK-Prüfungsfragen

## „Erläutern Sie vier Maßnahmen zur Erhöhung der Business Continuity.“

Mögliche Antworten:

1. redundante IT-Systeme
2. Notstromversorgung
3. alternative Lieferanten
4. Ausweicharbeitsplätze

Jeweils mit **Begründung und Projektbezug** erläutern.

---

## „Erläutern Sie die Funktion einer Business Impact Analyse.“

Antwortschema:

> Die BIA untersucht die Auswirkungen von Geschäftsprozessausfällen über die Zeit. Dadurch werden zeitkritische Geschäftsprozesse identifiziert und Anforderungen wie MTPD, RTO, RPO und MBCO festgelegt. Diese Werte bilden anschließend eine Grundlage für die Auswahl geeigneter BC-Strategien und Notfallmaßnahmen.

---

## „Unterscheiden Sie RTO und RPO.“

> Die RTO beschreibt die geforderte Wiederanlaufzeit einer Funktion bzw. BC-Lösung. Das RPO definiert dagegen den maximal zulässigen Datenverlust. Die RTO betrachtet somit primär die Wiederanlaufzeit, während das RPO den wiederherstellbaren Datenstand betrachtet.

---

## „Warum müssen Notfallpläne regelmäßig getestet werden?“

Mögliche Argumente:

- Fehler erkennen
- Aktualität überprüfen
- Mitarbeitende trainieren
- tatsächliche Wiederanlaufzeiten prüfen
- Kommunikationswege testen
- Wirksamkeit von Maßnahmen nachweisen
- kontinuierliche Verbesserung ermöglichen

---

# ⚡ Schnellcheck – 60 Sekunden vor der Prüfung

- **BC** = angestrebte Geschäftskontinuität
- **BCM** = Managementprozess
- **BCMS** = Managementsystem
- **BCM ≠ ITSCM** → BCM betrachtet alle für zeitkritische Prozesse benötigten Ressourcen
- **BIA** → Auswirkungen eines Ausfalls analysieren
- **Risikoanalyse** → Ursachen/Risiken eines Ausfalls betrachten
- **MTPD/MTA** → maximal tolerierbare Ausfallzeit
- **RTO/WAZ** → geforderte Wiederanlaufzeit
- **RPO** → maximal zulässiger Datenverlust
- **MBCO** → erforderliches Notbetriebsniveau
- **RTO < MTPD**
- **RTA ≤ RTO**
- **RPA ≤ RPO**
- **AAO** → normale Organisation
- **BAO** → besondere Organisation für Notfall/Krise
- **Störung** → AAO kann sie bewältigen
- **Notfall** → zeitkritischer Prozess betroffen, BAO erforderlich
- **GFP** → Geschäft im Notbetrieb fortführen
- **WAP** → Ressourcen/Funktionen wiederanlaufen lassen
- **WHP** → vollständige Rückkehr zum Normalbetrieb
- **BCB** → zentrale BCM-Koordination; leitungsnahe Stabsstelle empfohlen
- **PDCA** → Plan – Do – Check – Act
- **3 Stufen** → Reaktiv – Aufbau – Standard
- **Standard-BCMS** → vollständig und ISO-22301-kompatibel
- **BSI 200-4 ersetzt BSI 100-4**
- **SPoF** → einzelner Ausfallpunkt ohne ausreichende Redundanz

---

# Prüfungs-Merksätze

> **BIA = Was passiert, wenn etwas ausfällt?**

> **Risikoanalyse = Was kann den Ausfall verursachen?**

> **BC-Strategie = Wie reagieren wir grundsätzlich auf den möglichen Ausfall?**

> **Notfallplan = Was tun wir konkret im Ernstfall?**

---

> **MTPD = absolute zeitliche Toleranzgrenze.**

> **RTO = Zielzeit für den Wiederanlauf.**

> **RPO = tolerierbarer Datenverlust.**

> **MBCO = Mindestleistung des Notbetriebs.**

---

> **AAO = Alltag.**

> **BAO = Ausnahmezustand.**

---

> **GFP = Geschäft fortführen.**

> **WAP = wieder anlaufen.**

> **WHP = vollständig wiederherstellen.**

---

> **Prävention versucht den Ausfall zu verhindern.**

> **BCM sorgt dafür, dass die Institution trotz Ausfall handlungsfähig bleibt.**

---

# Quellen

- Bundesamt für Sicherheit in der Informationstechnik (BSI): BSI-Standard 200-4 – Business Continuity Management, Version 1.0
- BSI: Hilfsmittel zum BSI-Standard 200-4
- BSI: Glossar und Abkürzungsverzeichnis zum BSI-Standard 200-4
- ISO 22301:2019 – Security and resilience – Business continuity management systems