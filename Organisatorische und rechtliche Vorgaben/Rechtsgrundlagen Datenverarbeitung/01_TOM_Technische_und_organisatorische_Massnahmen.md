# Lernblatt / Handout: Technische und organisatorische Maßnahmen (TOM)

### Kompaktes Nachschlagewerk für die IHK-Prüfung „Geprüfter Berufsspezialist für Informationssicherheit“

**Stand: 31. August 2026**

> **Hinweis:** Dieses Handout dient der Weiterbildung und Prüfungsvorbereitung und ersetzt keine Rechtsberatung im Einzelfall.

---

## ⚡ Schnellcheck vor der Prüfung

- Rechtsgrundlage: vor allem **Art. 32 DSGVO**, ergänzt durch **Art. 25 DSGVO**.
- TOM müssen **risikoadäquat**, **angemessen** und am **Stand der Technik** ausgerichtet sein.
- Art. 32 nennt keine starre Checkliste.
- Kernthemen: **Pseudonymisierung/Verschlüsselung**, **Vertraulichkeit**, **Integrität**, **Verfügbarkeit**, **Belastbarkeit**, **Wiederherstellbarkeit** und **regelmäßige Wirksamkeitsprüfung**.
- Verantwortlicher **und** Auftragsverarbeiter müssen geeignete TOM treffen.
- TOM müssen dokumentiert, überprüft und angepasst werden.
- Ein ISO-27001-Zertifikat ersetzt keine eigene Risikobewertung.
- Die alten „8 Kontrollen“ aus der Anlage zu § 9 BDSG a. F. sind historisch nützlich, aber nicht mehr die aktuelle gesetzliche Systematik.

## 1. Definition

TOM sind technische und organisatorische Schutzmaßnahmen, mit denen personenbezogene Daten und die Rechte betroffener Personen geschützt werden.

```text
Risiko
  ↓
Schutzbedarf / Verarbeitungskontext
  ↓
geeignete TOM
  ↓
Umsetzung
  ↓
Wirksamkeitsprüfung
  ↓
Anpassung
```

## 2. Rechtsgrundlagen

### Art. 32 DSGVO – Sicherheit der Verarbeitung

Bei der Auswahl sind zu berücksichtigen:

- Stand der Technik
- Implementierungskosten
- Art, Umfang, Umstände und Zwecke der Verarbeitung
- Eintrittswahrscheinlichkeit
- Schwere der Risiken für Rechte und Freiheiten natürlicher Personen

### Art. 25 DSGVO – Datenschutz durch Technikgestaltung und Voreinstellungen

Datenschutz muss bereits bei Konzeption und Auswahl von Systemen berücksichtigt werden.

### Art. 5 Abs. 1 lit. f DSGVO

Personenbezogene Daten müssen durch geeignete Maßnahmen vor:

- unbefugter Verarbeitung
- unrechtmäßiger Verarbeitung
- unbeabsichtigtem Verlust
- Zerstörung
- Schädigung

geschützt werden.

## 3. TOM nach Art. 32

Art. 32 nennt insbesondere:

1. Pseudonymisierung und Verschlüsselung
2. dauerhafte Sicherstellung von Vertraulichkeit, Integrität, Verfügbarkeit und Belastbarkeit
3. rasche Wiederherstellung der Verfügbarkeit und des Zugangs nach Zwischenfällen
4. Verfahren zur regelmäßigen Überprüfung, Bewertung und Evaluierung der Wirksamkeit

## 4. Technische Maßnahmen

Beispiele:

- Verschlüsselung at rest / in transit
- MFA
- Firewalls
- Netzwerksegmentierung
- EDR
- Patchmanagement
- Backup
- Immutable Backup
- Logging
- SIEM
- sichere Konfiguration
- Härtung
- DLP
- Pseudonymisierung

## 5. Organisatorische Maßnahmen

Beispiele:

- Rollen- und Berechtigungskonzept
- Datenschutzrichtlinien
- Schulungen
- Vier-Augen-Prinzip
- Change Management
- Incident Response
- Berechtigungsrezertifizierung
- Lieferantenmanagement
- Löschkonzept
- Notfallübungen

## 6. Historische Kontrollgruppen

Die frühere Anlage zu § 9 BDSG a. F. verwendete u. a.:

- Zutrittskontrolle
- Zugangskontrolle
- Zugriffskontrolle
- Weitergabekontrolle
- Eingabekontrolle
- Auftragskontrolle
- Verfügbarkeitskontrolle
- Trennungsgebot

Diese Begriffe werden in der Praxis weiter verwendet, sind aber **keine aktuelle abschließende DSGVO-Liste**.

## 7. TOM und Schutzbedarf

Beispiel:

```text
Newsletter-E-Mail
→ geringeres Risiko
→ Standard-TOM

Gesundheitsdaten
→ höheres Risiko
→ stärkere Zugriffskontrolle, Verschlüsselung,
   Monitoring und ggf. DSFA
```

## 8. TOM und Auftragsverarbeitung

Im AVV nach Art. 28 DSGVO müssen TOM des Auftragsverarbeiters angemessen beschrieben bzw. vertraglich einbezogen werden.

Der Verantwortliche muss prüfen, ob der Dienstleister hinreichende Garantien bietet.

## 9. TOM-Lifecycle

```text
Planen
 ↓
Implementieren
 ↓
Betreiben
 ↓
Überwachen
 ↓
Testen
 ↓
Verbessern
```

## 10. Nachweise

Geeignete Nachweise:

- TOM-Dokument
- Netzplan
- Berechtigungsmatrix
- Patchreport
- Backupreport
- Restore-Test
- Auditbericht
- Zertifikat
- Penetrationstest
- Schulungsnachweis

## 11. Typische Prüfungsfrage

### „Nennen Sie drei TOM und erläutern Sie deren Zweck.“

**MFA:** verhindert, dass ein gestohlenes Passwort allein zum Systemzugang reicht.

**Verschlüsselung:** reduziert die Folgen bei Verlust oder unbefugtem Zugriff.

**Backup und Restore-Test:** ermöglicht die Wiederherstellung von Daten nach technischen oder sicherheitsrelevanten Zwischenfällen.

## 12. Prüfungsfallen

- TOM = nicht nur Technik
- Verschlüsselung = nicht automatisch ausreichend
- ISO-Zertifikat = nicht automatisch DSGVO-konform
- Backup ohne Restore-Test = keine nachgewiesene Wiederherstellbarkeit
- alte 8 BDSG-Kontrollen = nicht aktuelle gesetzliche Vollständigkeitsliste
- „Stand der Technik“ = dynamisch

## ⚡ 60-Sekunden-Schnellcheck

- Art. 32 = Sicherheit
- Art. 25 = Privacy by Design/Default
- Risiko → Maßnahme
- CIA + Belastbarkeit
- Pseudonymisierung
- Verschlüsselung
- Backup/Restore
- regelmäßige Tests
- Dokumentation
- kontinuierliche Anpassung

## Quellen

- DSGVO, insbesondere Art. 5, 25, 28, 32 und 35
- DSK/BfDI Orientierungshilfen
- BSI IT-Grundschutz als mögliche Konkretisierung technischer Maßnahmen
