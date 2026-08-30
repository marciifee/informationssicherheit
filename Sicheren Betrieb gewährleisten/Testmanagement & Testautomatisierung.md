# Lernblatt / Handout: Testmanagement & Testautomatisierung

### Kompaktes Nachschlagewerk für die IHK-Prüfung „Geprüfter Berufsspezialist für Informationssicherheit“

**Stand: 30. August 2026**

---

# ⚡ Schnellcheck vor der Prüfung

## Grundbegriffe

- **Testmanagement** = Planung, Überwachung, Steuerung und Abschluss von Testaktivitäten
- **Testautomatisierung** = softwaregestützte automatische Ausführung, Auswertung und Protokollierung von Tests
- **Testobjekt** = das zu prüfende Produkt, System oder Bestandteil
- **Testfall** = Menge aus Vorbedingungen, Eingaben, Aktionen und erwarteten Ergebnissen für ein Testziel
- **Testumgebung** = Hardware, Software, Netzwerk, Werkzeuge und weitere Ressourcen für Tests
- **Testdaten** = für die Testdurchführung benötigte Daten
- **Testbasis** = Dokumente bzw. Informationen, aus denen Testfälle abgeleitet werden
- **Testware** = alle während des Testprozesses erzeugten und verwendeten Testartefakte

## Die 7 ISTQB-Testaktivitäten

1. **Testplanung**
2. **Testüberwachung und Teststeuerung**
3. **Testanalyse**
4. **Testentwurf**
5. **Testrealisierung**
6. **Testdurchführung**
7. **Testabschluss**

## Die 5 Teststufen nach ISTQB CTFL v4

1. **Komponententest / Unit Test**
2. **Komponentenintegrationstest**
3. **Systemtest**
4. **Systemintegrationstest**
5. **Abnahmetest**

## Wichtige Testarten

- **funktional** → Was soll das System tun?
- **nicht-funktional** → Wie gut arbeitet das System?
- **Black-Box** → Testentwurf ohne Kenntnis interner Struktur
- **White-Box** → Testentwurf anhand interner Struktur
- **Änderungsbezogen** → Bestätigungstest und Regressionstest

## Testtechniken

- Äquivalenzklassenbildung
- Grenzwertanalyse
- Entscheidungstabellentest
- Zustandsübergangstest
- Anweisungs-/Zweigüberdeckung
- exploratives Testen

## Merksätze

> **Teststufe = Auf welcher Ebene wird getestet?**

> **Testart = Welche Eigenschaft bzw. welcher Zweck wird getestet?**

> **Testtechnik = Wie werden Testfälle systematisch abgeleitet?**

## Regression vs. Bestätigung

- **Bestätigungstest (Re-Test)** → Ist der konkrete Fehler wirklich behoben?
- **Regressionstest** → Hat die Änderung andere bereits funktionierende Bereiche beschädigt?

## Testautomatisierung

Gut geeignet für:

- Unit Tests
- Regressionstests
- API-Tests
- wiederkehrende Smoke-Checks
- datengetriebene Tests
- CI/CD-Pipelines

Weniger geeignet für:

- exploratives Testen
- subjektive Usability-Bewertungen
- einmalige Tests mit hohem Automatisierungsaufwand

## Testpyramide

> **Viele schnelle Unit Tests → weniger Integrations-/API-Tests → wenige End-to-End-/UI-Tests**

---

# 1. Grundlagen

**Testmanagement** umfasst die Planung, Überwachung, Steuerung und den Abschluss der Testaktivitäten eines Projekts oder einer Organisation.

Ziel ist es, Testaktivitäten so zu organisieren, dass Risiken und Qualitätsprobleme frühzeitig erkannt und ausreichende Informationen für Entscheidungen über die Produktqualität bereitgestellt werden.

**Testautomatisierung** bezeichnet den Einsatz von Software zur automatisierten Durchführung bestimmter Testaktivitäten.

Dazu können insbesondere gehören:

- Vorbereitung von Tests
- Ausführung von Testfällen
- Vergleich von Ist- und Soll-Ergebnissen
- Protokollierung
- Auswertung
- Reporting

Testautomatisierung ist somit kein Ersatz für Testmanagement, sondern ein mögliches Mittel innerhalb des gesamten Testprozesses.

## Ziele des Testmanagements

- Testziele festlegen
- Testumfang bestimmen
- Risiken berücksichtigen
- Ressourcen planen
- Testaktivitäten koordinieren
- Fortschritt überwachen
- Abweichungen erkennen
- Testergebnisse bewerten
- Entscheidungsgrundlagen für Stakeholder bereitstellen

### Merksatz

> **Testmanagement organisiert das Testen – Testautomatisierung unterstützt dessen technische Durchführung.**

---

# 2. Normen und Standards

## Wichtige Normen und Referenzwerke

| Norm / Rahmenwerk | Bedeutung |
|---|---|
| **ISO/IEC/IEEE 29119** | internationale Normenfamilie für Softwaretests |
| **ISTQB** | international etabliertes Zertifizierungssystem und Wissensmodell für Softwaretesting |
| **ISO/IEC 25010** | Qualitätsmodell für Systeme und Software |
| **IEEE 829** | historischer Standard für Testdokumentation; inzwischen abgelöst |
| **BS 7925** | historischer britischer Standard zu Software-Testtechniken |

Die älteren Standards wie **IEEE 829** wurden weitgehend durch die ISO/IEC/IEEE-29119-Familie abgelöst.

---

# 3. ISO/IEC/IEEE 29119

Die **ISO/IEC/IEEE 29119** ist eine internationale Normenfamilie für Softwaretesting.

Sie definiert:

- grundlegende Begriffe
- Testprozesse
- Testdokumentation
- Testtechniken
- Keyword-Driven Testing
- Hinweise für agile Entwicklungsmodelle

## Die wichtigsten Teile

| Teil | Inhalt |
|---|---|
| **29119-1** | General Concepts – grundlegende Konzepte und Begriffe |
| **29119-2** | Test Processes – Testprozesse |
| **29119-3** | Test Documentation – Testdokumentation |
| **29119-4** | Test Techniques – Testtechniken |
| **29119-5** | Keyword-Driven Testing |
| **29119-6 (TR)** | Anwendung der 29119-Familie in agilen Projekten |

## ISO/IEC/IEEE 29119-2

Teil 2 beschreibt Testprozesse, die unabhängig vom verwendeten Softwareentwicklungs-Lebenszyklusmodell eingesetzt werden können.

Unterschieden werden insbesondere:

- organisatorische Testprozesse
- Testmanagementprozesse
- dynamische Testprozesse

## ISO/IEC/IEEE 29119-3

Behandelt Testdokumentation und Testartefakte.

Beispiele:

- Testplan
- Testspezifikation
- Teststatusbericht
- Testabschlussbericht

## ISO/IEC/IEEE 29119-4

Beschreibt Testentwurfstechniken.

Beispiele:

- Äquivalenzklassenbildung
- Grenzwertanalyse
- Entscheidungstabellentest
- Zustandsübergangstest
- strukturbasierte Techniken

## ISO/IEC/IEEE 29119-5

Behandelt **Keyword-Driven Testing**.

Dabei werden Testabläufe mithilfe fachlich verständlicher Schlüsselwörter beschrieben.

Beispiel:

```text
Karte_einführen
PIN_eingeben
Betrag_auswählen
Auszahlung_bestätigen
```

Die technische Implementierung dieser Schlüsselwörter erfolgt getrennt davon.

Vorteil:

> Fachliche Testfälle können auch von Personen verstanden werden, die keine Programmiersprache beherrschen.

---

# 4. ISTQB

Das **International Software Testing Qualifications Board (ISTQB)** stellt ein international verbreitetes Zertifizierungssystem für Softwaretester bereit.

Das ISTQB definiert unter anderem:

- einheitliche Fachbegriffe
- Testprozesse
- Testtechniken
- Rollen und Aufgaben
- Testmanagementwissen
- Testautomatisierungswissen

## Zertifizierungsstufen

Beispiele:

- **Certified Tester Foundation Level (CTFL)**
- Advanced Level
- Specialist-Zertifizierungen
- Expert Level

Das aktuelle Foundation-Level-Modell basiert auf **CTFL v4.x**.

### Abgrenzung

> **ISO 29119 normiert Prozesse und Konzepte für Organisationen.**

> **ISTQB vermittelt standardisiertes Wissen und zertifiziert Personen.**

Beide Systeme überschneiden sich in vielen Begriffen und Konzepten, sind jedoch nicht identisch.

---

# 5. Grundbegriffe

| Begriff | Bedeutung |
|---|---|
| **Testobjekt** | zu prüfendes Arbeitsergebnis, Produkt, System oder Bestandteil |
| **Testbasis** | Grundlage, aus der Testfälle abgeleitet werden |
| **Testfall** | Menge von Vorbedingungen, Eingaben, Aktionen, erwarteten Ergebnissen und Nachbedingungen für ein Testziel |
| **Testdaten** | Daten, die zur Durchführung eines Tests benötigt werden |
| **Testumgebung** | technische und organisatorische Umgebung für die Durchführung von Tests |
| **Testware** | Artefakte, die während des Testprozesses erstellt oder verwendet werden |
| **Testprotokoll** | Aufzeichnung von Testausführungen und Ereignissen |
| **Entry-Kriterien** | Bedingungen für den sinnvollen Beginn einer Testaktivität |
| **Exit-Kriterien** | Bedingungen für den Abschluss einer Testaktivität |
| **Testabdeckung** | Grad, zu dem ein definierter Abdeckungsgegenstand durch Tests erfasst wurde |

---

# 6. Testprozess nach ISTQB CTFL v4

Der aktuelle ISTQB-Testprozess umfasst sieben grundlegende Aktivitäten.

```text
Testplanung
     ↓
Testüberwachung und Teststeuerung
     ↓
Testanalyse
     ↓
Testentwurf
     ↓
Testrealisierung
     ↓
Testdurchführung
     ↓
Testabschluss
```

Die Aktivitäten müssen nicht streng nacheinander durchgeführt werden.

In:

- agilen Projekten,
- iterativen Entwicklungsmodellen,
- DevOps-Umgebungen

können sie sich überschneiden oder mehrfach wiederholt werden.

---

# 7. Testplanung

Bei der **Testplanung** wird festgelegt:

- was getestet werden soll,
- warum getestet wird,
- wie getestet wird,
- wer testet,
- wann getestet wird,
- welche Ressourcen benötigt werden,
- welche Risiken bestehen,
- welche Ergebnisse erwartet werden.

Typische Inhalte:

- Testziele
- Testumfang
- Testansatz
- Teststufen
- Testarten
- Testressourcen
- Zeitplan
- Rollen
- Verantwortlichkeiten
- Testumgebungen
- Testdaten
- Testwerkzeuge
- Entry-/Exit-Kriterien
- Testmetriken

---

# 8. Testüberwachung und Teststeuerung

## Testüberwachung

Beim Monitoring werden tatsächliche Werte mit der Planung verglichen.

Beispiele:

- Anzahl ausgeführter Testfälle
- Anzahl fehlgeschlagener Tests
- Defect-Zahlen
- Testabdeckung
- Fortschritt gegenüber Zeitplan
- Erfüllung von Exit-Kriterien

## Teststeuerung

Wenn Abweichungen festgestellt werden, werden Steuerungsmaßnahmen eingeleitet.

Beispiele:

- Testprioritäten ändern
- Ressourcen umverteilen
- Testumfang anpassen
- zusätzliche Testfälle durchführen
- Termine oder Testumgebungen anpassen

### Merksatz

> **Monitoring erkennt Abweichungen – Control reagiert darauf.**

---

# 9. Testanalyse

In der **Testanalyse** wird untersucht, **was getestet werden muss**.

Aus der Testbasis werden sogenannte **Testbedingungen** abgeleitet.

Beispiele:

Anforderung:

> Eine Chipkarte muss nach drei falschen PIN-Eingaben gesperrt werden.

Testbedingungen:

- richtige PIN
- einmal falsche PIN
- zweimal falsche PIN
- dreimal falsche PIN
- Verhalten nach Sperrung

---

# 10. Testentwurf

Im **Testentwurf** wird bestimmt, **wie die Testbedingungen geprüft werden**.

Dabei entstehen beispielsweise:

- Testfälle
- erwartete Ergebnisse
- benötigte Testdaten
- Anforderungen an Testumgebungen

Hier kommen Testtechniken zum Einsatz.

---

# 11. Testrealisierung

Bei der Testrealisierung werden die Tests für die Durchführung vorbereitet.

Dazu gehören beispielsweise:

- Testfälle konkretisieren
- Testfälle priorisieren
- Testsuiten bilden
- Testdaten bereitstellen
- automatisierte Testskripte erstellen
- Testumgebung vorbereiten
- Testabläufe festlegen

---

# 12. Testdurchführung

Während der Testdurchführung werden:

1. Tests ausgeführt,
2. tatsächliche Ergebnisse erfasst,
3. Ist- und Soll-Ergebnisse verglichen,
4. Abweichungen analysiert,
5. Fehler dokumentiert.

Ergebnis:

```text
Testfall
  ↓
Durchführung
  ↓
Ist-Ergebnis
  ↓
Vergleich mit Soll-Ergebnis
  ↓
Pass / Fail
```

---

# 13. Testabschluss

Beim Testabschluss werden Testaktivitäten formal beendet.

Dazu gehören:

- Teststatus abschließend bewerten
- Exit-Kriterien überprüfen
- offene Fehler dokumentieren
- Testware archivieren
- Testumgebungen zurückbauen oder übergeben
- Lessons Learned durchführen
- Testabschlussbericht erstellen
- Verbesserungsmöglichkeiten ableiten

---

# 14. Teststrategie und Testkonzept

## Teststrategie

Die Teststrategie legt den grundsätzlichen Testansatz fest.

Typische Inhalte:

- Qualitätsziele
- Testziele
- Teststufen
- Testarten
- Risikofokus
- Automatisierungsstrategie
- Testtechniken
- Testumgebungen
- Metriken
- Verantwortlichkeiten

## Testkonzept

Das Testkonzept beschreibt die konkrete Umsetzung der Teststrategie für ein Projekt oder Testobjekt.

### Prüfungsorientierte W-Fragen

| Frage | Inhalt |
|---|---|
| **Warum?** | Testziele |
| **Was?** | Testobjekte und Testumfang |
| **Wer?** | Rollen und Verantwortlichkeiten |
| **Wann?** | Zeitplanung |
| **Wo?** | Testumgebung |
| **Wie?** | Testmethoden und Testtechniken |
| **Womit?** | Testwerkzeuge und Testdaten |
| **Wann abgeschlossen?** | Exit- bzw. Abnahmekriterien |

---

# 15. Testorganisation und Rollen

Je nach Projekt können unterschiedliche Rollen beteiligt sein.

## Testmanager

Typische Aufgaben:

- Testplanung
- Ressourcenplanung
- Risikomanagement
- Testüberwachung
- Teststeuerung
- Reporting
- Koordination von Stakeholdern
- kontinuierliche Verbesserung

## Tester

Typische Aufgaben:

- Testanalyse
- Testentwurf
- Testrealisierung
- Testdurchführung
- Fehlerdokumentation

## Entwickler

Typische Aufgaben:

- Komponententests
- technische Fehleranalyse
- Fehlerbehebung
- Unterstützung bei Integrationstests

## Product Owner / Fachbereich

Typische Aufgaben:

- fachliche Anforderungen
- Akzeptanzkriterien
- Priorisierung
- fachliche Abnahmetests

## Security-Spezialist

Typische Aufgaben:

- Sicherheitstests
- Schwachstellenanalysen
- Penetrationstests
- Bewertung sicherheitsrelevanter Defekte

## Betrieb / DevOps

Typische Aufgaben:

- Testumgebungen
- Deployment
- CI/CD
- Monitoring
- Wiederanlauf- und Betriebstests

---

# 16. Teststufen

Teststufen bündeln Testaktivitäten in Bezug auf eine bestimmte Entwicklungs- bzw. Systemebene.

Der ISTQB CTFL v4 beschreibt fünf wesentliche Teststufen.

## 16.1 Komponententest / Unit Test

Test einzelner Komponenten in Isolation.

Beispiele:

- Funktion
- Methode
- Klasse
- Modul

Typische Eigenschaften:

- meist durch Entwickler
- häufig automatisiert
- sehr schnell
- Nutzung von Unit-Test-Frameworks

### AAA-Prinzip

```text
Arrange → vorbereiten
Act     → Aktion ausführen
Assert  → Ergebnis prüfen
```

---

## 16.2 Komponentenintegrationstest

Prüft die Schnittstellen und Interaktionen zwischen Komponenten.

Beispiele:

- Modul A ↔ Modul B
- Klasse ↔ Datenbankabstraktion
- Microservice-interne Komponenten

Fokus:

> Funktioniert das Zusammenspiel der Komponenten?

---

## 16.3 Systemtest

Test des vollständig integrierten Systems.

Geprüft werden:

- funktionale Anforderungen
- nicht-funktionale Anforderungen
- End-to-End-Abläufe
- Systemverhalten

Beispiel:

> Kann ein Benutzer eine Bestellung vollständig vom Login bis zur Bestätigung durchführen?

---

## 16.4 Systemintegrationstest

Test der Schnittstellen zwischen:

- unterschiedlichen Systemen,
- externen Diensten,
- Fremdsystemen,
- APIs.

Beispiel:

```text
Onlineshop
   ↓
Payment Provider
   ↓
Bank
```

Hier wird insbesondere das Zusammenspiel zwischen den Systemen geprüft.

---

## 16.5 Abnahmetest

Der Abnahmetest prüft die Eignung des Systems für den vorgesehenen Einsatz und die Erfüllung fachlicher bzw. geschäftlicher Anforderungen.

Formen sind unter anderem:

- User Acceptance Testing (UAT)
- betrieblicher Abnahmetest
- vertraglicher Abnahmetest
- regulatorischer Abnahmetest
- Alpha-Test
- Beta-Test

### Alpha-Test

Test durch potenzielle oder repräsentative Benutzer innerhalb bzw. unter Kontrolle der Herstellerorganisation.

### Beta-Test

Test durch externe Benutzer in realitätsnahen Einsatzbedingungen.

---

# 17. Testarten

Testarten können grundsätzlich auf unterschiedlichen Teststufen durchgeführt werden.

## Funktionale Tests

Prüfen:

> **Was soll das System tun?**

Beispiele:

- Login
- Zahlung
- Datenspeicherung
- Berechtigungsprüfung

---

## Nicht-funktionale Tests

Prüfen:

> **Wie gut erfüllt das System bestimmte Qualitätsmerkmale?**

Beispiele:

- Performance
- Sicherheit
- Zuverlässigkeit
- Usability
- Kompatibilität
- Wartbarkeit

---

## Black-Box-Tests

Die Tests werden aus Anforderungen oder Spezifikationen abgeleitet.

Die interne Implementierung ist für den Testentwurf nicht relevant.

---

## White-Box-Tests

Die Tests werden anhand der internen Struktur des Systems entwickelt.

Beispiele:

- Anweisungsüberdeckung
- Zweigüberdeckung

---

## Änderungsbezogene Tests

Dazu gehören insbesondere:

### Bestätigungstest

Prüft:

> Wurde ein konkreter Fehler erfolgreich behoben?

### Regressionstest

Prüft:

> Hat eine Änderung unbeabsichtigt bereits funktionierende Bereiche beeinträchtigt?

---

# 18. Testtechniken

Testtechniken dienen der systematischen Ableitung von Testfällen.

## Black-Box-Techniken

### Äquivalenzklassenbildung

Eingabewerte werden in Klassen eingeteilt, bei denen ein ähnliches Verhalten erwartet wird.

Beispiel:

Alter erlaubt:

```text
18–100
```

Äquivalenzklassen:

- < 18 → ungültig
- 18–100 → gültig
- > 100 → ungültig

---

## Grenzwertanalyse

Fehler treten besonders häufig an Grenzen auf.

Beispiel:

Erlaubter Bereich:

```text
18–100
```

Interessante Testwerte:

```text
17
18
19
99
100
101
```

---

## Entscheidungstabellentest

Geeignet für Kombinationen mehrerer Bedingungen.

Beispiel:

```text
Karte gültig?
PIN korrekt?
Guthaben ausreichend?
→ Auszahlung erlaubt?
```

---

## Zustandsübergangstest

Geeignet für Systeme mit definierten Zuständen.

Beispiel:

```text
Karte aktiv
   ↓ 3 falsche PINs
Karte gesperrt
```

---

# 19. Statische und dynamische Tests

## Statische Tests

Das Testobjekt wird **nicht ausgeführt**.

Beispiele:

- Review
- Walkthrough
- Inspektion
- statische Codeanalyse

Ziel:

> Fehler möglichst früh erkennen.

---

## Dynamische Tests

Das Testobjekt wird ausgeführt.

Beispiele:

- Unit Test
- Systemtest
- Performance-Test
- Sicherheitstest

---

# 20. Weitere wichtige Testformen

Diese Begriffe sind prüfungsrelevant, aber **keine eigenständigen Teststufen im ISTQB-Sinne**.

## Smoke-Test

Kurzer Test zentraler Kernfunktionen eines neuen Builds.

Ziel:

> Prüfen, ob das System stabil genug für weitere Tests ist.

Beispiel:

- Anwendung startet
- Login funktioniert
- Datenbank erreichbar
- zentrale Oberfläche lädt

---

## Regressionstest

Prüft, ob Änderungen unbeabsichtigte Auswirkungen auf bestehende Funktionalität verursacht haben.

Sehr gut automatisierbar.

---

## Bestätigungstest / Re-Test

Prüft gezielt, ob ein zuvor gefundener Fehler behoben wurde.

### Unterschied

> **Re-Test = Fehler behoben?**

> **Regression = Nebenwirkungen entstanden?**

---

## Wartungstest

Tests nach Änderungen an einem bestehenden System.

Auslöser können sein:

- Fehlerbehebung
- neue Funktion
- Migration
- Betriebssystemupdate
- Infrastrukturänderung
- Stilllegung

Wartungstests können mehrere Teststufen und Testarten umfassen.

---

## Wiederanlauftest

Prüft, ob ein System nach:

- Absturz
- Stromausfall
- Infrastrukturfehler
- Netzwerkunterbrechung

ordnungsgemäß und konsistent wieder in Betrieb genommen werden kann.

Geprüft werden beispielsweise:

- Datenkonsistenz
- Wiederherstellbarkeit
- Reihenfolge des Wiederanlaufs
- Abhängigkeiten
- definierte Wiederanlaufzeiten

---

# 21. Sicherheitstests

Sicherheitstests überprüfen sicherheitsrelevante Eigenschaften eines Systems.

Beispiele:

- Authentifizierung
- Autorisierung
- Verschlüsselung
- Session Management
- Eingabevalidierung
- Logging
- Zugriffsschutz
- Schwachstellen

## Penetrationstest

Ein Penetrationstest simuliert unter definierten Bedingungen reale Angriffsmöglichkeiten.

Ein mögliches vereinfachtes Vorgehen ist:

```text
Auftrag und Scope festlegen
        ↓
Informationsbeschaffung
        ↓
Schwachstellen identifizieren
        ↓
Schwachstellen bewerten
        ↓
ggf. kontrolliert ausnutzen
        ↓
Auswirkungen analysieren
        ↓
Dokumentieren und berichten
```

**Wichtig:**

> Es gibt kein universell verbindliches „ISTQB-6-Schritte-Modell“ für Penetrationstests.

Für Penetrationstests existieren eigene Vorgehensmodelle und Standards, beispielsweise aus dem BSI-, OWASP- oder PTES-Umfeld.

---

# 22. Testautomatisierung

**Testautomatisierung** ist der Einsatz von Software zur automatisierten Unterstützung von Testaktivitäten.

Automatisiert werden können beispielsweise:

- Testvorbereitung
- Testdatenerzeugung
- Testausführung
- Ergebnisvergleich
- Logging
- Reporting
- Wiederholungen

## Vorteile

- schnelle Wiederholung
- konsistente Testdurchführung
- hohe Wiederholbarkeit
- Unterstützung von Regressionstests
- Integration in CI/CD
- schnelle Rückmeldung an Entwickler
- umfangreiche Tests mit vielen Datensätzen

## Nachteile und Risiken

- initialer Entwicklungsaufwand
- Wartungsaufwand
- Werkzeugkosten
- erforderliches Fachwissen
- Abhängigkeit von Testumgebungen
- instabile Tests
- falsches Sicherheitsgefühl bei schlechter Testqualität

### Merksatz

> **Automatisierung verbessert nicht automatisch schlechte Tests – sie führt schlechte Tests nur schneller aus.**

---

# 23. Geeignete Tests für Automatisierung

## Besonders geeignet

- Unit Tests
- Regressionstests
- API-Tests
- Integrationstests
- wiederkehrende Smoke-Tests
- datengetriebene Tests
- häufig ausgeführte Tests

## Weniger geeignet

- explorative Tests
- subjektive Usability-Bewertungen
- Tests mit häufig wechselnder Benutzeroberfläche
- einmalig durchgeführte Tests
- Tests mit sehr hohem Automatisierungsaufwand und geringer Wiederholungsrate

---

# 24. Testautomatisierungspyramide

Die Testpyramide ist ein verbreitetes Modell für die Verteilung automatisierter Tests.

```text
             /\
            /  \
           / UI \
          /------\
         /  API / \
        /Integration\
       /-------------\
      /  Unit Tests   \
     /_________________\
```

## Grundidee

### Unten

Viele:

- schnelle
- kleine
- stabile
- günstige

Unit Tests.

### Mitte

Weniger:

- API-Tests
- Service-Tests
- Integrationstests

### Oben

Wenige:

- UI-Tests
- End-to-End-Tests

Diese sind typischerweise:

- langsamer
- komplexer
- wartungsintensiver
- fehleranfälliger

### Anti-Pattern: Ice Cream Cone

Eine umgekehrte Pyramide:

- sehr viele manuelle/UI-Tests
- wenige API-Tests
- kaum Unit Tests

führt häufig zu:

- langsamen Tests
- hoher Wartung
- instabilen Testläufen
- spätem Feedback

---

# 25. Automatisierungsansätze

| Ansatz | Prinzip |
|---|---|
| **Capture & Replay** | Benutzerinteraktionen werden aufgezeichnet und wiedergegeben |
| **Scripted Testing** | Tests werden direkt programmiert |
| **Data-Driven Testing** | Testlogik und Testdaten werden getrennt |
| **Keyword-Driven Testing** | Tests werden über fachliche Schlüsselwörter beschrieben |
| **BDD** | Verhalten wird anhand fachlich lesbarer Szenarien beschrieben |

---

# 26. Data-Driven Testing

Testlogik und Testdaten werden getrennt.

Beispiel:

```text
Login-Test
```

Datensätze:

```text
user1 / richtig
user2 / falsch
user3 / gesperrt
user4 / abgelaufen
```

Eine Testlogik wird mit vielen unterschiedlichen Datensätzen ausgeführt.

Vorteile:

- weniger duplizierter Testcode
- hohe Testabdeckung
- einfache Erweiterung um neue Testdaten

---

# 27. Keyword-Driven Testing

Testschritte werden als Schlüsselwörter beschrieben.

Beispiel:

```text
Öffne_Login
Gib_Benutzername_ein
Gib_Passwort_ein
Klicke_Anmelden
Prüfe_Startseite
```

Die eigentliche technische Implementierung ist getrennt.

Vorteil:

> Fachliche und technische Sicht können voneinander getrennt werden.

---

# 28. Behaviour-Driven Development / BDD

BDD beschreibt erwartetes Verhalten häufig anhand der Struktur:

```text
Given
When
Then
```

Beispiel:

```text
Given der Benutzer ist angemeldet
When er seine Chipkarte sperrt
Then darf mit der Karte keine Zahlung mehr möglich sein
```

**Gherkin** ist eine verbreitete Sprache für solche Szenarien.

**Cucumber** ist ein Werkzeug, das Gherkin-Szenarien verarbeiten kann.

---

# 29. Testautomatisierungsarchitektur

Eine Testautomatisierung sollte nicht lediglich aus einzelnen unstrukturierten Skripten bestehen.

Eine **Test Automation Architecture (TAA)** definiert die technische Struktur einer Automatisierungslösung.

Der aktuelle ISTQB-CTAL-TAE verwendet als abstraktes Referenzmodell die:

> **Generic Test Automation Architecture – gTAA**

Die gTAA betrachtet insbesondere die Kommunikation zwischen der Testautomatisierung und:

- dem **System Under Test (SUT)**
- dem Testmanagement
- dem Projektmanagement
- dem Konfigurationsmanagement

Aus der abstrakten gTAA wird für ein konkretes Projekt eine geeignete Testautomatisierungsarchitektur abgeleitet.

## Wichtige Ziele

- Modularität
- Wartbarkeit
- Wiederverwendbarkeit
- klare Schnittstellen
- Erweiterbarkeit
- Trennung von Testlogik und technischer Anbindung

---

# 30. CI/CD und Testautomatisierung

Automatisierte Tests können in **Continuous-Integration- und Continuous-Delivery-Pipelines** eingebunden werden.

Beispiel:

```text
Code Commit
    ↓
Build
    ↓
Unit Tests
    ↓
Static Analysis
    ↓
Integration/API Tests
    ↓
Deployment Testumgebung
    ↓
System-/E2E-Tests
    ↓
Quality Gate
    ↓
Deployment
```

Vorteile:

- frühes Feedback
- Fehler schneller erkennen
- reproduzierbare Tests
- automatisierte Qualitätskontrollen

---

# 31. Quality Gates

Ein **Quality Gate** ist eine definierte Qualitätsbedingung, die erfüllt sein muss, bevor ein Prozess weitergeführt werden darf.

Beispiele:

```text
100 % kritische Tests bestanden
0 offene kritische Defects
≥ 80 % definierte Code Coverage
Security Scan ohne kritischen Fund
```

Wichtig:

> Ein Quality Gate sollte anhand projektspezifischer Risiken und Qualitätsziele definiert werden.

---

# 32. Flaky Tests

Ein **Flaky Test** liefert bei unverändertem Testobjekt unterschiedliche Ergebnisse.

Beispiel:

```text
Lauf 1 → PASS
Lauf 2 → FAIL
Lauf 3 → PASS
```

Mögliche Ursachen:

- Timing-Probleme
- Race Conditions
- Netzwerkprobleme
- instabile Testumgebung
- gemeinsam genutzte Testdaten
- externe Abhängigkeiten
- schlecht synchronisierte UI-Tests

Folge:

> Vertrauen in die automatisierten Tests sinkt.

---

# 33. Testautomatisierungswerkzeuge

Werkzeuge sollten anhand des jeweiligen Einsatzbereichs ausgewählt werden.

| Bereich | Beispiele |
|---|---|
| **Unit Tests** | JUnit, pytest, NUnit, Jest |
| **Web UI** | Selenium, Playwright, Cypress |
| **Mobile Apps** | Appium |
| **BDD** | Cucumber |
| **Keyword-Driven** | Robot Framework |
| **API-Tests** | Postman/Newman, REST Assured, pytest |
| **Testmanagement** | Jira mit Testmanagement-Erweiterungen, ALM-Werkzeuge |

Die Auswahl sollte nicht allein anhand der Popularität erfolgen.

Zu berücksichtigen sind:

- vorhandener Technologie-Stack
- Programmiersprachen
- Know-how
- Wartbarkeit
- Schnittstellen
- CI/CD-Unterstützung
- Lizenzmodell
- langfristige Pflege
- Testziele

---

# 34. ROI der Testautomatisierung

Automatisierung verursacht zunächst Aufwand.

```text
Kosten Automatisierung
=
Entwicklung
+ Werkzeuge
+ Infrastruktur
+ Wartung
```

Manuelle Tests verursachen bei jeder Wiederholung Aufwand.

Vereinfacht lohnt sich Automatisierung insbesondere dann, wenn:

```text
eingesparter manueller Testaufwand
>
Entwicklungs- und Wartungsaufwand der Automatisierung
```

## Gute Automatisierungskandidaten

Ein Testfall eignet sich besonders, wenn er:

- häufig wiederholt wird
- stabil spezifiziert ist
- reproduzierbar ist
- hohe geschäftliche Bedeutung besitzt
- automatisiert eindeutig bewertet werden kann
- manuell hohen Aufwand verursacht

---

# 35. Testmetriken

Testmetriken unterstützen Testüberwachung und Entscheidungen.

Beispiele:

## Testfortschritt

```text
ausgeführte Testfälle / geplante Testfälle
```

## Erfolgsquote

```text
bestandene Tests / ausgeführte Tests
```

## Fehleranzahl

Nach:

- Priorität
- Schweregrad
- Komponente
- Status

## Testabdeckung

Beispiele:

- Requirements Coverage
- Code Coverage
- Branch Coverage

### Wichtig

> Eine hohe Testabdeckung bedeutet nicht automatisch eine hohe Softwarequalität.

100 % Code Coverage kann beispielsweise trotzdem schlechte oder unvollständige Testfälle enthalten.

---

# 36. Fehlerpriorität und Fehlerschwere

## Severity / Schweregrad

Beschreibt:

> Wie stark ist die technische oder geschäftliche Auswirkung des Fehlers?

Beispiel:

**kritisch:** Zahlungssystem funktioniert nicht.

## Priority / Priorität

Beschreibt:

> Wie dringend muss der Fehler behoben werden?

Ein Fehler kann:

- hohe Severity, niedrige Priority
- niedrige Severity, hohe Priority

haben.

Beispiel:

Ein Schreibfehler auf der Startseite besitzt technisch geringe Severity, kann vor einem wichtigen Produktlaunch aber hohe Priorität haben.

---

# 37. Risikobasiertes Testen

Beim **risikobasierten Testen** werden Testaktivitäten anhand von Risiken priorisiert.

Grundidee:

```text
höheres Produktrisiko
      ↓
höhere Testpriorität
      ↓
größere Testtiefe
```

Typische Kriterien:

- Schadensausmaß
- Eintrittswahrscheinlichkeit
- Geschäftskritikalität
- Komplexität
- Änderungshäufigkeit
- historische Fehlerdichte
- Sicherheitsrelevanz

### Beispiel

Eine Chipkartenfunktion für:

```text
Zahlungsfreigabe
```

benötigt eine höhere Testtiefe als:

```text
Änderung der Hintergrundfarbe
```

---

# 38. Testmanagement und Informationssicherheit

Für Informationssicherheitsprojekte sind insbesondere folgende Testbereiche relevant:

- Authentifizierung
- Autorisierung
- Zugriffskontrolle
- Kryptografie
- Logging
- Eingabevalidierung
- Datenschutz
- Wiederherstellung
- Backup
- Hochverfügbarkeit
- sichere Konfiguration
- Schwachstellenmanagement

Testmanagement sorgt dafür, dass diese Bereiche:

- geplant,
- priorisiert,
- dokumentiert,
- nachvollziehbar überprüft

werden.

---

# 39. Typische IHK-Prüfungsfragen

## „Erläutern Sie fünf Teststufen.“

Mögliche Antwort:

1. **Komponententest** → einzelne Komponenten isoliert prüfen
2. **Komponentenintegrationstest** → Zusammenarbeit interner Komponenten prüfen
3. **Systemtest** → vollständiges System gegen Anforderungen testen
4. **Systemintegrationstest** → Schnittstellen zu anderen Systemen testen
5. **Abnahmetest** → fachliche und betriebliche Einsatzfähigkeit bestätigen

---

## „Erläutern Sie drei Testarten.“

Beispiel:

### Funktionstest

Prüft, ob das System die fachlich geforderten Funktionen korrekt ausführt.

### Sicherheitstest

Prüft beispielsweise Authentifizierung, Berechtigungen und Schutz vor Angriffen.

### Performance-Test

Prüft Antwortzeiten, Durchsatz und Verhalten unter Last.

---

## „Erläutern Sie einen Regressionstest.“

> Ein Regressionstest prüft nach einer Änderung, ob bereits vorhandene und zuvor funktionierende Funktionen unbeabsichtigt beeinträchtigt wurden. Aufgrund der häufigen Wiederholung eignen sich Regressionstests besonders für die Testautomatisierung.

---

## „Erläutern Sie einen Wiederanlauftest.“

> Ein Wiederanlauftest prüft, ob ein System nach einem ungeplanten Ausfall kontrolliert, konsistent und innerhalb der vorgegebenen Zeit wieder in Betrieb genommen werden kann. Dabei werden beispielsweise Datenkonsistenz, Abhängigkeiten und die Wiederanlaufreihenfolge geprüft.

---

## „Nennen Sie Vorteile der Testautomatisierung.“

Mögliche Antworten:

- schnellere Testausführung
- hohe Wiederholbarkeit
- frühes Feedback
- geringerer manueller Aufwand bei häufigen Wiederholungen
- gute Integration in CI/CD
- umfangreiche Regressionstests möglich

---

# ⚡ Schnellcheck – 60 Sekunden vor der Prüfung

- **Testmanagement** → planen, überwachen, steuern, abschließen
- **7 Aktivitäten** → Planung – Monitoring/Control – Analyse – Design – Implementierung – Durchführung – Abschluss
- **Testbasis** → Grundlage für Testanalyse
- **Testfall** → Bedingungen, Eingaben, Aktionen und erwartetes Ergebnis
- **5 Teststufen** → Component – Component Integration – System – System Integration – Acceptance
- **UAT** → Form des Abnahmetests
- **Alpha/Beta** → Formen des Abnahmetests, keine eigenen Teststufen
- **Smoke-Test** → kurzer Kernfunktionstest, keine Teststufe
- **Wartungstest** → Testen nach Änderungen am bestehenden System
- **Funktional** → Was tut das System?
- **Nicht-funktional** → Wie gut tut es das?
- **Black-Box** → Test aus Spezifikation
- **White-Box** → Test aus interner Struktur
- **Re-Test** → konkreten Fix überprüfen
- **Regressionstest** → Nebenwirkungen einer Änderung erkennen
- **Statisch** → ohne Ausführung
- **Dynamisch** → mit Ausführung
- **Äquivalenzklassen** → ähnliche Eingaben gruppieren
- **Grenzwertanalyse** → Werte an Grenzen testen
- **BDD** → Given – When – Then
- **Testpyramide** → viele Unit Tests, wenige UI/E2E-Tests
- **Flaky Test** → wechselndes Ergebnis ohne relevante Änderung
- **Quality Gate** → definierte Qualitätsbedingung vor nächster Prozessstufe
- **CI/CD** → automatisierte Tests früh und regelmäßig ausführen
- **gTAA** → abstraktes Architekturmodell für Testautomatisierung
- **Automatisierung ≠ Qualität** → schlechte Tests werden durch Automatisierung nicht besser

---

# Prüfungs-Merksätze

> **Testplanung = Was wollen wir wie testen?**

> **Testanalyse = Was müssen wir testen?**

> **Testentwurf = Wie prüfen wir es?**

> **Testrealisierung = Tests ausführbar machen.**

> **Testdurchführung = Soll und Ist vergleichen.**

> **Testabschluss = Ergebnisse bewerten und Testaktivitäten sauber beenden.**

---

> **Teststufe = Ebene des Testobjekts.**

> **Testart = Zweck bzw. Qualitätsmerkmal des Tests.**

> **Testtechnik = Verfahren zur Ableitung der Testfälle.**

---

> **Bestätigungstest = Hat der Fix funktioniert?**

> **Regressionstest = Hat der Fix etwas anderes kaputtgemacht?**

---

> **Statische Tests finden Fehler ohne Programmausführung.**

> **Dynamische Tests prüfen das Verhalten während der Ausführung.**

---

> **Testautomatisierung ist besonders sinnvoll bei häufigen, stabilen und eindeutig auswertbaren Tests.**

---

# Quellen

- ISTQB: Certified Tester Foundation Level Syllabus v4.0.1
- ISTQB: Certified Tester Advanced Level – Test Management
- ISTQB: Certified Tester Advanced Level – Test Automation Engineering v2.0
- ISTQB Glossary
- ISO/IEC/IEEE 29119-1:2022 – General Concepts
- ISO/IEC/IEEE 29119-2:2021 – Test Processes
- ISO/IEC/IEEE 29119-3:2021 – Test Documentation
- ISO/IEC/IEEE 29119-4:2021 – Test Techniques
- ISO/IEC/IEEE 29119-5:2024 – Keyword-Driven Testing
- ISO/IEC TR 29119-6:2021 – Guidelines for agile projects