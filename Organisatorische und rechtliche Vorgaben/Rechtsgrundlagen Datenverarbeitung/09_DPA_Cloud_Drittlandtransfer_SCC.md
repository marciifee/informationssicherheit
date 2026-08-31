# Lernblatt / Handout: DPA, Cloud-Datenschutz & Drittlandtransfers

### Kompaktes Nachschlagewerk für die IHK-Prüfung „Geprüfter Berufsspezialist für Informationssicherheit“

**Stand: 31. August 2026**

> **Hinweis:** Dieses Handout dient der Weiterbildung und Prüfungsvorbereitung und ersetzt keine Rechtsberatung im Einzelfall.

---

## ⚡ Schnellcheck

- **DPA** = Data Processing Addendum/Agreement.
- Kann den AVV nach Art. 28 DSGVO abbilden.
- Drittlandtransfer zusätzlich nach **Art. 44 ff. DSGVO** prüfen.
- Angemessenheitsbeschluss → Art. 45.
- SCC → Art. 46.
- BCR → Art. 47.
- Art. 49 → Ausnahmen, nicht Standardlösung für dauerhafte Massentransfers.
- SCC 2021/914 besitzen vier Module.
- Transfer Impact Assessment (TIA) kann bei SCC erforderlich sein.
- EU-US Data Privacy Framework ist weiterhin ein Angemessenheitsmechanismus für **zertifizierte US-Unternehmen**.
- DPA ≠ automatische vollständige DSGVO-Compliance.

## 1. DPA

Ein DPA ist typischerweise ein Vertragsanhang zu:

- Cloudvertrag
- SaaS-Vertrag
- Managed Service
- Hosting

Er behandelt Datenverarbeitung und Datenschutzrollen.

## 2. Art.-28-Inhalte

Ein DPA sollte die AVV-Pflichten abbilden:

- Weisung
- Vertraulichkeit
- TOM
- Subprozessoren
- Betroffenenrechte
- Data Breach
- Löschung/Rückgabe
- Audit

## 3. Beispiel AWS

Das hochgeladene AWS-DPA ordnet AWS bei Customer Data als Processor ein, enthält dokumentierte Weisungen, Vertraulichkeit, TOM, Subprozessoren und Unterstützung bei Betroffenenrechten.

AWS-Servicebedingungen beziehen aktuell den DPA und – bei einschlägigen Drittlandtransfers – die SCC ein.

## 4. Drittland

Drittland = Staat außerhalb EU/EWR im Sinne des DSGVO-Transferregimes.

Eine normale Art.-6-Rechtsgrundlage reicht **nicht**.

Zusätzliche „zweite Stufe“:

```text
Verarbeitung zulässig?
      ↓
Drittlandtransfer?
      ↓
Kapitel V Mechanismus
```

## 5. Art. 45 – Angemessenheit

Kommission kann angemessenes Datenschutzniveau feststellen.

Dann ist kein zusätzlicher Art.-46-Transfermechanismus erforderlich.

## 6. EU-US Data Privacy Framework

Datenübermittlung in die USA kann auf dem Angemessenheitsbeschluss beruhen, wenn der konkrete Empfänger am DPF teilnimmt und zertifiziert ist.

### Prüfungsfalle

> USA als Land sind nicht pauschal vollständig „angemessen“. Entscheidend ist beim DPF die Teilnahme des Empfängers.

## 7. SCC – Standardvertragsklauseln

Beschluss (EU) 2021/914.

Module:

1. Controller → Controller
2. Controller → Processor
3. Processor → Processor
4. Processor → Controller

## 8. TIA

Bei SCC muss geprüft werden, ob Recht/Praxis des Drittlandes die Wirksamkeit der Garantien beeinträchtigt.

Prüfen:

- Empfängerland
- Zugriffsmöglichkeiten Behörden
- Datenart
- technische Maßnahmen
- Verschlüsselung
- Schlüsselkontrolle

## 9. Ergänzende Maßnahmen

- starke Verschlüsselung
- Schlüsselhoheit im EWR
- Pseudonymisierung
- organisatorische Prozesse
- vertragliche Transparenz

## 10. Subprozessoren

DPA muss Kette abbilden:

```text
Kunde
 ↓
Processor
 ↓
Subprocessor
 ↓
weiterer Subprocessor
```

Pflichten müssen vertraglich weitergegeben werden.

## 11. Region ≠ rechtlicher Speicherort allein

Cloudregion hilft, beantwortet aber nicht alle Fragen:

- Supportzugriff
- Subprozessoren
- Metadaten
- Telemetrie
- Rechtszugriffe
- Backups

## 12. Shared Responsibility

DPA entbindet Kunden nicht von:

- IAM
- Konfiguration
- Klassifizierung
- Verschlüsselungsentscheidungen
- Löschung
- Rechtsgrundlage

## 13. Exit

DPA/Cloudvertrag sollte regeln:

- Export
- Rückgabe
- Löschung
- Löschbestätigung
- Fristen
- Backup-Retention

## Prüfungsfallen

- DPA = SCC → falsch, kann SCC enthalten
- SCC = Angemessenheitsbeschluss → falsch
- EU-US DPF = jeder US-Anbieter → falsch
- EU-Region = garantiert kein Drittlandzugriff → zu pauschal
- Art. 49 = Standardlösung → falsch

## Quellen

- DSGVO Art. 28, 44–49
- Durchführungsbeschluss (EU) 2021/914
- Europäische Kommission – Angemessenheitsbeschlüsse
- EDPB Guidelines
- AWS DPA / AWS Service Terms als Praxisbeispiel
