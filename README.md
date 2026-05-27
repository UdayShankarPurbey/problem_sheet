# Angular 21 Interview Problem Sheet

A graded question bank covering Angular 21 plus the broader frontend platform (HTML/CSS/JS/TS, DOM, RxJS, testing, performance, accessibility, SSR). Use it for self-study, mock interviews, or onboarding ramp plans.

---

## Angular 21 — Feature Reference

The interview questions in this sheet are written against the Angular 21 surface area. The headline additions and current state of the framework:

### Reactivity & State
- **Signals (stable)** — `signal()`, `computed()`, `.set()`, `.update()`, `.asReadonly()` as the canonical reactive primitive.
- **`linkedSignal` (stable)** — writable signal derived from a source; resets when the source changes but can also be manually overridden. Supports `{ source, computation }` form with access to `previous` value.
- **`resource()` (stable)** — async data fetching that returns signal-based status: `value()`, `hasValue()`, `isLoading()`, `error()`, `status()`, `.reload()`, optimistic `.value.set()`, automatic abort via `abortSignal`.
- **`httpResource()` (stable)** — `HttpClient`-backed wrapper around `resource()` that flows through interceptors.
- **`effect()` / `afterRenderEffect()` (stable)** — side-effect primitives; `afterRenderEffect` for DOM-touching effects after render.
- **`untracked()` (stable)** — read a signal without registering a dependency in the surrounding reactive context.
- **Signal queries (stable)** — `viewChild`, `viewChildren`, `contentChild`, `contentChildren` returning signals.

### Forms
- **Signal Forms (stable in v21)** — new `@angular/forms/signals` package. Model-driven via a `signal()` plus a `form()` schema. Includes:
  - Field rules: `required`, `email`, `min`, `max`, `minLength`, `maxLength`, `pattern`, `disabled`, `hidden`, `readonly`, `debounce`.
  - Composition helpers: `schema`, `applyWhen`, `applyEach`, `metadata`.
  - Validation: `validate`, `validateAsync` (requires `onError`), `validateHttp`, `validateStandardSchema`.
  - Binding via `[formField]` directive (auto-handles `value`, `disabled`, `readonly`, `name`).
  - Submission with `submit(form, async () => …)` — async callback is required.
  - Replaces `FormControl` / `FormGroup` / `FormBuilder` for new code; reactive & template-driven forms remain supported.

### Templates & Control Flow
- **Built-in control flow (stable)** — `@if`, `@else`, `@for` (with `track`), `@switch`, `@case`, `@default`, `@empty`.
- **`@defer` blocks (stable)** — lazy load template chunks with triggers: `on idle`, `on viewport`, `on interaction`, `on hover`, `on immediate`, `on timer(ms)`, `when <signal>`; sub-blocks `@placeholder`, `@loading`, `@error`.
- **`@let` (stable)** — template-local bindings.

### Rendering, SSR & Hydration
- **Full hydration (stable)** — `provideClientHydration()`.
- **Incremental hydration (stable in v21)** — `withIncrementalHydration()`, paired with `@defer (hydrate on …)` triggers (`idle`, `viewport`, `interaction`, `hover`, `immediate`, `timer`, `when`, `never`).
- **Hybrid rendering** — per-route `RenderMode.Server | Prerender | Client` via `serverRoutes`.
- **Event replay** — buffered DOM events replayed after hydration.
- **Internationalized routes & route-level rendering modes**.

### Zoneless
- **Zoneless change detection (stable)** — `provideZonelessChangeDetection()`; zone.js becomes optional. Components must rely on signals, async pipe, or explicit `ChangeDetectorRef`.

### Routing
- Standalone-friendly route configs, lazy `loadComponent` / `loadChildren`, typed `RouterLink`, View Transitions API via `withViewTransitions()`, `withComponentInputBinding()` to wire route params into signal inputs.

### Components & DI
- **Standalone-by-default**; `NgModule` is legacy.
- **`inject()`** as the primary DI mechanism inside injection contexts.
- **`input()` / `output()` / `model()`** — signal-based component IO; `input.required<T>()`, transforms via `{ transform }`.
- **`host` metadata block** for host bindings/listeners; `HostAttributeToken` for attribute injection.
- **`afterNextRender` / `afterEveryRender`** lifecycle hooks (browser-only).

### Accessibility
- **Angular Aria (developer preview / stable depending on primitive)** — headless `@angular/aria` primitives for Accordion, Listbox, Combobox, Menu, Tabs, Toolbar, Tree, Grid.

### Styling & Animation
- **CSS-first animations (recommended)** — View Transitions API for routes; component-scoped styles via `:host`, `::ng-deep` (deprecated for new code).
- **Tailwind CSS** first-class via `ng add`.

### Tooling & DX
- **Angular CLI** — `ng new`, `ng generate`, `ng build` (esbuild by default), `ng serve` (Vite dev server), `ng test` (Vitest support).
- **Migration schematics** — `ng update` runs codemods for control flow, standalone, signal inputs, inject, etc.
- **Angular MCP Server** — agent integration surface.
- **Vitest** as the recommended unit-test runner; `RouterTestingHarness` and `ComponentHarness` patterns.
- **Build performance** — esbuild + Vite; production builds with persistent disk cache.

### Deprecated / Discouraged in v21
- `NgModule`-based bootstrap for new apps (use `bootstrapApplication`).
- Decorator-based `@Input()` / `@Output()` / `@ViewChild()` (prefer signal equivalents).
- Animations DSL (`@angular/animations`) — prefer CSS/View Transitions.
- `FormBuilder`, `FormControl`, `FormGroup`, `FormArray` for new code (prefer Signal Forms).
- Zone.js dependency for new apps (prefer zoneless).
- Class-based route guards (prefer functional `CanActivateFn`, `CanMatchFn`, `ResolveFn`).
- `*ngIf`, `*ngFor`, `*ngSwitch` (prefer `@if`, `@for`, `@switch`).

---

## Difficulty Legend

| Level    | Symbol | Target audience                 | Typical time per question | What it tests                                                                 |
| -------- | ------ | ------------------------------- | ------------------------- | ----------------------------------------------------------------------------- |
| Easy     | E      | Junior / first-job              | 1–3 min                   | Definitions, syntax, "what does X do", single-file snippets.                  |
| Medium   | M      | 1–3 yrs experience              | 3–7 min                   | Multi-step reasoning, common patterns, debugging small snippets.              |
| Hard     | H      | Mid–senior                      | 7–15 min                  | Architecture choice, tricky edge cases, perf/SSR, multi-component flows.      |
| Extreme  | X      | Senior / staff                  | 15–30 min                 | System-level design, framework internals, complex perf or migration.          |
| Legends  | L      | Principal / framework authors   | 30–90 min                 | Open-ended design, custom primitives, deep internals, novel problem solving.  |

Time is a *budget for a candidate*, not a stopwatch. For self-study, double the time on first pass.

---

## Question Bank

Each level lives in its own file so the index stays light:

**By difficulty level (each tagged with a per-question time budget):**

- [Easy (1000)](questions/easy.md) — fundamentals, syntax, common Angular 21 APIs.
- [Medium (1000)](questions/medium.md) — multi-step reasoning, common patterns, small-snippet debugging.
- [Hard (1000)](questions/hard.md) — architecture choices, multi-component flows, SSR/perf, framework edge cases.
- [Extreme (1000)](questions/extreme.md) — system-level design, framework internals, complex perf, large migrations.
- [Legends (1000)](questions/legends.md) — open-ended design, custom primitives, deep internals, framework authoring.

**By question style (each spans all five levels with inline `Easy/Medium/Hard/Extreme/Legends` sections):**

- [Fix the Bug (500)](questions/fix-the-bug.md) — broken code snippets and misuse patterns; identify the bug and state the fix. 100 per level.
- [Scenarios (500)](questions/scenarios.md) — production incidents, architecture forks, team disagreements, stakeholder negotiations. 100 per level.

**Total: 6,000 questions** (5,000 by-level + 1,000 by-style). Every question carries a time budget aligned with the difficulty legend above.

Topics covered across the bank: HTML, CSS, modern JS, TypeScript, DOM/Browser APIs, Angular components (standalone, inputs/outputs/model, host metadata), parent–child and cross-component communication, content projection, signal queries, signals/computed/effect/linkedSignal/resource, Signal Forms, reactive forms (legacy), routing & guards, lazy loading, HttpClient & interceptors, RxJS, zoneless change detection, hybrid rendering & incremental hydration, `@defer`, Tailwind/styles, accessibility & Angular Aria, animations, i18n, testing (Vitest, harnesses, E2E), performance, security, build & CLI, migrations, and architecture.

---

## How to Use This Sheet

1. Pick a level matching the role you're preparing for.
2. Time-box yourself per the legend; mark questions you couldn't answer cleanly.
3. For Angular questions, validate your answer against the linked references in the [angular-developer skill](https://github.com/anthropics/angular-developer) or [angular.dev](https://angular.dev).
4. Re-attempt failed questions a week later — spaced repetition beats re-reading.
