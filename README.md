# Angular-Patterns – modernes Angular zum Anfassen

77 Lektionen zu modernem Angular (Stand Angular 22): Signals, Komponenten, Control Flow,
Dependency Injection, RxJS, Forms, Router, Zustand & Daten, robuste Apps und Performance.
Jedes Muster hat eine Kernregel,
eine Live-Simulation, „So nicht – so“-Code und Links auf die genaue Stelle der Angular-Doku.
Auf Deutsch und Englisch.

Online: https://daniel-hopium.github.io/angular-patterns/

## Starten

`index.html` im Browser öffnen, per Doppelklick. Kein Build, kein Server, keine
Abhängigkeiten. Internet braucht es nur für die Google-Schriften.

## Inhalt

| Kapitel | Lektionen |
|---|---|
| Signals | `signal()`, `computed()`, `effect()`, `untracked()`, `linkedSignal()`, `resource()`/`httpResource()`, eigenes `equal` |
| Komponenten | `input()`, `output()`, `model()`, Content Projection, `host`, Signal Queries, Lebenszyklus |
| Templates & Control Flow | `@if`, `@for` mit `track`, `@switch`, `@let`, `@defer`, Pipes, Class- und Style-Bindings |
| Dependency Injection | `inject()`, `providedIn`/`@Service()`, `InjectionToken`, Component-Provider, Resolution Modifiers, `provideX()` |
| RxJS & HTTP | Flattening-Operatoren, Typeahead, Abmelden, Interop mit Signals, Fehlerbehandlung, `shareReplay`, Interceptors |
| Forms | Typed Forms, Validatoren, `FormArray`, Fehler anzeigen, `ControlValueAccessor`, Template-driven vs. Reactive, Signal Forms |
| Router | Routen, Inputs aus der Route, zurück in die URL schreiben, Deep Linking, Scroll Restoration, Lazy Loading, Guards, Resolver, Links, Titel |
| Zustand & Daten | Discriminated Union statt Boolean-Flags, State Machine, Server- vs. Client-State und Normalisierung, Optimistic Update, Race Conditions, Stale-While-Revalidate, Optimistic Locking, Draft State, Pagination mit Cursor, Selektoren & Memoization |
| Robuste Apps | Undo/Redo (Command Pattern), Autosave, Polling vs. Push, Persisted State mit Migrationen, Offline-Queue (Outbox), Facade & Events, Cross-Tab-Sync, Fehler-Ebenen, Feature Flags |
| Performance & Architektur | OnPush, Zoneless, Container/Presentational, State-Service, Hydration, `NgOptimizedImage` |

Jede Lektion ist gleich aufgebaut: Version und Status, Kernregel, „Auf einen Blick“ (APIs),
Live-Simulation, „So nicht – so“, Richtig/Falsch, „Warum?“ und oft „So testest du es“. Die
Code-Beispiele sind im Stil von VS Code „Dark+“ eingefärbt – ein kleiner eigener Tokenizer
für TypeScript und Angular-Templates, keine Bibliothek.

## Die Simulationen

Die Beispiele laufen ohne Build: kleine Nachbauten in reinem JavaScript, die sich so
verhalten wie Angular und sichtbar machen, was sonst verborgen passiert – etwa wann ein
`computed()` neu rechnet, welche Komponenten die Change Detection prüft, wie `switchMap`
innere Requests abbricht oder in welcher Reihenfolge Guards und Resolver laufen. Die APIs
und ihr Status sind gegen die Typdefinitionen von Angular 22.1 geprüft.

- **`NG`**: Mini-Signals mit derselben Semantik (lazy `computed`, gebündelte `effect`s,
  Gleichheitsprüfung).
- **`RX`**, **`NGDI`**, **`NGRT`**, **`TPL`**: kleine Modelle für RxJS mit Marble-Diagrammen,
  den Injector-Baum, den Router und Change Detection bzw. `@for`.
- **`NET`**: ein Fake-Server mit einstellbarer Latenz, Fehlern und Offline-Schalter plus
  einer Netzwerk-Leiste wie in den Devtools – jede Anfrage mit Status und Dauer.

## Bedienung

- **Sprache:** Der Link oben rechts wechselt zwischen Deutsch und Englisch (`?lang=en`).
- `Strg+K` (Mac: `Cmd+K`) springt in die Suche, jede Lektion lässt sich als gelernt
  markieren (nur im Browser gespeichert).
- Hell und dunkel folgen der Systemeinstellung.

## Die Schwester-Apps

- [Daumenregel](https://daniel-hopium.github.io/pattern-library/) – UI-Regeln mit
  Live-Beispielen, WCAG-Kompass und Quiz
- [CSS-Atlas](https://daniel-hopium.github.io/css-atlas/) – CSS-Eigenschaften mit
  Live-Vorschau
- [HTML-Atlas](https://daniel-hopium.github.io/html-atlas/) – HTML-Elemente und Attribute mit
  Live-Vorschau
- [ARIA-Kompass](https://daniel-hopium.github.io/aria-compass/) – WAI-ARIA mit Inspektor und
  Screenreader-Trainer
