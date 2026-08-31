# Lernblatt / Handout: ITIL 4 – IT Service Management

### Kompaktes Nachschlagewerk für die IHK-Prüfung „Geprüfter Berufsspezialist für Informationssicherheit“

**Stand: 31. August 2026**  
**Schwerpunkt:** ITIL 4 Foundation, Service Value System, Four Dimensions, Service Value Chain, Guiding Principles und zentrale Practices

> **Hinweis:** ITIL ist ein kommerziell veröffentlichtes Best-Practice-Framework. Dieses Handout fasst die prüfungsrelevanten Konzepte in eigenen Worten zusammen.

---

# ⚡ Schnellcheck vor der Prüfung

- **ITIL** = Best-Practice-Framework für IT Service Management.
- **ITSM** = Management von IT-Services zur gemeinsamen Wertschöpfung.
- **Service** = ermöglicht Wertschöpfung, ohne dass der Kunde alle spezifischen Kosten und Risiken selbst managen muss.
- **Value** = wahrgenommener Nutzen, Bedeutung und Vorteil.
- **Utility** = „fit for purpose“ – was der Service leistet.
- **Warranty** = „fit for use“ – wie zuverlässig er nutzbar ist.
- ITIL 4 denkt in **Wertströmen**, nicht nur in starren Prozessen.
- **SVS** = Service Value System.
- SVS enthält: Guiding Principles, Governance, Service Value Chain, Practices, Continual Improvement.
- **4 Dimensions** = Organizations & People; Information & Technology; Partners & Suppliers; Value Streams & Processes.
- **7 Guiding Principles**.
- **6 Service Value Chain Activities**.
- **34 Management Practices**.
- Kategorien: **14 General Management**, **17 Service Management**, **3 Technical Management Practices**.
- Incident Management → Service schnell wiederherstellen.
- Problem Management → Ursachen und Wiederholungen behandeln.
- Service Request Management → standardisierte Nutzeranfragen.
- Change Enablement → erfolgreiche Changes maximieren und Risiken kontrollieren.
- Service Level Management → geschäftsbasierte Serviceziele vereinbaren und überwachen.
- Service Desk → zentraler Kommunikationspunkt.
- Continual Improvement → Verbesserungen auf allen Ebenen.
- **ISO/IEC 20000-1** = zertifizierbare Service-Management-Systemnorm; ITIL = Best Practice, keine Organisationszertifizierung nach „ITIL“.

---

# 1. Was ist ITIL?

ITIL wurde ursprünglich im Umfeld der britischen öffentlichen Verwaltung entwickelt und hat sich zu einem international verbreiteten Framework für Service Management entwickelt.

ITIL beschreibt:

- Konzepte
- Prinzipien
- Practices
- Wertströme
- Governance
- kontinuierliche Verbesserung

Es ist kein Gesetz und keine technische Produktnorm.

---

# 2. Was ist IT Service Management?

ITSM beschreibt die organisatorischen Fähigkeiten zur Bereitstellung und Steuerung von IT-Services.

Ziel:

> IT-Leistungen so gestalten und betreiben, dass sie gemeinsam mit Kunden und anderen Stakeholdern Wert schaffen.

---

# 3. Produkt und Service

## Produkt

Konfiguration von Ressourcen einer Organisation, die Wertangebote ermöglicht.

## Service

Mittel zur gemeinsamen Wertschöpfung, indem gewünschte Ergebnisse unterstützt werden, ohne dass der Kunde alle spezifischen Kosten und Risiken selbst steuern muss.

---

# 4. Value – Wert

Wert ist keine rein technische Größe.

Er entsteht aus Sicht der Stakeholder.

Beispiel:

```text
Technisch:
Server läuft.

Geschäftlich:
Kunden können Bestellungen bearbeiten.

→ erst der Geschäftsnutzen erzeugt Wert.
```

---

# 5. Utility und Warranty

## Utility – Fit for Purpose

> Was kann der Service?

Beispiel:

- Datei speichern
- Bestellung verarbeiten
- Videokonferenz ermöglichen

## Warranty – Fit for Use

> Wie zuverlässig kann er genutzt werden?

Beispiele:

- Verfügbarkeit
- Kapazität
- Kontinuität
- Sicherheit

### Merksatz

> **Utility = Funktion/Nutzen. Warranty = Nutzbarkeit/Zusicherung.**

---

# 6. Output und Outcome

## Output

direktes Ergebnis einer Aktivität.

Beispiel:

> neuer E-Mail-Server installiert.

## Outcome

Ergebnis für einen Stakeholder.

Beispiel:

> Mitarbeitende können zuverlässig kommunizieren.

ITIL fokussiert stärker auf Outcomes und Value als nur auf technische Outputs.

---

# 7. Kosten und Risiken

Servicebeziehungen verändern:

- Kosten
- Risiken

für Kunde und Provider.

Ein Service kann bestimmte Kosten/Risiken vom Kunden übernehmen, andere bleiben beim Kunden.

---

# 8. Service Provider, Consumer und Stakeholder

## Service Provider

stellt Services bereit.

## Service Consumer

nutzt bzw. bezieht Services.

Rollen können sein:

- Customer
- User
- Sponsor

## Stakeholder

alle relevanten interessierten Parteien.

---

# 9. Service Relationship

Servicebeziehung umfasst:

- Service Provision
- Service Consumption
- Service Relationship Management

Wert entsteht durch Zusammenarbeit, nicht ausschließlich durch den Provider.

---

# 10. Co-Creation of Value

ITIL 4 betont:

> Wert wird gemeinsam geschaffen.

Beispiel:

```text
Provider liefert Cloudservice
+
Kunde konfiguriert Berechtigungen korrekt
+
Nutzer verwenden Service zweckmäßig
=
Wert
```

---

# 11. Service Value System – SVS

Das SVS zeigt, wie Komponenten und Aktivitäten einer Organisation zusammenwirken, um Wert zu ermöglichen.

```text
Opportunity / Demand
        ↓
┌──────────────────────────────┐
│ Service Value System         │
│                              │
│ Guiding Principles           │
│ Governance                   │
│ Service Value Chain          │
│ Practices                    │
│ Continual Improvement        │
└──────────────────────────────┘
        ↓
       Value
```

---

# 12. Bestandteile des SVS

1. Guiding Principles
2. Governance
3. Service Value Chain
4. Practices
5. Continual Improvement

---

# 13. Die 7 Guiding Principles

1. **Focus on value**
2. **Start where you are**
3. **Progress iteratively with feedback**
4. **Collaborate and promote visibility**
5. **Think and work holistically**
6. **Keep it simple and practical**
7. **Optimize and automate**

---

# 14. Focus on Value

Jede Aktivität sollte direkt oder indirekt zur Wertschöpfung beitragen.

Frage:

> Welchen Nutzen hat diese Maßnahme für Kunden oder andere Stakeholder?

---

# 15. Start Where You Are

Nicht alles neu bauen.

Vorhandenes prüfen:

- Prozesse
- Systeme
- Daten
- Fähigkeiten

Was funktioniert, soll sinnvoll weiterverwendet werden.

---

# 16. Progress Iteratively with Feedback

Große Vorhaben in beherrschbare Schritte teilen.

```text
kleiner Schritt
 ↓
Feedback
 ↓
Anpassung
 ↓
nächster Schritt
```

Vorteile:

- früher Nutzen
- geringeres Risiko
- schnelleres Lernen

---

# 17. Collaborate and Promote Visibility

Relevante Stakeholder einbeziehen.

Transparenz schaffen durch:

- Dashboards
- Backlogs
- Reports
- Reviews
- gemeinsame Ziele

---

# 18. Think and Work Holistically

Services bestehen aus miteinander verbundenen Komponenten.

Nicht isoliert optimieren.

Beispiel:

> schnellere Softwareentwicklung bringt wenig, wenn Deployment, Security oder Support nicht mithalten.

---

# 19. Keep It Simple and Practical

Nur so komplex wie nötig.

Unnötige:

- Freigaben
- Prozessschritte
- Dokumente

reduzieren.

---

# 20. Optimize and Automate

Zuerst verstehen und optimieren, dann sinnvoll automatisieren.

### Prüfungsfalle

> **Einen schlechten Prozess zu automatisieren macht ihn nicht automatisch gut.**

---

# 21. Governance

Governance umfasst auf oberster Ebene:

- Evaluate
- Direct
- Monitor

Die Leitung bewertet Anforderungen, gibt Richtung vor und überwacht Ergebnisse.

---

# 22. Four Dimensions Model

Jeder Service und jede Practice soll ganzheitlich betrachtet werden.

```text
Organizations & People
          │
Information & Technology
          │
Partners & Suppliers
          │
Value Streams & Processes
```

---

# 23. Organizations and People

Themen:

- Rollen
- Kompetenzen
- Kultur
- Kommunikation
- Verantwortlichkeiten
- Führung

---

# 24. Information and Technology

Themen:

- Informationen
- Anwendungen
- Infrastruktur
- Architektur
- Automatisierung
- Security
- Cloud

---

# 25. Partners and Suppliers

Themen:

- Lieferanten
- Outsourcing
- Verträge
- Cloudprovider
- Abhängigkeiten
- Sourcing-Strategie

---

# 26. Value Streams and Processes

## Value Stream

Abfolge von Schritten, mit denen Wert geschaffen wird.

## Process

zusammenhängende Aktivitäten, die Inputs in Outputs transformieren.

ITIL 4 betrachtet Prozesse als Bestandteil einer größeren Wertschöpfung.

---

# 27. Externe Faktoren – PESTLE

Bei den vier Dimensionen können externe Faktoren berücksichtigt werden:

- Political
- Economic
- Social
- Technological
- Legal
- Environmental

---

# 28. Service Value Chain – SVC

Die Service Value Chain ist das zentrale operative Modell innerhalb des SVS.

Sie besitzt sechs Aktivitäten:

1. Plan
2. Improve
3. Engage
4. Design & Transition
5. Obtain/Build
6. Deliver & Support

---

# 29. Plan

Zweck:

gemeinsames Verständnis von:

- Vision
- aktuellem Status
- Richtung
- Verbesserungsprioritäten

---

# 30. Improve

Sichert kontinuierliche Verbesserung von:

- Services
- Produkten
- Practices
- Wertströmen

---

# 31. Engage

Pflegt Beziehungen zu:

- Kunden
- Nutzern
- Lieferanten
- Partnern

Ziel:

- Anforderungen verstehen
- Transparenz
- kontinuierliche Kommunikation

---

# 32. Design & Transition

Sicherstellen, dass neue/geänderte Produkte und Services:

- Anforderungen erfüllen
- Qualität erreichen
- Kosten und Zeit berücksichtigen

---

# 33. Obtain/Build

Servicekomponenten:

- beschaffen
- entwickeln
- bereitstellen

Beispiele:

- Software
- Hardware
- externe Services

---

# 34. Deliver & Support

Services:

- bereitstellen
- betreiben
- unterstützen

gemäß vereinbarter Erwartungen.

---

# 35. Value Streams

Die sechs Aktivitäten sind **kein starrer lineare Prozess**.

Ein Wertstrom kombiniert benötigte Aktivitäten je nach Situation.

Beispiel Incident:

```text
Engage
  ↓
Deliver & Support
  ↓
Obtain/Build (falls Fix)
  ↓
Improve
```

---

# 36. Continual Improvement Model

Prüfungsgeeignete Fragenfolge:

1. Was ist die Vision?
2. Wo stehen wir jetzt?
3. Wo wollen wir hin?
4. Wie kommen wir dorthin?
5. Maßnahmen durchführen
6. Haben wir das Ziel erreicht?
7. Wie halten wir den Schwung aufrecht?

---

# 37. Management Practices

ITIL 4 gruppiert **34 Practices** in drei Kategorien:

- 14 General Management Practices
- 17 Service Management Practices
- 3 Technical Management Practices

---

# 38. 14 General Management Practices

- Architecture Management
- Continual Improvement
- Information Security Management
- Knowledge Management
- Measurement and Reporting
- Organizational Change Management
- Portfolio Management
- Project Management
- Relationship Management
- Risk Management
- Service Financial Management
- Strategy Management
- Supplier Management
- Workforce and Talent Management

---

# 39. 17 Service Management Practices

- Availability Management
- Business Analysis
- Capacity and Performance Management
- Change Enablement
- Incident Management
- IT Asset Management
- Monitoring and Event Management
- Problem Management
- Release Management
- Service Catalogue Management
- Service Configuration Management
- Service Continuity Management
- Service Design
- Service Desk
- Service Level Management
- Service Request Management
- Service Validation and Testing

---

# 40. 3 Technical Management Practices

- Deployment Management
- Infrastructure and Platform Management
- Software Development and Management

---

# 41. Information Security Management

Zweck:

Informationen so schützen, dass erforderliche:

- Vertraulichkeit
- Integrität
- Verfügbarkeit

sowie weitere Sicherheitsanforderungen erfüllt werden.

Verbindung zu:

- ISMS
- ISO 27001
- BSI IT-Grundschutz
- Risk Management

---

# 42. Incident Management

Ziel:

> normalen Servicebetrieb schnell wiederherstellen.

Fokus:

- schnelle Wiederherstellung
- Business Impact reduzieren

Nicht primär:

> Root Cause vollständig beseitigen.

---

# 43. Problem Management

Ziel:

- Ursachen von Incidents reduzieren
- Wiederholungen verhindern
- bekannte Fehler verwalten
- Workarounds bereitstellen

---

# 44. Incident vs. Problem

```text
Incident:
Service ausgefallen
→ schnell wiederherstellen

Problem:
Warum passiert es?
→ Ursache analysieren
```

---

# 45. Known Error

Ein Problem, das analysiert wurde und für das Ursache bzw. geeignete Informationen oder ein Workaround bekannt sind.

---

# 46. Workaround

Temporäre Lösung zur Verringerung der Auswirkung.

Beispiel:

> auf sekundären Server umschalten.

Workaround ≠ dauerhafter Fix.

---

# 47. Service Request Management

Service Request = vordefinierte, normale Nutzeranfrage.

Beispiele:

- Passwort zurücksetzen
- Software bestellen
- Berechtigung beantragen
- Information anfordern

---

# 48. Service Desk

Zweck:

Kommunikationsschnittstelle zwischen Provider und Nutzern.

Aufgaben:

- Kontakt
- Kommunikation
- Incident-Erfassung
- Requests
- Nutzerunterstützung

### Merksatz

> **Service Desk ist eine Practice/Funktion der Kommunikation – nicht nur ein Ticketsystem.**

---

# 49. Change Enablement

Ziel:

Anzahl erfolgreicher Changes maximieren durch:

- Risikobewertung
- Autorisierung
- Change-Kalender
- Steuerung

---

# 50. Change-Typen

## Standard Change

- vorab autorisiert
- risikoarm
- gut verstanden

## Normal Change

- reguläre Bewertung und Autorisierung

## Emergency Change

- dringlich
- beschleunigter Prozess
- dennoch kontrolliert

---

# 51. Organizational Change Management vs. Change Enablement

| Organizational Change Management | Change Enablement |
|---|---|
| Menschen und Organisation | Produkte/Services/IT |
| Akzeptanz | Risiko/Autorisation |
| Kultur/Verhalten | technische/Service-Änderung |

---

# 52. Release Management

Ziel:

neue/geänderte Services und Features zur Nutzung verfügbar machen.

Release ≠ Deployment.

---

# 53. Deployment Management

Bewegt neue/geänderte Komponenten in Umgebungen.

Beispiele:

- VM ausrollen
- Software installieren
- Container deployen

---

# 54. Release vs. Deployment

> **Deployment** = technische Bewegung/Installation.

> **Release** = Bereitstellung zur Nutzung bzw. Freigabe von Funktionalität.

Beide können zeitlich getrennt sein.

---

# 55. Service Configuration Management

Sorgt dafür, dass zuverlässige Informationen zu:

- Services
- Configuration Items (CIs)
- Beziehungen

verfügbar sind.

---

# 56. CI – Configuration Item

Komponente, die verwaltet werden muss, um einen Service bereitzustellen.

Beispiele:

- Server
- Anwendung
- Netzwerkgerät
- Dokument
- Cloudressource

---

# 57. CMDB

Configuration Management Database kann Informationen zu CIs und Beziehungen speichern.

### Prüfungsfalle

> ITIL schreibt nicht vor, dass jede Organisation zwingend genau eine klassische CMDB besitzen muss.

---

# 58. IT Asset Management

Steuert den Lebenszyklus von IT-Assets zur:

- Wertmaximierung
- Kostenkontrolle
- Risikosteuerung
- Entscheidungsunterstützung

Asset und CI können sich überschneiden, sind aber nicht identisch.

---

# 59. Monitoring and Event Management

## Event

Zustandsänderung, die für die Steuerung eines Service oder CI relevant ist.

Typen können organisatorisch sein:

- Information
- Warning
- Exception

Monitoring erkennt und beobachtet Zustände.

---

# 60. Availability Management

Ziel:

Services erfüllen vereinbarte Verfügbarkeitsanforderungen.

Bezug:

- SLA
- Architektur
- Redundanz
- Monitoring

---

# 61. Capacity and Performance Management

Stellt sicher:

- ausreichende Kapazität
- angemessene Performance
- wirtschaftlicher Ressourceneinsatz

---

# 62. Service Continuity Management

Unterstützt ausreichende Serviceverfügbarkeit und Leistungsfähigkeit nach größeren Störungen.

Verbindung:

- BCM
- BIA
- RTO/RPO
- Disaster Recovery

---

# 63. Service Level Management

Ziel:

geschäftsbasierte Serviceziele setzen und Servicequalität wirksam steuern.

Werkzeuge:

- SLA
- Reporting
- Review
- Kundenfeedback

---

# 64. Service Catalogue Management

Sorgt für konsistente Informationen über verfügbare Services und Serviceangebote.

---

# 65. Supplier Management

Ziel:

Lieferanten und deren Leistungen passend steuern.

Themen:

- Verträge
- Performance
- Risiken
- Beziehung
- Lieferanten-SLAs

---

# 66. Relationship Management

Baut Beziehungen zu Stakeholdern auf und pflegt sie.

Ziele:

- Bedürfnisse verstehen
- Vertrauen
- Prioritäten abstimmen

---

# 67. Risk Management

Unterstützt:

- Risiken identifizieren
- bewerten
- behandeln
- überwachen

ITIL-Risikomanagement ersetzt keine spezialisierten ISMS-/Compliance-Risikomethoden.

---

# 68. Knowledge Management

Stellt Wissen für Entscheidungen und Tätigkeiten passend bereit.

Beispiele:

- Knowledge Base
- Known Error Database
- Runbooks
- Lessons Learned

---

# 69. Measurement and Reporting

Zweck:

Entscheidungsfindung durch geeignete:

- Kennzahlen
- Messungen
- Berichte

unterstützen.

### Prüfungsfalle

> Nur zu messen, was technisch leicht messbar ist, kann falsche Steuerungsanreize erzeugen.

---

# 70. Continual Improvement

Verbesserung betrifft:

- Services
- Practices
- Prozesse
- Produkte
- Beziehungen

und ist keine einmalige Projektphase.

---

# 71. ITIL 4 vs. ITIL V3

| ITIL V3 | ITIL 4 |
|---|---|
| Service Lifecycle | Service Value System |
| stark prozessorientiert | wertstrom-/practice-orientiert |
| Strategy, Design, Transition, Operation, CSI | SVS + SVC + Practices |
| 26 Processes | 34 Practices |

ITIL-V2-/V3-Begriffe können historisch in alten Prüfungsunterlagen vorkommen.

---

# 72. ITIL und Agile/DevOps

ITIL 4 ist bewusst kompatibel mit modernen Arbeitsweisen.

Gemeinsame Prinzipien:

- Feedback
- Iteration
- Automatisierung
- Zusammenarbeit
- Value
- Continual Improvement

---

# 73. ITIL und Informationssicherheit

Security darf nicht isoliert betrachtet werden.

Beispiele:

- Incident Management ↔ Security Incident
- Change Enablement ↔ sichere Changes
- Supplier Management ↔ Lieferkettensicherheit
- Continuity ↔ BCM
- Configuration Management ↔ Asset-/Angriffsflächenkenntnis
- Information Security Management ↔ ISMS

---

# 74. ITIL und SLA

```text
Business Requirement
        ↓
Service Design
        ↓
Service Level Management
        ↓
SLA / SLO
        ↓
Monitoring
        ↓
Reporting
        ↓
Review
        ↓
Improvement
```

---

# 75. ITIL und ISO/IEC 20000

## ITIL

- Best-Practice-Framework
- flexibel
- beschreibt hilfreiche Konzepte und Practices
- Personenzertifizierungen existieren

## ISO/IEC 20000-1

- internationale Anforderungsnorm
- Service Management System (SMS)
- Organisationen können gegen die Norm zertifiziert werden

### Präzisierung

> ISO/IEC 20000 und ITIL sind **nicht „weitestgehend identisch“**. Sie verfolgen verwandte Ziele und sind kompatibel, aber Struktur, Zweck und normative Verbindlichkeit unterscheiden sich.

---

# 76. ISO/IEC 20000-1 aktueller Stand

**ISO/IEC 20000-1:2018** ist weiterhin aktuell und wurde 2023 bestätigt.

2024 kam:

**ISO/IEC 20000-1:2018/Amd 1:2024 – Climate action changes**

hinzu.

---

# 77. Typische IHK-Prüfungsfrage

## „Nennen Sie die Bestandteile des Service Value Systems.“

- Guiding Principles
- Governance
- Service Value Chain
- Practices
- Continual Improvement

---

# 78. Typische IHK-Prüfungsfrage

## „Nennen Sie die vier Dimensionen von ITIL 4.“

1. Organizations and People
2. Information and Technology
3. Partners and Suppliers
4. Value Streams and Processes

---

# 79. Typische IHK-Prüfungsfrage

## „Unterscheiden Sie Incident und Problem.“

> Ein Incident ist eine ungeplante Unterbrechung oder Qualitätsminderung eines Service. Incident Management versucht, den Service schnell wiederherzustellen. Ein Problem ist eine Ursache oder mögliche Ursache eines oder mehrerer Incidents; Problem Management reduziert die Wahrscheinlichkeit und Auswirkungen wiederkehrender Incidents.

---

# 80. Typische IHK-Prüfungsfrage

## „Unterscheiden Sie Release und Deployment.“

> Deployment beschreibt das technische Überführen von Komponenten in eine Zielumgebung. Release Management stellt neue oder geänderte Services beziehungsweise Funktionalität zur Nutzung bereit. Ein Deployment kann deshalb stattfinden, bevor eine Funktion tatsächlich für Nutzer freigeschaltet wird.

---

# 81. Typische IHK-Prüfungsfrage

## „Welche Funktion hat Service Level Management?“

> Service Level Management stellt sicher, dass geschäftlich relevante Serviceziele vereinbart, überwacht und regelmäßig überprüft werden. Ein wichtiges Instrument ist das SLA.

---

# 82. Typische Prüfungsfallen

- ITIL = Norm → falsch
- ITIL = Gesetz → falsch
- ITIL-Organisation wird „ITIL-zertifiziert“ → so nicht
- ISO 20000 = identisch mit ITIL → falsch
- SVS = nur Service Value Chain → falsch
- Service Value Chain = starrer Ablauf → falsch
- Incident = Ursache analysieren → primär Problem Management
- Problem = immer bereits Incident → falsch
- Service Request = Incident → falsch
- Change Enablement = Organizational Change Management → falsch
- Release = Deployment → falsch
- CI = nur Hardware → falsch
- CMDB = zwingend genau eine Datenbank → falsch
- Continual Improvement = erst am Projektende → falsch
- Automatisierung vor Optimierung → widerspricht Guiding Principle

---

# ⚡ 60-Sekunden-Schnellcheck

- ITIL = Best Practice
- ITSM = Services managen
- Value = Stakeholdernutzen
- Utility = fit for purpose
- Warranty = fit for use
- Output ≠ Outcome
- Co-Creation
- SVS = GP + Governance + SVC + Practices + Improvement
- 7 Guiding Principles
- 4 Dimensions
- 6 SVC Activities
- 34 Practices
- 14 / 17 / 3
- Incident → restore
- Problem → root cause
- Request → Standardanfrage
- Change Enablement → Changes steuern
- Release ≠ Deployment
- Service Desk = Kommunikationspunkt
- SLM → SLA
- Continuity → BCM
- ISO 20000 = zertifizierbares SMS

---

# Quellen

- Kursunterlage „Präsentation ITIL Zusammenfassung“
- Kursunterlage „ITIL V4 Services“
- Kursunterlagen SLA
- ISO/IEC 20000-1:2018
- ISO/IEC 20000-1:2018/Amd 1:2024
