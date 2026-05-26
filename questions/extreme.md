# Extreme — 1000 Questions

Target audience: senior / staff engineers. Budget: **15–30 minutes per question**. System-level design, framework internals, complex perf or migration, and Angular 21-specific deep dives. Answers are not included.

---

## Framework Internals (1–80)

1. Walk through Angular's signal graph: producers, consumers, version counters, dirty flags. Sketch a 4-node graph and trace an update. — 25m
2. Explain how `computed()` achieves glitch-free propagation including the role of the "epoch" or "version". — 25m
3. Reimplement the signals algorithm in ~150 lines: writable, computed, effect, untracked, with cycle detection. — 30m
4. Explain how Angular schedules effects after change detection without microtask races. — 25m
5. Walk through how `linkedSignal` is structurally different from a `computed + signal` pair (state carry-over, source semantics). — 20m
6. Explain how `resource()` represents idle/loading/resolved/error/reloading/local internally; sketch the state machine. — 20m
7. Explain how `resource()` aborts in-flight requests when params change; what guarantees does it provide? — 20m
8. Explain `httpResource` integration with `HttpClient` interceptors and how `TransferState` plugs in. — 25m
9. Walk through Angular's change-detection algorithm in zoneful mode: CheckOnce, Default, OnPush, Detached. — 25m
10. Explain how zoneless CD is scheduled and why no `tick()` storms occur. — 20m
11. Explain how signals integrate with `LView` and dirty propagation in zoneless. — 25m
12. Sketch how `@for` reuses `EmbeddedView`s when items are reordered. — 25m
13. Sketch how `@if` switches active templates and the cost it adds. — 20m
14. Sketch how `@defer` compiles: separate chunk, placeholder, loading/error blocks, triggers. — 25m
15. Explain `@defer (hydrate on X)` compilation differences from `@defer (on X)`. — 20m
16. Explain how `@defer (on viewport)` wires its `IntersectionObserver`. — 15m
17. Explain how `@defer (on interaction)` records its target element and re-binds after hydration. — 20m
18. Explain how `@defer (prefetch on idle)` schedules using `requestIdleCallback` fallback. — 15m
19. Explain how Angular's template engine compiles a component to a render function (Ivy concept). — 25m
20. Explain how `host` metadata compiles into host bindings/listeners. — 20m
21. Explain how `input()` differs from `@Input()` at the AOT-compiled output level. — 20m
22. Explain how `output()` differs from `EventEmitter` at the compiled level. — 20m
23. Explain how `model()` is compiled (input + output pair + binding contract). — 20m
24. Explain how signal queries differ from `QueryList` queries at the runtime level. — 25m
25. Explain how `viewChild()` is populated after view init and how its signal updates. — 20m
26. Sketch the `LView` data structure conceptually. — 25m
27. Explain `TView` and component definitions. — 20m
28. Explain how `ComponentFactory` was replaced by `createComponent()` API. — 15m
29. Explain `ApplicationRef.bootstrap` flow from `bootstrapApplication`. — 25m
30. Explain `EnvironmentInjector` creation chain at bootstrap. — 20m
31. Explain `EnvironmentInjector.destroy()` semantics and resources cleaned up. — 15m
32. Sketch how Angular SSR serializes signal state for hydration. — 25m
33. Explain `TransferState` payload size budgets and SSR trade-offs. — 20m
34. Explain how `provideClientHydration` modifies the SSR HTML output. — 25m
35. Explain `withIncrementalHydration` how it tracks deferred blocks for selective hydration. — 25m
36. Explain how Angular's event replay buffers pre-hydration events. — 20m
37. Explain why event replay is limited to "click/submit/keydown" by default (or current default set). — 15m
38. Explain how `RouterOutlet` participates in CD. — 20m
39. Explain how lazy route loading composes new injectors. — 20m
40. Explain how `withComponentInputBinding` wires URL params into `input()` signals. — 20m
41. Explain how `Router.events` are scheduled vs CD. — 15m
42. Explain `provideExperimentalCheckNoChangesForDebug` and the second-pass CD it performs. — 20m
43. Explain "ExpressionChangedAfterItHasBeenChecked" detection algorithm. — 20m
44. Explain why signals reduce the error rate (immediate vs deferred reads). — 15m
45. Explain how `inject()` resolves up the injector tree. — 20m
46. Explain `EnvironmentInjector` vs `ElementInjector` resolution order. — 20m
47. Explain `@Self`, `@SkipSelf`, `@Host`, `@Optional` resolution semantics. — 20m
48. Explain how `viewProviders` differ from `providers` at the resolution level. — 20m
49. Explain how Angular compiles `<ng-content>` for content projection. — 20m
50. Explain how `select="[slot=foo]"` works at compile time. — 15m
51. Explain how `[formField]` directive integrates with the underlying field state. — 20m
52. Explain how `form()` builds an internal tree of `FieldState` nodes. — 25m
53. Explain `applyEach` codegen and runtime mapping. — 20m
54. Explain `applyWhen` runtime semantics with `valueOf`/`stateOf`. — 20m
55. Explain `validateAsync` lifecycle and integration with `resource`. — 25m
56. Explain `validateHttp` deduplication and cancellation. — 20m
57. Explain `validateStandardSchema` adapter. — 15m
58. Explain how `submit()` traverses the tree to mark all touched. — 15m
59. Explain how `schema()` composition works (re-runs vs merge). — 20m
60. Explain how `metadata()` is stored and retrieved per field. — 15m
61. Explain how `host` metadata's `[class.x]` compiles to a host-binding render op. — 15m
62. Explain how `style.x` host bindings differ from class bindings in render ops. — 15m
63. Explain `ChangeDetectorRef.markForCheck` propagation algorithm. — 20m
64. Explain `ChangeDetectorRef.detach()` and `reattach()` traversal. — 15m
65. Explain `ApplicationRef.attachView` semantics. — 15m
66. Explain how Angular implements `ngTemplateOutlet` context. — 15m
67. Explain how `ngComponentOutlet` swaps components. — 15m
68. Explain how `provideRouter` returns `EnvironmentProviders` and integrates via `withFoo()` features. — 20m
69. Explain how `provideHttpClient(withInterceptors([...]))` builds the interceptor chain. — 20m
70. Explain interceptor ordering: registration vs DI vs execution order. — 15m
71. Explain how `withFetch()` swaps the HTTP backend. — 15m
72. Explain how `HttpClient` cancels via `Subscription.unsubscribe()`. — 15m
73. Explain how `HttpResource` cancels via the resource lifecycle. — 15m
74. Explain how `@for` `track` interacts with `EmbeddedView` reuse. — 20m
75. Explain how `@for` decides to move vs remove+create DOM nodes. — 20m
76. Explain how Angular's template compiler handles `@let`. — 15m
77. Explain how `untracked()` is implemented (consumer-side flag). — 15m
78. Explain how `afterRenderEffect` schedules into phases (read/write/mixed). — 20m
79. Explain `afterNextRender`'s queue and one-shot semantics. — 15m
80. Explain `afterEveryRender`'s cost and use cases. — 15m

## Build, Bundling & Tooling (81–140)

81. Walk through esbuild's role in Angular 21's build. — 20m
82. Walk through Vite's role in `ng serve`. — 20m
83. Explain `application` builder vs `browser-esbuild` builder. — 15m
84. Explain how Angular handles ESM-only dependencies. — 20m
85. Explain `optimizer: { scripts, styles, fonts }`. — 15m
86. Explain how `aot` is compiled in v21 (always-on). — 15m
87. Explain how `outputHashing` produces immutable URLs for caching. — 15m
88. Explain how `assets` are pipelined. — 10m
89. Explain how `polyfills` are computed. — 10m
90. Explain `target` and `module` interaction in `tsconfig`. — 15m
91. Explain `useDefineForClassFields` and decorator interactions. — 20m
92. Explain `experimentalDecorators` and Angular's stance. — 15m
93. Explain "module side-effect tracking" for tree-shaking. — 20m
94. Explain `sideEffects: false` package.json field. — 10m
95. Explain how Angular's runtime ships tree-shakeable. — 15m
96. Explain `provideRouter` tree-shaking benefits over `RouterModule.forRoot`. — 15m
97. Explain how dead-code elimination interacts with `class extends`. — 15m
98. Explain how `@defer` chunks are named and loaded. — 20m
99. Explain how `loadComponent` chunks are named and loaded. — 15m
100. Explain how Angular splits CSS per component. — 15m
101. Explain `inlineCritical` for CSS extraction. — 15m
102. Explain Tailwind's role in build (JIT). — 15m
103. Explain `purge` (deprecated) vs `content` patterns. — 10m
104. Explain "bundle stats" output and CI gates. — 15m
105. Explain `--source-map` modes (`hidden`, `inline`, `eval`). — 15m
106. Explain source-map upload to Sentry as a CI step. — 15m
107. Explain monorepo strategies: Nx vs lerna vs pnpm workspaces. — 20m
108. Explain Nx executors for Angular. — 15m
109. Explain "buildable libraries" vs "publishable libraries". — 15m
110. Explain `nx affected` for Angular monorepos. — 15m
111. Explain incremental builds with esbuild. — 15m
112. Explain "Vite middleware mode" for SSR. — 20m
113. Explain dev SSR vs prod SSR build differences. — 20m
114. Explain how `ng serve --ssr` works. — 15m
115. Explain how Express-based server entrypoint is wired. — 20m
116. Explain `provideServerRendering` providers. — 15m
117. Explain hybrid prerender + on-demand SSR. — 20m
118. Explain `serverRoutes` config compilation. — 15m
119. Explain `RenderMode.Prerender` build-time generation. — 15m
120. Explain `RenderMode.Server` runtime cost. — 15m
121. Explain how to deploy SSR to Cloudflare Workers. — 25m
122. Explain Workers limitations: no `fs`, no native modules. — 15m
123. Explain `node:` import polyfills for Workers. — 15m
124. Explain edge SSR with Vercel/Netlify. — 20m
125. Explain "ISR" (Incremental Static Regeneration) analog with Angular. — 20m
126. Explain CDN cache layering for SSR HTML. — 20m
127. Explain `Vary: Cookie` and personalization caveats. — 15m
128. Explain CSRF with edge SSR. — 15m
129. Explain CSP with edge SSR (nonces). — 15m
130. Explain micro-frontend strategies: module federation vs separate apps. — 25m
131. Explain how to share an Angular library across micro-frontends. — 20m
132. Explain version skew handling across micro-frontends. — 20m
133. Explain shared state across micro-frontends. — 20m
134. Explain cross-MFE routing. — 20m
135. Explain "single-spa" integration with Angular. — 20m
136. Explain "qiankun" integration with Angular. — 20m
137. Explain "Web Components" wrapping for cross-framework. — 20m
138. Explain `@angular/elements` and current state in v21. — 15m
139. Explain Shadow DOM trade-offs for Web Components. — 15m
140. Explain "feature toggles" implemented at build time vs runtime. — 20m

## SSR Architecture (141–220)

141. Design SSR for an editorial site with 100k pages: prerender vs on-demand. — 25m
142. Design SSR for a SaaS dashboard: SSR shell, CSR app. — 25m
143. Design SSR for an e-commerce site: hybrid render modes per route. — 25m
144. Explain "TTFB vs LCP" and SSR trade-offs. — 20m
145. Explain streaming SSR with Angular. — 25m
146. Explain `pendingTasks` and SSR readiness. — 20m
147. Explain `ApplicationRef.isStable` integration with SSR. — 20m
148. Explain SSR error boundaries. — 20m
149. Design an SSR fallback to static for crashes. — 20m
150. Design an SSR cache with per-tenant invalidation. — 25m
151. Design SSR with auth: SSR with cookies vs CSR-only auth. — 25m
152. Explain CSRF in SSR-rendered forms. — 20m
153. Explain SSR with a CDN: caching personalized vs anonymous pages. — 25m
154. Explain "edge rendering" vs "origin rendering". — 20m
155. Explain how to detect bots and skip SSR for them. — 15m
156. Explain how Open Graph tags are set per route under SSR. — 20m
157. Explain "JSON-LD" injection in SSR. — 15m
158. Explain how SSR handles redirects (server-side `301/302`). — 20m
159. Explain hydration of `<form>` elements. — 20m
160. Explain how `[formField]` rehydrates. — 20m
161. Explain hydration with `@defer (hydrate on viewport)`. — 20m
162. Explain hydration with `@defer (hydrate on interaction)`. — 20m
163. Explain hydration error recovery. — 20m
164. Explain SSR and animations (CSS-first wins). — 20m
165. Explain SSR and Tailwind purging. — 15m
166. Explain SSR and code splitting. — 20m
167. Explain SSR + `httpResource` flow with `TransferState`. — 25m
168. Explain SSR + signal store hydration. — 25m
169. Explain SSR + auth cookies + CSRF. — 25m
170. Explain SSR + i18n + locale negotiation. — 25m
171. Explain SSR + analytics (first-party only). — 20m
172. Explain SSR + third-party scripts. — 20m
173. Explain SSR + GDPR consent injection. — 20m
174. Explain SSR + A/B testing with sticky variant. — 25m
175. Explain SSR + dark/light theme negotiation via `Sec-CH-Prefers-Color-Scheme`. — 20m
176. Explain SSR + `viewport` meta tweaks for device. — 15m
177. Explain SSR + critical CSS extraction. — 25m
178. Explain SSR + font preload tuning. — 20m
179. Explain SSR + `Link rel=preload` for JS bundles. — 20m
180. Explain SSR + `Speculation Rules API` integration. — 20m
181. Explain SSR memory growth and per-request injector tear-down. — 25m
182. Explain SSR concurrency limits and back-pressure. — 25m
183. Explain SSR observability: traces per request. — 20m
184. Explain SSR performance budgets and what to alert on. — 20m
185. Explain how SSR interacts with feature flags fetched per-request. — 25m
186. Explain SSR + multi-tenant data routing. — 25m
187. Explain SSR + cookie-based affinity for stateful backends. — 20m
188. Explain SSR + WebSocket bootstrap (defer to client). — 20m
189. Explain SSR + EventSource (SSE). — 20m
190. Explain SSR + Push notifications subscription (CSR-only). — 15m
191. Explain SSR + Service Worker registration timing. — 20m
192. Explain SSR + cache busting for SW updates. — 20m
193. Explain SSR + 404 strategy. — 15m
194. Explain SSR + 500 strategy. — 15m
195. Explain SSR + 503/maintenance pages. — 15m
196. Explain SSR + retries from CDN. — 15m
197. Explain SSR + slow-loris detection. — 15m
198. Explain SSR + request body size limits. — 15m
199. Explain SSR + `Accept-Encoding` negotiation. — 15m
200. Explain SSR + Brotli vs gzip trade-offs. — 15m
201. Explain SSR + image optimization at edge. — 20m
202. Explain SSR + `NgOptimizedImage` integration. — 20m
203. Explain SSR + `loading=lazy` interaction with hydration. — 15m
204. Explain SSR + `fetchpriority` integration. — 15m
205. Explain SSR + `responsive images` strategy. — 20m
206. Explain SSR + `Image CDN` integrations. — 20m
207. Explain SSR + AMP (legacy) considerations. — 15m
208. Explain SSR + RSS feed generation per route. — 15m
209. Explain SSR + sitemap.xml generation. — 20m
210. Explain SSR + robots.txt per environment. — 15m
211. Explain SSR + canonical URL injection. — 15m
212. Explain SSR + `hreflang` for multi-locale SEO. — 15m
213. Explain SSR + Schema.org structured data. — 20m
214. Explain SSR + accessible HTML rendering. — 20m
215. Explain SSR + screen reader announcements on initial load. — 20m
216. Explain SSR + view transitions (server can't run them, client does). — 20m
217. Explain SSR + animation suppression on first paint. — 15m
218. Explain SSR + skeleton rendering. — 20m
219. Explain SSR + lazy stylesheet loading. — 20m
220. Explain SSR + multi-region deployment. — 25m

## Micro-Frontends & Multi-App (221–280)

221. Design a micro-frontend host that loads Angular MFEs and a React MFE. — 30m
222. Design a shared design system MFE consumed by multiple apps. — 25m
223. Explain bundle de-duplication strategies (singleton React/Angular). — 25m
224. Explain version drift mitigation. — 20m
225. Explain how Module Federation handles shared deps. — 20m
226. Explain how to wire Module Federation with Angular's esbuild builder. — 25m
227. Design cross-MFE state sharing via custom events. — 25m
228. Design cross-MFE state sharing via shared store. — 25m
229. Explain SSR for micro-frontends. — 25m
230. Explain auth flow across MFEs. — 25m
231. Explain analytics across MFEs. — 20m
232. Explain CSP per MFE host. — 20m
233. Explain CSS isolation strategies across MFEs. — 25m
234. Explain when Web Components are the right MFE boundary. — 25m
235. Explain when iframes are the right MFE boundary. — 25m
236. Design "monorepo with multiple apps" vs "polyrepo with shared lib". — 25m
237. Explain CI/CD for a 5-app monorepo. — 25m
238. Explain shared lib versioning inside a monorepo. — 20m
239. Explain `nx affected` deeply. — 20m
240. Explain "release please" for Angular libs. — 15m
241. Design a CLI for scaffolding feature modules across apps. — 25m
242. Design a "platform team" library policy. — 20m
243. Explain "API gateway per MFE" pattern. — 20m
244. Explain "BFF (Backend for Frontend)" per MFE. — 25m
245. Design auth between BFF and MFE. — 25m
246. Explain "session cookie at root domain" pitfalls. — 20m
247. Explain SameSite=Lax constraints in MFE scenarios. — 20m
248. Explain "CORS allowlist" management. — 20m
249. Explain "shared HttpClient instance" anti-pattern across MFEs. — 20m
250. Explain shared router (single SPA) vs multiple routers (federation). — 25m
251. Explain "navigation lock" across MFEs. — 20m
252. Explain shared error handler across MFEs. — 20m
253. Explain shared feature flags across MFEs. — 20m
254. Explain shared i18n across MFEs. — 20m
255. Explain shared analytics across MFEs. — 20m
256. Explain shared theme switcher across MFEs. — 20m
257. Explain shared notifications across MFEs. — 20m
258. Explain shared modal stack across MFEs. — 25m
259. Explain shared keyboard shortcuts across MFEs. — 20m
260. Explain MFE testing strategy (contract tests, E2E). — 25m
261. Explain MFE deployment independence and version skew tests. — 20m
262. Explain MFE rollback strategy. — 20m
263. Explain MFE canary deployments. — 20m
264. Explain MFE A/B at host level. — 20m
265. Explain blue/green deploys for MFEs. — 20m
266. Explain MFE observability: trace propagation. — 20m
267. Explain MFE error reporting attribution. — 20m
268. Explain MFE perf monitoring per host vs per MFE. — 20m
269. Explain MFE security boundary considerations. — 20m
270. Explain MFE shared SW (only one). — 20m
271. Explain MFE shared IndexedDB schema strategy. — 20m
272. Explain "team-owned data store" vs "shared store" trade-offs. — 20m
273. Explain MFE shared design tokens. — 20m
274. Explain MFE shared icons (single sprite vs per MFE). — 15m
275. Explain MFE shared fonts. — 15m
276. Explain MFE shared images (CDN). — 15m
277. Explain MFE shared error pages. — 15m
278. Explain MFE shared loading states. — 15m
279. Explain "Single SPA" host + Angular MFE. — 25m
280. Explain "qiankun" + Angular MFE. — 25m

## State Management at Scale (281–360)

281. Design a state architecture for a 5-feature app with 100 services. — 30m
282. Choose: signal store, NgRx classic, Akita, Zustand-style. Justify. — 25m
283. Design entity adapters for normalized state. — 25m
284. Design selectors for cross-entity joins. — 25m
285. Design caching strategy for read endpoints. — 25m
286. Design optimistic updates with rollback. — 25m
287. Design conflict resolution for last-write-wins. — 25m
288. Design CRDT-based collaborative state. — 30m
289. Implement a tiny LWW-Element-Set in TS. — 25m
290. Implement a G-Counter CRDT. — 20m
291. Implement an OR-Set CRDT. — 25m
292. Explain Operational Transformation vs CRDT trade-offs. — 25m
293. Design real-time presence across features. — 25m
294. Design real-time cursors across features. — 25m
295. Design "tab leader election" via Web Locks. — 20m
296. Design cross-tab state sync via BroadcastChannel. — 20m
297. Design cross-tab leader for WS connection (one socket per browser). — 25m
298. Design offline-first writes with sync. — 25m
299. Design IndexedDB schema for offline queue. — 25m
300. Design Service Worker sync for offline queue. — 25m
301. Design conflict detection on sync. — 25m
302. Design "outbox" pattern in IndexedDB. — 25m
303. Design "inbox" pattern for server pushes. — 25m
304. Design optimistic local state vs server state divergence. — 25m
305. Design "delta sync" with timestamps. — 25m
306. Design "page-level cache invalidation" on data write. — 25m
307. Design "memo trees" for derived state. — 25m
308. Design "selector memoization" with parameterization. — 25m
309. Design "store splits per feature". — 20m
310. Design "store composition" at root. — 20m
311. Design "store hydration from SSR". — 25m
312. Design "store rehydration on tab restore". — 25m
313. Design "store middleware pipeline". — 25m
314. Design "logger middleware" with redaction. — 20m
315. Design "throttle middleware" for high-frequency actions. — 20m
316. Design "persistence middleware" with whitelist. — 20m
317. Design "undo/redo middleware" with capped history. — 25m
318. Design "action audit middleware" for compliance. — 20m
319. Design "feature flag-aware reducer". — 20m
320. Design "feature flag-aware selectors". — 20m
321. Design "store for collaborative cursor". — 25m
322. Design "store for offline doc edits". — 25m
323. Design "store for chat messages with optimistic send". — 25m
324. Design "store for notification queue". — 25m
325. Design "store for analytics events". — 20m
326. Design "store for permissions tree". — 25m
327. Design "store for user prefs sync across tabs". — 25m
328. Design "store for shopping cart with offline support". — 30m
329. Design "store for checkout flow with idempotency". — 30m
330. Design "store for multi-step form with autosave". — 25m
331. Design "store for live dashboard with refresh". — 25m
332. Design "store for editor with collaborative cursors". — 30m
333. Design "store for video chat presence". — 30m
334. Design "store for code editor with multi-cursor". — 30m
335. Design "store for spreadsheet with formulas". — 30m
336. Design "store for whiteboard with shapes + multi-user". — 30m
337. Design "store for game state with rollback netcode". — 30m
338. Design "store for trading orderbook updates". — 30m
339. Design "store for IoT telemetry feeds". — 25m
340. Design "store for live ride tracking (map)". — 25m
341. Design "store for collaborative todo list". — 25m
342. Design "store for live polling votes". — 25m
343. Design "store for newsfeed with infinite scroll". — 25m
344. Design "store for chat room list". — 25m
345. Design "store for nested comments tree". — 25m
346. Design "store for nested folder structure". — 25m
347. Design "store for kanban board with drag-and-drop". — 25m
348. Design "store for calendar with events". — 25m
349. Design "store for scheduling with conflicts". — 25m
350. Design "store for booking with availability". — 25m
351. Design "store for inventory with low-stock alerts". — 25m
352. Design "store for shipping tracker". — 20m
353. Design "store for invoicing/billing". — 25m
354. Design "store for subscription management". — 25m
355. Design "store for user impersonation". — 20m
356. Design "store for audit logs". — 25m
357. Design "store for permissions matrix". — 25m
358. Design "store for activity timeline". — 25m
359. Design "store for search history with TTL". — 20m
360. Design "store for analytics insights cache". — 25m

## TypeScript Type-Level Programming (361–440)

361. Implement `MergeDeep<A, B>` mapped/conditional type. — 25m
362. Implement `Diff<A, B>` returning differences. — 20m
363. Implement `Equal<A, B>` boolean type. — 20m
364. Implement `Expect<true>` and `ExpectExtends<A, B>` test helpers. — 15m
365. Implement `UnionToTuple<U>` and explain why it's unstable. — 25m
366. Implement `IsTuple<T>` type. — 15m
367. Implement `TupleLength<T>` type. — 15m
368. Implement `Reverse<T extends any[]>`. — 20m
369. Implement `Last<T>` for tuples. — 15m
370. Implement `Drop<T, N>` removing N elements. — 20m
371. Implement `Take<T, N>` taking N elements. — 20m
372. Implement `Range<From, To>` returning literal union. — 25m
373. Implement `Repeat<T, N>` returning tuple. — 20m
374. Implement `Zip<A, B>` tuple zipping. — 20m
375. Implement `Flatten<T>` (1-level). — 15m
376. Implement `DeepFlatten<T>`. — 25m
377. Implement `Path<T>` for object path strings. — 25m
378. Implement `Get<T, P>` for path resolution. — 25m
379. Implement `Set<T, P, V>` returning a modified T. — 25m
380. Implement `Has<T, K>` keyof check. — 15m
381. Implement `MutableKeys<T>`. — 20m
382. Implement `ReadonlyKeys<T>`. — 20m
383. Implement `RequiredKeys<T>`. — 20m
384. Implement `OptionalKeys<T>`. — 20m
385. Implement `DeepPartial<T>` with array support. — 20m
386. Implement `DeepRequired<T>` with array support. — 20m
387. Implement `DeepReadonly<T>` with Map/Set support. — 25m
388. Implement `DeepMutable<T>`. — 25m
389. Implement `PromiseValue<T>` extracting `T` from `Promise<T>`. — 15m
390. Implement `Resolve<T>` to flatten intersection display. — 15m
391. Implement `Prettify<T>` (display helper). — 15m
392. Implement `Branded<T, B>` and `unbrand`. — 20m
393. Implement `Nominal<T, B>` with phantom. — 20m
394. Implement `ParseInt<S>` template literal type. — 25m
395. Implement `ParseFloat<S>`. — 25m
396. Implement `Add<A, B>` for small numbers. — 25m
397. Implement `Subtract<A, B>` for small numbers. — 25m
398. Implement `Multiply<A, B>` for small numbers. — 25m
399. Implement `Divide<A, B>` for small numbers. — 25m
400. Implement `GreaterThan<A, B>` type. — 25m
401. Implement `LessThan<A, B>` type. — 25m
402. Implement `Compare<A, B>` returning `'lt' | 'eq' | 'gt'`. — 25m
403. Implement `Sum<T extends number[]>`. — 25m
404. Implement `Product<T extends number[]>`. — 25m
405. Implement `Max<T>` over tuple. — 25m
406. Implement `Min<T>` over tuple. — 25m
407. Implement `Sort<T>` over tuple of numbers. — 30m
408. Implement `Unique<T>` over tuple. — 25m
409. Implement `IndexOf<T, X>` returning index or -1. — 20m
410. Implement `Includes<T, X>`. — 20m
411. Implement `Count<T, X>` occurrences. — 20m
412. Implement `Replace<T, From, To>` over tuple. — 20m
413. Implement `Map<T, F>` over tuple. — 25m
414. Implement `Filter<T, P>` over tuple. — 25m
415. Implement `Reduce<T, F, Init>` over tuple. — 30m
416. Implement `Chunk<T, N>` over tuple. — 25m
417. Implement `GroupBy<T, K>` over tuple. — 25m
418. Implement `Permutations<U>` of a union. — 30m
419. Implement `Combinations<U, K>`. — 30m
420. Implement `Subsets<U>`. — 25m
421. Implement `Powerset<U>`. — 25m
422. Implement `Capitalize<S>` template literal. — 15m
423. Implement `Uncapitalize<S>`. — 15m
424. Implement `Snake<S>` to snake_case. — 25m
425. Implement `Kebab<S>` to kebab-case. — 25m
426. Implement `Camel<S>` from snake_case. — 25m
427. Implement `Pascal<S>` from snake_case. — 25m
428. Implement `Title<S>` (each word capitalized). — 20m
429. Implement `Trim<S>` removing leading/trailing whitespace. — 20m
430. Implement `Split<S, Sep>` template literal. — 25m
431. Implement `Join<T, Sep>` template literal. — 25m
432. Implement `Replace<S, From, To>` template literal. — 20m
433. Implement `StartsWith<S, P>`. — 15m
434. Implement `EndsWith<S, P>`. — 15m
435. Implement `Contains<S, P>`. — 15m
436. Implement `EvalExpr<S>` for a small expression DSL. — 30m
437. Implement `ParseRoute<S>` to extract params. — 25m
438. Implement `MatchRoute<R, U>` to match a URL. — 30m
439. Implement `BuildUrl<R, P>` to construct URL from params. — 25m
440. Implement `SQLToType<S>` (simple `CREATE TABLE` parser). — 30m

## Performance at Scale (441–520)

441. Diagnose a 10MB JS bundle: walk through investigation. — 25m
442. Diagnose 5s LCP on a SSR page. — 25m
443. Diagnose poor INP after hydration. — 25m
444. Diagnose CLS from late-loading fonts. — 20m
445. Diagnose CLS from late-loading images. — 20m
446. Diagnose CLS from late-loading third-party widgets. — 20m
447. Diagnose CLS from animated headers. — 20m
448. Diagnose long-tasks > 200ms after hydration. — 25m
449. Diagnose memory growth after 30 minutes of use. — 25m
450. Diagnose memory leak from `effect()`. — 20m
451. Diagnose memory leak from `subscribe()`. — 20m
452. Diagnose memory leak from `setInterval`. — 20m
453. Diagnose memory leak from `IntersectionObserver`. — 20m
454. Diagnose memory leak from `ResizeObserver`. — 20m
455. Diagnose memory leak from event listeners on document. — 20m
456. Diagnose CPU pegged at 100% during scroll. — 25m
457. Diagnose jank in a complex form on key press. — 25m
458. Diagnose jank in a long list on selection. — 25m
459. Diagnose jank in a chart on data update. — 25m
460. Diagnose jank in `view-transitions` on route change. — 25m
461. Diagnose slow startup on low-end devices. — 25m
462. Diagnose slow startup on slow 3G. — 25m
463. Diagnose poor TTI on first navigation. — 25m
464. Diagnose poor FCP on prerendered routes. — 25m
465. Diagnose flicker on hydration. — 20m
466. Diagnose layout shift on hydration. — 20m
467. Diagnose double network request on hydration. — 20m
468. Diagnose duplicate work on SSR + CSR boundary. — 25m
469. Diagnose `httpResource` re-fetch on hydration. — 20m
470. Diagnose chunk waterfall in network panel. — 25m
471. Diagnose blocking script in `<head>`. — 20m
472. Diagnose render-blocking CSS. — 20m
473. Diagnose third-party iframe blocking main thread. — 20m
474. Diagnose poor performance from `:has(...)` selectors. — 20m
475. Diagnose poor performance from `@property` animations. — 20m
476. Diagnose poor performance from `box-shadow` on scroll. — 20m
477. Diagnose poor performance from `filter: blur()` on scroll. — 20m
478. Diagnose poor performance from too many CSS variables. — 20m
479. Diagnose poor performance from large `<svg>` inline. — 20m
480. Diagnose poor performance from large `<table>`. — 20m
481. Implement virtualization for a 100k-row table. — 30m
482. Implement chunked rendering for a 10k-item list. — 25m
483. Implement off-main-thread CSV parsing. — 25m
484. Implement off-main-thread image decoding. — 25m
485. Implement off-main-thread JSON parsing for huge payloads. — 25m
486. Implement a worker pool for parallel image processing. — 30m
487. Implement `OffscreenCanvas` for chart rendering. — 25m
488. Implement `OffscreenCanvas` for video frame analysis. — 25m
489. Implement `WebGPU` for big data viz (high-level). — 30m
490. Implement code-splitting at the route level with strategic preloads. — 25m
491. Implement `@defer` for below-the-fold content. — 25m
492. Implement `@defer (hydrate on viewport)` for late hydration. — 25m
493. Implement adaptive serving based on `navigator.connection.effectiveType`. — 25m
494. Implement save-data mode: skip heavy assets. — 20m
495. Implement priority hints for hero image. — 20m
496. Implement reduced motion bundle pruning. — 20m
497. Implement i18n bundle pruning per locale. — 20m
498. Implement CSS pruning per route. — 25m
499. Implement font subsetting for primary glyphs. — 25m
500. Implement font preconnect + preload. — 20m
501. Implement DNS prefetch and `Speculation Rules`. — 20m
502. Implement preload of next route during idle. — 25m
503. Implement prerender via `Speculation Rules API`. — 25m
504. Implement `bfcache` compatibility. — 20m
505. Implement bfcache-safe service worker. — 20m
506. Implement bfcache-safe WebSocket. — 20m
507. Implement bfcache-safe `unload` avoidance. — 20m
508. Implement service-worker precaching with versioning. — 25m
509. Implement service-worker runtime caching strategies. — 25m
510. Implement stale-while-revalidate strategy. — 25m
511. Implement cache-first for static assets. — 20m
512. Implement network-first for HTML. — 20m
513. Implement background sync for offline writes. — 25m
514. Implement periodic background sync. — 25m
515. Implement push notifications. — 25m
516. Implement notification click → route. — 20m
517. Implement notification grouping. — 20m
518. Implement notification quiet hours. — 20m
519. Implement notification opt-in UX. — 20m
520. Implement notification opt-out UX. — 20m

## Real-Time & Collaborative Apps (521–580)

521. Design a real-time collaborative document editor. — 30m
522. Choose CRDT vs OT and justify. — 25m
523. Design presence (who's online). — 25m
524. Design cursor sharing across users. — 25m
525. Design selection sharing across users. — 25m
526. Design "follow user" mode. — 25m
527. Design "session recording" for replay. — 25m
528. Design "comments" anchored to selections. — 25m
529. Design "version history" with branching. — 30m
530. Design "merge conflicts" UI. — 25m
531. Design "offline edits" reconciliation. — 25m
532. Design "operations log" sync. — 25m
533. Design "snapshots" + "deltas" sync. — 25m
534. Design "back-pressure" on slow clients. — 25m
535. Design "spam protection" for collab. — 20m
536. Design "rate limiting" for cursor updates. — 20m
537. Design "presence heartbeats". — 20m
538. Design "TTL" for stale cursors. — 20m
539. Design "user color assignment" stable across sessions. — 20m
540. Design "permissions" per document. — 25m
541. Design "real-time chat" inside the doc. — 25m
542. Design "notifications" for mentions. — 25m
543. Design "shareable links" with permissions. — 25m
544. Design "anonymous viewers". — 20m
545. Design "guest editors". — 25m
546. Design "video call inside doc". — 30m
547. Design "screen share" UX. — 25m
548. Design "annotations on video frames". — 25m
549. Design "live transcription". — 25m
550. Design "live translation". — 25m
551. Design "real-time dashboards" with incoming events. — 25m
552. Design "live sports score" widget. — 20m
553. Design "stock ticker" with real-time updates. — 25m
554. Design "auction" with live bids. — 25m
555. Design "live poll" with results. — 20m
556. Design "live Q&A" with upvotes. — 25m
557. Design "live whiteboard" with shapes + multi-user. — 30m
558. Design "live spreadsheet" with formulas. — 30m
559. Design "live kanban" with cards + drag. — 30m
560. Design "live map" with moving entities. — 30m
561. Design "live game lobby". — 25m
562. Design "live game match" netcode. — 30m
563. Design "spectator mode". — 25m
564. Design "live trading view" with order book. — 30m
565. Design "live chat moderation". — 25m
566. Design "live show with reactions". — 25m
567. Design "live shopping with viewers". — 25m
568. Design "live music sync". — 25m
569. Design "live video sync (watch party)". — 25m
570. Design "live podcast room". — 25m
571. Design WS reconnection backoff. — 20m
572. Design WS subscription resume. — 20m
573. Design WS message ordering guarantees. — 25m
574. Design WS message dedup. — 20m
575. Design WS auth token rotation. — 25m
576. Design WS heartbeat protocol. — 20m
577. Design WS multiplexing channels. — 25m
578. Design WS fallback to long-polling. — 25m
579. Design SSE for read-only streams. — 25m
580. Design webhook → push notification pipeline. — 25m

## Animation & View Transitions Deep (581–630)

581. Implement a FLIP animation for list reorder. — 25m
582. Implement a `view-transition`-based list reorder. — 25m
583. Implement a "shared element" view transition for list → detail. — 25m
584. Implement a route fade with `withViewTransitions`. — 20m
585. Implement a route slide with `withViewTransitions`. — 25m
586. Implement scroll-driven animation with `animation-timeline`. — 25m
587. Implement parallax with `animation-timeline: scroll()`. — 25m
588. Implement "sticky header that morphs on scroll". — 25m
589. Implement an animated tab indicator that slides. — 20m
590. Implement an animated drawer with backdrop fade. — 20m
591. Implement an animated modal with content scale. — 20m
592. Implement an accordion with smooth `height: auto` via animation. — 25m
593. Implement `transition-behavior: allow-discrete` for `display:none`. — 20m
594. Implement an animated tooltip with collision detection. — 25m
595. Implement an animated popover that respects anchor. — 25m
596. Implement a "carousel" with snap + transitions. — 25m
597. Implement a "stepper" with animated transitions. — 25m
598. Implement an animated stepper progress bar. — 20m
599. Implement an animated chart redraw. — 25m
600. Implement a typewriter effect. — 20m
601. Implement a count-up number. — 20m
602. Implement a shake-on-error input. — 15m
603. Implement a confetti burst on success. — 20m
604. Implement a fireworks burst on milestone. — 25m
605. Implement page-load fade-in. — 15m
606. Implement page-unload fade-out. — 15m
607. Implement route preloading visualization. — 20m
608. Implement skeleton-to-content cross-fade. — 25m
609. Implement a "shimmer" skeleton. — 20m
610. Implement reduced-motion variants for all of the above. — 25m
611. Implement a "draggable list" with FLIP. — 25m
612. Implement "swipe to delete" with rubber-band. — 25m
613. Implement "long-press to enter selection mode". — 25m
614. Implement "drag to reorder" with FLIP. — 25m
615. Implement "drag between lists" with FLIP. — 25m
616. Implement "pinch-zoom" image viewer. — 25m
617. Implement "pull-to-refresh" with animation. — 25m
618. Implement "swipe between pages" gesture. — 25m
619. Implement "spring physics" via Web Animations. — 25m
620. Implement "magnetic snap" between elements. — 25m
621. Implement "live preview" of style changes. — 20m
622. Implement "ghost element" for drag. — 25m
623. Implement "drop preview" highlight. — 25m
624. Implement "drag handle" affordance with hover state. — 20m
625. Implement "snapping grid" for dropped items. — 25m
626. Implement "auto-scroll on drag near edge". — 25m
627. Implement "keyboard reorder" alternative to drag. — 25m
628. Implement "announce reorder" via `aria-live`. — 20m
629. Implement "undo reorder" with toast. — 20m
630. Implement "redo reorder". — 20m

## Internationalization & Localization (631–670)

631. Design an i18n strategy for 20 locales. — 25m
632. Design RTL support for an existing app. — 25m
633. Design pluralization for complex languages (Russian, Arabic). — 25m
634. Design currency display per locale. — 20m
635. Design date display per locale. — 20m
636. Design number formatting per locale. — 20m
637. Design relative time per locale. — 20m
638. Design list formatting per locale. — 15m
639. Design name formatting per locale. — 15m
640. Design address formatting per locale. — 20m
641. Design phone formatting per locale. — 20m
642. Design ICU message format usage in templates. — 25m
643. Design "missing translation" handling. — 20m
644. Design translation extraction CI workflow. — 25m
645. Design "translate this page" UX. — 20m
646. Design "translation memory" reuse. — 25m
647. Design "translation review" workflow. — 25m
648. Design "in-context translation" overlay. — 25m
649. Design "machine translation" fallback. — 25m
650. Design "locale negotiation" SSR-side. — 25m
651. Design "locale switcher" UX. — 20m
652. Design "URL locale prefix" routing. — 25m
653. Design "hreflang" tags per route. — 20m
654. Design "language fallback chain". — 20m
655. Design "RTL CSS via logical properties". — 25m
656. Design "icons that need flipping in RTL". — 20m
657. Design "image variants per locale". — 20m
658. Design "font subset per locale". — 25m
659. Design "input methods per locale" (IME). — 25m
660. Design "spellcheck per locale". — 15m
661. Design "currency conversion" with cached rates. — 25m
662. Design "time zone display" with user preference. — 25m
663. Design "calendar systems" (Gregorian/Hijri/Hebrew). — 25m
664. Design "first day of week" per locale. — 15m
665. Design "weekend days" per locale. — 15m
666. Design "holiday calendar" per locale. — 20m
667. Design "i18n a11y" considerations. — 20m
668. Design "i18n SEO" considerations. — 25m
669. Design "i18n analytics" with locale dimension. — 20m
670. Design "i18n A/B testing" with locale matching. — 25m

## Security Architecture (671–720)

671. Threat-model a typical Angular SPA. — 25m
672. Design CSP for an Angular SPA + SSR. — 25m
673. Design Trusted Types policy + Angular integration. — 25m
674. Design auth: cookie + CSRF vs Bearer + JWT. — 25m
675. Design refresh token rotation safely. — 25m
676. Design token theft mitigation (rotation + revocation). — 25m
677. Design "device-bound session" with Web Authentication API. — 25m
678. Design "passkeys" sign-in flow. — 25m
679. Design "social login" integration safely. — 25m
680. Design "magic link" login. — 25m
681. Design "phone OTP" login. — 25m
682. Design "TOTP" 2FA. — 25m
683. Design "WebAuthn" 2FA. — 25m
684. Design "session timeout" with grace warnings. — 20m
685. Design "concurrent session limits". — 20m
686. Design "session lock" after inactivity. — 20m
687. Design "audit logs" for security events. — 20m
688. Design "permissions" enforcement client + server. — 25m
689. Design "data minimization" in cache layers. — 20m
690. Design "PII redaction" in logs/telemetry. — 20m
691. Design "GDPR delete me" UX. — 25m
692. Design "GDPR export my data" UX. — 25m
693. Design "consent banner" with re-prompt. — 25m
694. Design "cookie inventory" disclosure. — 20m
695. Design "third-party script" review process. — 20m
696. Design "supply chain attack" prevention (lockfiles, SRI). — 25m
697. Design "secret management" (no secrets in bundle). — 25m
698. Design "env-var injection" at build time safely. — 20m
699. Design "feature flag values" as non-sensitive. — 20m
700. Design "DOM clobbering" prevention. — 20m
701. Design "JSON hijacking" prevention. — 20m
702. Design "open redirect" prevention. — 20m
703. Design "iframe sandbox" pattern. — 20m
704. Design "embed allowlist" for partner sites. — 25m
705. Design "CSRF for SPAs" properly. — 25m
706. Design "XSS audits" via automated tests. — 25m
707. Design "ZAP/Burp" integration in CI. — 25m
708. Design "security headers" baseline. — 20m
709. Design "HSTS preload" considerations. — 15m
710. Design "Subresource Integrity" for CDN scripts. — 20m
711. Design "Permissions Policy" defaults. — 20m
712. Design "Referrer Policy" defaults. — 15m
713. Design "Cross-Origin-Opener-Policy" + COEP. — 25m
714. Design "SharedArrayBuffer" enabling safely (COOP/COEP). — 25m
715. Design "rate limiting" client signals to backend. — 20m
716. Design "request signing" client-side. — 25m
717. Design "Web Crypto API" usage for client encryption. — 25m
718. Design "E2E encryption" UX for chat. — 25m
719. Design "key escrow" UX. — 25m
720. Design "audit a third-party script" workflow. — 20m

## Testing Strategy at Scale (721–780)

721. Design test pyramid for a 100-component app. — 25m
722. Design unit/integration/E2E split rationale. — 25m
723. Design Vitest config for a monorepo. — 25m
724. Design "smoke tests" run on every deploy. — 20m
725. Design "regression suite" run nightly. — 20m
726. Design "perf budget tests" with Lighthouse CI. — 25m
727. Design "a11y tests" with axe in CI. — 25m
728. Design "visual regression" with Chromatic/Percy. — 25m
729. Design "contract tests" between FE and BE. — 25m
730. Design "MSW-based" integration tests. — 25m
731. Design "Playwright" E2E suite organization. — 25m
732. Design "test data factories" for shared fixtures. — 20m
733. Design "deterministic timestamps" for tests. — 20m
734. Design "test environment per PR" preview deploy. — 25m
735. Design "flaky test detection" pipeline. — 25m
736. Design "flaky test quarantine" workflow. — 25m
737. Design "mutation testing" rollout. — 25m
738. Design "test sharding" for fast CI. — 20m
739. Design "test parallelism" with deterministic seeds. — 20m
740. Design "test isolation" for global state. — 25m
741. Design "DI override patterns" for tests. — 25m
742. Design "harness library" per design system. — 25m
743. Design "router test patterns". — 20m
744. Design "interceptor test patterns". — 20m
745. Design "signal store test patterns". — 20m
746. Design "Signal Form test patterns". — 25m
747. Design "SSR test patterns". — 25m
748. Design "hydration test patterns". — 25m
749. Design "view transition test patterns". — 25m
750. Design "real-time test patterns" (WS, SSE). — 25m
751. Design "service worker test patterns". — 25m
752. Design "PWA install flow tests". — 20m
753. Design "offline mode tests". — 25m
754. Design "background sync tests". — 25m
755. Design "performance regression tests". — 25m
756. Design "load tests for SSR". — 25m
757. Design "chaos tests" for SSR cache. — 25m
758. Design "browser matrix" tests. — 20m
759. Design "mobile viewport tests". — 20m
760. Design "RTL layout tests". — 25m
761. Design "screen reader tests" (NVDA/VoiceOver). — 25m
762. Design "i18n tests" per locale. — 25m
763. Design "permissions tests" per role. — 25m
764. Design "feature flag tests" per variant. — 25m
765. Design "data migration tests". — 25m
766. Design "backwards-compat tests" for APIs. — 25m
767. Design "schema validation tests" for Signal Forms. — 25m
768. Design "fuzz tests" for form inputs. — 25m
769. Design "property-based tests" for state machines. — 25m
770. Design "snapshot tests" for component output. — 20m
771. Design "golden master tests" for complex outputs. — 25m
772. Design "approval tests" workflow. — 20m
773. Design "test coverage targets" per module. — 20m
774. Design "coverage" as a CI gate. — 20m
775. Design "test taxonomy" for triage. — 20m
776. Design "ownership" per test suite. — 20m
777. Design "test report dashboards". — 20m
778. Design "test analytics" for slowest tests. — 20m
779. Design "test analytics" for flakiest tests. — 20m
780. Design "AI-generated tests" review workflow. — 25m

## Forms at Scale (781–840)

781. Design a 50-section enterprise form using Signal Forms. — 30m
782. Design a "form spec" config that drives UI + validation. — 30m
783. Design "form versioning" for backward compat. — 25m
784. Design "form migration" between versions. — 25m
785. Design "form A/B testing" per variant. — 25m
786. Design "form analytics" (field abandonment). — 25m
787. Design "field-level autosave". — 25m
788. Design "form-level autosave". — 25m
789. Design "draft management" UI. — 25m
790. Design "draft conflict resolution". — 25m
791. Design "multi-tab editing" of same form. — 25m
792. Design "real-time co-editing" of same form. — 30m
793. Design "form snapshots" for undo. — 25m
794. Design "form audit logs" for compliance. — 25m
795. Design "form e-signature" integration. — 30m
796. Design "form workflows" (approval chains). — 30m
797. Design "form templates" reusable across features. — 25m
798. Design "form preview" before submit. — 25m
799. Design "form print" (PDF export). — 25m
800. Design "form clone" workflow. — 20m
801. Design "form rules engine" for conditional logic. — 30m
802. Design "form pricing engine" with live calc. — 30m
803. Design "form upload" with chunking. — 30m
804. Design "form upload" with resume. — 30m
805. Design "form upload" with virus scan. — 25m
806. Design "form attachments" management. — 25m
807. Design "form signatures" capture. — 25m
808. Design "form GPS capture" with permission. — 25m
809. Design "form camera capture". — 25m
810. Design "form barcode scan". — 25m
811. Design "form NFC scan". — 20m
812. Design "form QR scan". — 25m
813. Design "form OCR" client-side. — 25m
814. Design "form voice input". — 25m
815. Design "form handwriting input". — 25m
816. Design "form locale-aware inputs". — 25m
817. Design "form currency inputs". — 20m
818. Design "form date pickers" with TZ awareness. — 25m
819. Design "form duration inputs". — 20m
820. Design "form recurrence inputs" (RRULE). — 25m
821. Design "form address autocomplete". — 25m
822. Design "form geolocation pickers". — 25m
823. Design "form map pickers". — 25m
824. Design "form image pickers". — 25m
825. Design "form file pickers". — 25m
826. Design "form chips/tags". — 25m
827. Design "form rich text". — 30m
828. Design "form code editor". — 30m
829. Design "form table editing". — 30m
830. Design "form spreadsheet editing". — 30m
831. Design "form charts inline". — 25m
832. Design "form repeater groups". — 25m
833. Design "form wizard with branching". — 30m
834. Design "form review summary". — 25m
835. Design "form submit + redirect" pattern. — 20m
836. Design "form submit + stay" pattern. — 20m
837. Design "form submit + next" pattern. — 20m
838. Design "form submit + share" pattern. — 20m
839. Design "form recovery from crash". — 25m
840. Design "form metrics" (time to submit, error rate). — 25m

## Routing Architecture (841–900)

841. Design routing for a 100-route app. — 25m
842. Design "lazy-load tree" per business area. — 25m
843. Design "shared layout per area". — 25m
844. Design "drawer layout vs full layout per route". — 25m
845. Design "auth-required routes" globally. — 25m
846. Design "role-gated routes". — 25m
847. Design "feature-flag-gated routes". — 25m
848. Design "tenant-aware routes". — 25m
849. Design "tenant routing" (subdomain vs path). — 25m
850. Design "i18n routing" (locale prefix). — 25m
851. Design "SSR routing config". — 25m
852. Design "static routes" via prerender. — 25m
853. Design "server routes" with personalization. — 25m
854. Design "edge routes". — 25m
855. Design "preloading per area". — 25m
856. Design "preloading per role". — 25m
857. Design "preloading per connection". — 25m
858. Design "navigation lock during save". — 25m
859. Design "unsaved changes prompt" via guard. — 25m
860. Design "title strategy" with locale. — 20m
861. Design "meta strategy" per route. — 25m
862. Design "canonical URL" per route. — 20m
863. Design "deep linking" per feature. — 25m
864. Design "shareable links" with state. — 25m
865. Design "back-button-friendly modal" pattern. — 25m
866. Design "back-button-friendly drawer" pattern. — 25m
867. Design "wizards with browser back". — 25m
868. Design "wizards with route per step". — 25m
869. Design "wizards with single route + query". — 25m
870. Design "single-page nested tabs" via child routes. — 25m
871. Design "auxiliary outlets" for side panels. — 25m
872. Design "named outlets" for modals. — 25m
873. Design "stacked navigation" pattern. — 25m
874. Design "iOS-style swipe back". — 25m
875. Design "Android-style up/back". — 25m
876. Design "scroll restoration" per route. — 25m
877. Design "scroll to anchor" pattern. — 20m
878. Design "scroll preservation on tab switch". — 25m
879. Design "URL state vs store state" boundary. — 25m
880. Design "URL filters" pattern. — 25m
881. Design "URL search" pattern. — 25m
882. Design "URL pagination" pattern. — 25m
883. Design "URL sort" pattern. — 25m
884. Design "URL pre-filter from referrer". — 25m
885. Design "URL pre-filter from cookie". — 25m
886. Design "URL pre-filter from saved view". — 25m
887. Design "navigation analytics" pipeline. — 25m
888. Design "route-level error pages". — 25m
889. Design "route-level loading states". — 25m
890. Design "route-level skeletons". — 25m
891. Design "route-level error boundaries". — 25m
892. Design "retry on navigation error". — 25m
893. Design "fallback to cached route". — 25m
894. Design "graceful 404" pages. — 20m
895. Design "graceful 500" pages. — 20m
896. Design "graceful 503" pages. — 20m
897. Design "graceful offline" pages. — 25m
898. Design "graceful slow" UX. — 25m
899. Design "navigation breadcrumb" from route tree. — 25m
900. Design "navigation drawer" reactive to route. — 25m

## DevOps, Monitoring & Migration (901–1000)

901. Design CI/CD pipeline for Angular 21 app. — 25m
902. Design "preview deploy per PR". — 25m
903. Design "feature flag gates" tied to PRs. — 25m
904. Design "rollback procedure" with one click. — 25m
905. Design "blue/green deploy" for SSR. — 25m
906. Design "canary deploy" for SSR. — 25m
907. Design "progressive rollout" via flags. — 25m
908. Design "kill switch" for emergencies. — 20m
909. Design "incident response" runbook for prod. — 25m
910. Design "post-mortem template". — 20m
911. Design "alerting" thresholds for FE. — 25m
912. Design "error budget" per feature. — 25m
913. Design "SLI/SLO" for FE perf. — 25m
914. Design "RUM" pipeline. — 25m
915. Design "synthetic monitoring" pipeline. — 25m
916. Design "uptime checks" for SSR. — 20m
917. Design "log shipping" for SSR errors. — 25m
918. Design "metrics shipping" for FE perf. — 25m
919. Design "trace propagation" FE → BE. — 25m
920. Design "trace sampling" strategy. — 25m
921. Design "session replay" with PII redaction. — 25m
922. Design "feature analytics" for adoption. — 25m
923. Design "conversion funnels" for product. — 25m
924. Design "experimentation platform" integration. — 25m
925. Design "experiment safety" (no SSR mismatch). — 25m
926. Design "kill an experiment" workflow. — 25m
927. Design "experiment results dashboard". — 25m
928. Design "feature retirement" workflow. — 25m
929. Design "code retirement" tooling. — 25m
930. Design "deprecation timeline" UX. — 25m
931. Migrate a v15 NgModule app to v21 standalone: full plan. — 30m
932. Migrate `*ngIf`/`*ngFor` to `@if`/`@for` at scale. — 25m
933. Migrate `@Input()` to `input()` at scale. — 25m
934. Migrate `@Output()` to `output()` at scale. — 25m
935. Migrate constructor inject to `inject()` at scale. — 25m
936. Migrate Reactive Forms to Signal Forms at scale. — 30m
937. Migrate NgRx classic to signal store at scale. — 30m
938. Migrate `RouterModule.forRoot` to `provideRouter` at scale. — 25m
939. Migrate `HttpClientModule` to `provideHttpClient` at scale. — 25m
940. Migrate to zoneless: identify blockers and stages. — 30m
941. Migrate to incremental hydration: identify candidates. — 25m
942. Migrate from `@angular/animations` to CSS. — 25m
943. Migrate from Karma to Vitest. — 25m
944. Migrate from Protractor to Cypress/Playwright. — 25m
945. Migrate from webpack to esbuild builder. — 25m
946. Migrate from custom builders to native ones. — 25m
947. Migrate from JS to TS in a legacy module. — 25m
948. Migrate from class components to functional patterns. — 20m
949. Migrate from Moment to date-fns/Luxon. — 25m
950. Migrate from lodash to native ES. — 25m
951. Migrate from `lodash-es` to per-method imports. — 20m
952. Migrate from a state machine lib to XState v5. — 25m
953. Migrate from `RxJS 6` to `RxJS 7+` (pipe-only). — 25m
954. Migrate from `BehaviorSubject` services to signal stores. — 25m
955. Migrate from `Effect()` to `linkedSignal`/`computed` where appropriate. — 25m
956. Migrate from `HttpClient.get` to `httpResource` where appropriate. — 25m
957. Migrate from `viewChild('foo')` decorator to signal queries. — 25m
958. Migrate from `ngOnDestroy` to `DestroyRef.onDestroy`. — 25m
959. Migrate from `Renderer2` to `host` metadata. — 25m
960. Migrate from `:ng-deep` to CSS variables. — 25m
961. Migrate from `View Encapsulation.ShadowDom` to `Emulated`. — 25m
962. Migrate from CSS Modules to scoped component styles. — 25m
963. Migrate from `SCSS` to `CSS` with `:where()` and nesting. — 25m
964. Migrate from `Material` to a custom design system. — 30m
965. Migrate from `CDK` to `@angular/aria`. — 25m
966. Migrate from `i18n` legacy to `$localize`. — 25m
967. Migrate from `NgPackagr` defaults to APF v17. — 25m
968. Migrate from a polyrepo to a monorepo. — 30m
969. Migrate from a monorepo to a polyrepo. — 30m
970. Migrate from `Yarn` to `pnpm`. — 25m
971. Migrate from `npm` to `pnpm`. — 25m
972. Migrate from `Karma` to `Web Test Runner`. — 25m
973. Migrate from `Jest` to `Vitest`. — 25m
974. Migrate from `Cypress` to `Playwright`. — 25m
975. Migrate from `Sentry` to `Datadog`. — 25m
976. Migrate from `Google Analytics` to a first-party analytics. — 25m
977. Migrate from a third-party CDN to a self-hosted CDN. — 25m
978. Migrate from a third-party auth to in-house. — 30m
979. Migrate from session cookies to JWT and back. — 25m
980. Migrate from REST to GraphQL (partial). — 30m
981. Migrate from REST to tRPC (partial). — 30m
982. Migrate from polling to SSE. — 25m
983. Migrate from polling to WS. — 25m
984. Migrate from WS to SSE. — 25m
985. Migrate from `iframe` widgets to in-app components. — 30m
986. Migrate from `script` widgets to in-app components. — 30m
987. Migrate from web app to PWA. — 25m
988. Migrate from PWA to TWA. — 25m
989. Migrate from PWA to Capacitor app. — 30m
990. Migrate from CSR to SSR. — 30m
991. Migrate from SSR to SSG. — 25m
992. Migrate from SSG to SSR. — 25m
993. Migrate from on-prem hosting to edge. — 25m
994. Migrate from `vercel` to `cloudflare`. — 25m
995. Migrate from `cloudflare` to `aws`. — 25m
996. Migrate from `aws` to `gcp`. — 25m
997. Migrate from `gcp` to `azure`. — 25m
998. Migrate from one node version to next major. — 20m
999. Migrate from one Angular major to next major. — 25m
1000. Plan the next 5 years: roadmap for an Angular 21 app facing v22, v23, v24, v25. — 30m
