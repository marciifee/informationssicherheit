# Lernblatt / Handout: Claim-Management in IT-Projekten

### Kompaktes Nachschlagewerk für die IHK-Prüfung „Geprüfter Berufsspezialist für Informationssicherheit“

**Stand: 31. August 2026**  
**Schwerpunkt:** Vertragsabweichungen, Change Requests, Nachforderungen, Claim-Prävention und Claim-Bearbeitung

> **Hinweis:** Claim-Management ist Vertrags- und Projektmanagement. Dieses Handout ersetzt keine rechtliche Prüfung konkreter Ansprüche.

---

# ⚡ Schnellcheck vor der Prüfung

- **Claim** = geltend gemachte Forderung wegen einer tatsächlichen oder behaupteten Vertragsabweichung.
- Claims können **finanziell, terminlich oder sachlich** sein.
- **Eigenclaim** = eigene Forderung gegenüber Vertragspartner.
- **Fremdclaim** = Forderung des Vertragspartners gegen das eigene Unternehmen.
- **Potenzial ≠ Anspruch** → Eine Soll-Ist-Abweichung ist zunächst nur eine mögliche Claim-Situation.
- **Change Request ≠ Claim** → ein Änderungswunsch wird erst durch Vereinbarung bzw. Anspruchsgrundlage rechtlich relevant.
- **Claim-Prävention beginnt vor Vertragsunterzeichnung.**
- **Dokumentation ist der Kern des Claim-Managements.**
- **Abnahme (§ 640 BGB)** ist bei Werkverträgen ein zentraler Rechtszeitpunkt.
- **Verzug (§ 286 BGB)** kann Schadensersatzansprüche auslösen.
- **Mängelrechte (§ 634 BGB)** sind von zusätzlichen Änderungsleistungen zu unterscheiden.
- **Mitwirkungsverzug des Bestellers (§ 642 BGB)** kann Ansprüche des Auftragnehmers begründen.
- **Vertragsstrafen müssen vereinbart sein.**
- **Claim Register** = zentrale Übersicht aller Claims.
- **Eskalation** erst nach strukturierter Prüfung und Verhandlung.
- **Lessons Learned** reduzieren Claims in Folgeprojekten.

---

# 1. Definition

Ein Claim ist eine Forderung eines Vertragspartners, die aus einer Abweichung vom vereinbarten Vertrags-Soll hergeleitet wird.

Mögliche Forderungen:

- zusätzliche Vergütung
- Fristverlängerung
- Nachbesserung
- Schadensersatz
- Vertragsstrafe
- Minderung
- Rücktritt
- zusätzliche Leistungen

---

# 2. Ziele des Claim-Managements

Claim-Management umfasst:

- frühzeitiges Erkennen
- Vermeidung unnötiger Claims
- Bewertung
- Dokumentation
- Durchsetzung berechtigter Eigenclaims
- Abwehr unberechtigter Fremdclaims
- Verhandlung und Beilegung

### Merksatz

> **Claim-Management ist kein „Streitmanagement“, sondern kontrolliertes Management von Vertragsabweichungen.**

---

# 3. Claim-Prävention

Die beste Claim-Situation ist die, die durch klare Verträge gar nicht entsteht.

Prävention:

- klarer Scope
- eindeutige Leistungsbeschreibung
- Rollen/RACI
- Abnahmekriterien
- Change-Prozess
- Mitwirkungspflichten
- Terminplan
- Eskalationsweg
- Dokumentationspflichten
- Claim-Fristen
- Haftungsregeln
- SLA

---

# 4. Vertrags-Soll

Das Vertrags-Soll kann sich ergeben aus:

- Vertrag
- Leistungsbeschreibung
- Spezifikation
- Pflichtenheft
- Terminplan
- Preisblatt
- SLA
- Sicherheitsanforderungen
- Change Orders
- Protokollen, soweit verbindlich
- freigegebenen Planständen

---

# 5. Ausführungs-Ist

Das Ist wird dokumentiert durch:

- tatsächliche Leistung
- Ist-Termine
- Testergebnisse
- Abnahmeprotokolle
- Tickets
- E-Mails
- Meeting Minutes
- Zeiterfassung
- Logs
- Change Records
- As-Built-Dokumentation

---

# 6. Soll-Ist-Vergleich

```text
Vertrags-Soll
      │
      ▼
Soll-Ist-Vergleich
      ▲
      │
Ausführungs-Ist
      ↓
Abweichung?
      ↓
Claim-Potenzial prüfen
```

### Korrektur zur Ausgangsfolie

> **Nicht jede Abweichung ist bereits ein Claim.**

Sie ist zunächst eine **potenzielle Claim-Situation**. Ein durchsetzbarer Anspruch benötigt eine tragfähige rechtliche oder vertragliche Grundlage.

---

# 7. Eigenclaim und Fremdclaim

## Eigenclaim

Eigene Forderung gegen den Vertragspartner.

Beispiele:

- Mehrvergütung
- Terminverlängerung
- Schadensersatz
- Entschädigung

## Fremdclaim

Forderung des Vertragspartners.

Beispiele:

- Vertragsstrafe
- Minderung
- Nachbesserung
- Schadensersatz

---

# 8. Typische Claim-Ursachen

- Scope Creep
- Zusatzwünsche
- unklare Anforderungen
- verspätete Freigaben
- verspätete Bereitstellung von Infrastruktur
- fehlende Testdaten
- Änderungen von Gesetzen
- geänderte technische Rahmenbedingungen
- Personalwechsel
- Lieferprobleme
- Qualitätsprobleme
- Sicherheitsanforderungen nach Projektstart
- unklare Schnittstellen

---

# 9. Claim-Schwerpunkte

| Dimension | Beispiele |
|---|---|
| **Zeit** | Meilensteinverzug, Freigaben |
| **Kosten** | Zusatzaufwand, Nacharbeit |
| **Leistung** | Scope, Mehrleistung |
| **Qualität** | Mängel, Tests |
| **Mitwirkung** | fehlende Daten/Zugänge |
| **Compliance** | neue gesetzliche Anforderungen |

---

# 10. Change Request

Ein Change Request beschreibt eine geplante Änderung.

Typischer Inhalt:

- Beschreibung
- Anlass
- Nutzen
- Auswirkungen auf Scope
- Kosten
- Termin
- Ressourcen
- Risiken
- Sicherheit
- Compliance

---

# 11. Change Request vs. Claim

| Change Request | Claim |
|---|---|
| Änderungswunsch/-antrag | Forderung |
| kann einvernehmlich sein | kann streitig sein |
| zielt auf Vertragsänderung | beruft sich auf Anspruch |
| prospektiv | oft aufgrund bereits eingetretener Abweichung |

### Merksatz

> **Change steuert Änderungen – Claim steuert Forderungen aus Abweichungen.**

---

# 12. Change-Control-Prozess

```text
Change identifizieren
      ↓
Change Request
      ↓
Auswirkungen analysieren
      ↓
Kosten / Termin / Risiko
      ↓
Freigabe oder Ablehnung
      ↓
Vertragsänderung
      ↓
Baseline aktualisieren
```

Ohne aktualisierte Baseline entsteht später Streit über Soll und Ist.

---

# 13. Anspruchsgrundlage prüfen

Vor jedem Claim:

1. Was wurde vereinbart?
2. Was ist tatsächlich passiert?
3. Welche Pflicht wurde verletzt/geändert?
4. Wer ist verantwortlich?
5. Gibt es Fristen/Formvorgaben?
6. Welche Auswirkungen entstanden?
7. Ist Kausalität nachweisbar?
8. Kann Schaden/Aufwand beziffert werden?

---

# 14. Wichtige BGB-Grundlagen

Je nach Fall:

- § 280 BGB – Schadensersatz wegen Pflichtverletzung
- § 286 BGB – Verzug
- § 288 BGB – Verzugszinsen
- § 631 BGB – Werkvertrag
- § 633 BGB – Sach-/Rechtsmangel
- § 634 BGB – Mängelrechte
- § 640 BGB – Abnahme
- § 641 BGB – Fälligkeit der Werkvergütung
- § 642 BGB – Mitwirkung des Bestellers
- §§ 339 ff. BGB – Vertragsstrafe

---

# 15. Leistungsstörung

Eine Leistungsstörung kann bestehen durch:

- Nichtleistung
- verspätete Leistung
- mangelhafte Leistung
- Verletzung von Nebenpflichten

Nicht jede Leistungsstörung führt automatisch zu jedem denkbaren Rechtsbehelf.

Voraussetzungen sind jeweils zu prüfen.

---

# 16. Verzug

Nach § 286 BGB kann Verzug eintreten, wenn eine fällige Leistung trotz erforderlicher Mahnung nicht erbracht wird.

Mahnung kann entbehrlich sein, z. B. bei kalendermäßig festgelegtem Termin.

Claim-relevant:

- Verzögerungskosten
- Mehrpersonal
- Stillstand
- Terminverschiebungen
- Folgeprobleme

---

# 17. Kausalität

Ein Claim benötigt häufig einen nachvollziehbaren Zusammenhang:

```text
Pflichtverletzung
      ↓
Abweichung
      ↓
Auswirkung
      ↓
Mehrkosten / Terminfolge
```

### Prüfungsmerksatz

> **Ohne Kausalitätsnachweis ist ein hoher Mehraufwand noch kein guter Claim.**

---

# 18. Mitwirkung des Auftraggebers

Bei IT-Werkprojekten können Mitwirkungshandlungen erforderlich sein.

Beispiele:

- Zugänge
- Daten
- Entscheidungen
- Fachpersonal
- Hardware
- Freigaben

§ 642 BGB kann bei unterlassener erforderlicher Mitwirkung eine Entschädigung begründen.

---

# 19. Abnahme

§ 640 BGB:

- vertragsgerechtes Werk ist grundsätzlich abzunehmen
- unwesentliche Mängel rechtfertigen keine Verweigerung
- Mängelvorbehalte dokumentieren

Abnahme ist claim-relevant für:

- Vergütung
- Beweisfragen
- Mängelrechte
- Fristen

---

# 20. Abnahmeprotokoll

Sollte mindestens enthalten:

- Leistung
- Datum
- Kriterien
- Testergebnisse
- Mängel
- Restpunkte
- Vorbehalte
- Nachfrist
- Verantwortliche

---

# 21. Mangel oder Change?

Wichtige Abgrenzung:

> **Mangel:** vereinbarte Leistung ist nicht vertragsgerecht.

> **Change:** gewünschte Leistung war bislang nicht geschuldet und soll geändert/erweitert werden.

Diese Unterscheidung entscheidet häufig über zusätzliche Vergütung.

---

# 22. Mängelrechte

Nach § 634 BGB:

- Nacherfüllung
- Selbstvornahme unter Voraussetzungen
- Rücktritt/Minderung
- Schadensersatz

### Prüfungsfalle

> **Ein Auftragnehmer darf nicht jeden Fehler als kostenpflichtigen Change behandeln.**

Wenn die Funktion bereits geschuldet war, kann ein Mangel vorliegen.

---

# 23. Vertragsstrafe

Vertragsstrafen müssen vertraglich vereinbart sein.

Beispiele:

- verspäteter Go-Live
- Verletzung definierter Verpflichtungen

### Korrektur

> Vertragsstrafe ist nicht pauschal „verschuldensunabhängig“. Das gesetzliche Grundmodell des § 339 BGB knüpft bei Leistungsstörungen an Verzug an; konkrete Klauseln sind zu prüfen.

---

# 24. Claim-Fristen

Verträge können vorsehen:

- unverzügliche Anzeige
- formale Claim Notice
- Nachweisfristen
- Eskalationsfristen

Versäumte Fristen können die Durchsetzbarkeit erschweren oder – je nach wirksamer Vertragsregelung – ausschließen.

---

# 25. Claim Notice

Eine frühe Claim Notice sollte sachlich sein.

Inhalt:

- Vertragsreferenz
- Ereignis
- Datum
- betroffene Leistung
- vermutete Auswirkung
- Vorbehalt weiterer Bewertung
- gewünschte Reaktion

---

# 26. Claim-Ausarbeitung

Eine vollständige Ausarbeitung enthält:

1. Sachverhalt
2. Vertrags-Soll
3. Ist-Zustand
4. Abweichung
5. Anspruchsgrundlage
6. Verantwortlichkeit
7. Kausalität
8. Kosten
9. Terminwirkung
10. Belege
11. Forderung

---

# 27. Dokumentation

Besonders wichtig:

- Verträge
- Nachträge
- Protokolle
- Freigaben
- Tickets
- E-Mails
- Zeitnachweise
- Testberichte
- Logs
- Fotos/Screenshots
- Rechnungen
- Liefernachweise

---

# 28. Claim Register

Beispielspalten:

| Feld | Inhalt |
|---|---|
| ID | CLM-001 |
| Datum | Erkennung |
| Typ | Eigen/Fremd |
| Thema | Zeit/Kosten/Leistung |
| Vertrag | Klausel |
| Betrag | Schätzung |
| Terminfolge | Tage |
| Status | offen/in Prüfung/verhandelt |
| Owner | Verantwortlicher |

---

# 29. Claim-Bewertung

Mögliche Dimensionen:

- rechtliche Stärke
- Beweisbarkeit
- finanzielle Bedeutung
- Terminwirkung
- Beziehung zum Kunden
- Reputationsrisiko
- Prozesskosten
- Erfolgswahrscheinlichkeit

---

# 30. Aufwand-Nutzen-Betrachtung

Nicht jeder theoretische Claim sollte eskaliert werden.

Beispiel:

```text
Claimwert 2.000 €
Anwalts-/Projektaufwand 8.000 €
Beziehungsrisiko hoch
```

→ wirtschaftliche Beilegung kann sinnvoller sein.

---

# 31. Fremdclaim-Abwehr

Prüfen:

- Anspruchsgrundlage vorhanden?
- Vertrags-Soll richtig dargestellt?
- Verantwortlichkeit?
- Fristen eingehalten?
- Kausalität?
- Schaden belegt?
- Mitverschulden?
- Gegenclaims?

---

# 32. Eigenclaim-Durchsetzung

Erfolgsfaktoren:

- früh anzeigen
- Anspruch sauber belegen
- Kosten nachvollziehbar
- Termine nachvollziehbar
- konsistente Kommunikation
- keine widersprüchlichen Protokolle

---

# 33. Kommunikationsregeln

Claim-Kommunikation sollte:

- sachlich
- eindeutig
- nachvollziehbar
- termingerecht
- autorisiert

sein.

Emotionale Schuldzuweisungen erschweren Verhandlungen.

---

# 34. Eskalationsstufen

```text
Projektteam
   ↓
Projektleitung
   ↓
Commercial/Contract Management
   ↓
Management
   ↓
Mediation / Schlichtung
   ↓
Schiedsverfahren / Gericht
```

Die konkrete Eskalationskette wird vertraglich bzw. organisatorisch festgelegt.

---

# 35. Verhandlung

Ziele:

- Interessen verstehen
- Fakten trennen
- Forderungen priorisieren
- Vergleichsoptionen bilden
- Gesamtrisiko reduzieren

Mögliche Ergebnisse:

- Zahlung
- Teilzahlung
- Terminverlängerung
- Leistungsänderung
- Gutschrift
- gegenseitiger Verzicht

---

# 36. Claim und Informationssicherheit

Typische Security-Claims:

- verspätete Patchbereitstellung
- nicht erfüllte Verschlüsselungsanforderung
- fehlende MFA
- falscher Datenstandort
- nicht bestandener Penetrationstest
- unzureichende Logging-Funktion
- Security-Anforderung nachträglich eingeführt

Abgrenzung:

> War die Sicherheitsanforderung bereits vereinbart → mögliche Nichterfüllung/Mangel.

> War sie nicht vereinbart → möglicher Change.

---

# 37. Claim und Compliance Change

Neue Gesetze oder regulatorische Anforderungen können Projektänderungen auslösen.

Vorab im Vertrag klären:

- Wer trägt regulatorische Änderungsrisiken?
- Wer beobachtet Rechtsänderungen?
- Gibt es Change-in-Law-Klauseln?
- Wie werden Mehrkosten verteilt?

---

# 38. Claim und agile Projekte

Agile Entwicklung beseitigt Claim-Risiken nicht.

Zu klären:

- Product Backlog
- Definition of Done
- Sprint-Abnahme
- Budget
- Priorisierung
- Änderungsbefugnisse
- Scope

### Prüfungsfalle

> „Agil“ bedeutet nicht „vertraglich unbegrenzt änderbar“.

---

# 39. Claim und Festpreis

Ein Festpreis reduziert nicht jede Nachforderung.

Wenn Scope geändert wird, kann zusätzliche Vergütung entstehen.

Entscheidend:

- ursprünglicher Leistungsumfang
- Change-Prozess
- vertragliche Risikozuweisung

---

# 40. Claim und Time & Material

Bei Time & Material liegt mehr Kostenrisiko beim Auftraggeber.

Daher wichtig:

- Budgetgrenzen
- Freigabestufen
- Zeiterfassung
- Reporting
- Forecasts

---

# 41. Claim und SLA

SLA-Verstöße können auslösen:

- Service Credits
- Vertragsstrafe, falls wirksam vereinbart
- Schadensersatz
- Eskalation
- Sonderkündigung

Der Vertrag muss die Rechtsfolge bestimmen.

---

# 42. Projektcontrolling

Früherkennung durch:

- Meilensteintrend
- Earned Value
- Budgetabweichung
- Risikoregister
- Change Register
- Claim Register
- Issue Log

---

# 43. Rollen

Mögliche Beteiligte:

- Projektleitung
- Contract Manager
- Claim Manager
- Einkauf
- Legal
- Controlling
- Fachbereich
- Security/Compliance
- Management

---

# 44. Lessons Learned

Nach Projektende:

- Welche Claims entstanden?
- Warum?
- Welche Klauseln waren unklar?
- Welche Dokumente fehlten?
- Welche Change-Prozesse versagten?
- Welche Standards sollen künftig gelten?

---

# 45. Typische IHK-Prüfungsfrage

## „Erläutern Sie den Claim-Management-Prozess.“

> Zunächst wird eine Soll-Ist-Abweichung erkannt und dokumentiert. Danach wird geprüft, ob eine vertragliche oder gesetzliche Anspruchsgrundlage besteht. Anschließend werden Auswirkungen auf Kosten und Termine bewertet, Belege zusammengestellt und der Claim formal angemeldet. Danach folgen Verhandlung, gegebenenfalls Eskalation und abschließende Dokumentation.

---

# 46. Typische IHK-Prüfungsfrage

## „Nennen Sie Maßnahmen zur Claim-Prävention.“

- klare Leistungsbeschreibung
- messbare Abnahmekriterien
- geregelter Change-Prozess
- definierte Mitwirkungspflichten
- Fristen
- vollständige Dokumentation
- Claim-/Eskalationsprozess

---

# 47. Typische Prüfungsfallen

- Soll-Ist-Abweichung = nicht automatisch Anspruch
- Change Request = nicht automatisch Claim
- Mangel = nicht automatisch kostenpflichtiger Change
- Abnahme = nicht nur „körperliche Übergabe“
- „Wandelung“ = veralteter Begriff
- Vertragsstrafe = nicht immer verschuldensunabhängig
- mündliche Änderungen ohne Dokumentation = hohes Risiko
- verspätete Claim Notice = kann Durchsetzung gefährden
- Claim-Management beginnt nicht erst beim Streit

---

# ⚡ 60-Sekunden-Schnellcheck

- Claim = Forderung aus Abweichung
- Eigenclaim = eigene Forderung
- Fremdclaim = gegnerische Forderung
- Vertrags-Soll vs. Ausführungs-Ist
- Change ≠ Claim
- Mangel ≠ Change
- Claim Notice = frühzeitige Anzeige
- Claim Register = zentrale Steuerung
- § 280 = Schadensersatz
- § 286 = Verzug
- § 633/634 = Werkmangel/Mängelrechte
- § 640 = Abnahme
- § 641 = Fälligkeit
- § 642 = Mitwirkung
- §§ 339 ff. = Vertragsstrafe
- Dokumentation = Beweisgrundlage
- Eskalation = stufenweise
- Lessons Learned = Prävention

---

# Quellen

- Bürgerliches Gesetzbuch (BGB), aktuelle Fassung
- Projektverträge und jeweilige Vertragsbedingungen
- Rechtsprechung und vertragsspezifische Regelwerke
