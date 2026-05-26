# Fix the Bug — 500 Questions

Each question shows broken code or a misuse pattern. Identify the bug and state the fix. Difficulty escalates by section. Times are per the legend in the [root README](../README.md): Easy 1–3m, Medium 3–7m, Hard 7–15m, Extreme 15–30m, Legends 30–90m.

---

## Easy (1–100)

1. `const s = signal(0); s.set(s + 1);` — bug? — 2m
2. Template `{{ count }}` where `count = signal(0)` — bug? — 1m
3. `effect(() => count.set(count() + 1));` — bug? — 3m
4. `computed(() => { fetch('/x'); return 1; })` — bug? — 3m
5. `<input [formField]="form.name" [value]="x" />` — bug? — 2m
6. `<input [formField]="form.age" min="18" />` — bug? — 2m
7. `validate(s.email, ({ touched }) => touched() ? ... : ...)` — bug? — 3m
8. `submit(form, () => { save(); })` — bug? — 2m
9. `validateAsync(s.x, { params: s.x, factory: ... })` — bug? — 3m
10. `validateAsync(s.x, { params: ({value}) => value(), factory: ..., onSuccess: ... })` — bug? — 2m
11. `if (form.name.valid()) {...}` — bug? — 2m
12. `applyEach(s.items, (item, i) => required(item.name))` — bug? — 2m
13. `model = signal({ name: null, age: null });` for a form — bug? — 2m
14. `pattern(s.zip, /^\d{5}$/, { when: cond })` — bug? — 3m
15. `@for (item of items) { {{ item }} }` — bug? — 2m
16. `@for (item of items; track item)` where items are `string[]` of empty strings — bug? — 3m
17. `*ngIf="user()"` in v21 standalone component — bug? — 1m
18. `<button (click)="onClick">Save</button>` — bug? — 1m
19. `<input [(value)]="x" />` — bug? — 2m
20. `inject(SomeService)` written in `constructor() { this.x = inject(...) }` for arrow-function class field — bug? — 3m
21. `inject(SomeService)` called inside `ngOnInit()` — bug? — 3m
22. `@Component({ template: '...', imports: [NgIf] })` v21 still using `NgIf` — bug? — 2m
23. Two-way bind `[(checked)]="value"` where component uses `@Input() checked` — bug? — 3m
24. `output()` declared as `output = output<void>()` then called `output.emit('hello')` — bug? — 2m
25. `@ViewChild('x') x!: ElementRef;` then `this.x.nativeElement` in constructor — bug? — 3m
26. `viewChild('x')` read in `ngOnInit()` returns `undefined` — bug? why? — 3m
27. `http.get('/api').then(r => ...)` — bug? — 2m
28. `http.get('/x')` called but result never used — bug? — 2m
29. `obs$.subscribe(...)` in a component, no cleanup — bug? — 3m
30. `setInterval(() => count.set(count() + 1), 1000)` in `ngOnInit` no clearInterval — bug? — 3m
31. `effect(() => console.log(value()))` declared at file top level — bug? — 3m
32. `provideRouter(routes)` listed in component `providers` — bug? — 3m
33. `HttpClient` injected with `provideHttpClient()` missing from bootstrap — bug? — 2m
34. `RouterOutlet` used but not in `imports` — bug? — 2m
35. `bootstrapApplication(App)` with `App` decorated `@NgModule` — bug? — 2m
36. `class Foo { name = input(''); }` then template `{{ name }}` — bug? — 2m
37. `selector: 'app-x'` plus `<AppX />` in template — bug? — 1m
38. `<a routerLink="users/{{id}}">` — bug? — 2m
39. `<a [routerLink]="['/users', id]" queryParams="{a:1}">` — bug? — 2m
40. `Router.navigate('/users')` (string not array) — bug? — 2m
41. `route.snapshot.params.id` to react to changes — bug? — 3m
42. `route.params.subscribe(p => ...)` no unsubscribe — bug? — 3m
43. `<form (submit)="onSubmit()">` with no `preventDefault` — bug? — 2m
44. `<button type="button">Submit</button>` inside a `<form>` expecting submit — bug? — 2m
45. `[class.active]="isActive"` where `isActive = signal(true)` — bug? — 2m
46. `[style.width]="w"` where `w = 100` (number) — bug? — 2m
47. `{{ items.length }}` for Signal-Form array, missing `()` somewhere — bug? — 3m
48. `@if (form().valid)` (parenthesis on wrong call) — bug? — 2m
49. `errors().length > 0 && errors()[0].message` access on undefined — bug? — 3m
50. `signal(null)` then `s().toUpperCase()` — bug? — 2m
51. `input.required<string>()` parent passes `undefined` — bug? — 2m
52. `input('')` with `transform: booleanAttribute` where caller passes a number — bug? — 3m
53. `output()` then parent uses `(output)="..."` but child emits twice per click — bug? — 3m
54. `model('')` parent binds `[ngModel]` instead of `[(value)]` — bug? — 3m
55. `host: { '[class.active]': 'active' }` where `active` is a signal — bug? — 2m
56. `host: { '(click)': onClick }` (missing parentheses on handler) — bug? — 2m
57. `@HostBinding('class.x') x = true;` in v21 standalone — preferred pattern? — 2m
58. `@HostListener('click') onClick() {}` in v21 standalone — preferred pattern? — 2m
59. `imports: [FormsModule]` then `<input [formField]="..." />` — bug? — 2m
60. `<input ngModel name="x" />` outside `<form>` — bug? — 2m
61. `provideClientHydration()` plus `window.x = 1` in component code — bug? — 3m
62. `localStorage.getItem('x')` in `ngOnInit` of SSR app — bug? — 3m
63. `new Date().toString()` rendered in template on SSR — bug? — 3m
64. `Math.random()` in component template — bug? — 3m
65. `routerLinkActive="active"` with no `[routerLinkActiveOptions]` exact for `/` route — bug? — 3m
66. `redirectTo: '/home'` but route also has `component:` — bug? — 2m
67. `path: '**'` declared above `path: 'users'` — bug? — 2m
68. `pathMatch: 'full'` missing on redirect with empty path — bug? — 2m
69. `canActivate: [authGuard]` where `authGuard` returns `Promise<void>` — bug? — 2m
70. `resolve: { user: userResolver }` and component reads `route.snapshot.data.user` once — caveat? — 3m
71. `inject()` called inside `setTimeout` callback — bug? — 3m
72. `runInInjectionContext` missing for `inject()` in a non-component class — bug? — 3m
73. `inject(SomeToken, { optional: true })` typed `T` not `T | null` — bug? — 2m
74. `providedIn: 'any'` in v21 — concerns? — 2m
75. `providers: [SomeService]` repeated at multiple components — bug? — 3m
76. `provideHttpClient()` plus `provideHttpClient(withFetch())` (both registered) — bug? — 2m
77. `provideHttpClient(withInterceptors([a, b]))` and assuming `b` runs before `a` — bug? — 2m
78. `HttpClient.get('/x')` with `responseType: 'text'` and JSON body — bug? — 2m
79. `HttpHeaders` mutated via `headers.append(...)` and reused — bug? — 3m
80. `HttpParams` mutated via `params.set('x', '1')` and reused — bug? — 3m
81. `from(promise).subscribe(...)` not handling rejection — bug? — 2m
82. `Promise.all([a, b])` where `b` rejects — handling? — 2m
83. `async ngOnInit() { await fetch(...) }` no error handling — bug? — 2m
84. `obs$.pipe(switchMap(...))` for a write operation — bug? — 3m
85. `setTimeout(() => this.value(), 0)` in OnPush — bug? — 3m
86. `BehaviorSubject<string | null>(null)` with downstream `s.toUpperCase()` — bug? — 2m
87. `merge(a$, b$).subscribe(...)` expecting only the latest — bug? — 3m
88. `Observable.create(...)` — bug? what's the modern API? — 2m
89. `interface User { name: string; age?: number; }` then `user.age + 1` — bug? — 2m
90. `as Type` cast bypassing real check — bug? — 2m
91. `JSON.parse(raw)` typed as `User` directly — bug? — 2m
92. `any` used as catch parameter type — bug? — 2m
93. `Array<User>` typed but `null` passed — bug? — 2m
94. `Map.prototype.size()` (function call) — bug? — 1m
95. `[...new Set([NaN, NaN])]` expected length 1, gets — caveat? — 2m
96. `'use strict'` not in module (no effect) — caveat? — 1m
97. `const obj = {}; obj.x = 1; obj.y = 2;` typed `Record<string, never>` — bug? — 2m
98. `if (x = 1)` (assignment vs comparison) — bug? — 1m
99. `for (var i = 0; i < 3; i++) setTimeout(() => console.log(i))` — bug? fix? — 3m
100. `function f() { return\n {x:1} }` (auto-semicolon insertion) — bug? — 3m

## Medium (101–200)

101. `effect(() => state.set(other()))` keeps re-firing — fix without `allowSignalWrites`. — 5m
102. `computed(() => fetch('/x').then(r => r.json()))` — wrong primitive — what should it be? — 4m
103. `linkedSignal(() => list()[0])` resets selection on every refresh — preserve last selection — 5m
104. `resource({ params: () => id, loader: ... })` with `id` not a signal — bug? — 5m
105. `resource({ params: () => ({id: id()}), loader: async ({params}) => fetch(`/x/${params.id}`) })` no `abortSignal` — bug? — 5m
106. `httpResource(url)` then in tests, request not cancelled between params changes — fix? — 6m
107. `toSignal(obs$)` then template `{{ data().name }}` crashes initially — fix? — 4m
108. `toObservable(s)` subscribed in service constructor (no DI context) — bug? — 5m
109. `form().valid()` returns `true` even with empty required fields — bug? — 5m
110. `validateAsync` factory creates a new `resource` per call instead of using `params` — bug? — 6m
111. `applyEach(s.items, (item) => { required(item); })` no error but never validates — bug? — 5m
112. `applyWhen(s.x, () => s.x() === 'a', (path) => ...)` — bug? — 5m
113. `submit(form, async () => { await save(); router.navigate(['/done']); })` navigation fails on invalid — bug? — 5m
114. `form.items().length` array length — bug? — 3m
115. `form.tags` is `string[]`, template `<select [formField]="form.tags">` — bug? — 4m
116. `<input type="checkbox" [formField]="form.tags">` where `tags: string[]` — bug? — 4m
117. `@for (x of items; track x.id) { ... }` items have no `id` — fix? — 4m
118. `@for (item of items; track $index)` items have stable ids — bug? — 4m
119. `@if (user(); as u) { {{ u.name }} }` — bug? what's the v21 syntax? — 3m
120. `@let total = price() * qty()` updates only on first render — bug? — 5m
121. OnPush component re-renders too often because parent passes `{a: 1}` literal each time — fix? — 5m
122. OnPush component never re-renders after parent mutates an array in place — fix? — 5m
123. `viewChild('foo')` returns `undefined` when accessed in `ngOnInit` — fix? — 4m
124. `viewChildren('item')` template uses `#item` on a structural-directive root — bug? — 5m
125. Content projection: `<ng-content select=".header">` not matching `<div header>` — fix? — 4m
126. `contentChildren(TabItem)` returns empty even though `<TabItem>` projected — fix? — 5m
127. `model('value')` parent uses `(valueChange)="..."` — bug? — 4m
128. Two-way `[(checked)]` with `model<boolean>()` plus `(checkedChange)` listener fires twice — fix? — 5m
129. `effect()` declared in service has no cleanup when subscribers leave — fix? — 5m
130. `takeUntilDestroyed()` called inside `inject(SomeService).initialize()` — bug? — 5m
131. `ngOnDestroy` called manually from parent — bug? — 4m
132. `setInterval` in `ngOnInit`, cleared in `ngOnDestroy`, but component is part of OnPush subtree — works? — 5m
133. `provideHttpClient(withInterceptors([a]))` plus class interceptor via `HTTP_INTERCEPTORS` — bug? — 4m
134. Auth interceptor uses `inject(AuthService)` but is registered as class — bug? — 5m
135. 401 refresh interceptor causes infinite loop on /refresh failure — fix? — 6m
136. `firstValueFrom(http.get('/x'))` no error handling — bug? — 4m
137. `forkJoin([a$, b$])` where one observable never emits — bug? — 4m
138. `switchMap` cancels in-flight save when user clicks again — fix? — 4m
139. `subscribe` inside `subscribe` (nested) — fix with operator? — 5m
140. `BehaviorSubject<User>` exposed publicly, consumers mutate — fix? — 4m
141. `Subject` exposed as `Observable` but consumers cast back to call `.next` — fix? — 4m
142. `interval(1000)` in component, no unsubscribe, OnPush — bug? — 5m
143. `route.params` subscribed without `distinctUntilChanged` — bug for same-param reload? — 5m
144. `Router.navigate(['/users', { id: 1 }])` query string surprise — fix? — 4m
145. `canActivate: [() => true]` typed wrong — fix? — 3m
146. `canMatch: [authGuard]` returns `Observable` but never completes — bug? — 5m
147. `loadComponent: () => import('./x').then(m => m.default)` always loads — make conditional? — 5m
148. `provideRouter(routes, withInMemoryScrolling())` — scroll restore broken — fix? — 5m
149. SSR: `if (window) { ... }` in component — bug? — 4m
150. SSR: `document.cookie` read during render — bug? — 4m
151. SSR: a `resource()` runs twice (server + client) — fix with `TransferState`? — 6m
152. SSR: hydration mismatch on a `*ngIf="now() > t"` — fix? — 5m
153. SSR: `prefers-color-scheme` causes mismatch — fix? — 5m
154. SSR: random IDs on server differ from client — fix? — 5m
155. SSR: `httpResource` cached on server, refetched on client — fix? — 5m
156. SSR: server-side `effect()` mutates `localStorage` — bug? — 4m
157. View transitions: route change triggers transition but layout shifts visibly — fix? — 5m
158. View transitions: `view-transition-name` set inside `@for` collisions — fix? — 5m
159. Tailwind classes not applied in a lazy-loaded standalone component — fix? — 5m
160. CSS variables on `:root` not reaching projected content — fix? — 5m
161. `[ngStyle]` and signals — re-runs every CD — fix? — 4m
162. `ngClass` array form recomputed each CD because `[a, b]` literal — fix? — 4m
163. `pipe` used for heavy compute in template — runs many times — fix? — 5m
164. `track` used with `Math.random()` — chaos in `@for` — fix? — 4m
165. `@for` with `track item.name` items renamed in place — bug? — 4m
166. Custom pipe `pure: false` recalculates excessively — fix? — 5m
167. Custom pipe imported but template throws "No pipe with name" — fix? — 3m
168. `inject(NgZone).run(() => ...)` for a CD update under zoneless — bug? — 5m
169. `ChangeDetectorRef.detectChanges()` called inside `ngAfterViewInit` causes ExpressionChanged — fix? — 5m
170. `effect()` reads `viewChild()` immediately — `undefined` — fix? — 4m
171. `afterNextRender` used in service — needs injection context — fix? — 4m
172. `afterEveryRender` used for analytics every CD — too expensive — fix? — 5m
173. `signal({})` then `s.update(x => x)` triggers consumers — bug? — 4m
174. `signal({a:1}, {equal: deepEqual})` deepEqual references parent state — bug? — 5m
175. `computed(() => Date.now())` cached after first read — bug? what to use? — 4m
176. `effect` doing DOM measurement — wrong primitive — fix? — 4m
177. `effect` writes to signal then reads it — fires twice — fix? — 5m
178. `linkedSignal` with `source` not a function — bug? — 4m
179. `resource.value()` accessed before `hasValue()` — undefined — fix? — 4m
180. `resource.reload()` called in loop — fix? — 4m
181. `httpResource(() => '/api')` URL is static, but still re-renders endlessly — bug? — 4m
182. `httpResource(() => '/api/' + id())` `id()` is null briefly — fix? — 5m
183. Signal Forms: `form()` called twice on different model signals returning same model copy — fix? — 5m
184. Signal Forms: `disabled(s.x, ({valueOf}) => !valueOf(s.y))` `y` is the field's own state — fix? — 4m
185. Signal Forms: `hidden()` hides field but model retains stale value on submit — fix? — 5m
186. Signal Forms: array delete by index removes wrong row — fix? — 5m
187. Signal Forms: schema reused across two forms shares validation state — bug? — 5m
188. Signal Forms: async validator never resolves due to params not changing — fix? — 5m
189. TypeScript: generic `function f<T>(x: T): T` infers `T = unknown` for object literal — fix? — 4m
190. TypeScript: `as const` on array of literals then `arr.includes('z')` errors — fix? — 4m
191. TypeScript: union narrowing fails because of `Array.isArray` on tuple — fix? — 4m
192. TypeScript: `Record<string, X>` allows `x.foo` even when missing — fix with `noUncheckedIndexedAccess`? — 4m
193. TypeScript: `exhaustiveCheck(x: never)` fails because of extra union member added — purpose? — 4m
194. TypeScript: `enum Color` declared in two files, both imported — bug? — 4m
195. TypeScript: `import type X` then `new X()` — bug? — 3m
196. ESM: `import './polyfills'` for side effects but `sideEffects: false` in package.json — bug? — 4m
197. Bundle includes whole `lodash` because of `import _ from 'lodash'` — fix? — 4m
198. Bundle includes `moment` for one date format — alternatives? — 4m
199. Build error "ngcc" appears in v21 — bug? — 3m
200. `ng build` succeeds but prod page crashes on `inject()` — fix? (likely AOT-related) — 5m

## Hard (201–300)

201. Signal store: `withMethods` calls `inject()` lazily and breaks under SSR — fix? — 10m
202. Signal store: `entityAdapter.upsert` triggers full re-render of unrelated lists — fix? — 10m
203. Signal store: `rxMethod` swallows errors silently — fix? — 8m
204. Signal store: state mirrored to URL via `effect()` keeps re-syncing — fix? — 10m
205. Signal store: persistence middleware writes on every keystroke — fix? — 8m
206. Signal forms: nested `applyEach(applyEach(...))` callbacks share state by reference — fix? — 12m
207. Signal forms: 5-section form mounted lazily loses validation when re-shown — fix? — 12m
208. Signal forms: server-side validation maps errors to wrong field due to nested path mismatch — fix? — 12m
209. Signal forms: rich-text editor field reports stale `dirty` after `applyEach` array reorder — fix? — 12m
210. Signal forms: `validateAsync` resource caching causes "already taken" sticky after free — fix? — 10m
211. SSR: `httpResource` returns server-cached value but auth differs per request — fix? — 12m
212. SSR: `TransferState` payload exceeds 2MB on a list page — strategy? — 10m
213. SSR: incremental hydration: `@defer (hydrate on viewport)` fires before user can interact — debug? — 12m
214. SSR: incremental hydration: event replay misses keyboard events on a deferred block — fix? — 12m
215. SSR: edge runtime crashes because of `crypto.subtle` polyfill mismatch — fix? — 10m
216. SSR: per-request injector retains references via a singleton `EventEmitter` — leak fix? — 12m
217. Hydration mismatch only on first session (cookieless), repeats reproducibly — debug? — 12m
218. Hydration logs warn about a child node mismatch when third-party widget injects nodes pre-hydration — fix? — 12m
219. View transitions: nav from `/list` to `/list/:id` skips animation when same component — fix? — 8m
220. View transitions: shared element flickers because `view-transition-name` set after activation — fix? — 10m
221. Routing: lazy module loads twice when navigating back/forward fast — fix? — 10m
222. Routing: `withComponentInputBinding` doesn't update child `input.required<string>()` on same-route param change — fix? — 10m
223. Routing: preloading strategy preloads all routes including auth-gated — fix? — 8m
224. Routing: custom `RouteReuseStrategy` keeps stale state when nav between same component with different params — fix? — 12m
225. HttpClient: interceptor adds `Authorization` to *all* requests including third-party CDN — fix? — 8m
226. HttpClient: retry-on-401 loop fires after permanent logout — fix? — 10m
227. HttpClient: `withFetch()` plus `responseType: 'blob'` returns wrong MIME — fix? — 8m
228. HttpClient: in-memory cache keyed by URL only, ignoring `Authorization`, leaking data — fix? — 12m
229. Perf: typing in search box re-renders unrelated `<Header>` due to root-level signal change — fix? — 10m
230. Perf: a `@for` with 10k items rebuilds DOM on every selection toggle — fix? — 10m
231. Perf: scroll handler triggers CD every pixel — fix without leaving zone? — 10m
232. Perf: `view-transition` triggers full-page layout when only one section changes — scope it? — 10m
233. Perf: route nav blocks for 200ms on guard's `firstValueFrom` of slow API — fix? — 10m
234. Perf: lazy chunk waterfall 1→2→3 visible in Network panel — fix? — 12m
235. Perf: shimmer skeleton CSS triggers paint on every CD — fix? — 8m
236. Perf: `ngOnInit` does heavy synchronous work — convert to deferred? — 10m
237. Memory leak: WebSocket reconnect grows listener count linearly — fix? — 10m
238. Memory leak: `IntersectionObserver` retained because element kept in JS map — fix? — 10m
239. Memory leak: `ResizeObserver.observe(node)` on a node later removed without `unobserve` — fix? — 10m
240. Memory leak: `effect()` in a service captures closure over old component refs — fix? — 12m
241. Change detection: ExpressionChangedAfterItHasBeenChecked only fires in dev, not in prod — why? — 10m
242. Change detection: dynamic component `setInput` doesn't render until next external CD — fix? — 10m
243. Change detection: `detectChanges()` called twice in same tick — find culprit. — 10m
244. Change detection: signals not reflected because component is `detach()`ed — fix? — 8m
245. Zoneless: a third-party lib's `setTimeout` no longer triggers CD — fix? — 10m
246. Zoneless: Router events don't refresh sidebar — fix? — 10m
247. Zoneless: Animations trigger but signals don't update — fix? — 10m
248. Tests: signal effect test passes locally, fails in CI — flakiness root cause? — 12m
249. Tests: `TestBed.runInInjectionContext` not used for `effect()` — fix? — 8m
250. Tests: HTTP test leaks across test files due to shared module config — fix? — 10m
251. Tests: Component harness can't find element rendered inside `@defer` — fix? — 8m
252. Tests: Snapshot mismatch on every CI run due to time/locale — fix? — 8m
253. Build: bundle 2× larger after upgrade — find the culprit. — 12m
254. Build: dev server crashes with "Cannot find module 'foo'" only after `ng update` — fix? — 10m
255. Build: `ng build --prerender` fails for one route returning 500 — diagnose? — 10m
256. Build: PWA SW caches an old chunk, users stuck on stale UI — fix? — 12m
257. Build: source maps missing in prod, errors unreadable — fix? — 8m
258. Build: Tailwind classes purged from a lazy template — fix? — 10m
259. Build: monorepo lib's secondary entry point not resolved by consumer — fix? — 10m
260. Build: project references' `composite: true` not regenerating decls — fix? — 10m
261. Migration: schematic converts `@Input()` to `input()` but breaks setter logic — fix? — 12m
262. Migration: `*ngIf` to `@if` conversion drops the `as` alias — fix? — 8m
263. Migration: `*ngFor` to `@for` conversion uses `track $index` everywhere — risk? — 8m
264. Migration: standalone migration leaves `CommonModule` import unused but required — fix? — 10m
265. Migration: signal-input migration breaks `OnChanges` consumers — fix? — 10m
266. Migration: Reactive Forms → Signal Forms breaks `markAsTouched` consumers — fix? — 12m
267. CSS: `:has(.error)` on `<form>` not matching error from child due to encapsulation — fix? — 10m
268. CSS: container query `@container (min-width: 400px)` not firing for projected children — fix? — 10m
269. CSS: subgrid breaks when card content uses `display: contents` — fix? — 8m
270. CSS: dark mode flash on load — fix? — 10m
271. CSS: `view-transition-name` triggers root-level transition unintentionally — fix? — 8m
272. CSS: focus ring missing on a custom button after `outline: none` — fix? — 8m
273. CSS: scroll-driven animation runs in non-Chromium browsers as static — fallback? — 8m
274. CSS: `font-display: swap` causes layout shift — fix? — 10m
275. A11y: screen reader doesn't announce route changes — fix? — 10m
276. A11y: focus lost after closing modal — fix? — 8m
277. A11y: tab order breaks after `@defer` block hydrates — fix? — 10m
278. A11y: custom select doesn't announce active option — fix? — 10m
279. A11y: live region announces every keystroke (noisy) — fix? — 8m
280. A11y: skip link only works on first page load — fix? — 8m
281. Security: SSRF via user-provided URL in `httpResource` — fix? — 10m
282. Security: stored XSS via `[innerHTML]` of user content — fix? — 8m
283. Security: CSP nonce missing on dynamically injected script — fix? — 10m
284. Security: refresh token stored in `localStorage` exfiltrated via XSS — fix? — 10m
285. Security: open redirect on `?returnUrl=` after login — fix? — 8m
286. RxJS: race condition in interceptor between two refresh-token attempts — fix? — 12m
287. RxJS: `shareReplay()` without `refCount` retains stream forever — fix? — 8m
288. RxJS: `combineLatest` never emits because one source is cold and not subscribed — fix? — 10m
289. RxJS: `tap` used as a sink — debug — fix? — 8m
290. RxJS: `catchError` returns `of(null)` losing types downstream — fix? — 8m
291. State: signal store imported in two MFEs creates two singletons — fix? — 12m
292. State: BroadcastChannel sync causes infinite ping-pong — fix? — 10m
293. State: optimistic update applied twice (server returns confirmation, client also adds) — fix? — 12m
294. State: undo middleware grows unbounded — fix? — 8m
295. State: hydration of store sets initial values that override URL filters — fix? — 10m
296. SSR + auth: cookies present on server but client request to same path fails CORS — fix? — 12m
297. SSR + i18n: locale negotiated server-side but client routes to default — fix? — 10m
298. SSR + analytics: page view fires twice (server then client) — fix? — 8m
299. SSR + experiment: variant differs between server and client — fix? — 12m
300. SSR + theme: dark mode flicker due to client overriding cookie — fix? — 10m

## Extreme (301–400)

301. Cross-cutting: signal store + Signal Form + SSR with TransferState — but reload causes duplicate writes. Trace the chain and fix. — 25m
302. Cross-cutting: route-driven `httpResource` + `withComponentInputBinding` + lazy module — input binding doesn't fire after first nav. Diagnose. — 25m
303. Cross-cutting: micro-frontend host loads two Angular MFEs sharing `@angular/core` — runtime "two NgZones" warning. Fix. — 25m
304. Cross-cutting: incremental hydration + view transitions = transitions fire before hydration completes, JS not yet bound to clicks. Fix. — 25m
305. Cross-cutting: zoneless + third-party WS lib + animations = drops events. Diagnose. — 25m
306. Architecture: feature flag toggled mid-session causes inconsistent UI across components. Fix without full reload. — 25m
307. Architecture: tenant context loaded async at bootstrap, components inject `Tenant` and get default. Fix DI ordering. — 25m
308. Architecture: cross-feature event bus uses RxJS `Subject`; one consumer subscribes synchronously on bootstrap, missing first events. Fix. — 25m
309. Architecture: shared modal stack across MFEs results in z-index war. Fix. — 25m
310. Architecture: shared notification queue uses `signal[]` mutated from multiple MFEs — duplicates after browser back. Fix. — 25m
311. Performance: dashboard with 50 widgets, each running its own `httpResource`, exceeding HTTP/2 connection limits. Strategy? — 25m
312. Performance: long task during route nav due to large bundle parse — diagnose + plan a fix. — 25m
313. Performance: pinch-zoom on a map laggy because of layout-affecting CSS — find and fix. — 20m
314. Performance: `ng-content` with `select=[slot=…]` projects 10k items per slot, view init slow. Fix. — 25m
315. Performance: `view-transitions` flashes white during shared-element morph — fix root cause. — 20m
316. Performance: SW caches old API responses while clients expect fresh — design eviction. — 25m
317. Performance: SSR p99 latency 2s due to one slow downstream — strategy? — 25m
318. Performance: CDN cache HIT-with-Vary causes per-user cache fragmentation — fix. — 25m
319. Build: monorepo `nx affected` rebuilds all apps after a one-line change in a deep shared lib. Diagnose. — 20m
320. Build: esbuild chunk dedup leaves stale references after lazy chunk change — fix. — 25m
321. Build: TypeScript project references break `tsc --build --watch` due to circular dep introduced. Fix. — 20m
322. Build: persistent CI cache invalidated every run because of nondeterministic build input — fix. — 20m
323. Build: prerender for 100k routes takes 8h — strategy? — 25m
324. State: collaborative document state diverges between two clients after WS reconnect — fix with sequence numbers. — 30m
325. State: offline queue replays writes after reconnect but server rejects ordering — fix. — 25m
326. State: presence list stale after user closes tab without unload event — fix. — 25m
327. State: signal store reset on logout still has subscribers from old session — fix lifecycle. — 25m
328. State: undo/redo across multi-feature actions breaks because feature B isn't aware of A's snapshot — design. — 25m
329. SSR: streaming SSR — `<head>` appended after stream begins ignored by browser — fix. — 25m
330. SSR: hydration error in a `@defer (hydrate on interaction)` block — recorded interaction lost — diagnose. — 25m
331. SSR: per-request injector instantiates a heavy service every request — memoize? caveat? — 25m
332. SSR: TransferState payload contains PII — design redaction. — 25m
333. SSR: `httpResource` server cache races with client navigation, two outcomes possible — fix. — 25m
334. Routing: shared `RouterOutlet` swaps between two routes, animations conflict with `view-transition` — coordinate. — 25m
335. Routing: deep link to `/orders/:id/items` from email skips auth flow — fix with `CanMatchFn` returning UrlTree. — 20m
336. Routing: per-tenant URL prefix breaks `RouterLink` relative navigation — fix. — 25m
337. Routing: lazy module providers leak across tenants on logout — fix. — 25m
338. Routing: `withViewTransitions` triggers transition on initial navigation, causing FOUC — disable for first nav. — 20m
339. HttpClient: 30k concurrent SSE connections cause backend overload — design backoff and reconnect jitter. — 25m
340. HttpClient: WebSocket library bypasses interceptors — design wrapper. — 25m
341. HttpClient: GraphQL adapter on top of `httpResource` deduplicates queries but breaks tracing IDs. Fix. — 25m
342. HttpClient: file upload chunking races with resumable uploads server, leaving partial uploads — fix. — 25m
343. HttpClient: per-request retries amplify backend load during outage — circuit breaker design. — 25m
344. Signals: glitch observed because two computeds depend on same signal but read in opposite order — fix without breaking memoization. — 25m
345. Signals: `linkedSignal` reset losing local edits — design preserve-on-conflict policy. — 25m
346. Signals: `resource` returns stale value briefly after `reload()` — UX fix? — 20m
347. Signals: `effect()` chain across 5 services causes CD storm — refactor with `computed`. — 25m
348. Signals: cross-store derived state in two stores creates circular dependency — refactor. — 25m
349. Signal Forms: dynamic schema swap mid-edit loses field-level dirty/touched — preserve via migration. — 25m
350. Signal Forms: massive array (5k rows) editable inline — per-keystroke CD storm — fix without losing reactivity. — 25m
351. Signal Forms: conditional sections rendered via `@if` re-mount and reset form state — fix. — 20m
352. Signal Forms: cross-field validation depending on async lookup races itself — fix. — 25m
353. Signal Forms: nested `applyWhen` conditions clash, one rule overrides the other — fix. — 25m
354. Migration: 200-component NgModule app migrating to standalone — schematic crashes on a custom decorator. Fix path. — 25m
355. Migration: Reactive Forms → Signal Forms migration breaks `setValidators` consumers across 50 forms — strategy. — 25m
356. Migration: NgRx classic → signal store migration breaks 30 effect classes — strategy. — 25m
357. Migration: `@angular/animations` → CSS migration leaves 5 cross-route transitions broken — strategy. — 25m
358. Migration: Karma → Vitest migration: 200 tests rely on Jasmine APIs — strategy. — 25m
359. Migration: zoneless rollout breaks 12 third-party libs across 3 features — strategy. — 25m
360. A11y: custom virtual list breaks NVDA scroll due to virtualized DOM. Fix. — 25m
361. A11y: focus jumps to top on every signal update inside a custom listbox. Fix. — 20m
362. A11y: live region announces same message twice when triggered from two stores. Dedupe. — 20m
363. A11y: dialog focus-trap conflicts with browser autofill prompt. Fix. — 25m
364. A11y: tab order broken in RTL layout. Fix. — 25m
365. Security: CSP-strict deployment breaks Angular `<style>` injection — fix without weakening CSP. — 25m
366. Security: Trusted Types policy strips Angular's sanitized HTML — fix. — 25m
367. Security: CSRF token rotated mid-form-submit, second submit fails — fix. — 25m
368. Security: JWT contains tenant claim that drifts after admin change — fix. — 25m
369. Security: WebAuthn re-registration breaks for users with multiple devices — fix. — 25m
370. Real-time: collaborative cursor positions diverge due to WebSocket back-pressure — fix. — 25m
371. Real-time: presence "online" stuck after server restart — fix heartbeat. — 25m
372. Real-time: chat message ordering breaks on reconnect — fix. — 25m
373. Real-time: live transcript loses words on slow client — fix. — 25m
374. Real-time: video grid drops frames after 10 participants — design downgrade strategy. — 25m
375. Observability: traces from FE not joining BE spans due to header drop at CDN — fix. — 25m
376. Observability: session replay records form fields with PII — fix masking. — 25m
377. Observability: error monitoring reports thousands of duplicate errors — design dedup. — 25m
378. Observability: perf metrics show p99 high but median fine — what's the next step? — 20m
379. Observability: heatmap data exfiltrated because of misconfigured analytics — fix. — 25m
380. Deployment: blue/green flip causes Service Worker version skew, users stuck. Fix. — 25m
381. Deployment: canary rollout causes hydration errors for some users due to chunk-version mismatch. Fix. — 25m
382. Deployment: edge SSR cold start spikes after each deploy. Fix. — 25m
383. Deployment: CDN cache busting fails for one region — debug. — 25m
384. Deployment: feature flag rollback causes data inconsistency between FE and BE. Fix. — 25m
385. i18n: locale fallback chain returns wrong key for plural cases — fix. — 25m
386. i18n: RTL switch causes view-transition mirror flicker — fix. — 25m
387. i18n: bundle splitting per locale loads wrong chunk for fallback — fix. — 25m
388. i18n: ICU plural rule for Arabic missing zero case — fix. — 20m
389. i18n: SSR locale negotiation conflicts with cookie-set locale — fix. — 25m
390. PWA: service worker update never applies because of long-lived tabs — fix. — 25m
391. PWA: install prompt fires repeatedly after dismiss — fix. — 25m
392. PWA: notification click loses navigation context — fix. — 25m
393. PWA: background sync runs on wifi but not cellular — fix. — 25m
394. PWA: cache exceeds quota on iOS Safari — fix. — 25m
395. Edge: Cloudflare Worker SSR fails for routes using `Buffer` — fix. — 25m
396. Edge: edge KV cache invalidation lag causes stale page — strategy. — 25m
397. Edge: durable object holds state per room; reconnect chooses different DO — fix sticky routing. — 25m
398. Edge: streaming HTML truncated by intermediate proxy — fix. — 25m
399. Edge: edge functions cold start 500ms ruins LCP — strategy. — 25m
400. Cross-cutting bug bash: app loads, then 2s later 5 different bugs surface simultaneously — outline a triage approach. — 30m

## Legends (401–500)

401. Hand-rolled signal lib has a "diamond" bug — given graph A → B, A → C, D depends on B and C, D fires twice on A.set. Fix the propagation algorithm. — 60m
402. Hand-rolled signal lib emits glitch when computed reads two signals updated in same tick. Identify the missing step. — 60m
403. Hand-rolled `linkedSignal` fails the `previous` argument when source is set to same value — fix dirty tracking. — 60m
404. Hand-rolled `resource` deadlocks when `params` change while loader is awaiting — fix abort semantics. — 60m
405. Custom hydration system replays click events but skips focus events — diagnose buffer policy. — 75m
406. Custom incremental hydration "hydrate on viewport" double-hydrates when element re-enters viewport — fix idempotency. — 60m
407. Custom Router's `CanMatchFn` resolves async but matching engine treats it as sync, falling through. Fix. — 60m
408. Custom Router's `RouteReuseStrategy` caches view but `viewChild` queries return stale `ElementRef`s after re-attach. Fix. — 75m
409. Custom HttpClient backend: cancellation via `AbortController` works for fetch but not when wrapped in `Observable` — fix subscription teardown. — 60m
410. Custom HttpClient backend: interceptor chain ordering breaks when an interceptor re-issues the request — fix loop detection. — 60m
411. Custom Signal Forms: `validateAsync` cancels too aggressively, replacing a valid result with `pending` — fix race. — 75m
412. Custom Signal Forms: `applyEach` over a re-ordered array re-validates wrong items — fix identity tracking. — 75m
413. Custom Signal Forms: schema composition has subtle precedence — last `required(message)` wins, but consumers expect first — fix. — 60m
414. Custom Signal Store: middleware pipeline replays actions on undo but missing side-effect ordering — fix. — 75m
415. Custom Signal Store: entity adapter `upsertMany` mutates input array — fix immutability without doubling memory. — 60m
416. Custom Signal Store: cross-store derived store invalidates on every action regardless of changed slice — fix. — 75m
417. Custom Render Engine: WebGL list virtualization drops frames on scroll-back due to texture rebuild — fix. — 75m
418. Custom Render Engine: Canvas chart leaks contexts after zoom-out — fix. — 60m
419. Custom Render Engine: WebGPU buffer reuse causes visual glitch — fix. — 75m
420. Custom View Transition: shared-element morph between routes drops alpha on Safari — fix. — 60m
421. Custom Compiler: TypeScript transformer that converts `*ngIf` to `@if` mishandles `as` aliases when alias is also a method name. Fix. — 75m
422. Custom Compiler: AST transformer converting `inject()` skips arrow-function class fields. Fix. — 75m
423. Custom Compiler: schematic to convert Reactive Forms to Signal Forms loses async validator wiring. Fix. — 90m
424. Custom Compiler: i18n extractor misses messages inside `@defer` blocks. Fix. — 75m
425. Custom ESLint rule for "no effect-write" yields false positives for `model.set` inside effect. Refine. — 60m
426. Custom MFE shell: shared `@angular/core` between MFE A (v21.2) and MFE B (v21.0) — runtime drift breaks DI. Fix. — 75m
427. Custom MFE shell: SSR streaming combines two MFE streams but `<head>` from MFE B arrives late. Fix. — 75m
428. Custom CRDT: LWW-Element-Set diverges when two clients add the same element with same timestamp — fix tie-breaker. — 75m
429. Custom CRDT: G-Counter overflows on long-lived doc — design pruning. — 60m
430. Custom CRDT: OR-Set "tombstones" grow unbounded — fix compaction. — 75m
431. Custom CRDT: RGA inserts in wrong order after replay — fix ID generation. — 90m
432. Custom Edge SSR: streaming HTML breaks when downstream pre-fetches `</body>` early — fix. — 75m
433. Custom Edge SSR: per-request signals leak via the global signal graph — fix isolation. — 90m
434. Custom Edge SSR: per-request Injector retains references via long-lived `Subject` in module — fix lifecycle. — 75m
435. Custom Edge SSR: Cloudflare KV cache eviction policy causes "thundering herd" on popular routes — fix. — 75m
436. Custom Edge SSR: SSR + AI streaming response — Angular tries to render before stream completes — fix. — 90m
437. Type-level: `Path<T>` recursion hits TS depth limit on 5-level nested types — fix without losing inference. — 60m
438. Type-level: `Get<T, P>` for tuple indices breaks when `P` includes a number literal — fix. — 60m
439. Type-level: `DeepReadonly<T>` distributes over union and loses original union — fix. — 75m
440. Type-level: `UnionToTuple<U>` produces inconsistent order across TS versions — design a stable alternative. — 75m
441. Type-level: branded type `Email = string & { __brand }` is bypassed when consumer uses `Object.assign`. Fix. — 60m
442. Type-level: `EventEmitter<{[K]: P}>` infers `P` as `never` when key is a union — fix variance. — 75m
443. Build: persistent disk cache becomes the bottleneck because hash includes node version — fix without rebuilds. — 60m
444. Build: monorepo `tsc --build` produces `.d.ts` mismatched with `.js` — fix. — 60m
445. Build: tree shaker keeps a side-effectful import declared with `import 'foo/style.css'` — fix without losing styles. — 60m
446. Test: Vitest worker leaks memory in CI when tests share `TestBed` globally — fix isolation. — 75m
447. Test: Playwright flakes on `view-transition` animations — fix without disabling them. — 60m
448. Test: Cypress component test for `httpResource` hangs because of pending tasks — fix. — 60m
449. Test: snapshot test for streaming SSR is non-deterministic due to chunk boundaries. Fix. — 75m
450. Test: a11y axe check passes locally but fails CI due to font load order — fix. — 60m
451. Real-time: collaborative editor desyncs after 30 minutes due to clock drift — fix with logical clocks. — 90m
452. Real-time: video conference drops one participant when 5 join simultaneously — fix race in WebRTC negotiation. — 75m
453. Real-time: presence "follow user" mode loses lock when followee navigates — fix re-acquisition. — 60m
454. Real-time: live cursor smoothing introduces 200ms latency, jittery for fast movements — design adaptive smoothing. — 60m
455. AI integration: LLM streaming response cancelled mid-flight causes inconsistent UI state — fix. — 75m
456. AI integration: tool-use loop fires `inject()` outside DI context — fix without losing streaming. — 75m
457. AI integration: prompt cache miss causes p99 latency spike — strategy. — 75m
458. AI integration: agent loop unbounded after malformed tool response — fix safety. — 75m
459. Compiler RFC: `@defer` block dependencies inferred at build-time fail when dependencies are dynamic. Design fallback. — 75m
460. Compiler RFC: `Type-safe template` (RFC) breaks for `[ngClass]` object literal — design narrowing. — 75m
461. Compiler RFC: `Resumability` design conflicts with `effect()` semantics — reconcile. — 90m
462. Compiler RFC: Server Components analog for Angular streams partial trees — design state hydration. — 90m
463. Framework Author: zoneless mode breaks `Renderer2` when used with third-party libs — design adapter. — 75m
464. Framework Author: signals + RxJS interop double-emit on `toSignal/toObservable` round-trip — fix. — 75m
465. Framework Author: `provideClientHydration` emits warning on every dynamic component — fix without false positives. — 75m
466. Framework Author: `provideRouter(routes, withViewTransitions())` causes a leak when `view-transition` rejected — fix. — 75m
467. Framework Author: incremental hydration of `@defer (hydrate on interaction)` fires before event listeners bound — fix race. — 90m
468. Framework Author: `httpResource` doesn't dedupe across two components reading same URL — design module-level cache. — 75m
469. Framework Author: `[formField]` directive doesn't compose with NG_VALUE_ACCESSOR custom widgets — design adapter. — 90m
470. Framework Author: `signal()` equality `Object.is` defeats array references — design opt-in deep equality without footguns. — 75m
471. Framework Author: `effect()` cleanup order with parent component destroyed first — design ordering. — 75m
472. Framework Author: `viewChild()` returns `undefined` in SSR — design SSR-safe queries. — 75m
473. Framework Author: `@defer (hydrate when isReady())` evaluates `isReady` on server — design SSR contract. — 90m
474. Framework Author: `provideZonelessChangeDetection` breaks tests that use `fakeAsync` — design migration. — 75m
475. Framework Author: `provideAnimationsAsync()` doesn't ship without DOM, breaks SSR — fix. — 75m
476. Cross-runtime: Angular running in Web Worker needs DOM-free `Renderer2` — design. — 90m
477. Cross-runtime: Angular running in Cloudflare Worker hits `node:async_hooks` polyfill — design isolation. — 75m
478. Cross-runtime: Angular running in Deno fails `import.meta` checks — fix. — 60m
479. Cross-runtime: Angular running in Bun differs in `setImmediate` semantics — fix. — 60m
480. Cross-runtime: Angular running in Capacitor fails to receive deep links — design. — 75m
481. Security: prototype pollution via JSON body bypasses Angular's sanitizer in a transitive dep — diagnose and fix. — 75m
482. Security: SSR template injection via untrusted URL param — fix without breaking valid params. — 75m
483. Security: Trusted Types violation in a third-party widget breaks the app on Chrome — design quarantine. — 75m
484. Security: refresh token rotation race causes session loss for half of users — fix. — 75m
485. Security: WebAuthn UV bypass when user has no biometric — design fallback. — 75m
486. Org-scale: 5 teams shipping Angular packages with different v21 minors — design version policy. — 75m
487. Org-scale: design-system v6 breaks 200 consumers — design rollout. — 75m
488. Org-scale: shared validation library used by FE (Signal Forms) and BE (Node) — design contract. — 75m
489. Org-scale: cross-team observability dashboards inconsistent — design unification. — 75m
490. Org-scale: feature-flag system rollout across 50 features — design naming + lifecycle. — 75m
491. Industry-scale: Angular powers 60% of internal apps; design a 5-year roadmap including v22, v23, v24, v25. — 90m
492. Industry-scale: choose Angular vs Next.js for a new product; defend with constraints. — 75m
493. Industry-scale: migrate a 20-year-old AngularJS app to Angular 21 — phased plan. — 90m
494. Industry-scale: merge two SPAs from acquired companies into one Angular 21 monorepo — plan. — 90m
495. Industry-scale: ship a public SDK based on Angular 21 to third-party developers — design. — 90m
496. Industry-scale: enforce SSR + a11y + perf + security across 200 repos automatically — design platform. — 90m
497. Industry-scale: design a private "Angular for our org" wrapper with overrides per team — strategy. — 90m
498. Industry-scale: contribute a feature upstream to Angular — design RFC, PR plan, rollout. — 90m
499. Industry-scale: replace `@angular/forms` legacy entirely with Signal Forms across 1000 forms — plan. — 90m
500. Industry-scale: pitch a single Angular 21 feature whose removal would force a fork — defend or refute. — 90m
