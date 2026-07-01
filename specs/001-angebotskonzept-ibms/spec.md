# Feature Specification: Angebotskonzept iBMS 3.0

**Feature Branch**: `[001-angebotskonzept-ibms]`

**Created**: 2026-07-01

**Status**: Draft

**Input**: User description: "Analyse the documents in the folder ./documents/ that describe the tender. We need to generate files that help in creating a proper offer for the functional scope described. The files should be generated in german language. Focus on the file Angbotskonzept which should describe, how we picture a solution for the given requirements. Create the file in markdown format."

## User Scenarios & Testing *(mandatory)*

### User Story 1 - Angebotskonzept erzeugen (Priority: P1)

Als Angebotsteam moechten wir aus den Vergabeunterlagen ein strukturiertes
Angebotskonzept in deutscher Sprache erzeugen, damit wir fristgerecht ein
inhaltlich passendes und bewertungsfaehiges Konzeptdokument einreichen koennen.

**Why this priority**: Das Angebotskonzept ist zentral fuer das Kriterium
"Konzept" (60 % Gewichtung) und damit der wichtigste Hebel fuer den Zuschlag.

**Independent Test**: Kann vollstaendig getestet werden, indem aus den
eingebrachten Vergabedokumenten eine Datei `Angebotskonzept.md` mit allen
Pflichtkapiteln und nachvollziehbaren Quellenbezuegen entsteht.

**Acceptance Scenarios**:

1. **Given** relevante Vergabe-PDFs liegen vor, **When** das Konzept erstellt
   wird, **Then** entsteht eine deutsche Markdown-Datei mit klarer
   Loesungsskizze fuer den funktionalen Scope.
2. **Given** Anforderungen zu Rollen/Funktionen, Testumgebung und
   Meilensteinen sind dokumentiert, **When** das Konzept erzeugt wird, **Then**
   werden diese Themen in separaten, fachlich konsistenten Abschnitten
   adressiert.

---

### User Story 2 - Wertungsorientierte Ausarbeitung (Priority: P2)

Als Bid-Manager moechte ich, dass das Angebotskonzept explizit auf die
bewerteten Unterkriterien eingeht (u. a. Umsetzung, Organisation,
Personalorganisation, Service-Delivery), damit die Angebotsqualitaet
zielgerichtet erhoeht wird.

**Why this priority**: Die inhaltliche Passung zur Wertungsmatrix entscheidet
ueber die erzielbare Punktzahl im Konzeptteil.

**Independent Test**: Kann unabhaengig getestet werden, indem jeder
Wertungsblock in `Angebotskonzept.md` mindestens ein eigenes Unterkapitel mit
konkretem Beitrag zur Wertung besitzt.

**Acceptance Scenarios**:

1. **Given** die Hinweise zur Wertung sind verfuegbar, **When** das Konzept
   finalisiert wird, **Then** sind die bewertungsrelevanten Kriterien sichtbar
   und nachvollziehbar abgedeckt.

---

### User Story 3 - Teamfaehige Weiterbearbeitung (Priority: P3)

Als Angebotsteam moechten wir die erzeugte Konzeptdatei strukturiert
weiterbearbeiten koennen, damit Fachverantwortliche ohne Medienbruch Inhalte
ergaenzen, pruefen und freigeben koennen.

**Why this priority**: Iterative Qualitaetssicherung ist fuer finale
Einreichungsreife notwendig.

**Independent Test**: Kann getestet werden, indem mehrere Teammitglieder die
Markdown-Abschnitte getrennt aktualisieren und der Dokumentaufbau stabil bleibt.

**Acceptance Scenarios**:

1. **Given** ein Erstentwurf liegt vor, **When** redaktionelle Anpassungen
   erfolgen, **Then** bleiben Abschnittsstruktur, Quellenbezug und
   Nachvollziehbarkeit erhalten.

### Edge Cases

- Wie wird verfahren, wenn ein PDF nur teilweise maschinell auslesbar ist und
  Inhalte manuell nachgepflegt werden muessen?
- Wie wird mit widerspruechlichen Aussagen zwischen Leistungsbeschreibung,
  Funktionsbeschreibung und Zahlungs-/Leistungsplan umgegangen?
- Wie wird sichergestellt, dass unklare Anforderungen als Annahmen markiert
  werden und nicht als Tatsachen in das Konzept einfliessen?

## Requirements *(mandatory)*

### Functional Requirements

- **FR-001**: Das System MUST die bereitgestellten PDF-Vergabeunterlagen im
  Ordner `documents/` als Eingabequelle beruecksichtigen.
- **FR-002**: Das System MUST eine Datei `Angebotskonzept.md` als zentrales
  Ergebnisartefakt erzeugen.
- **FR-003**: Die Ausgabedatei MUST vollstaendig in deutscher Sprache verfasst
  sein.
- **FR-004**: Die Datei MUST eine nachvollziehbare Loesungsdarstellung fuer den
  funktionalen Scope des iBMS 3.0 enthalten.
- **FR-005**: Das Konzept MUST die Themen Rollen/Funktionsrollen, Module bzw.
  Bereiche, Test- und Abnahmeumgebung sowie Meilensteinbezug adressieren.
- **FR-006**: Das Konzept MUST die wertungsrelevanten Konzept-Unterkriterien
  strukturiert abbilden.
- **FR-007**: Jede wesentliche inhaltliche Aussage MUST auf eine identifizierte
  Vergabequelle rueckfuehrbar sein.
- **FR-008**: Nicht direkt belegbare Punkte MUST als Annahmen gekennzeichnet
  werden.
- **FR-009**: Das Artefakt MUST so strukturiert sein, dass es iterativ durch
  mehrere Bearbeiter fortgeschrieben werden kann.
- **FR-010**: Das Ergebnis MUST als Grundlage fuer weitere Angebotsunterlagen
  (z. B. Umsetzungs-, Personal- oder Service-Kapitel) geeignet sein.

### Compliance and Confidentiality Requirements *(mandatory)*

- Das Konzept muss mit den formalen Vorgaben der Vergabeunterlagen vereinbar
  sein und darf keine widerspruechlichen Leistungszusagen enthalten.
- Personenbezogene oder sensible Angaben duerfen nur in dem Umfang verwendet
  werden, wie es die Unterlagen und die Angebotsbearbeitung erfordern.
- Es duerfen keine externen, nicht verifizierten Quellen als verbindliche
  Vergabegrundlage dargestellt werden.

### Evidence and Traceability Requirements *(mandatory)*

- Die Spezifikation muss festlegen, welche Kapitel des Konzepts auf welche
  Vergabedokumente abgestuetzt sind.
- Fuer zentrale Aussagen (Funktionsumfang, Testumgebung, Meilensteine,
  Wertungskriterien) muss ein Quellenbezug dokumentiert werden.
- Jede Annahme muss als solche markiert und spaeter verifizierbar sein.

### Key Entities *(include if feature involves data)*

- **Vergabequelle**: Relevantes Ausschreibungsdokument mit Titel,
  Vergabenummer, thematischem Schwerpunkt und Verwendungsstatus.
- **Anforderung**: Fachliche oder organisatorische Vorgabe aus den
  Vergabeunterlagen mit Prioritaet und Bezug zur Angebotsdarstellung.
- **Wertungskriterium**: Bewertungsaspekt inklusive Gewichtung und erwartetem
  Nachweis im Konzept.
- **Konzeptabschnitt**: Kapitel innerhalb `Angebotskonzept.md` mit Ziel,
  Kernaussagen und Quellenbezug.
- **Annahme**: Vorlaeufige Festlegung fuer unvollstaendige Informationen,
  inklusive Begruendung und Validierungsbedarf.

## Success Criteria *(mandatory)*

### Measurable Outcomes

- **SC-001**: Ein vollstaendiger Erstentwurf von `Angebotskonzept.md` liegt vor
  und deckt 100 % der definierten Pflichtkapitel ab.
- **SC-002**: Mindestens 90 % der kritischen Anforderungen aus den ausgewerteten
  PDF-Unterlagen sind im Konzept explizit adressiert.
- **SC-003**: 100 % der wertungsrelevanten Unterkriterien des Konzeptanteils sind
  in mindestens einem klar benannten Abschnitt abgebildet.
- **SC-004**: 100 % der zentralen Aussagen im Konzept sind mit Quellenbezug oder
  expliziter Annahmekennzeichnung versehen.
- **SC-005**: Das Angebotsteam kann innerhalb von 2 Arbeitstagen nach Erstellung
  eine erste Review-Runde auf Basis des Dokuments abschliessen.

## Assumptions

- Die initiale Bearbeitung fokussiert auf PDF-Unterlagen; XLSX-Dateien werden in
  dieser Feature-Iteration bewusst nicht ausgewertet.
- Die Dateibezeichnung fuer das zentrale Artefakt wird als
  `Angebotskonzept.md` standardisiert.
- Die Vergabeunterlagen im Ordner `documents/` gelten als massgebliche
  Arbeitsgrundlage fuer den Erstentwurf.
- Detailtiefen fuer Preis- und Ressourcenkalkulation werden in nachgelagerten
  Angebotsdokumenten vertieft.
