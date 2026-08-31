# Lernblatt / Handout: TDDDG, Cookies & Online-Datenschutz

### Kompaktes Nachschlagewerk für die IHK-Prüfung „Geprüfter Berufsspezialist für Informationssicherheit“

**Stand: 31. August 2026**

> **Hinweis:** Dieses Handout dient der Weiterbildung und Prüfungsvorbereitung und ersetzt keine Rechtsberatung im Einzelfall.

---

## ⚡ Schnellcheck

- TDDDG = Telekommunikation-Digitale-Dienste-Datenschutz-Gesetz.
- Wichtig für Websites/Apps: **§ 25 TDDDG**.
- Speichern/Auslesen von Informationen auf Endeinrichtungen grundsätzlich nur mit Einwilligung, sofern keine gesetzliche Ausnahme greift.
- DSGVO und TDDDG sind getrennt zu prüfen.
- Cookie ≠ automatisch personenbezogen; § 25 kann trotzdem greifen.
- technisch notwendig ≠ „alles, was Betreiber gern hätte“.

## 1. Zwei-Ebenen-Prüfung

```text
Zugriff auf Endgerät?
   ↓
§ 25 TDDDG
   ↓
anschließende personenbezogene Verarbeitung?
   ↓
DSGVO
```

## 2. § 25

Grundsatz:

Einwilligung für Speichern oder Zugriff auf Informationen im Endgerät.

Ausnahmen insbesondere, wenn:

- alleiniger Zweck Übertragung einer Nachricht oder
- unbedingt erforderlich zur Bereitstellung eines ausdrücklich gewünschten digitalen Dienstes

## 3. Beispiele

### typischerweise eher notwendig

- Session Cookie für Warenkorb
- Login-Session
- Sicherheitscookie

### typischerweise einwilligungsbedürftig

- Cross-Site Tracking
- Marketing Pixel
- Profiling
- viele Werbe-/Analytics-Technologien

Konkrete Bewertung bleibt einzelfallabhängig.

## 4. Consent Management Platform

CMP sollte:

- Wahl ermöglichen
- Ablehnen gleichwertig ermöglichen
- Zwecke klar darstellen
- Widerruf ermöglichen
- Einwilligung nachweisen

## 5. Dark Patterns

Einwilligung darf nicht durch manipulative Gestaltung erzwungen werden.

## 6. Server-Side Tracking

Verlagert Tracking technisch, beseitigt aber nicht automatisch Datenschutzpflichten.

## 7. Fingerprinting

Auch Zugriff auf/Verarbeitung von Endeinrichtungsinformationen kann § 25-relevant sein.

## 8. Newsletter/Tracking

Zusätzlich UWG beachten.

## Prüfungsfallen

- nur Cookies betroffen → falsch
- berechtigtes Interesse ersetzt §-25-Einwilligung → nicht automatisch
- Cookiebanner = automatisch wirksame Einwilligung → falsch
- „Ablehnen“ verstecken → riskant

## Quellen

- TDDDG
- DSGVO
- DSK Orientierungshilfe Digitale Dienste
