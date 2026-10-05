# Changelog

Alle nennenswerten Änderungen an Angular-Patterns. Die Einträge beschreiben, was das Projekt
danach kann bzw. was sich für den Nutzer ändert – kein Commit-Protokoll.

**Regel:** Jeder Commit bekommt seinen Eintrag, im selben Commit. Neues kommt oben unter
„Unveröffentlicht“ dazu; beim Release wird daraus ein Abschnitt mit Versionsnummer und Datum.

Kategorien: **Neu** (neue Funktionen), **Verbessert** (bestehendes Verhalten), **Behoben**
(Fehler), **Intern** (Struktur, Tooling, nicht sichtbar).

## Unveröffentlicht

### Neu
- Lektion „Zurück in die URL schreiben“: Query- und Pfad-Parameter mit `router.navigate()`
  ändern – `queryParamsHandling: 'merge'`, `null` zum Entfernen, `replaceUrl` beim Tippen –,
  mit einer Simulation samt Browser-Verlauf, Zurück-Button und Neuladen.
- Syntax-Highlighting im Stil von VS Code „Dark+“ für alle Code-Beispiele, inklusive
  Angular-Templates mit Bindings, `@if`/`@for` und `{{ }}`.
- Kapitel RxJS & HTTP (8 Lektionen) mit Marble-Diagrammen: die vier Flattening-Operatoren im
  Vergleich, Typeahead, Abmelden, Interop mit Signals, Fehlerbehandlung, `shareReplay`,
  Interceptors und Subjects. Dazu Forms (7 Lektionen): Typed Forms, Validatoren, `FormArray`,
  Fehler zur richtigen Zeit anzeigen, `ControlValueAccessor`, Template-driven vs. Reactive und
  Signal Forms, die seit Angular 22 stabil sind.
- Angular-Patterns als eigene App: 40 Lektionen zu modernem Angular (Stand Angular 22) in
  sechs Kapiteln – Signals, Komponenten, Templates & Control Flow, Dependency Injection,
  Router sowie Performance & Architektur.
- Jede Lektion mit Kernregel, API-Tabelle, Live-Simulation in reinem JavaScript, „So nicht –
  so“-Code, Richtig/Falsch, „Warum?“ und oft einem Test-Beispiel. Dazu Version und Status
  (stabil, Developer Preview, experimentell) und Links auf die genaue Stelle der Angular-Doku.
- Spickzettel mit allen APIs aus allen Lektionen, durchsuchbar; Lernfortschritt,
  zweisprachig, hell und dunkel, `Strg+K` für die Suche.

### Verbessert
- Neues App-Symbol im Stil der Schwester-App Daumenregel: dunkler Grund, blasse Linien und
  ein goldener Akzent – alle fünf Apps sehen jetzt im Tab wie eine Familie aus. Dazu
  `favicon.ico` für ältere Browser und ein Icon für den Homescreen (`apple-touch-icon.png`).

### Intern
- `tools/make_icons.py` erzeugt SVG, ICO und PNG aus einer einzigen Geometrie (braucht
  Pillow).
