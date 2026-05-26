# Medium — 1000 Questions

Target audience: 1–3 years experience. Budget: **3–7 minutes per question**. Questions require multi-step reasoning, knowledge of common patterns, and the ability to debug small snippets. Answers are not included; verify against [angular.dev](https://angular.dev) or the [root README](../README.md) feature list.

---

## HTML, Semantics & Accessibility (1–40)

1. Explain the accessibility tree and how it differs from the DOM tree. — 4m
2. When would you choose `<button>` over `<a>` and vice versa? Give two concrete cases each. — 4m
3. What is `aria-live` and what are the trade-offs between `polite` and `assertive`? — 4m
4. Describe the correct heading hierarchy for an SPA where routes change the main content. — 5m
5. Explain why `tabindex="-1"` is useful and one case where it's misused. — 4m
6. What is a "focus trap" and when is it required? Sketch the algorithm. — 6m
7. Explain how a screen reader announces a form input — what elements/attributes contribute? — 5m
8. What is the difference between `<input type="search">` and `<input type="text" role="searchbox">`? — 4m
9. Compare `<details><summary>` against a custom disclosure component for accessibility. — 5m
10. Explain why `display: contents` can break accessibility for some elements. — 4m
11. When does the `<dialog>` element trap focus automatically and when does it not? — 5m
12. Describe how `inert` works and when you would use it. — 4m
13. Why is "color contrast" still a hard problem for theming? Give a real example. — 4m
14. What is the WAI-ARIA "authoring practices" pattern for a combobox? Outline its DOM. — 7m
15. Explain why you should not use `aria-hidden="true"` on a focusable element. — 4m
16. What is the difference between `role="alert"` and `aria-live="assertive"`? — 5m
17. Explain when `aria-describedby` is preferred over `aria-label`. — 4m
18. Sketch the DOM for an accessible icon-only button. — 4m
19. What are the accessibility differences between `<select>` and a custom listbox? — 5m
20. Explain why a "carousel" is often a bad UX choice from an a11y perspective. — 4m
21. How do you build a navigation skip-link, and why does it matter? — 4m
22. How do reduced-motion media queries interact with `view-transition`? — 5m
23. Describe an SSR-safe way to render `<noscript>` fallbacks. — 4m
24. What are the implications of injecting `lang` on `<html>` dynamically for screen readers? — 4m
25. What is `loading="lazy"` and what are its caveats above the fold? — 4m
26. Compare `<picture>` with `srcset` for art direction vs. resolution switching. — 5m
27. Explain how `fetchpriority` can interact with LCP. — 5m
28. Describe a case where `<meta http-equiv="refresh">` is dangerous. — 3m
29. When does a `name` attribute on an `<a>` still matter? — 3m
30. What is the difference between `download` attribute behavior across Safari and Chrome? — 4m
31. What is `<input type="file" capture>` and when does it matter? — 3m
32. Explain `enterkeyhint` and one mobile UX win it enables. — 3m
33. Why prefer `inputmode="numeric"` over `type="number"` for OTP fields? — 4m
34. Explain `autocomplete="one-time-code"` and platform support. — 3m
35. What does `referrerpolicy` on `<a>` and `<img>` control? — 4m
36. What is the impact of `crossorigin="anonymous"` on script error reporting? — 4m
37. Explain why `defer` scripts execute in document order while `async` does not. — 4m
38. Describe the order of execution for: inline script, `defer` script, `async` script, ES module. — 5m
39. What is the difference between `srcdoc` and `src` on an `<iframe>`? — 3m
40. Explain how `sandbox` attribute restrictions on `<iframe>` work. — 4m

## CSS Layout, Animation & Scaling (41–100)

41. Compare Flexbox `flex: 1` vs `flex: 1 1 0` vs `flex: 1 1 auto`. — 5m
42. Why does `min-width: 0` on a flex item often fix overflow? — 5m
43. Explain `grid-auto-flow: dense` and a downside. — 4m
44. How do `minmax(0, 1fr)` columns prevent grid items from blowing out? — 5m
45. Explain `align-self` vs `align-items` in Grid. — 3m
46. What does `place-items: center` shorthand expand to? — 3m
47. When does `margin: auto` work inside Flexbox? — 4m
48. Explain `aspect-ratio: 16 / 9` interaction with image `height: auto`. — 4m
49. What's the difference between `100vh` and `100dvh` on mobile Safari? — 4m
50. Explain `svh`, `lvh`, `dvh`. — 4m
51. Describe a CSS-only sticky header with shadow that appears only on scroll. — 6m
52. Explain `position: sticky` and the requirement on the scrolling ancestor. — 4m
53. Why does `overflow: auto` on an ancestor break `position: sticky`? — 4m
54. Implement a 3-column responsive card grid in pure CSS without media queries. — 6m
55. Explain `auto-fit` vs `auto-fill` in `repeat()`. — 5m
56. How do you create equal-height cards with content of varying length? — 4m
57. Explain "containment" (`contain: layout|paint|size`) and when each helps. — 6m
58. What does `content-visibility: auto` do for off-screen content? — 5m
59. What is `contain-intrinsic-size` and why does it pair with `content-visibility`? — 5m
60. Compare CSS animations and Web Animations API. — 5m
61. Why does animating `top` cause jank but `transform: translateY` does not? — 5m
62. Explain `will-change` overuse and its memory cost. — 4m
63. Implement a CSS-only modal backdrop using `:has()`. — 6m
64. Explain `:has()` selector and three practical uses. — 5m
65. What does `@scope` (CSS scoping at-rule) do? — 5m
66. Compare CSS `@layer` with specificity ordering. — 5m
67. Explain `cascade layers` and a use case for a design system. — 5m
68. Why does `:root` have higher specificity than `html`? Actually compare. — 3m
69. Explain `:where()` vs `:is()`. — 4m
70. Show a single rule that styles links that contain an image differently from text links using `:has`. — 4m
71. Explain how container queries (`@container`) differ from media queries. — 5m
72. What does `container-type: inline-size` enable? — 4m
73. Implement a card that switches layout at 400px of *container* width. — 5m
74. Explain CSS subgrid and one place it solves a real layout problem. — 5m
75. Why is `display: grid` preferred over `display: table` for tabular data? — 3m
76. When is `display: table` still the right choice? — 3m
77. What is the difference between `gap` and `grid-gap`? — 2m
78. Why is `gap` not supported by older Safari versions with Flexbox? — 3m
79. Implement a 12-column responsive grid using Grid. — 6m
80. Explain `grid-template: "a a b" / 2fr 1fr 1fr;`. — 5m
81. How do you make `position: sticky` work inside a Grid? — 4m
82. Describe a "masonry" layout strategy in modern CSS. — 5m
83. Explain `text-wrap: balance` and one place it matters. — 4m
84. Explain `text-wrap: pretty` vs `balance`. — 4m
85. What is `field-sizing: content` and what does it solve? — 4m
86. What is `accent-color` and what controls does it affect? — 3m
87. Explain `color-scheme: light dark` on `:root`. — 4m
88. Show how to implement a light/dark theme using CSS custom properties. — 5m
89. What is `oklch()` and one advantage over `hsl()`? — 4m
90. Explain `color-mix()` for theming. — 4m
91. What is `@property` and why is it useful for animations? — 5m
92. Explain why animating a CSS custom property fails without `@property`. — 5m
93. Describe a CSS-only loading spinner with reduced-motion support. — 5m
94. Explain how `transition: discrete allow-discrete` enables `display:none` animations. — 5m
95. What is `transition-behavior: allow-discrete`? — 4m
96. Implement a tooltip with CSS only that respects `prefers-reduced-motion`. — 5m
97. Describe a focus ring strategy that works for keyboard but not mouse. — 4m
98. Explain `outline-offset` and why it's preferred over `box-shadow` for focus. — 3m
99. Why might `outline: none` on `:focus` be a regression? — 3m
100. Explain logical properties (`margin-inline-start`) and i18n benefits. — 4m

## JavaScript Intermediate (101–180)

101. Explain how `this` is determined in JavaScript (rule-by-rule). — 5m
102. What is the difference between an arrow function's `this` and a bound function's `this`? — 4m
103. Explain `Function.prototype.bind` and how partial application works. — 4m
104. What is currying and how can you implement a generic `curry(fn)`? — 6m
105. Explain a memoization wrapper and its memory pitfalls. — 5m
106. Describe a debounce implementation. — 5m
107. Describe a throttle implementation. — 5m
108. Difference between debounce-trailing, debounce-leading, and throttle. — 5m
109. Explain `requestAnimationFrame`-based throttling for scroll handlers. — 4m
110. Explain how the event loop processes a `Promise.resolve().then().then()` chain vs nested setTimeouts. — 6m
111. Explain why `await` in a `for` loop serializes work. — 4m
112. Explain `Promise.all` vs `for await of` for fan-out fan-in. — 5m
113. Implement a "limit concurrency" helper for async jobs. — 7m
114. Explain "unhandled rejection" — when does it fire and how do you handle globally? — 4m
115. Explain how generators interact with async iteration. — 5m
116. What is an async iterator and how do you consume one? — 4m
117. Implement a `range(start, end)` generator. — 3m
118. Explain how `Symbol.asyncIterator` differs from `Symbol.iterator`. — 4m
119. Explain prototype-based inheritance with a small example. — 5m
120. Difference between `Object.create(proto)` and `class extends`. — 4m
121. Explain `class Foo extends Bar` and what `super()` does. — 4m
122. Why must you call `super()` before using `this` in a derived constructor? — 4m
123. Explain private class fields (`#field`) and what makes them truly private. — 4m
124. Explain static class fields and static blocks. — 4m
125. Compare a class with private fields vs a closure factory. — 5m
126. Explain mixins via `Object.assign(prototype, …)`. — 5m
127. Explain a "function as a class" pattern (no `class` keyword). — 4m
128. Explain `instanceof` and how it traverses the prototype chain. — 4m
129. What is `Symbol.hasInstance` and what does customizing it allow? — 5m
130. Explain `Symbol.toPrimitive` with an example. — 5m
131. Explain `Symbol.toStringTag` for custom class identification. — 4m
132. What is the "iterator protocol"? — 4m
133. Implement a `take(iter, n)` helper. — 4m
134. Implement a `chain(...iters)` helper. — 4m
135. Explain `Object.entries` vs `Object.getOwnPropertyDescriptors`. — 4m
136. Explain why `JSON.stringify(undefined)` returns `undefined`. — 3m
137. Explain how `JSON.stringify` handles cyclic references. — 3m
138. Implement a safe `JSON.stringify` that ignores cycles. — 5m
139. Implement a deep clone that handles `Date`, `Map`, `Set`, and cycles. — 7m
140. Explain `structuredClone` and what it can't clone. — 4m
141. Difference between `WeakRef` and `WeakMap`. — 5m
142. Explain `FinalizationRegistry` with a use case. — 5m
143. Explain why holding references can leak DOM nodes. — 4m
144. Describe how `Map` iteration order is guaranteed. — 3m
145. Explain `Set` vs `Array.includes` for membership testing — when does each win? — 4m
146. Why does `[...new Set(arr)]` deduplicate? Edge cases for `NaN`? — 4m
147. Implement a polyfill for `Array.prototype.flat`. — 5m
148. Explain `Array.from({length: n}, (_, i) => i)` and why `new Array(n).map(...)` fails. — 4m
149. What is "holes" in arrays and how do methods treat them? — 4m
150. Explain `Array.prototype.copyWithin`. — 3m
151. Explain `Array.prototype.with(index, value)`. — 3m
152. Difference between `toReversed`, `toSorted`, `toSpliced` and their mutating versions. — 4m
153. Explain `Object.groupBy` and one use case. — 4m
154. Explain `Map.groupBy` and how it differs. — 3m
155. Implement a `pipe(...fns)` higher-order function. — 4m
156. Implement `compose(...fns)`. — 3m
157. Explain "tail call optimization" and JS engine support. — 4m
158. Explain why deep recursion can blow the stack and how to convert to iteration. — 5m
159. Implement a trampoline to make tail-recursive functions safe. — 7m
160. Explain how `eval` and `Function` constructor differ in scoping. — 5m
161. Explain "strict mode" effects in modules vs non-modules. — 4m
162. Explain how ESM imports are static and what that enables (tree-shaking). — 5m
163. Difference between named, default, and namespace imports. — 4m
164. Explain dynamic `import()` and where you'd use it. — 4m
165. Explain top-level `await` and one risk. — 4m
166. What is a module's "live binding" and how does it differ from CommonJS? — 5m
167. Why does mutating a default-exported object work but reassigning it doesn't? — 5m
168. Explain how circular imports behave in ESM. — 6m
169. Explain why `let` in a `for` loop creates a binding per iteration. — 4m
170. Show the classic `setTimeout` in a `for var` bug and three ways to fix it. — 5m
171. Explain why `==` triggers `ToPrimitive` and the conversion table. — 6m
172. Why does `[] == false` evaluate to `true`? — 4m
173. Why does `{}+[]` return `"0"` in some contexts and not others? — 4m
174. Explain `void 0` and why it's preferred over `undefined` in some legacy code. — 3m
175. Explain how `delete obj.prop` differs from `obj.prop = undefined`. — 4m
176. Explain `Object.preventExtensions`, `seal`, `freeze`. — 4m
177. Explain `Reflect` and one method you'd reach for. — 4m
178. Explain `Proxy` traps for `get`, `set`, `has`. — 5m
179. Implement a `Proxy` that logs every property access. — 4m
180. Explain a real-world use of a `Proxy` (e.g., reactive systems). — 5m

## TypeScript Intermediate (181–240)

181. Explain "structural typing" vs "nominal typing" in TS. — 4m
182. Why can two unrelated classes assign to each other if shapes match? — 4m
183. Explain "excess property checks" and how to bypass them. — 4m
184. Difference between `Type[]` and `ReadonlyArray<Type>`. — 3m
185. Explain `as const` and what it does to literal arrays vs objects. — 4m
186. Explain `satisfies` and contrast with `as`. — 5m
187. Explain narrowing via `typeof`, `instanceof`, `in`, and discriminants. — 5m
188. Implement a discriminated union for `Result<T, E>` and a `match()` helper. — 6m
189. Explain how `never` is used for exhaustiveness checks. — 4m
190. Show an exhaustive `switch` using `assertNever(x: never)`. — 4m
191. Explain conditional types (`T extends U ? X : Y`). — 5m
192. Implement `IsArray<T>` conditional type. — 3m
193. Explain `infer` with a `ReturnType` reimplementation. — 5m
194. Implement `Awaited<T>` (simplified). — 5m
195. Implement `DeepPartial<T>`. — 5m
196. Implement `DeepReadonly<T>`. — 5m
197. Explain "distributive conditional types". — 5m
198. How do you turn off distributivity in a conditional type? — 4m
199. Implement `Exclude<T, U>` and `Extract<T, U>` from scratch. — 5m
200. Implement a `Prettify<T>` type to flatten intersection display. — 4m
201. Explain template literal types with an example for CSS units. — 5m
202. Implement `Split<S, Delim>` template literal type. — 6m
203. Implement `Join<Arr, Delim>` template literal type. — 6m
204. Explain mapped types `[K in keyof T]: T[K]`. — 4m
205. Add a modifier to a mapped type to make all properties optional. — 3m
206. Explain key remapping in mapped types (`as Capitalize<K>`). — 5m
207. Implement `Getters<T>` mapped type that produces `getX(): T[K]`. — 5m
208. Explain function overload resolution order. — 5m
209. Why does TS prefer the *last* matching overload? — 3m
210. Implement a typed `pipe` with overloads for 1–3 args. — 7m
211. Explain "this" parameter typing in functions. — 4m
212. What is a "polymorphic this" return type? — 4m
213. Explain "type predicates" with `is`. — 4m
214. Implement `isNonNullable<T>(x: T): x is NonNullable<T>`. — 3m
215. Explain "assertion functions" (`asserts x is T`). — 4m
216. Implement `assertDefined(x)`. — 4m
217. Explain `unique symbol` and a nominal-typing pattern. — 5m
218. Explain "branded types" with an `Email = string & { __brand: 'Email' }`. — 5m
219. Why are branded types still vulnerable to casts? — 3m
220. Explain `const` type parameters (TS 5.x). — 5m
221. Implement a function whose argument is preserved as a literal via `const T`. — 5m
222. Explain variance: covariance vs contravariance. — 6m
223. Explain why function parameters are bivariant by default. — 5m
224. Explain `--strictFunctionTypes` and what it changes. — 4m
225. Difference between `--noImplicitAny` and `--strict`. — 4m
226. Explain `--exactOptionalPropertyTypes`. — 5m
227. Explain `--noUncheckedIndexedAccess`. — 5m
228. Why does `noUncheckedIndexedAccess` add `| undefined` to array reads? — 4m
229. Explain `--isolatedModules` and the constraints it enforces. — 5m
230. Why does `const enum` clash with `isolatedModules`? — 4m
231. Explain "ambient declarations" (`declare module 'foo'`). — 4m
232. Implement module augmentation to add a method to `Array`. — 5m
233. Explain `declare global` and a risk of polluting the global namespace. — 4m
234. Explain how `tsc --noEmit` is used in CI. — 3m
235. Explain `incremental` and `composite` tsconfig options. — 4m
236. Explain Project References and when you'd use them. — 5m
237. Explain `paths` and `baseUrl` for module aliases. — 4m
238. Why might `paths` aliases break at runtime if the bundler isn't configured? — 4m
239. Explain `import type` and why it matters for bundlers. — 4m
240. Difference between `import type` and `verbatimModuleSyntax`. — 4m

## DOM & Browser Intermediate (241–280)

241. Explain layout, paint, and composite phases. — 5m
242. Which CSS properties trigger only composite? — 4m
243. Explain "layout thrashing" and how to avoid it. — 5m
244. Explain how `getBoundingClientRect` causes layout. — 4m
245. What is a "forced synchronous layout"? — 4m
246. Explain how `requestAnimationFrame` aligns with rendering. — 4m
247. Explain `Intersection Observer` thresholds and root margin. — 5m
248. Implement a "lazy-load images" with `IntersectionObserver`. — 5m
249. Implement an "infinite scroll" with `IntersectionObserver`. — 6m
250. Explain `MutationObserver` characteristics options. — 4m
251. Implement a "watch for class added" helper with `MutationObserver`. — 5m
252. Explain `ResizeObserver` and `contentBoxSize` vs `borderBoxSize`. — 4m
253. Implement a `useElementSize` style hook (vanilla). — 5m
254. Explain `PerformanceObserver` for LCP. — 5m
255. Explain `PerformanceObserver` for CLS. — 5m
256. Explain `PerformanceObserver` for INP. — 5m
257. What are Web Vitals (LCP, INP, CLS) thresholds? — 4m
258. Explain how to report Web Vitals to an analytics endpoint. — 4m
259. Explain the `Navigation Timing API`. — 4m
260. Explain `Resource Timing API` and how to surface slow assets. — 4m
261. Explain Service Worker lifecycle (install/activate/fetch). — 6m
262. Difference between `caches.match` and `caches.matchAll`. — 4m
263. Implement a stale-while-revalidate fetch handler. — 6m
264. Explain how a SW updates and "skipWaiting" / "clients.claim". — 5m
265. Difference between Web Workers and Service Workers and SharedWorkers. — 5m
266. Explain `postMessage` and Transferable Objects. — 4m
267. Implement a worker that processes images in parallel. — 7m
268. Explain `OffscreenCanvas` and where it shines. — 4m
269. Explain `requestIdleCallback` vs `scheduler.postTask`. — 5m
270. Explain `AbortController` chained across multiple fetches. — 4m
271. Explain `History.scrollRestoration`. — 3m
272. Explain how to gracefully handle `popstate` for an SPA. — 5m
273. Explain `BroadcastChannel` for cross-tab sync. — 4m
274. Explain `Storage Event` for `localStorage` cross-tab sync. — 4m
275. Explain `Page Visibility API` and a use case. — 3m
276. Explain `Background Sync API`. — 4m
277. Explain `Wake Lock API`. — 3m
278. Explain `Web Share API` and platform constraints. — 3m
279. Explain `CSP` `script-src` and one common misconfiguration. — 5m
280. Explain `Trusted Types` API. — 4m

## Angular Architecture & Bootstrap (281–330)

281. Walk through `bootstrapApplication(App, {providers: [...]})`. — 5m
282. Difference between providing `HttpClient` in app config vs route config. — 4m
283. When does an injectable provided at a route become destroyed? — 4m
284. Explain how `EnvironmentInjector` chains with parent injectors. — 5m
285. Explain `createComponent()` and when you'd use it imperatively. — 5m
286. Explain `ViewContainerRef.createComponent` vs `ComponentRef.setInput`. — 5m
287. Implement a dynamic component host driven by an enum. — 6m
288. Explain `ComponentMirror`/`reflectComponentType` (if applicable). — 4m
289. Explain how a route's `providers` array creates an environment injector. — 5m
290. Why is `provideRouter` an `EnvironmentProviders` and not just `Provider[]`? — 4m
291. Explain `withEnabledBlockingInitialNavigation` vs `withDisabledInitialNavigation`. — 5m
292. Explain `provideRouter(routes, withHashLocation())`. — 3m
293. What does `provideExperimentalCheckNoChangesForDebug` do (when present)? — 4m
294. Explain "tree-shakeable providers" and `providedIn: 'root'`. — 4m
295. Explain `provideExperimentalZonelessChangeDetection` (history) and the stable `provideZonelessChangeDetection`. — 4m
296. Explain how `inject(NgZone)` differs in zoneless vs zoneful apps. — 5m
297. Why might a third-party library still trigger CD via zone in a "zoneless" app? — 4m
298. Explain `provideAnimations()` vs `provideAnimationsAsync()`. — 4m
299. Explain how Angular's i18n is configured at build time. — 5m
300. Explain `$localize` and the difference between compile-time and runtime locales. — 5m
301. Explain `provideHttpClient(withInterceptorsFromDi())` interop with class interceptors. — 5m
302. Why is `withFetch()` recommended for SSR? — 4m
303. Explain `provideClientHydration` and what it changes about SSR markup. — 5m
304. Explain `withIncrementalHydration` and pairing with `@defer (hydrate on …)`. — 5m
305. Sketch a route with `RenderMode.Prerender`. — 4m
306. Difference between `RenderMode.Server` and `RenderMode.Prerender`. — 4m
307. Explain how `serverRoutes` lets you mix render modes per path. — 5m
308. Explain why CSR-only routes still benefit from SSR shell. — 4m
309. Explain event replay during hydration. — 5m
310. Why are signals well-suited to incremental hydration? — 4m
311. Explain `withRouterConfig({onSameUrlNavigation: 'reload'})`. — 4m
312. Explain `withPreloading(QuicklinkStrategy)` (third-party). — 4m
313. Implement a custom `PreloadingStrategy` that preloads only routes with `data.preload`. — 6m
314. Explain how to wire `withComponentInputBinding()` to a signal `input.required<string>()`. — 5m
315. Explain how `Title` and `Meta` services interact with SSR. — 5m
316. Explain when to use `TransferState` and a concrete example. — 6m
317. Explain `makeStateKey` and SSR rehydration. — 4m
318. Explain how `httpResource` interacts with `TransferState`. — 5m
319. Explain why directly using `window` in components breaks SSR. — 4m
320. Show two safe ways to access `window` in Angular SSR. — 5m
321. Explain how to detect platform with `inject(PLATFORM_ID)`. — 3m
322. Why should `localStorage` access be gated by platform check? — 4m
323. Explain how `afterNextRender` is a safe place to touch the DOM. — 4m
324. Compare `ngOnInit` and `afterNextRender` for DOM measurement. — 5m
325. Explain why animations are now CSS-first in v21. — 4m
326. Explain `provideAnimationsAsync` impact on bundle size. — 4m
327. Explain how to organize a feature module the standalone way. — 5m
328. Explain "barrel files" pros and cons. — 4m
329. Explain why one big `index.ts` barrel can hurt tree-shaking. — 4m
330. Explain how to lazy-load a feature in v21 without NgModules. — 4m

## Components: Inputs, Outputs, Model & Queries (331–390)

331. Explain `input()` with a default value vs `input.required()`. — 4m
332. Why is `input.required<string>()` safer than checking for `undefined` at runtime? — 4m
333. Explain `input(initial, { alias: 'name' })`. — 3m
334. Explain `input(initial, { transform: booleanAttribute })`. — 4m
335. Implement a transform that trims whitespace. — 4m
336. Why must a transform be deterministic? — 4m
337. Explain `output()` vs `EventEmitter` lifetime. — 4m
338. Explain `output<void>()` for click-like signals. — 3m
339. Implement `output<{id: string}>()` and emit. — 3m
340. Explain `model()` and the two-way binding contract. — 5m
341. Show a parent two-way binding to `[(value)]` on a custom input. — 4m
342. Explain how `model().set()` vs `model().update()` differ. — 3m
343. Explain why `model()` is preferred over input + output pair. — 4m
344. Implement a `model.required<T>()` and what it implies for the parent. — 4m
345. Explain `viewChild()` and what its signal returns before view init. — 5m
346. Difference between `viewChild()` and `viewChild.required()`. — 4m
347. Explain `viewChild('templateRef', { read: TemplateRef })`. — 4m
348. Explain `viewChildren()` and how its signal updates. — 4m
349. Explain `contentChild()` for projected content. — 4m
350. Explain `contentChildren({descendants: true})`. — 4m
351. When are signal queries first stable? — 4m
352. Why do queries not work in the constructor? — 4m
353. Explain reading a `QueryList` vs reading a signal of an array. — 4m
354. Explain `viewChild<ElementRef<HTMLInputElement>>('input')` typing. — 4m
355. Implement a focus-on-load directive using `viewChild` + `afterNextRender`. — 5m
356. Explain how `signal()` inputs interact with `ngOnChanges`. — 4m
357. What is a "model-input" two-way binding for a checkbox group? — 5m
358. Show a parent driving a `model()` with a `linkedSignal`. — 5m
359. Explain why passing a signal as an input value is rarely what you want. — 4m
360. Explain how `input()` propagates change-detection in OnPush. — 4m
361. Show why `@Input() set foo()` setter pattern is replaced by `input()` + `effect()`. — 5m
362. Explain when you'd still want a setter-based input. — 4m
363. Explain the difference between `output()` and `EventEmitter<void>().emit()`. — 4m
364. Show how to forward an `output()` from a child to a parent via host. — 5m
365. Implement a host-class binding for selected state. — 4m
366. Implement a host-listener for `keydown.escape`. — 4m
367. Show two ways to set host attributes: `host` metadata vs `inject(ElementRef)`. — 5m
368. Why is `host: { '[class.active]': 'active()' }` preferred over an `effect()`? — 4m
369. Explain how `host: { '(click)': 'onClick($event)' }` resolves `this`. — 4m
370. Implement an attribute selector with `host` decorators. — 4m
371. Explain the difference between `selector: '[appFoo]'` and `selector: 'app-foo'`. — 3m
372. Explain how a host element type is inferred by Angular DOM bindings. — 4m
373. Explain `HostAttributeToken` and a use case. — 4m
374. Implement a `Button` that reads `type` via `HostAttributeToken('type')`. — 5m
375. Explain `inputs` and `outputs` arrays on `@Component` metadata. — 4m
376. When would `inputs: ['foo']` be used instead of `input()`? — 4m
377. Explain `standalone: true` and what it removes. — 3m
378. Explain `imports: [SomeModule]` interop in standalone. — 4m
379. Why might you still need `CommonModule` import in a standalone component? — 4m
380. Explain how to use `*ngIf` if a third party emits it (legacy interop). — 4m
381. Explain how `OnPush` flow changes with signal inputs vs property inputs. — 5m
382. Implement a stateless "controlled" component using only inputs/outputs. — 5m
383. Implement a stateful "uncontrolled" component using `model()`. — 5m
384. Explain `effect()` vs `computed()` for derived props from inputs. — 5m
385. Why prefer `computed()` over a getter for derived UI state? — 4m
386. Explain "presentational vs container" component split in Angular. — 5m
387. Implement a "container" that drives a presentational child via signals. — 6m
388. Explain how to type a component's `output<T>()` correctly for consumers. — 4m
389. Show how to subscribe to an `output()` programmatically (consumer side). — 4m
390. Explain `OutputRef.subscribe(fn).unsubscribe()` lifecycle. — 4m

## Parent–Child & Cross-Component Patterns (391–440)

391. Compare `@Input/@Output`, `model()`, services, signals, and route data for cross-component communication. — 6m
392. When should a child *not* know who its parent is? — 4m
393. Explain "lifting state up" in Angular signals. — 5m
394. Implement a "selected row" pattern across a sibling toolbar and table. — 6m
395. Explain why a shared service is better than `@Output` chains 3 levels deep. — 5m
396. Implement a `SelectionService` using signals. — 5m
397. Explain how to scope a shared service to a subtree. — 5m
398. Show using route-level providers to scope a service. — 4m
399. Explain `viewProviders` vs `providers` for a directive/component that's projected. — 5m
400. Explain "ambient context" pattern via `InjectionToken`. — 5m
401. Implement a "theme context" via DI and `inject()`. — 5m
402. Explain how to propagate a "loading" state from child up to parent. — 5m
403. Implement a parent banner that listens to *any* descendant's loading signal. — 6m
404. Explain how to broadcast an error from child to root via a service signal. — 5m
405. Explain how content projection enables "compound components". — 5m
406. Implement a `<Tabs><Tab/></Tabs>` compound component skeleton. — 7m
407. Explain how `contentChildren` powers compound components. — 5m
408. Implement an `<Accordion>` where `<AccordionItem>` registers itself. — 7m
409. Explain why "self registration" beats `@Input arr`. — 4m
410. Implement a "form section" that registers with a parent form. — 6m
411. Explain how to communicate from a dialog back to its opener. — 5m
412. Implement a dialog service that returns a `Promise<Result>` of the close value. — 6m
413. Explain how to forward `aria-controls` from parent to child trigger element. — 4m
414. Explain a "render prop" pattern using `ng-template`. — 5m
415. Implement a "DataTable" with `<ng-template let-row>` projection for cells. — 7m
416. Explain how `TemplateRef<T>` enables typed template contexts. — 5m
417. Show passing `let-foo` context from `ngTemplateOutlet`. — 5m
418. Explain why `ng-template` with `ngTemplateOutletContext` outperforms inline component creation. — 5m
419. Implement a "list virtualization" sketch using `IntersectionObserver` and `ng-template`. — 7m
420. Explain how a parent can imperatively call a child via `viewChild` and a public method. — 4m
421. Explain why a public method on a child is sometimes the wrong abstraction. — 4m
422. Explain how `effect()` in a parent can react to a child's emitted signal. — 4m
423. Implement an "undo" service that all siblings subscribe to. — 6m
424. Explain how `model()` cascades through a chain `Grandparent → Parent → Child`. — 5m
425. Show a chain of `model()` and what happens when the leaf updates. — 5m
426. Explain change-detection cost of OnPush vs signals in a deep tree. — 5m
427. Explain why "always passing a new object" defeats `OnPush` caching. — 4m
428. Show two ways to memoize an immutable shape between renders. — 5m
429. Explain "patch" vs "set" semantics in signals for nested objects. — 5m
430. Implement an immutable update helper for nested signals. — 6m
431. Explain why deeply nested signals should usually be flattened. — 5m
432. Explain a "store" abstraction over signals (NgRx Signal Store light sketch). — 6m
433. Explain how `linkedSignal` enables "props as default state" pattern. — 5m
434. Implement a `selected` linked to a list with fallback to first. — 5m
435. Explain "URL as source of truth" pattern with `withComponentInputBinding`. — 5m
436. Show how a child reads a `userId` route param via signal `input()`. — 5m
437. Explain how to keep a child input in sync with a parent search box. — 4m
438. Implement a `debounceSignal(source, ms)` helper. — 6m
439. Implement a `throttleSignal(source, ms)` helper. — 6m
440. Explain why "two signals binding to the same source" is fine but two `effect()`s mutating each other is not. — 5m

## Content Projection Patterns (441–470)

441. Implement a `Card` component with `header`, `body`, `footer` slots. — 5m
442. Explain how `<ng-content select="[slot=header]">` matches an attribute. — 4m
443. Show fallback content for an empty slot. — 4m
444. Explain why `<ng-content>` should not be inside `@if`. — 4m
445. Explain why projecting a structural directive (`*ngIf`) into a slot requires care. — 5m
446. Implement a `List` with projected `Item`s and an `EmptyState` slot. — 6m
447. Explain how `contentChildren` retrieves projected child components. — 4m
448. Implement a `RadioGroup` that registers `Radio` items via `contentChildren`. — 6m
449. Explain content projection ordering with multiple matching selectors. — 4m
450. Explain CSS encapsulation across projected boundaries. — 4m
451. Explain why `:host ::ng-deep .child` works but `.parent .child` from the host CSS does not affect projected content reliably. — 5m
452. Implement a `Modal` that projects header/body/footer and uses CSS variables for theming. — 6m
453. Explain how to forward `id` from host to a projected child for `aria-labelledby`. — 5m
454. Implement a `Field` wrapper for `<input>` that wires label/id/aria-describedby. — 6m
455. Explain why "content children" cannot include nested grand-children by default. — 4m
456. Explain `{descendants: true}` for `contentChildren`. — 4m
457. Implement a sortable list where items project their own drag handles. — 7m
458. Explain "transcluded directive" pattern. — 4m
459. Explain how `ng-template` projection differs from element projection. — 5m
460. Implement a `Stepper` whose steps are `<ng-template>`s. — 7m
461. Explain how `EmbeddedViewRef` differs from `ComponentRef`. — 4m
462. Implement a dynamic outlet that switches between two `<ng-template>`s. — 5m
463. Explain how `ngTemplateOutlet` typed context propagates. — 5m
464. Show a generic `<ListView>` that types its row context. — 6m
465. Explain why pure-text projection differs from element projection in selector match. — 4m
466. Explain how `select="*"` works in `<ng-content>`. — 3m
467. Explain projection precedence when multiple `<ng-content>` slots match. — 4m
468. Implement a `Card` whose footer is hidden if not projected. — 5m
469. Explain pitfalls with conditional projection and `OnPush`. — 5m
470. Show how to test a component that uses content projection. — 5m

## Signals — Advanced Basics (471–530)

471. Explain why `signal()` reads inside a template create a dependency. — 4m
472. Explain how Angular schedules CD when a signal updates. — 5m
473. Explain "glitch-free" propagation in signals. — 5m
474. Why is `computed(() => a() + b())` safer than caching manually? — 4m
475. Explain `signal({ a: 1 }, { equal: deepEqual })`. — 4m
476. Implement a `signal<Date>(new Date(), { equal: (a,b) => +a === +b })`. — 4m
477. Explain why `signal({})` and `set({})` always fires consumers. — 4m
478. Show an idiomatic immutable update for a list signal. — 4m
479. Show an idiomatic immutable update for a nested object signal. — 5m
480. Explain `computed(() => Array.from(set()))` and why it's stable enough. — 5m
481. Explain `linkedSignal(() => first(opts()))` and reset behavior. — 4m
482. Implement `linkedSignal({source, computation})` that preserves selection if still valid. — 6m
483. Explain `previous` argument in linked signal. — 4m
484. Compare `linkedSignal` with `computed` + manual `signal`. — 5m
485. Explain why an `effect()` is the wrong place to sync two signals. — 4m
486. Show how `linkedSignal` removes the need for a sync effect. — 5m
487. Explain `resource({ params, loader })` lifecycle. — 5m
488. Explain `params` reactivity rules. — 4m
489. Implement a paginated `resource` with `pageIndex` and `pageSize` signals. — 6m
490. Explain how cancellation works in `resource`. — 4m
491. Show using `abortSignal` with `fetch` inside a loader. — 4m
492. Explain `httpResource(url, options)` differences from `resource`. — 4m
493. Implement an `httpResource` with auth headers via interceptor. — 5m
494. Explain `httpResource` interaction with `TransferState`. — 5m
495. Explain optimistic UI with `resource.value.set(...)`. — 5m
496. Show a "create item" with optimistic add then real reconcile. — 7m
497. Explain `resource.reload()` vs param-change reload. — 4m
498. Explain `status() === 'reloading'` UX. — 4m
499. Show a skeleton-loader strategy using `isLoading()`. — 5m
500. Explain `hasValue()` typeguard benefits. — 4m
501. Explain `error()` and rendering a retry UI. — 4m
502. Implement an exponential backoff retry for a `resource`. — 7m
503. Explain why `resource` is not always a replacement for an Observable pipeline. — 5m
504. Explain pairing `resource` with `linkedSignal` to choose default selected item. — 5m
505. Explain how `afterRenderEffect` differs from `effect` in scheduling. — 5m
506. Show when to use `afterRenderEffect` for a chart redraw. — 5m
507. Explain why DOM measurement in `effect()` is unsafe. — 4m
508. Show measuring an element inside `afterNextRender`. — 5m
509. Explain `afterEveryRender` cost. — 4m
510. Explain `untracked()` in detail with two real scenarios. — 5m
511. Show `untracked(() => stamp())` inside an `effect`. — 4m
512. Explain `Signal<T>` vs `WritableSignal<T>` type incompatibility. — 4m
513. Explain `signal<T | null>(null)` vs `signal<T | undefined>(undefined)`. — 4m
514. Explain why a `Signal<readonly T[]>` is friendlier to consumers. — 4m
515. Implement a `derive<T>(deps, fn)` typed helper around `computed`. — 5m
516. Explain how signals avoid stale closures common in React Hooks. — 5m
517. Compare signals with React `useSyncExternalStore`. — 5m
518. Explain why signals make memoization mostly automatic. — 4m
519. Explain how signals enable fine-grained DOM updates. — 5m
520. Explain "push-based templates" in Angular's renderer. — 5m
521. Explain how signals interact with `*ngFor`'s `trackBy`. — 4m
522. Why is `@for` `track` mandatory when iterating? — 4m
523. Show identity-based `track item.id`. — 3m
524. Show `track $index` and when it's appropriate. — 4m
525. Explain `track` performance impact in long lists. — 4m
526. Explain `@for` with `let last`, `let first`, `let even`. — 4m
527. Explain how `@for` reorders DOM nodes vs recreates them. — 5m
528. Explain `@defer (when isReady())` reactivity contract. — 4m
529. Explain `@defer (prefetch on idle)`. — 4m
530. Explain why `@defer (hydrate on viewport)` only matters in SSR. — 4m

## Computed, Effect & Scheduling (531–570)

531. Explain how `computed()` deduplicates emissions with structural equality (or lack thereof). — 4m
532. Explain why `computed(() => Math.random())` is a bug. — 4m
533. Explain "tracked vs untracked reads" inside a computed. — 5m
534. Implement a `computedAsync` style helper using `resource`. — 6m
535. Explain `computed(() => longComputation())` caching cost. — 4m
536. When is splitting a single computed into two beneficial? — 4m
537. Show splitting `filteredAndSorted` into `filtered` and `sorted`. — 5m
538. Explain `computed` recursion error scenarios. — 5m
539. Explain `effect()` vs `effect(..., { allowSignalWrites: true })`. — 5m
540. Why has `allowSignalWrites` been gated/deprecated? — 4m
541. Explain "syncing to localStorage" via effect. — 4m
542. Show an effect that persists a signal to localStorage and rehydrates. — 6m
543. Show using `effect()` for analytics on signal change. — 4m
544. Explain why effects run *after* CD by default. — 5m
545. Explain `effect({ injector: ... })` for use outside a component. — 4m
546. Show creating an `effect()` in a service. — 5m
547. Explain `effect.destroy()`. — 4m
548. Explain how to manually clean up an effect via `onCleanup`. — 4m
549. Show an effect that owns a `setInterval` and clears it on cleanup. — 5m
550. Explain how `DestroyRef` ties to component lifetime. — 4m
551. Explain `takeUntilDestroyed()` in a service. — 4m
552. Explain why `takeUntilDestroyed` needs an injection context (or `DestroyRef` injected). — 4m
553. Implement `takeUntilDestroyed(this.destroyRef)` for an observable in a class. — 5m
554. Explain `afterNextRender({read, write, mixedReadWrite, earlyRead})` phases. — 6m
555. Explain how phases order helps avoid layout thrash. — 5m
556. Show measuring an element in `read` and writing in `write` phase. — 5m
557. Explain why side-effecting in `computed` is forbidden. — 4m
558. Show a "throttle to animation frame" pattern with `afterRenderEffect`. — 6m
559. Explain "render-then-effect" sequencing pitfalls. — 5m
560. Explain how signal updates batch within a microtask. — 5m
561. Explain why two `set()` calls in the same microtask produce one notification. — 5m
562. Explain manually flushing signals (if API exists). — 4m
563. Explain how to test an effect runs the expected number of times. — 5m
564. Show a `TestBed.runInInjectionContext(() => effect(...))` pattern. — 5m
565. Explain why testing effects requires fake async or flush. — 5m
566. Show `TestBed.flushEffects()` (if applicable in your version). — 4m
567. Explain effect scheduling under `provideExperimentalCheckNoChangesForDebug`. — 4m
568. Explain how to debug "effect ran too many times". — 5m
569. Show using `DevTools` Profiler to inspect signal dependencies. — 4m
570. Explain `effect()` interaction with SSR (server-side). — 5m

## Signal Forms — Intermediate (571–650)

571. Implement a multi-section signup form (account/profile/preferences) as a single Signal Form. — 7m
572. Implement conditional required: address required only if "ship to me" is true. — 6m
573. Show `applyWhen(s.shippingAddress, ({valueOf}) => valueOf(s.sameAsBilling) === false, ...)`. — 5m
574. Explain why `applyWhen` needs the *path* and *condition* separately. — 4m
575. Implement cross-field validation: `confirmPassword` must equal `password`. — 6m
576. Show using `stateOf(p.password).dirty()` inside validation. — 4m
577. Implement an array field of "phone numbers" with per-item validation. — 6m
578. Show `applyEach(s.phones, (phone) => required(phone))`. — 4m
579. Explain why `applyEach` callback takes one arg, not (item, index). — 4m
580. Implement adding/removing items in an array field. — 5m
581. Explain why arrays are mutated via the model signal `.update()`. — 4m
582. Implement an async unique-username validator with `validateAsync`. — 7m
583. Show the required `onError` handler in `validateAsync`. — 4m
584. Explain why `params` must be a function returning the value. — 4m
585. Explain `factory: (sig) => resource({...})` typing. — 4m
586. Show `validateAsync` with `debounce()` to avoid spamming the server. — 5m
587. Explain `validateHttp` for backend-driven validation. — 5m
588. Implement a server-side validation that returns a list of errors mapped to fields. — 7m
589. Explain `validateStandardSchema` integration with Zod/Valibot. — 5m
590. Show using Zod schema as the validation source of truth. — 6m
591. Explain "schema reuse" via `schema()` helper. — 5m
592. Implement an `addressSchema` reused in billing and shipping. — 6m
593. Explain pitfalls of binding `<select multiple>` to an array field. — 4m
594. Show binding `<input type="checkbox">` to a boolean field. — 3m
595. Explain why a checkbox cannot bind to a `string[]` directly. — 4m
596. Implement a "tags" multi-select with checkboxes mapped from array. — 6m
597. Show conditionally `disabled(s.password, ({valueOf}) => !valueOf(s.createAccount))`. — 4m
598. Implement `readonly(s.username)` and a UI hint. — 4m
599. Implement `hidden(s.extras, ({valueOf}) => valueOf(s.tier) === 'free')` and explain it doesn't remove model. — 5m
600. Explain "soft-hide vs unmount" pattern with `hidden` vs `@if`. — 5m
601. Show submitting only valid forms and marking all as touched first. — 4m
602. Explain `submit(form, async () => {})` and why it must be `async`. — 4m
603. Implement an error toast on submit failure. — 5m
604. Explain how `form().pending()` differs from `form().valid() === false`. — 4m
605. Show disabling submit while pending. — 3m
606. Implement an "unsaved changes" guard tied to `form().dirty()`. — 6m
607. Explain how to integrate Signal Forms with a `CanDeactivateFn`. — 5m
608. Implement saving partial progress (autosave) tied to `debounce(s.everything, 500)`. — 6m
609. Explain why `metadata()` is useful for storing field-level UI hints. — 4m
610. Implement `metadata(s.email, { label: 'Email' })` and read in template. — 5m
611. Show a generic `<FieldError>` component that reads `errors()` from a field. — 6m
612. Explain `errors()` array semantics and showing only first error. — 4m
613. Show internationalizing error messages via a function. — 5m
614. Explain why `pattern(s.zip, /^\d{5}$/, { when })` is wrong. — 4m
615. Use `applyWhen` to enable a pattern conditionally. — 5m
616. Show `minLength` and `maxLength` for password requirements. — 4m
617. Implement a strength meter computed from the password field. — 6m
618. Explain reading the form value via `form().value()` vs the source signal. — 5m
619. Explain when those two diverge (debounce). — 4m
620. Implement a "save draft to localStorage" pattern. — 6m
621. Implement a "rehydrate draft" on init. — 5m
622. Show resetting a form to initial values. — 4m
623. Explain replacing the whole model signal vs mutating it. — 4m
624. Show "reset to last saved state" pattern. — 5m
625. Explain testing a Signal Form with `TestBed`. — 5m
626. Show writing a test that sets a value and asserts validity. — 5m
627. Explain how to test async validators with fake timers. — 6m
628. Show writing a test for `submit` failure path. — 5m
629. Implement a generic `FormSection` component that takes a sub-form. — 7m
630. Explain typing `FormField<T>` as a parameter. — 5m
631. Show passing `bookingForm.personalInfo` into a `<PersonalInfoSection [section]="...">`. — 5m
632. Explain why splitting big forms into section components helps OnPush. — 5m
633. Implement an "edit vs read-only" mode that toggles `readonly` on all fields. — 6m
634. Show using `applyWhen(s, () => isReadonly(), (p) => readonly(p.everyField))`. — 5m
635. Explain how `applyWhen` handles the *root* path. — 4m
636. Explain `schema()` composition vs `applyWhen` composition. — 5m
637. Show schema with shared `required` rules and overridden messages per locale. — 6m
638. Explain typing constraint on `form(model)` — model must not have `null`. — 4m
639. Show migrating a Reactive Form to Signal Forms incrementally. — 7m
640. Explain why you cannot mix `FormControl` and `[formField]` on the same input. — 4m
641. Show using a hybrid: Reactive parent + Signal child via two components. — 6m
642. Explain `FieldTree` vs `FieldState`. — 4m
643. Explain `pathKeys()` and a use case. — 4m
644. Implement a generic "label + error" wrapper around any `FormField<T>`. — 7m
645. Show projecting form controls into a wrapper that handles label/error/hint. — 7m
646. Explain accessibility wiring: `aria-invalid`, `aria-describedby` for error messages. — 5m
647. Implement an `aria-describedby` link to an error message id. — 5m
648. Explain SSR and Signal Forms (server-side validation result). — 5m
649. Explain how to test the `[formField]` directive output binding behavior. — 5m
650. Explain `validateAsync` and SSR caveats with `resource`. — 5m

## Reactive Forms — Intermediate (651–680)

651. Implement a `FormGroup` with nested `FormArray` of items. — 5m
652. Show dynamic add/remove of `FormGroup`s inside a `FormArray`. — 5m
653. Implement a cross-field validator on a `FormGroup`. — 5m
654. Implement an async validator with debounce. — 6m
655. Explain `updateOn: 'blur'` vs `'submit'` vs `'change'`. — 4m
656. Implement a `ControlValueAccessor` for a custom input. — 7m
657. Explain `registerOnChange`, `registerOnTouched`, `writeValue`, `setDisabledState`. — 5m
658. Show NG_VALUE_ACCESSOR multi-provider on a custom input. — 5m
659. Implement a custom validator that depends on injected service. — 5m
660. Explain `Validators.composeAsync`. — 4m
661. Explain why `setValue` requires all keys and `patchValue` does not. — 3m
662. Show using `valueChanges` with `distinctUntilChanged` and `debounceTime`. — 5m
663. Explain `controls` map typing pitfalls. — 4m
664. Implement strongly typed forms with `FormControl<string>`. — 5m
665. Explain `NonNullableFormBuilder`. — 4m
666. Show using `formBuilder.nonNullable.group({...})`. — 4m
667. Explain how to integrate a Reactive Form with `NgRx`. — 5m
668. Show `selectFormValue$` selector pattern. — 5m
669. Explain why Reactive Forms can leak via `valueChanges` without cleanup. — 5m
670. Implement cleanup using `takeUntilDestroyed`. — 4m
671. Explain how Reactive Forms interact with `OnPush`. — 4m
672. Show using `markAsTouched()` to surface validation errors on submit. — 4m
673. Implement focusing the first invalid field on submit. — 5m
674. Show validating a date range across two controls. — 5m
675. Explain how to handle file uploads in Reactive Forms. — 5m
676. Show using `[(ngModel)]` with `name=""` inside a template-driven `<form>`. — 4m
677. Explain a subtle bug when mixing Reactive and template-driven forms. — 4m
678. Implement a wizard with three sub-forms and one `submit`. — 7m
679. Explain "form arrays vs records of forms" trade-offs. — 4m
680. Migrate a 100-line Reactive Form to Signal Forms — outline the steps. — 7m

## Services & Dependency Injection (681–730)

681. Explain when a service should be `providedIn: 'root'` vs at a feature route. — 5m
682. Explain why two routes can independently get separate instances of the same provider. — 4m
683. Implement a "session per route" service. — 5m
684. Explain "config service" pattern using `InjectionToken<Config>` and `provideX(config)`. — 5m
685. Implement `provideMyLib({apiBase: '...'})` returning `EnvironmentProviders`. — 6m
686. Explain `makeEnvironmentProviders([...])`. — 4m
687. Show using `inject(MY_TOKEN, {optional: true})` with a default. — 4m
688. Explain "feature providers" pattern with `with...` helpers. — 5m
689. Implement `withLogging()` feature for a custom router-style provider. — 6m
690. Explain `multi: true` providers and how to consume an array. — 5m
691. Implement registering pluggable interceptors via `multi: true`. — 6m
692. Explain "abstract class as token" pattern. — 4m
693. Implement an `abstract class Logger` and `useClass: ConsoleLogger` provider. — 5m
694. Explain how to swap `Logger` in tests. — 4m
695. Show using `useFactory` with `deps`. — 4m
696. Explain why arrow-function `useFactory` in `bootstrapApplication` is fine without `deps`. — 4m
697. Explain "lazy provider" — provide only when needed via factory. — 4m
698. Explain `forwardRef` and circular declarations. — 4m
699. Explain `useExisting` to alias one token to another. — 4m
700. Show `provide: BaseService, useExisting: SpecificService`. — 4m
701. Explain `Self` injector flag with a structural directive example. — 5m
702. Explain `SkipSelf` for accessing parent-only providers. — 5m
703. Explain `Host` with content projection considerations. — 5m
704. Implement a `RowContext` service injected only by direct row children. — 6m
705. Explain `viewProviders` vs `providers` for projected vs view children. — 5m
706. Why does `viewProviders` not leak into projected content? — 4m
707. Explain `@SkipSelf() inject(ParentTabs)`. — 4m
708. Implement a `Tabs` parent + `Tab` child using `@Optional() @SkipSelf()`. — 6m
709. Explain a "context per route" service initialized via route data. — 6m
710. Implement `provideRoutes(routes)` for sub-libraries. — 4m
711. Explain why `useFactory` runs in injection context. — 4m
712. Show `useFactory` calling `inject(HttpClient)`. — 4m
713. Explain `EnvironmentInitializerFn` and replacement of `APP_INITIALIZER`. — 5m
714. Implement an initializer that fetches config before bootstrap. — 6m
715. Explain how an initializer can be `async`. — 4m
716. Explain why initializers should be small. — 3m
717. Implement an initializer that registers a Service Worker. — 5m
718. Explain `runInInjectionContext` for outside-Angular callbacks. — 4m
719. Show using `runInInjectionContext` in a router resolver function. — 5m
720. Explain `EnvironmentInjector.runInContext()` (legacy form). — 4m
721. Explain how multiple injectors chain at runtime. — 5m
722. Implement a feature that creates its own `EnvironmentInjector`. — 6m
723. Explain `EnvironmentInjector.destroy()` semantics. — 4m
724. Explain how to test a service with DI mocks. — 5m
725. Show `TestBed.overrideProvider(Logger, { useValue: spy })`. — 4m
726. Explain how `inject()` interacts with `TestBed.runInInjectionContext`. — 4m
727. Show writing a unit test for a function that uses `inject()`. — 5m
728. Explain why services should expose readonly signals. — 4m
729. Implement a `CounterService` exposing `count` (readonly) and `increment()`. — 5m
730. Explain "tell, don't ask" applied to services. — 4m

## Routing (731–790)

731. Implement a route config with eager and lazy parts and explain. — 5m
732. Explain `canMatch` vs `canActivate` and why `canMatch` is preferred. — 5m
733. Implement a `canMatch` guard that hides a route from lazy bundle. — 5m
734. Implement a functional `CanActivateFn` that checks user role. — 5m
735. Explain `ResolveFn` and order with route activation. — 5m
736. Implement a `ResolveFn` returning data via `httpResource`. — 5m
737. Show reading resolved data with `data` signal binding. — 5m
738. Explain `withComponentInputBinding()` and how `id` becomes an `input()`. — 5m
739. Implement a `UserProfile` component with `id = input.required<string>()` from route. — 5m
740. Explain how lazy components inherit route data. — 4m
741. Implement nested routes with two `<router-outlet>`s. — 6m
742. Explain "named outlets" and the URL syntax `/foo(aux:bar)`. — 5m
743. Implement a side panel as a named outlet. — 6m
744. Explain `runGuardsAndResolvers: 'paramsChange'`. — 4m
745. Implement a tabbed view that swaps content via child routes. — 6m
746. Explain `routerLinkActive` exact vs partial matching. — 4m
747. Show using `routerLinkActiveOptions: {exact: true}`. — 3m
748. Explain how the router computes the active route. — 5m
749. Explain `Router.url` vs `Router.routerState`. — 4m
750. Explain `RouterState.snapshot` and `ActivatedRouteSnapshot`. — 4m
751. Explain `Title` and `Meta` services with route-level config. — 5m
752. Implement page title from route data. — 4m
753. Explain `withRouterConfig({paramsInheritanceStrategy: 'always'})`. — 4m
754. Explain how query params survive a redirect. — 4m
755. Show navigating with `queryParamsHandling: 'merge'`. — 4m
756. Explain `provideRouter(routes, withViewTransitions())`. — 5m
757. Show customizing view transitions per route. — 5m
758. Explain `withInMemoryScrolling({anchorScrolling: 'enabled'})`. — 4m
759. Explain `scrollPositionRestoration: 'enabled'` SSR caveats. — 5m
760. Explain `withDebugTracing` for diagnosing nav issues. — 4m
761. Implement a custom `RouteReuseStrategy` for keeping a tab alive. — 7m
762. Explain pitfalls of reusing a route component across navigations. — 5m
763. Explain why `OnPush` plays well with input-bound params. — 4m
764. Show reading multiple params via input binding. — 4m
765. Explain `withNavigationErrorHandler`. — 4m
766. Implement a global navigation error redirect to `/error`. — 5m
767. Explain `provideRouter(routes, withPreloading(PreloadAllModules))`. — 4m
768. Implement custom preloading: only preload routes with `data.preload = true`. — 6m
769. Explain how preloading interacts with `loadComponent`. — 4m
770. Explain priority of route matching when paths overlap. — 4m
771. Explain `pathMatch: 'full'` for the empty path. — 4m
772. Implement a redirect from `/` to `/dashboard`. — 3m
773. Explain `path: '**'` wildcard behavior. — 3m
774. Implement a `NotFoundComponent` for wildcard. — 4m
775. Explain how guards combine when multiple are present. — 4m
776. Explain `canLoad` (legacy) vs `canMatch`. — 4m
777. Why is `canMatch` strictly better than `canLoad`? — 4m
778. Explain `withInitialNavigation('enabledBlocking')` for SSR. — 5m
779. Implement a route that streams data with `resource` to a `userId` param. — 6m
780. Explain `router.events.pipe(filter(NavigationEnd))` pattern. — 4m
781. Show using `Router.getCurrentNavigation()`. — 4m
782. Explain how to pass state on navigation (`state` option). — 4m
783. Show reading `state` on the destination route. — 4m
784. Explain `router.config` mutation pitfalls. — 4m
785. Explain `Router.dispose()` and bootstrap-only constraints. — 4m
786. Explain how SSR knows which route to render. — 5m
787. Implement `serverRoutes` with per-route render mode. — 6m
788. Explain `RenderMode.Server` cost vs `RenderMode.Prerender`. — 5m
789. Explain hybrid rendering benefit for content-heavy + interactive sites. — 5m
790. Explain how SSR + incremental hydration improves TTI. — 5m

## HttpClient & Interceptors (791–840)

791. Explain `provideHttpClient(withInterceptors([...]))` order semantics. — 5m
792. Implement an auth interceptor that attaches a Bearer token. — 5m
793. Explain why interceptors should not block on `await`. — 4m
794. Implement an interceptor that handles 401 with a refresh-token flow. — 7m
795. Explain race conditions in concurrent refresh attempts and how to dedupe. — 7m
796. Implement a "single refresh in flight" with a shared promise. — 7m
797. Explain `HttpContext` and `HttpContextToken` for per-request flags. — 5m
798. Implement a `SKIP_AUTH` context token used by an interceptor. — 5m
799. Explain `provideHttpClient(withFetch())` benefits. — 4m
800. Explain how `withFetch` interacts with SSR streaming. — 5m
801. Implement an interceptor for telemetry timing (request duration). — 5m
802. Explain `HttpEventType` events: `Sent`, `UploadProgress`, `Response`. — 5m
803. Implement upload progress with `observe: 'events'`. — 6m
804. Implement download progress for a large file. — 6m
805. Explain `responseType: 'arraybuffer'` use cases. — 4m
806. Implement a `Blob` download with anchor click trigger. — 5m
807. Explain `HttpParams` immutability. — 4m
808. Show building `HttpParams` from a typed object. — 4m
809. Explain `encodeURIComponent` and `HttpUrlEncodingCodec`. — 4m
810. Explain CORS preflight in detail. — 6m
811. Explain why `Authorization` triggers preflight. — 4m
812. Explain how to avoid preflight for simple requests. — 5m
813. Implement a retry-with-backoff interceptor. — 7m
814. Explain `retry({ count: 3, delay: (err, retryCount) => timer(2 ** retryCount * 1000) })`. — 5m
815. Explain why server errors (5xx) should retry but client errors (4xx) should not. — 5m
816. Implement an interceptor that surfaces global toasts for 5xx. — 6m
817. Explain `firstValueFrom(http.get())` vs subscribing. — 4m
818. Explain `lastValueFrom` for a multi-emit observable. — 4m
819. Explain why HTTP observables complete after one emission. — 4m
820. Explain `httpResource(url)` reactivity to a `url()` signal. — 4m
821. Implement `httpResource(() => \`/api/users/\${userId()}\`)`. — 4m
822. Explain auto-cancellation when `userId` changes mid-request. — 4m
823. Show `httpResource` with method/body for POST. — 5m
824. Explain how interceptors apply to `httpResource`. — 4m
825. Implement an `httpResource` with `Accept: application/json` headers. — 4m
826. Implement caching via service worker + `provideHttpClient(withFetch())`. — 6m
827. Explain how to share an HTTP request across multiple consumers. — 5m
828. Implement an `inMemoryCache` interceptor for GETs. — 7m
829. Explain `If-Modified-Since` / `ETag` and how to leverage them. — 5m
830. Implement a "stale-while-revalidate" interceptor. — 7m
831. Explain testing interceptors with `provideHttpClientTesting()`. — 5m
832. Implement a test asserting `Authorization` header is set. — 5m
833. Explain `HttpTestingController.expectOne` and `verify`. — 4m
834. Explain failing tests when leftover requests remain. — 4m
835. Explain `provideExperimental*` API gating in Angular 21 (if applicable). — 4m
836. Explain `HttpResource.loading()` vs `httpResource.isLoading()` (current naming). — 3m
837. Explain why `httpResource` plus `TransferState` gives free SSR cache. — 5m
838. Explain how to test `httpResource` in a component. — 6m
839. Explain `HttpClient` and CSRF cookie handling. — 4m
840. Implement `xsrfCookieName` configuration. — 4m

## Change Detection & Lifecycle (841–880)

841. Explain how `signal()` updates are batched and trigger CD. — 5m
842. Compare CD cost between zoneful and zoneless apps. — 5m
843. Explain `markForCheck()` vs `detectChanges()` vs `tick()`. — 5m
844. Explain `tick()` in tests vs runtime. — 4m
845. Explain `ApplicationRef.tick()` and avoiding it. — 4m
846. Explain "ExpressionChanged…" errors and modern signal mitigations. — 5m
847. Implement a parent input updated synchronously inside `ngOnInit` and how that error shows. — 5m
848. Explain why signals minimize this error. — 4m
849. Explain `afterNextRender` for late binding to avoid the error. — 5m
850. Explain how OnPush works with route reuse. — 4m
851. Explain how `ChangeDetectorRef.markForCheck` and signals coexist. — 4m
852. Implement a tree where some leaves use signals and others use OnPush + observables. — 6m
853. Explain Lifecycle order: constructor → ngOnInit → ngAfterContentInit → ngAfterViewInit. — 4m
854. Explain when `ngOnChanges` does *not* fire (signal inputs). — 4m
855. Explain `ngDoCheck` performance pitfalls. — 4m
856. Explain `ngAfterContentChecked` and `ngAfterViewChecked` cost. — 4m
857. Explain why `ngOnDestroy` may be replaced by `DestroyRef.onDestroy`. — 4m
858. Show using `DestroyRef.onDestroy(() => clearInterval(id))`. — 4m
859. Explain `afterEveryRender` for "after CD" hooks. — 4m
860. Explain `afterNextRender({phase: 'read'})` ordering with `'write'`. — 5m
861. Implement a measure-then-set pattern using `afterNextRender` phases. — 6m
862. Explain CD inside `@defer` lifecycle. — 4m
863. Explain CD inside `@if` and `@for` (whether each iteration is its own view). — 5m
864. Explain `EmbeddedView` reuse in `@for` with `track`. — 5m
865. Explain how `track` affects DOM diffing. — 5m
866. Explain `track $index` cost on a reorderable list. — 4m
867. Explain why `track $index` can break input animations. — 4m
868. Explain "stable identity" requirement of `track`. — 4m
869. Implement `track item.id ?? $index` fallback pattern. — 4m
870. Explain `ChangeDetectorRef.detach()` and `reattach()`. — 5m
871. Show using `detach()` for an expensive chart and manual `detectChanges`. — 6m
872. Explain `ApplicationRef.attachView` for dynamic components. — 4m
873. Explain `ComponentRef.changeDetectorRef.markForCheck()` after `setInput`. — 4m
874. Explain how zoneless apps avoid `tick()` storms. — 4m
875. Explain `Zone.js` patching `setTimeout` vs unpatched globals. — 5m
876. Explain how to opt a callback out of zone with `NgZone.runOutsideAngular`. — 5m
877. Implement a scroll listener outside zone, with `markForCheck` on important events. — 6m
878. Explain "exit zone for animations" pattern. — 4m
879. Explain how `Router` events fire CD. — 4m
880. Explain why HTTP responses trigger CD in zoneful apps. — 4m

## RxJS — Intermediate (881–930)

881. Explain `switchMap` vs `mergeMap` vs `concatMap` vs `exhaustMap` with concrete UX scenarios. — 6m
882. Show using `switchMap` for typeahead. — 5m
883. Show using `concatMap` for write operations needing order. — 4m
884. Show using `exhaustMap` to ignore extra "save" clicks. — 4m
885. Explain `combineLatest` vs `forkJoin`. — 5m
886. Explain `withLatestFrom` and a use case. — 4m
887. Explain `pairwise` and `scan`. — 4m
888. Implement an "auto-save with debounce + retry" pipeline. — 7m
889. Explain `shareReplay({bufferSize: 1, refCount: true})`. — 5m
890. Explain why `shareReplay({refCount: false})` can leak. — 5m
891. Explain `share()` vs `shareReplay()`. — 4m
892. Explain `multicast` (legacy) and replacement with `share`. — 4m
893. Implement a "single in-flight request" pattern. — 6m
894. Explain `merge`, `concat`, `race`, `zip`. — 5m
895. Explain `defer` and "fresh source per subscription". — 4m
896. Show creating an observable from a function returning a Promise. — 4m
897. Explain `from(promise)` vs `defer(() => promise)`. — 4m
898. Explain `interval`, `timer`, and `animationFrameScheduler`. — 4m
899. Explain "hot vs cold" observables. — 5m
900. Implement a hot observable from a `Subject`. — 4m
901. Explain `BehaviorSubject`, `ReplaySubject`, `AsyncSubject`. — 5m
902. Explain why `BehaviorSubject(initial)` is useful for selectors. — 4m
903. Show converting `BehaviorSubject` to a signal via `toSignal`. — 4m
904. Explain `toSignal({initialValue})` ergonomics. — 4m
905. Explain `toObservable(signal)` and CD timing. — 5m
906. Implement a "select from a signal store" with `toObservable`. — 5m
907. Explain why most new code can avoid creating Observables manually. — 5m
908. Explain when a `Subject` is still cleaner than a signal. — 5m
909. Implement an event bus as a `Subject`. — 4m
910. Explain `EventEmitter` (Angular) vs `Subject` (RxJS). — 4m
911. Explain `takeUntil(this.destroy$)` legacy pattern. — 4m
912. Explain why `takeUntilDestroyed()` is the modern replacement. — 4m
913. Implement `takeUntilDestroyed()` in a service constructor. — 5m
914. Explain pipelines with `tap` for side effects vs `subscribe`. — 4m
915. Implement a `tap` that logs only in dev mode. — 4m
916. Explain `catchError` returning a fallback observable. — 4m
917. Show `catchError(() => of([]))` pattern. — 3m
918. Explain `retryWhen` vs new `retry({delay})`. — 4m
919. Implement exponential backoff with jitter. — 6m
920. Explain why "Promise.all" cannot easily express cancelation but `forkJoin` can. — 5m
921. Explain `toArray()` and bounded streams. — 4m
922. Implement a "buffer for N seconds" pipeline. — 5m
923. Explain `bufferTime`, `bufferCount`, `windowTime`. — 5m
924. Explain `throttleTime` vs `auditTime` vs `sampleTime`. — 5m
925. Implement a "save the latest within a 1s window" pattern. — 5m
926. Explain operator factories returning functions. — 4m
927. Implement a custom operator `logTap(label)`. — 5m
928. Explain `Subscriber` and how operators chain. — 5m
929. Explain marble testing basics. — 5m
930. Show a tiny marble test using `TestScheduler`. — 6m

## Testing — Intermediate (931–970)

931. Explain Angular 21's recommended test runner (Vitest) vs legacy Karma. — 4m
932. Implement a Vitest unit test for a service with signals. — 5m
933. Show `TestBed.configureTestingModule({providers: [...]})` for standalone. — 4m
934. Explain `TestBed.runInInjectionContext`. — 4m
935. Show writing a test for an `effect()`. — 5m
936. Explain `flushEffects` (where applicable). — 4m
937. Implement a ComponentHarness for a button. — 6m
938. Implement a harness for a custom input that toggles disabled. — 6m
939. Explain `harnessLoader.getHarness(MyHarness)`. — 4m
940. Show using `RouterTestingHarness.create()` and navigating. — 5m
941. Implement a test that navigates and asserts the page heading. — 5m
942. Explain testing route guards. — 5m
943. Implement a test for a `CanActivateFn` returning `false`. — 5m
944. Explain testing `ResolveFn`. — 5m
945. Implement a test for a `ResolveFn` returning data. — 5m
946. Explain testing async validators with fake timers. — 5m
947. Show `vi.useFakeTimers()` and `vi.advanceTimersByTime(1000)`. — 4m
948. Explain testing HTTP with `provideHttpClientTesting`. — 5m
949. Show a test for an interceptor that adds an `Authorization` header. — 5m
950. Explain testing components with content projection. — 5m
951. Implement a test that wraps a content-projecting component with `TestHost`. — 6m
952. Explain testing OnPush components — when do you need `fixture.detectChanges()`? — 5m
953. Show triggering CD after a signal change. — 4m
954. Explain `fixture.autoDetectChanges()`. — 4m
955. Explain why setting an input via `fixture.componentRef.setInput` is preferred. — 4m
956. Show `setInput('userId', 42)`. — 3m
957. Explain "shallow rendering" with `NO_ERRORS_SCHEMA` or test hosts. — 5m
958. Implement testing a directive in isolation. — 5m
959. Implement testing a pipe in isolation. — 4m
960. Explain testing a service that uses `inject()` outside a component. — 5m
961. Show using `TestBed.inject` with `runInInjectionContext`. — 4m
962. Explain Cypress component testing vs E2E. — 4m
963. Implement a Cypress E2E for "happy path login". — 6m
964. Explain Playwright as an alternative to Cypress. — 4m
965. Explain Storybook for component-driven development. — 4m
966. Explain "visual regression" testing approach. — 4m
967. Explain `jest-axe` (or `axe-core`) for a11y tests. — 5m
968. Implement an a11y test asserting no violations on a component. — 5m
969. Explain "contract testing" between frontend and backend. — 4m
970. Explain MSW (Mock Service Worker) for integration tests. — 5m

## Performance, Security, Tooling & Misc (971–1000)

971. Explain bundle analysis with `source-map-explorer` or `--stats-json`. — 5m
972. Identify two common Angular bundle bloat causes. — 4m
973. Explain "barrel re-exports" hurting tree-shaking. — 4m
974. Explain "side-effectful imports" and `"sideEffects": false` in package.json. — 5m
975. Explain `differential loading` (historical) and modern `target: ES2022`. — 4m
976. Explain how `@defer` reduces initial bundle. — 4m
977. Explain `@defer (on viewport)` for above-the-fold pruning. — 4m
978. Explain image optimization: `NgOptimizedImage` directive. — 5m
979. Show using `<img ngSrc>` with `priority` for LCP. — 4m
980. Explain `priority` attribute mapping to `fetchpriority`. — 4m
981. Explain `provideClientHydration` impact on Web Vitals. — 4m
982. Explain how `withIncrementalHydration` improves TTI. — 4m
983. Explain `provideServiceWorker('ngsw-worker.js')`. — 4m
984. Implement enabling SW in `production` only. — 4m
985. Explain SW update flow with `SwUpdate`. — 5m
986. Explain XSS in templates and how Angular mitigates. — 5m
987. Explain `bypassSecurityTrustHtml` and the danger. — 5m
988. Explain `DomSanitizer` and which contexts it covers. — 5m
989. Explain CSRF protections in `HttpClient`. — 4m
990. Explain `provideAppCheck` (or third-party) for backend mTLS-style identity. — 4m
991. Explain CSP and how to allow Angular runtime safely. — 5m
992. Explain a "trusted types" policy that Angular ships in v21. — 5m
993. Explain how to find prod-only crashes via source maps. — 4m
994. Explain `ng build --source-map=hidden`. — 3m
995. Explain how to integrate Sentry or similar with Angular. — 5m
996. Explain "feature flags" with DI tokens. — 5m
997. Implement a `featureFlag(name)` helper backed by a config token. — 6m
998. Explain how to ship per-tenant config via SSR injection. — 5m
999. Explain a strategy to migrate a 200-component app from NgModules to standalone. — 7m
1000. Explain the order in which you'd adopt: standalone → control flow → signals → Signal Forms → zoneless → incremental hydration. — 7m
