# Lernblatt / Handout: Löschkonzept & Aufbewahrung personenbezogener Daten

### Kompaktes Nachschlagewerk für die IHK-Prüfung „Geprüfter Berufsspezialist für Informationssicherheit“

**Stand: 31. August 2026**

> **Hinweis:** Dieses Handout dient der Weiterbildung und Prüfungsvorbereitung und ersetzt keine Rechtsberatung im Einzelfall.

---

## ⚡ Schnellcheck

- Art. 5 Abs. 1 lit. e DSGVO → Speicherbegrenzung.
- Art. 17 DSGVO → Recht auf Löschung.
- Aufbewahrungspflichten können Löschung zeitweise verhindern.
- „Backup vorhanden“ darf nicht zu unbegrenzter Speicherung führen.
- Löschkonzept muss Fachrecht, Technik und Backups einbeziehen.

## 1. Ziel

Personenbezogene Daten nur so lange speichern, wie:

- Zweck besteht oder
- gesetzliche Aufbewahrungspflicht greift.

## 2. Löschklassen

Beispiel:

| Klasse | Regel |
|---|---|
| L1 | sofort nach Zweckerfüllung |
| L2 | 30/90 Tage |
| L3 | nach Vertragsende |
| L4 | gesetzliche Aufbewahrungsfrist |
| L5 | Rechtsstreit/Legal Hold |

## 3. Quellen von Fristen

- DSGVO
- HGB
- AO
- Arbeitsrecht
- Fachgesetze
- Verträge
- Verjährungsrecht

## 4. Prozess

```text
Datenkategorie
 ↓
Zweck
 ↓
Frist
 ↓
Trigger
 ↓
Sperrung/Archiv?
 ↓
Löschung
 ↓
Nachweis
```

## 5. Backups

Praktische Lösung:

- regulärer Rotationszyklus
- kein erneutes produktives Nutzen gelöschter Daten
- bei Restore Löschstatus wieder anwenden
- Backup-Retention dokumentieren

## 6. Legal Hold

Bei Rechtsstreit/Ermittlung kann Löschung ausgesetzt werden, wenn eine Rechtsgrundlage besteht.

Dokumentieren:

- Anlass
- Umfang
- Beginn
- Ende
- Verantwortlicher

## 7. Sichere Löschung

Je Medium:

- logische Löschung
- Secure Erase
- Crypto Erase
- physische Vernichtung

## 8. Löschung in Cloud/SaaS

Vertraglich klären:

- aktive Daten
- Replikate
- Backups
- Fristen
- Löschbestätigung
- Exit

## Prüfungsfallen

- „Speicher ist billig, also behalten“ → unzulässige Logik
- Pseudonymisierung = Löschung → falsch
- Archivierung = Löschung → falsch
- Backup darf ewig bleiben → falsch

## Quellen

- DSGVO Art. 5, 17
- HGB/AO und einschlägige Spezialgesetze
