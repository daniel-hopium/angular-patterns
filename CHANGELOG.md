# Changelog

Alle nennenswerten Änderungen an Angular-Patterns. Die Einträge beschreiben, was das Projekt
danach kann bzw. was sich für den Nutzer ändert – kein Commit-Protokoll.

**Regel:** Jeder Commit bekommt seinen Eintrag, im selben Commit. Neues kommt oben unter
„Unveröffentlicht“ dazu; beim Release wird daraus ein Abschnitt mit Versionsnummer und Datum.

Kategorien: **Neu** (neue Funktionen), **Verbessert** (bestehendes Verhalten), **Behoben**
(Fehler), **Intern** (Struktur, Tooling, nicht sichtbar).

## Unveröffentlicht

### Neu
- Kapitel „Sicherheit“ mit 8 Lektionen: XSS und Angulars Sanitizer (mit nachgebautem Sanitizer,
  der nichts ausführt), Trusted Types & CSP, Token-Speicherung (HttpOnly-Cookie und BFF statt
  `localStorage`), CSRF/XSRF-Schutz im `HttpClient`, Refresh-Token-Flow ohne Refresh-Sturm,
  „Guards sind keine Sicherheit“, Open Redirect und URL-Validierung sowie Secrets im Bundle und
  die Absicherung von Abhängigkeiten.
- Zwei neue Kapitel mit 19 Lektionen zu Mustern, die man im Alltag braucht. **Zustand &
  Daten:** Discriminated Union statt Boolean-Flags, State Machine, Server- vs. Client-State
  mit Normalisierung, Optimistic Update mit Rollback, Race Conditions und Abbrechen,
  Stale-While-Revalidate, Optimistic Locking mit Konflikt-Dialog, Draft State mit
  Dirty-Tracking, Offset- vs. Cursor-Pagination und Selektoren mit Memoization. **Robuste
  Apps:** Undo/Redo mit Command Pattern, Autosave, Polling vs. Push mit Page Visibility,
  Persisted State mit Migrationen, Offline-Queue (Outbox), Facade & Events, Cross-Tab-Sync,
  Fehler-Ebenen und Feature Flags.
- Router-Lektionen „Deep Linking“ (Dialog, Tab und Auswahl in der URL) und „Scroll
  Restoration“ (`withInMemoryScrolling`, Anker, nachgeladene Listen).
- Gemeinsamer Fake-Server mit Netzwerk-Leiste wie in den Devtools: Latenz, Fehler und Offline
  lassen sich einstellen, jede Anfrage zeigt Status und Dauer.
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

### Behoben
- Faktenprüfung aller Lektionen gegen Angular 22.2 und die Quellen (Typdefinitionen, Quellcode,
  RFCs, MDN), alle Links samt Anker geprüft. Korrigiert u. a.: `@switch` mit `@default never;`
  braucht eine `@let`-Variable statt eines Signal-Aufrufs; fehlendes `pathMatch` meldet NG04014
  statt einer Redirect-Schleife; Signal-Forms-`submit()` wartet nicht auf laufende
  Async-Validatoren; Einheiten-Suffixe funktionieren nicht im `[style]`-Objekt; das
  Scroll-Restoration-Beispiel hatte einen Effect ohne Abhängigkeit; `@defer` lädt sofort nach
  dem Trigger; EventSource-Wiederverbindung, `keepalive`-Limit und Idempotency-Key präzisiert.
- Die Router-Simulation startet die Guards einer Gruppe jetzt gleichzeitig und wertet in
  Array-Reihenfolge aus – wie Angular; vorher liefen sie nacheinander.
- Ein Fehler in einem `effect()` der Simulationen stoppt nicht mehr die übrigen Effects.
- Die Startseite versprach bei jeder Lektion eine Versionsangabe; Muster-Lektionen haben keine.
- Auswahlfelder mit langen Optionen (etwa „RedirectCommand (skipLocationChange)“ bei den
  Guards) ragten auf schmalen Handys über den Rand; der Text bricht jetzt um.

### Intern
- `tools/make_icons.py` erzeugt SVG, ICO und PNG aus einer einzigen Geometrie (braucht
  Pillow).
