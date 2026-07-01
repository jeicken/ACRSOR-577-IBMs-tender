# Research: Angebotskonzept iBMS 3.0

## Decision 1: Ausgabeartefakt als eine zentrale Markdown-Datei `Angebotskonzept.md`
- Decision: Das primäre Ergebnis wird als Markdown-Dokument mit klaren Kapiteln, Quellenbezug und Annahmenkennzeichnung erstellt.
- Rationale: Der Auftrag fordert deutsche Inhalte; Markdown ist versionierbar, teamfaehig und fuer iterative Angebotsbearbeitung geeignet.
- Alternatives considered:
  - DOCX als Primaerformat: besser fuer manche Redaktionen, aber schlechter fuer nachvollziehbares Review im Repository.
  - Mehrere Teil-Dateien von Beginn an: granular, aber fuer Erstabgabe unnoetig komplex.

## Decision 2: Quellenbasis auf PDF-Vergabeunterlagen begrenzen
- Decision: In dieser Iteration werden ausschliesslich PDF-Unterlagen in `documents/` als verbindliche Quelle genutzt.
- Rationale: Explizite Nutzeranweisung, XLSX-Dateien nicht zu verwenden; dennoch ausreichende Abdeckung fuer funktionalen Scope und Wertungshinweise.
- Alternatives considered:
  - Einbezug von XLSX direkt: inhaltlich hilfreich fuer Preise/Rollen, aber aktuell ausserhalb des beauftragten Scopes.

## Decision 3: Kapitelstruktur entlang Wertungslogik und Leistungsumfang
- Decision: Die Struktur des Angebotskonzepts folgt zwei Achsen: (a) Loesungsbild fuer iBMS-Funktionsscope, (b) explizite Bedienung der Wertungskriterien.
- Rationale: Die Wertung gewichtet Konzept mit 60 %, inkl. Unterkriterien (Umsetzung, Organisation/Kommunikation, Personal, Service-Delivery).
- Alternatives considered:
  - Reine Funktionsbeschreibung: fachlich brauchbar, aber weniger wertungswirksam.
  - Reine Methodikdarstellung: zu wenig Bezug zum geforderten Funktionsumfang.

## Decision 4: Test- und Abnahmeumgebung als frueher Kernbaustein
- Decision: Die Konzeption adressiert die internetbasierte Test-/Abnahmeumgebung als fruehen Liefergegenstand und Qualitaetsanker.
- Rationale: Anlage 5 fordert u. a. gesicherte Zugriffe, Deutschland-Hosting, rollenbasierte Testuser und produktionsnahe Auspraegung vor Abnahme.
- Alternatives considered:
  - Spaetere Beruecksichtigung erst vor Abnahme: erhoeht Projektrisiko und verschlechtert Nachweisbarkeit in Sprint-/Abstimmungsformaten.

## Decision 5: Meilensteinorientierte Erzaehlstruktur fuer Umsetzungsbild
- Decision: Das Konzept beschreibt Lieferfaehigkeit entlang der in Anlage 7 benannten Meilensteine 1-10.
- Rationale: Ermoeglicht direkte Nachvollziehbarkeit fuer Abnahme- und Zahlungslogik und adressiert Planungserwartung (Gesamtdauer bis zu 2 Jahre).
- Alternatives considered:
  - Nur phasenorientierte Agile-Darstellung ohne Meilensteinabbildung: methodisch okay, aber schwacher Bezug zur Vergabevorgabe.

## Decision 6: Umgang mit partiell nicht extrahierbaren PDF-Inhalten
- Decision: Luecken aus technischer Textextraktion werden als explizite Annahmen bzw. offene Punkte markiert und spaeter manuell verifiziert.
- Rationale: Verhindert Scheinsicherheit und erhaelt Verfahrenssauberkeit.
- Alternatives considered:
  - Nicht markierte Interpretation: schneller, aber hohes Risiko fachlicher Fehlannahmen.

## Verifizierte Input-Hinweise (PDF)
- Leistungsbeschreibung (Vergabenummer ZA 4.2/1002001550/LS): Funktionsumfang inkl. Rollen, Module, Registrierungen, Nachweise, Bedarfe, automatisierte Funktionalitaeten.
- Funktionsbeschreibung (Anlage 4): detaillierte Rollen- und Funktionslandschaft, inkl. Rollenlogik und Bereichsorganisation.
- Anforderungen Testumgebung (Anlage 5): BSI-konformer Zugriffsschutz, Internetzugriff, ca. 60 Zugaenge, Deutschland-Hosting, rollenbasierte Testnutzer, produktionsnahe Umgebung vor Abnahme.
- Zahlungs- und Leistungsplan (Anlage 7): Meilensteine 1-10 von Umsetzungskonzeption bis Abnahme iBMS 3.0.
- Hinweise zur Wertung: Zuschlag nach Gesamtpreis (40 %) und Konzept (60 %) inkl. Unterkriterien.

## Open Clarifications
- Keine offenen `NEEDS CLARIFICATION`-Marker fuer die Planung.
- Inhaltliche Feinschaerfungen fuer einzelne Kapitel koennen bei der eigentlichen Erstellung von `Angebotskonzept.md` im Review mit Fachseite erfolgen.
