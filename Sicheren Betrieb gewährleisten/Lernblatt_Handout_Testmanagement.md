# Lernblatt / Handout: Testmanagement & Testautomatisierung
### Kompaktes Nachschlagewerk für die IHK-Prüfung "Geprüfter Berufsspezialist für Informationssicherheit"
**Stand: 29.August.2026**

**Testmanagement** ist die organisatorische Planung, Steuerung und Überwachung aller Testaktivitäten in einem Softwareprojekt, während die **Testautomatisierung** den technischen Prozess beschreibt, diese Tests mithilfe von speziellen Werkzeugen und Skripten automatisch auszuführen.
Beide Disziplinen arbeiten eng zusammen, um die Qualität, Stabilität und Fehlerfreiheit von Software vor der Einführung sicherzustellen

### Was ist Testmanagement?
Das Testmanagement bildet den organisatorischen Rahmen für die Qualitätssicherung. Ein Testmanager koordiniert den gesamten Testprozess:
- **Planung:** Festlegen von Testzielen, Zeitplänen, Ressourcen und dem Testumfang.
- **Steuerung:** Überwachen des Testfortschritts und Reagieren auf Abweichungen.
- **Dokumentation:** Auswerten und Berichten der Testergebnisse als Grundlage für die Freigabe der Software

### Was ist Testautomatisierung?
Die Testautomatisierung ist ein wichtiges Werkzeug innerhalb des Testmanagements. Statt Testfälle manuell durchzuführen, erstellen Testautomatisierer Programme und Skripte:
- **Effizienz:** Wiederkehrende Tests (wie Regressionstests) laufen schneller und beliebig oft ab.
- **Testabdeckung:** Erhöht die Genauigkeit und sorgt für eine höhere Prüftiefe in kurzer Zeit.
- **Integration:** Lässt sich nahtlos in moderne Entwicklungsprozesse (wie CI/CD-Pipelines) einbinden.

### Zusammenspiel
Während das Management die strategischen Fragen klärt *(Wer testet was, wann und womit?)*, liefert die Automatisierung die technische Ausführung für repetitive Aufgaben, um Zeit und Kosten zu sparen.

**Dieses Handout ist überwiegend mit Inhalten anhand von ISTQB/ISO 29119** recherchiert und ausformuliert. 


**Quellenverzeichnis:**
- https://gi.de/informatiklexikon/testmanagement-professionelles-testen
- https://de.wikipedia.org/wiki/ISO/IEC/IEEE_29119_Software_Testing

---

## 1. Grundlagen & Normen

**Testmanagement** = Konzeptionierung, Planung, Schätzung, Überwachung, Berichterstattung, Steuerung und Abschluss von Testaktivitäten.

| Norm | Inhalt |
|---|---|
| IEEE 829 | Form & Inhalt von Testdokumenten |
| IEEE 1008 | Vorgehen beim Modultest (Unit Test) |
| BS 7925 | Britischer Standard zu Testtechniken (Vorläufer von 29119) |

### ISO/IEC/IEEE 29119

ISO/IEC/IEEE 29119 ist eine international anerkannte Normenfamilie für Softwaretests, während das ISTQB (International Software Testing Qualifications Board) der weltweit führende Verband für die Ausbildung und Zertifizierung von Softwaretestern ist. Die Norm ersetzt die älteren Standards (wie IEEE 829 und BS 79225).

| Teil | Inhalt |
|---|---|
| 29119-1 | Konzepte und Definitionen: Grundlagen und Vokabular für das Softwaretesting.  |
| 29119-2 | Testprozesse: Beschreibt Prozesse für Organisationen, Testmanagement und dynamische Tests. |
| 29119-3 | Testdokumentation: Vorlagen und Vorgaben für Testpläne, Testberichte und Testspezifikationen. |
| 29119-4 | Testerfahren/Techniken: Methoden wie Äquivalenzklassenbildung oder Grenzwertanalyse. |
| 29119-5 | Keyword-Driven Testing: Richtlinien für schlüsselwortbasiertes Testen. |
| 29119-6 (TR) | Richtlinien für agile Projekte: Ergänzungen und Reports zur Anwendung der Norm in agilen Projekten |

**Keyword-Driven Testing**: Testfälle als fachliche Schlüsselwörter (z. B. „Führe Karte ein", „Gib PIN ein" beim Bankomat) statt technischem Code – lesbar auch für Fachanwender.

### ISTQB
Das ISTQB orientiert seine Definitionen und Vorgehensweisen oft an gängigen Standards wie ISO 29119.
- **Zweck:** Schafft ein einheitliches, weltweites Verständnis und standardisiertes Know-how für Softwaretester.
- **Zertifizierung:** Bietet den bekannten Certified Tester Foundation Level (CTFL) sowie fortgeschrittene Stufen (Advanced Level).
- **Bezug:** Das ISTQB liefert die Qualifikation für Personen, während ISO 29119 den organisatorischen und prozessualen Rahmen für Unternehmen vorgibt

---

## 2. Grundbegriffe

| Begriff | Bedeutung |
|---|---|
| Testfall | Eingaben + Bedingungen + erwartetes Ergebnis für ein Testziel |
| Testobjekt | das zu testende Element |
| Testumgebung | Hardware/Software/Netz/Daten, unter denen getestet wird |
| Testdaten | Daten, die vor/während des Tests verwendet werden |
| Testprotokoll | chronologische Aufzeichnung der Testdurchführung |
| Entry-/Exit-Kriterien | wann eine Testphase beginnen/enden darf |
| Testpyramide | viele Unit-Tests, weniger Integrationstests, wenige UI/E2E-Tests |

---

## 3. Testprozess-Modelle

- **ISTQB fundamentaler Testprozess**: Planung & Steuerung → Analyse & Design → Realisierung → Durchführung → Bewertung der Endekriterien & Bericht → Abschlussaktivitäten
- **"nach Böhm"**: gängige grafische Darstellung des ISTQB-Prozesses aus Rolf Böhms Lehrbuch – keine eigene Methodik
- **"nach Schlich"**: Darstellung mit zentraler Testdatenbank (Maud Schlich, "Softwaretesten nach ISTQB für Dummies"); 8 Testaktivitäten, je 4 für Testmanager und Tester
- **ISO 29119-2**: 3 Ebenen – organisatorische Prozesse, Testmanagementprozesse, dynamische Testprozesse

---

## 4. Testlebenszyklus, Teststrategie, Testkonzept

**Lebenszyklus**: Planung → Design → Vorbereitung → Ausführung → Auswertung → Abschluss

**Teststrategie**: Scope · Testarten · Qualitätsziele · Risiko-Fokus (risikobasiertes Testen) · Automatisierungsgrad · Metriken

**Erfolgskriterien**: Exit-Kriterien · KPIs · Abnahmeprozess · Quality Gates · Stakeholder-Zufriedenheit

### Testkonzept – die 9 W-Fragen

| Frage | Aspekt |
|---|---|
| Wer testet? | Testpersonal |
| Was wird getestet? | Testumfang |
| Wann wird getestet? | Testplanung |
| Wo im Prozess? | Teststufen |
| Wie wird getestet? | Testarten |
| Welche Tools? | Testwerkzeuge (ALM QC, Jira, Mantis, API-Tools) |
| Wo/womit getestet? | Testumgebung (Dev/Test/Prod) |
| Was/wie dokumentiert? | Dokumentation |
| Welche Risiken? | Personal, Termine, Datenverlust |

---

## 5. Organisation & Planung

**Testmanager**: Planung, Koordination, Reporting, Qualitätssicherung, Risikomanagement, kontinuierliche Verbesserung.<br>
**Stakeholder**: Tester, Entwicklung, Product Owner, Betrieb/DevOps, Security-/Datenschutzbeauftragter, Fachabteilungen, Management, externe Prüfer.<br>
**Testplanung**: Zeitplanung, Testumgebungen, Testdaten, Entry-/Exit-Kriterien, Meilensteine, Ressourcenplanung (Personal, Kosten, Aufwandsschätzung, Arbeitspakete).

---

## 6. Testarten vs. Teststufen

| Dimension | Testarten | Teststufen |
|---|---|---|
| Frage | Was testen wir? | Wo testen wir? |
| Fokus | Qualitätseigenschaft | Systemebene |
| Beispiele | Funktional, Sicherheit, Performance | Unit, Integration, System, UAT |
| Ziel | Fehlerarten finden | Fehlerort eingrenzen |
| Abhängigkeit | unabhängig vom Entwicklungsstand | entspricht Entwicklungsfortschritt |

### Teststufen im Überblick

| Stufe | Kernpunkt |
|---|---|
| **Unit Test** | isolierte Umgebung, AAA-Prinzip (Arrange–Act–Assert), Assertions, hoch automatisiert, schnell |
| **Integrationstest** | Datenflüsse, API-Contracts, Geschäftslogik über Systemgrenzen |
| **Systemtest** | vollständig integriertes System gegen Gesamtanforderungen |
| **Smoke-Test** | kurzer Kernfunktions-Check nach neuem Build |
| **Abnahmetest (UAT)** | Prüfung durch Auftraggeber/Endnutzer vor Freigabe |
| **Wartungstest** | Test nach Änderungen am Produktivsystem |
| **Release-Test** | Prüfung vor Produktions-Freigabe |
| **Alpha-Test** | intern beim Hersteller |
| **Beta-Test** | extern bei ausgewählten echten Nutzern |

### Grundlegende Testarten (ISTQB)

- **Funktional** (Anforderungen prüfen) vs. **nicht-funktional** (Performance, Usability, Security …)
- **Strukturbezogen** (Kontrollfluss/White-Box) vs. **änderungsbezogen** (Wartung, Regression)
- **White-Box** (Code bekannt) · **Black-Box** (nur Ein-/Ausgabe) · **Grey-Box** (Mischform)

### Spezielle Testarten
- **Penetrationstest**: 6-Schritte-Modell **[Recherche]** – Vorbereitung/Scoping → Reconnaissance → Schwachstellenanalyse → Exploitation → Auswertung → Berichterstattung
- **Regressionstest**: prüft, dass Änderungen bestehende Funktionalität nicht beeinträchtigen
- **Wiederanlauftest**: prüft korrekten, konsistenten Wiederanlauf nach Systemausfall (vgl. WAP/WHP im BCM)

---

## 7. Testdesign

Statische Tests (ohne Codeausführung: Reviews, statische Analyse) vs. dynamische Tests (mit Codeausführung). <br>
Testdesign = "eine spezifische Instanziierung eines Testprozesses" (ISTQB); i. d. R. 4 Teststufen entsprechend dem V-Modell.

---

## 8. Werkzeuge, Dokumentation, Abschluss

**Testwerkzeuge**: Micro Focus ALM Quality Center, Jira (+ Test-Management-Plugin), Mantis, API-Tools.<br>
**Dokumentation**: Testberichte, Testprotokolle, RfC, Abweichungsberichte, Abschlussberichte, Testspezifikationen.<br>
**Testabschluss**: Testabschlussbericht → Abschlussworkshop (Review, Best Practices, Lessons Learned) → kontinuierlicher Verbesserungsprozess (KVP).

---

# 9. Testautomatisierung

## Grundlagen

**Definition**: Einsatz von Software-Werkzeugen zur automatisierten Ausführung, Auswertung und Protokollierung von Testfällen.

| Vorteile | Nachteile/Grenzen |
|---|---|
| schnell & wiederholbar | hoher Erstellungs-/Wartungsaufwand |
| konsistent, keine menschlichen Flüchtigkeitsfehler | Flaky Tests möglich |
| CI/CD-fähig (jeder Build getestet) | ungeeignet für explorative/Usability-Tests |
| langfristig kosteneffizient bei Wiederholung | lohnt sich erst ab bestimmter Wiederholhäufigkeit (ROI) |

**Gut automatisierbar**: Regressions-, Smoke-, Unit-, API-Tests, datengetriebene Tests mit vielen Datensätzen. <br>
**Schlecht automatisierbar**: explorative Tests, Usability/UX, häufig wechselnde Oberflächen, Einmaltests.

## Testautomatisierungspyramide

```
         /*\
        /---\
       / UI  \       wenige, langsam, teuer, wartungsintensiv
      /-------\
     / Service \    mittel (Integration/API)
    /-----------\
   / Unit--Tests \  viele, schnell, günstig, stabil
  /---------------\
```
**Anti-Pattern "Ice-Cream-Cone"**: umgekehrte Pyramide – viele instabile UI-Tests, kaum Unit-Tests → langsame, unzuverlässige Testläufe.

## Automatisierungsansätze

| Ansatz | Prinzip |
|---|---|
| Capture & Replay | Interaktion aufzeichnen und abspielen – schnell, aber wartungsintensiv |
| Scripted | Testcode direkt programmiert – flexibel, braucht Know-how |
| Data-Driven | Testlogik von Testdaten getrennt, gleiche Logik mit vielen Datensätzen |
| Keyword-Driven | fachliche Schlüsselwörter, technische Umsetzung im Hintergrund (vgl. ISO 29119-5) |
| Behaviour-Driven (BDD) | „Given – When – Then" (Gherkin), z. B. mit Cucumber |

## Generische Testautomatisierungsarchitektur (ISTQB CTAL-TAE)

- **TAP** (Test Automation Process): Entscheidung → Planung → Design → Implementierung → Betrieb/Wartung
- **TAS/GTAA**-Schichten: Test-Generierung → Test-Definition → Test-Ausführung → **Test-Adaption** (Schnittstelle zum Testobjekt – kapselt technische Details, z. B. UI-Selektoren/API-Endpunkte)

## Werkzeuge (Stand 2026)

| Tool | Charakteristik |
|---|---|
| **Selenium** | W3C-Standard, größte installierte Basis, breite Sprachunterstützung (Java, C#, Python, …) |
| **Cypress** | starke Entwicklererfahrung, primär JavaScript, ursprünglich nur Chromium |
| **Playwright** (Microsoft) | jüngstes Tool, gute Cross-Browser-Unterstützung (inkl. WebKit/Firefox), Auto-Wait reduziert Flakiness – 2026 oft erste Wahl für neue Projekte |
| **Appium** | De-facto-Standard für native mobile Apps (iOS/Android), basiert auf Selenium WebDriver |
| **Robot Framework** | keyword-basiert, kombinierbar mit Selenium/Appium/API-Libraries, für Fachanwender geeignet |
| **Cucumber** | BDD-Framework mit Gherkin-Syntax |
| JUnit/pytest/NUnit/Jest | klassische Unit-Test-Frameworks je Sprache |

## CI/CD & Herausforderungen

- Integration in Pipelines (Jenkins, GitLab CI, GitHub Actions) → Tests laufen bei jedem Commit/Build
- **Flaky Test** = Test, der ohne Codeänderung mal besteht, mal fehlschlägt (Timing/Umgebung/Testdaten)
- Herausforderungen: Wartungsaufwand, Testdatenmanagement, benötigtes Automatisierungs-Know-how
- **ROI/Break-even**: Automatisierung lohnt sich, sobald eingesparte Zeit durch Wiederholung den Erstellungs-/Wartungsaufwand übersteigt

---

## Schnellcheck vor der Prüfung

- **ISO 29119-1 bis -6**: Konzepte – Prozesse – Dokumentation – Techniken – Keyword-Driven – Agile-Leitfaden
- **AAA-Prinzip**: Arrange – Act – Assert (Unit Test)
- **Testarten** = Was? · **Teststufen** = Wo?
- **6-Schritte-Penetrationstest**: Scoping – Recon – Analyse – Exploitation – Auswertung – Bericht
- **Testpyramide**: viele Unit-Tests, wenige UI-Tests
- **BDD**: Given – When – Then (Gherkin/Cucumber)
- **GTAA-Schichten**: Generierung – Definition – Ausführung – Adaption
- **2026-Trend**: Playwright meist erste Wahl für neue Web-Projekte, Appium für native Mobile-Apps
- **Flaky Test** = instabiler, nicht-deterministischer Testfehler
