# Lernblatt / Handout: Business Continuity Management (BCM)
### Kompaktes Nachschlagewerk für die IHK-Prüfung "Geprüfter Berufsspezialist für Informationssicherheit"
**Stand: 29.August.2026**

**Business Continuity Management (BCM)** (auf Deutsch: Betriebliches Kontinuitätsmanagement) ist ein ganzheitlicher Managementansatz, der sicherstellt, dass ein Unternehmen auch in Krisen-, Not- und Schadensfällen handlungsfähig bleibt und kritische Geschäftsprozesse schnellstmöglich wieder aufnimmt.
### Die Wichtigsten Säulen des BCM:
- **Vorbereitung:** Identifikation von Risiken (wie Cyberangriffe, Stromausfälle, Naturkatastrophen oder Lieferkettenprobleme) und Erstellung konkreter Notfallpläne.
- **Business Impact Analyse (BIA):** Untersuchung, welche Geschäftsprozesse überlebenswichtig sind und wie lange ein Ausfall maximal andauern darf.
- **Wiederherstellung:** Definierte Zielzeiten für den Wiederanlauf (Recovery Time Objective – RTO) und den maximal tolerierbaren Datenverlust (Recovery Point Objective – RPO).
- **Tests und Training:** Regelmäßige Überprüfung und Übung der Notfallpläne, damit im Ernstfall jeder Handgriff sitzt.
### Warum ist BCM wichtig?
- **Schadenminderung:** Minimierung von finanziellen Verlusten und Ausfallzeiten.
- **Klarheit:** Klare Zuständigkeiten und Rollen verhindern Panik und Verzögerungen im Ernstfall.
- **Wettbewerbsvorteil:** Kunden und Partner vertrauen Unternehmen, die auch unter Krisenbedingungen lieferfähig bleiben.
- **Compliance:** Gesetzliche Vorgaben und Richtlinien (wie NIS-2 oder DORA) fordern zunehmend ein professionelles Notfallmanagement.

**Dieses Handout ist überwiegend nach dem BSI-Standards 200-4 (Business Continuity Management)** recherchiert und aufbereitet – zentrale Begriffe sind mit **[BSI 200-4]** gekennzeichnet.


**Quellenverzeichnis:**
- https://www.bsi.bund.de/DE/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/IT-Grundschutz/BSI-Standards/BSI-Standard-200-4-Business-Continuity-Management/bsi-standard-200-4_Business_Continuity_Management_node.html

---

## 1. Grundlagen

**BCM** = Managementprozess, um gravierende Risiken frühzeitig zu erkennen und den strukturierten Umgang mit Geschäftsunterbrechungen sicherzustellen.

| Begriff | Bedeutung |
|---|---|
| **BC** (Business Continuity) | der angestrebte Zustand: Geschäftsbetrieb bleibt aufrecht |
| **BCM** | der Managementprozess, der BC erreicht |
| **BCMS** | das gesamte System aus Prozessen, Rollen, Dokumenten, Ressourcen |

**Abgrenzung zur IT-Sicherheit**: IT-Sicherheit schützt Vertraulichkeit/Integrität/Verfügbarkeit von IT. BCM sichert **alle** zeitkritischen Geschäftsprozesse – auch bei nicht-technischen Ursachen (Pandemie, Lieferkette, Personalausfall) – ganzheitlich ab. Beide sind eng verzahnt, aber BCM ist kein IT-Sicherheits-Teilbereich.

**Rechtliche Relevanz**: KRITIS (BSIG), NIS2-Risikomanagementpflichten, DSGVO Art. 32 ("geeignete technische und organisatorische Maßnahmen"), oft vertraglich gefordert.

**5 Ziele des BCM**: Aufrechterhaltung kritischer Prozesse · schnelle Wiederaufnahme · Minimierung existenzieller Schäden · Sicherstellung von Kundenleistungen · Erhöhung der organisatorischen Resilienz.

---

## 2. Verfügbarkeit & Störfälle

**Verfügbarkeit**: messbare Zielgröße, Redundanzprinzipien, Fehlervermeidung (Ursache verhindern) vs. Fehlerbewältigung (Auswirkung begrenzen), Kosten-Nutzen-Trade-off.
**SPoF** (Single Point of Failure) = eine Komponente, deren Ausfall den ganzen Prozess lahmlegt → durch Redundanz vermeiden.

**Störfall vs. Störung**: Eine Störung ist im Tagesgeschäft lösbar. Ein schwerer Störfall überschreitet normale Kapazitäten, gefährdet zeitkritische Prozesse und aktiviert die Notfallorganisation.
**Beurteilungskriterien**: Betroffenheit zeitkritischer Prozesse, Schadensausmaß/-dauer, Reichweite, Reputationsrisiko, Ressourcenausreichung.
**Typische Ursachen**: Cyberangriffe/Ransomware, Stromausfall, Naturkatastrophen, Pandemie, Lieferantenausfall, Personalausfall, Sabotage.

---

## 3. Business Impact Analyse (BIA)

**Ziel**: zeitkritische Prozesse identifizieren, Schadensverlauf über Zeit bewerten, RTO/RPO/MTPD ableiten.

**Ablauf**: Scope & Vorbereitung → Prozesse identifizieren → Schadensanalyse → RTO/RPO/MTPD ableiten → Abhängigkeiten & Ressourcen analysieren → Priorisierung & Freigabe durch Geschäftsführung.

**Schadensklassen**: Einordnung nach Schwere (gering – mittel – hoch – existenzbedrohend), monetär (Umsatzverlust, Vertragsstrafen) vs. nicht-monetär (Reputation, Personenschäden, Recht). Mehrfachschäden (mehrere Schadensarten gleichzeitig) müssen kumuliert betrachtet werden. Toleranzgrenzen legen fest, ab wann eskaliert wird.

---

## 4. Risikobehandlung & Verfügbarkeitsmaßnahmen

**4 Risikobehandlungsstrategien**:

| Strategie | Beschreibung |
|---|---|
| Vermeiden | Ursache/Prozess eliminieren |
| Reduzieren | präventive + reaktive Maßnahmen |
| Verlagern/Versichern | Transfer an Dritte (Versicherung, Outsourcing) |
| Tragen/Akzeptieren | bewusst innerhalb der Toleranzgrenze |

Präventiv = verhindert Eintritt; reaktiv = begrenzt Auswirkung nach Eintritt. In der Praxis meist **kombinierte Strategien**.

**Technische Verfügbarkeitsmaßnahmen**: redundante Systeme, Datenreplikation/Backups, Netzwerk-Resilienz, Monitoring & Alarmierung, kontrolliertes Change-/Release-Management (verhindert selbstverursachte Ausfälle).

---

## 5. Parameter der Krisenbewältigung (BIA-Kennzahlen) **[BSI 200-4]**

Zeitachse eines Störfalls (vereinfacht):

```
   RPO                    Störfall           Reaktionszeit    WAZ/RTO         MTN            
←──────────────────────────┤ ─────────────────►│───────────────►│──────────────►│
Datensicherung          Ausfall            Krisenstab      Notbetrieb    Normalbetrieb
                                           aktiviert       erreicht      wiederhergestellt
                                                                          
                                            ◄──────────── MTPD/MTA ─────────────►
                                            ◄─────────────── MTW ───────────────►
```

| Kürzel | Voller Name | Bedeutung |
|---|---|---|
| **RPO** | Recovery Point Objective (Wiederherstellungspunkt) | max. zulässiger Datenverlust (Zeit vor dem Ausfall) |
| **RTO / WAZ** | Recovery Time Objective (Wiederanlaufzeit) | Zeit bis zum **Notbetrieb** |
| **MTA / MTPD** | Maximal tolerierbare Ausfallzeit | Zeitpunkt, ab dem die Existenz gefährdet ist – RTO muss deutlich darunter liegen |
| **MTN** | Maximal tolerierbare Notbetriebszeit | wie lange darf der Notbetrieb höchstens dauern |
| **MTW** | Maximal tolerierbare Wiederherstellungszeit | = WAZ + MTN (gesamte Zeit bis Normalbetrieb) |
| **Wiederherstellungszeit** | tatsächliche Zeit bis Normalbetrieb | muss ≤ MTW sein |
| **RTA / RPA** | Recovery Time/Point *Actual* | tatsächlich erreichbare Werte (Soll: RTA ≤ RTO, RPA ≤ RPO) |
| **MBCO** | Minimum Business Continuity Objective | Mindestleistungsniveau im Notbetrieb |
| **Wiederanlauf-Niveau** | – | welche Kapazität der Notbetrieb mind. bieten muss |

**Reaktionszeit** = Erkennung/Meldung → Alarmierung → Einberufung Krisenstab → Erstbewertung → Sofortmaßnahmen.

**Merksatz**: RPO blickt **zurück** (Datenverlust), RTO/MTA blicken **vorwärts** (Wiederherstellung).

---

## 6. Organisation: Rollen, Krisenstab, Eskalation

| Rolle | Aufgabe |
|---|---|
| Geschäftsführung/Institutionsleitung | Gesamtverantwortung, Ressourcenfreigabe, BCM-Leitlinie verabschieden |
| **BCB** (Business-Continuity-Beauftragter) **[BSI 200-4]** | Aufbau/Betrieb des BCMS – als **Stabsstelle direkt unter der Leitung**, NICHT in der IT-Abteilung |
| BCM-Team | operative Umsetzung |
| Fachabteilungen | Prozessverantwortung |
| Externe Partner | z. B. Ausweichkapazitäten |

**BCM-Leitlinie**: Zweck, Geltungsbereich, Verantwortlichkeiten, Ziele/Kennzahlen, Freigabeprozess, regelmäßige Überprüfung.

**Krisenstab**: Lagebeurteilung, strategische Entscheidungen, Ressourcenfreigabe, Informationsmanagement, Dokumentation. Mindestbesetzung: Krisenstabsleiter, Geschäftsführung, IT/Technik, Kommunikation, ggf. Recht/Compliance.

**Notfallteams**: definierter Aufbau, Qualifikation, Bereitschaftsregelung, Notfallpläne als Arbeitsgrundlage, Koordination mit Krisenstab.

**Störfalleskalation**: Meldewege, Eskalationskriterien, automatisierte Alarme, Kommunikationsmatrix, Übungszyklen.

**Störfallklassen (Staffelung)**: Störung (Tagesgeschäft) → Notfall (Notfallpläne aktiv) → Krise (existenzbedrohend, Krisenstab zwingend).

---

## 7. Notfallhandbuch & Notfallvorsorge **[BSI 200-4]**

```
Notfallkonzept
├── Notfallvorsorgekonzept  (präventiv: Ausweichstandorte, Notstrom, Backups, Lieferantenmanagement, Versicherung)
│                           
└── Notfallhandbuch         (operativ, für den Ernstfall)
      ├── Krisenkommunikationsplan
      ├── Krisenstabsleitfaden
      ├── Wiederanlaufplan (WAP)       → Schritte bis zum Notbetrieb (RTO)
      └── Wiederherstellungsplan (WHP) → Schritte vom Notbetrieb zurück in Normalbetrieb
```

---

## 8. Krisenkommunikation

Zielgruppen definieren (intern/extern: Mitarbeitende, Kunden, Behörden, Presse) → vorbereitete Botschaften/Sprachregelungen → Medien & Kanäle festlegen → Freigabeprozesse → Transparenz & Konsistenz.
**NuK-Kommunikation [BSI 200-4]** = Notfall- und Krisen-Kommunikation, der BSI-Sammelbegriff dafür.

---

## 9. Übungen, PDCA & Stufenmodell **[BSI 200-4]**

### Der PDCA-Zyklus im BSI-Standard 200-4

| Phase | Inhalt |
|---|---|
| **Plan** | BCM-Leitlinie, Geltungsbereich, BIA + BCM-Risikoanalyse, BCM-Strategie/-Konzept |
| **Do** | Business-Continuity-Pläne erstellen, Notfallvorsorge & Wiederanlaufmaßnahmen umsetzen, Schulung/Sensibilisierung |
| **Check** | Wirksamkeit durch Übungen/Tests/Leistungsüberprüfung bewerten |
| **Act** | Verbesserungsmaßnahmen ableiten, nächster Zyklus |

### Die drei BCMS-Reifegradstufen

| Stufe | Merkmale |
|---|---|
| **Reaktiv-BCMS** | einfacher Einstieg, Sofortmaßnahmen-Katalog, reduzierter PDCA |
| **Aufbau-BCMS** | vollständige BIA, Wiederanlaufpläne, regelmäßige Übungen |
| **Standard-BCMS** | vollständige PDCA-Implementierung, audit-/zertifizierungsfähig, ISO-22301-kompatibel |

**Lessons Learned**: systematische Auswertung von Übungen/Vorfällen → Verbesserungsmaßnahmen.
**ISO 22301**: internationale BCMS-Norm, zu der BSI 200-4 kompatibel ist.
**BSI 200-4 löst BSI 100-4 ab**: Stufenmodell (analog 200-2), ISO-22301-Kompatibilität, klarere BC/BCM/BCMS-Trennung, Synergien zu ITSCM und anderen 200er-Standards.

---

## Schnellcheck vor der Prüfung

- **BCM ≠ IT-Sicherheit**: BCM sichert alle zeitkritischen Prozesse, nicht nur IT
- **BCB** sitzt als Stabsstelle **direkt unter der Leitung**, nicht in der IT
- **RPO** = Datenverlust (rückwärts) | **RTO/WAZ** = Zeit bis Notbetrieb (vorwärts)
- **MTA/MTPD** = Überlebensgrenze – RTO muss deutlich darunter liegen
- **MTW = WAZ + MTN**
- **WAP** = Weg in den Notbetrieb | **WHP** = Weg zurück in den Normalbetrieb
- **3 BCMS-Stufen**: Reaktiv → Aufbau → Standard
- **PDCA**: Plan – Do – Check – Act
- **4 Risikostrategien**: vermeiden – reduzieren – verlagern/versichern – tragen
- **BSI 200-4 ersetzt 100-4**, kompatibel zu **ISO 22301**
