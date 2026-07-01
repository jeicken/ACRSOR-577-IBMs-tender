# Quickstart: Validierung fuer Angebotskonzept iBMS 3.0

## Ziel
Diese Anleitung validiert Ende-zu-Ende, dass das Artefakt `Angebotskonzept.md` die fachlichen und formalen Mindestanforderungen fuer die Angebotsbearbeitung erfuellt.

## Voraussetzungen
- Lokales Repository mit Feature-Artefakten unter `specs/001-angebotskonzept-ibms/`
- Zugriff auf die PDF-Quellen unter `documents/`
- Vorhandene Referenzdokumente:
  - `spec.md`
  - `research.md`
  - `data-model.md`
  - `contracts/angebotskonzept-contract.md`

## Validierungsschritte

1. Strukturvalidierung
- Oeffne `Angebotskonzept.md`.
- Pruefe, ob alle Pflichtkapitel gemaess Contract vorhanden sind.
- Ergebnis: Kapitelstruktur vollstaendig.

2. Sprach- und Formatvalidierung
- Pruefe stichprobenartig alle Hauptabschnitte auf deutsche Sprache.
- Pruefe, dass das Dokument in Markdown konsistent strukturiert ist (Ueberschriften, Listen, Tabellen).
- Ergebnis: Sprache/Format konform.

3. Nachweisvalidierung
- Fuer jede zentrale Aussage im Kapitel "Fachliches Loesungskonzept" und "Meilenstein- und Lieferlogik" muss ein Quellenbezug vorhanden sein.
- Gegenpruefung mit Vergabequellen in `documents/`.
- Ergebnis: Nachweisquote 100 % fuer Schluesselaussagen.

4. Compliance- und Annahmenvalidierung
- Pruefe, dass Annahmen eindeutig markiert sind.
- Pruefe, dass Testumgebungsanforderungen (Internetzugang, Deutschland-Hosting, rollenbasierte Testnutzer) enthalten sind.
- Ergebnis: Keine unmarkierten Annahmen, Compliance-Aspekte abgedeckt.

5. Wertungsorientierungsvalidierung
- Pruefe Abdeckung der Konzept-Unterkriterien aus den Wertungshinweisen:
  - Umsetzung der Leistungsbeschreibung
  - Organisation und Kommunikation
  - Personalorganisation
  - Service-Delivery/Beschwerdemanagement
- Ergebnis: Alle Unterkriterien adressiert.

## Erwartete Ergebnisse
- `Angebotskonzept.md` ist als Erstentwurf freigabefaehig fuer Fachreview.
- Offene Punkte sind als Annahmen oder To-dos dokumentiert.
- Das Dokument ist als Grundlage fuer weitere Angebotsunterlagen verwendbar.

## Referenzen
- Contract: `contracts/angebotskonzept-contract.md`
- Datenmodell: `data-model.md`
- Spezifikation: `spec.md`
