# Easy — 1000 Questions

Target audience: junior / first-job candidates. Budget: **1–3 minutes per question**. Answers are not included by design — verify yourself against the official docs or the Angular 21 feature list in the [root README](../README.md).

> Time format: `— Xm` means the suggested upper bound in minutes for a clean, spoken answer.

---

## HTML Fundamentals (1–50)

1. What does HTML stand for and what is its role on the web? — 1m
2. Name three differences between HTML and XHTML. — 2m
3. What is the purpose of the `<!DOCTYPE html>` declaration? — 1m
4. Which HTML element holds metadata that is not rendered on screen? — 1m
5. List five semantic HTML5 elements and what each represents. — 2m
6. What is the difference between block-level and inline elements? Give two examples of each. — 2m
7. Why prefer `<button>` over `<div onclick>`? — 2m
8. What attribute associates a `<label>` with an input? — 1m
9. Name three valid `<input>` types added in HTML5. — 1m
10. What does the `alt` attribute on `<img>` do and when can it be empty? — 2m
11. What is the purpose of the `<picture>` element? — 2m
12. Difference between `<section>`, `<article>`, and `<div>`. — 2m
13. What does the `defer` attribute on `<script>` do? — 2m
14. Difference between `defer` and `async` on `<script>`. — 2m
15. What is the `<meta charset>` tag and why is it usually `utf-8`? — 1m
16. What is the purpose of the viewport meta tag for mobile? — 2m
17. Difference between `id` and `class` attributes. — 1m
18. What is `data-*` and when do you use it? — 2m
19. What does the `lang` attribute on `<html>` do? — 1m
20. Name three attributes used for form validation in HTML5. — 2m
21. What is the difference between `GET` and `POST` form submissions? — 2m
22. What is the `<template>` element used for? — 2m
23. What is the `<dialog>` element and what method opens it? — 2m
24. What does `contenteditable` do? — 1m
25. What is `tabindex` and what values are common? — 2m
26. Difference between `<strong>` and `<b>`. — 1m
27. Difference between `<em>` and `<i>`. — 1m
28. What is the role of the `<main>` element? — 1m
29. What is ARIA and why does it exist alongside semantic HTML? — 2m
30. Name three landmark roles defined by ARIA. — 2m
31. What is `aria-label` and when do you use it instead of a `<label>`? — 2m
32. What is `role="button"` and when is it acceptable to use? — 2m
33. What is the difference between `hidden` attribute and `display:none`? — 2m
34. What does the `download` attribute on `<a>` do? — 1m
35. What is the `rel="noopener"` attribute for? — 2m
36. What is the `rel="preload"` link used for? — 2m
37. Name three valid values for `<input type="text">`'s `autocomplete` attribute. — 1m
38. What is the `<noscript>` tag? — 1m
39. What is a "void element" in HTML? Give three examples. — 2m
40. What does the `form` attribute on an input that lives outside a `<form>` do? — 2m
41. What is the difference between `disabled` and `readonly` on inputs? — 2m
42. Name three `<input>` attributes that control numeric validation. — 1m
43. What does the `name` attribute do on a form control? — 1m
44. What is the `<output>` element used for? — 1m
45. What is the difference between `<ol>` and `<ul>`? — 1m
46. What is the `<dl>` element and what does it pair with? — 1m
47. What does the `colspan` attribute do? — 1m
48. What is the `<th scope>` attribute used for? — 2m
49. Why should every page have exactly one `<h1>`? — 1m
50. What is the difference between `<iframe>` and `<embed>`? — 2m

## CSS Fundamentals (51–110)

51. What are the three ways to apply CSS to a page? — 1m
52. What is specificity and how is it calculated? — 3m
53. What does `!important` do and when is it appropriate? — 2m
54. Explain the CSS box model. — 2m
55. Difference between `box-sizing: content-box` and `border-box`. — 2m
56. What is the difference between `margin` collapsing and `padding`? — 2m
57. Difference between `position: relative` and `position: absolute`. — 2m
58. What does `position: fixed` do? — 1m
59. What is `position: sticky`? — 2m
60. Name three values of the `display` property. — 1m
61. What does `display: none` vs `visibility: hidden` do? — 2m
62. What is the difference between `em`, `rem`, `px`, and `%` units? — 3m
63. What is a CSS pseudo-class? Give three examples. — 2m
64. What is a CSS pseudo-element? Give three examples. — 2m
65. Difference between `::before` and `:before`. — 1m
66. What does the universal selector `*` do? — 1m
67. What does the descendant combinator (space) mean? — 1m
68. What does the child combinator `>` mean? — 1m
69. What does the adjacent-sibling combinator `+` mean? — 1m
70. What does `:nth-child(odd)` select? — 1m
71. Difference between `:nth-child(2)` and `:nth-of-type(2)`. — 2m
72. What is `:not()` and what does it accept? — 2m
73. What is the difference between Flexbox and Grid? — 3m
74. Name the three Flexbox axis-related properties. — 2m
75. What does `justify-content` do? — 1m
76. What does `align-items` do? — 1m
77. What is `flex: 1 1 0`? — 2m
78. What is the default `flex-direction`? — 1m
79. Name three values of `flex-wrap`. — 1m
80. What is the purpose of `gap` in Flexbox and Grid? — 1m
81. What does `grid-template-columns: 1fr 2fr` produce? — 2m
82. What does `grid-area` do? — 2m
83. What is the difference between `grid-template-areas` and explicit `grid-column`/`grid-row` placement? — 3m
84. What is a CSS custom property (variable) and how is it read? — 2m
85. Can CSS variables be themed at runtime? Briefly how. — 2m
86. What is the difference between `transition` and `animation`? — 2m
87. Name three properties that are cheap to animate. — 2m
88. What does `will-change` hint to the browser? — 2m
89. What is `transform: translateZ(0)` commonly used for? — 2m
90. What is a CSS media query? Give a basic syntax example. — 2m
91. Name three common breakpoints. — 1m
92. What is a "mobile first" CSS strategy? — 2m
93. What does `min()` / `max()` / `clamp()` do? — 2m
94. What is the `aspect-ratio` property? — 1m
95. What is CSS specificity inheritance? — 2m
96. Which properties inherit by default? — 2m
97. What is the `inherit` keyword? — 1m
98. What does `currentColor` mean? — 1m
99. What is `rgba()` vs `hsl()`? — 2m
100. What is a "BEM" naming convention? — 2m
101. What is the difference between a CSS reset and `normalize.css`? — 2m
102. What is a "stacking context"? — 3m
103. Name three things that create a new stacking context. — 2m
104. What does `overflow: hidden` do? — 1m
105. Difference between `overflow-x` and `overflow-y`. — 1m
106. What does `pointer-events: none` do? — 1m
107. What is the `appearance` property used for? — 2m
108. What is the `:focus-visible` pseudo-class? — 2m
109. What does `prefers-color-scheme` media feature detect? — 1m
110. What does `prefers-reduced-motion` allow you to do? — 2m

## JavaScript Fundamentals (111–190)

111. Difference between `var`, `let`, and `const`. — 2m
112. What is hoisting? — 2m
113. What is the Temporal Dead Zone? — 2m
114. What is a closure? Give a one-line example. — 3m
115. What are the primitive types in JavaScript? — 1m
116. What is the difference between `==` and `===`? — 2m
117. What does `typeof null` return and why? — 1m
118. What is the difference between `null` and `undefined`? — 2m
119. What does `NaN === NaN` evaluate to? — 1m
120. How do you check if a value is `NaN` reliably? — 1m
121. Difference between function declaration and function expression. — 2m
122. What is an arrow function and how does it differ from a regular function? — 2m
123. Do arrow functions have their own `this`? — 1m
124. What is the value of `this` inside a method called as `obj.method()`? — 1m
125. What does `bind()` do? — 2m
126. What does `call()` vs `apply()` do? — 1m
127. What is the difference between synchronous and asynchronous code? — 2m
128. What is the event loop? — 3m
129. What is a microtask vs macrotask? — 2m
130. In what order do `Promise.resolve().then(...)` and `setTimeout(..., 0)` run? — 2m
131. What does `await` do? — 1m
132. Can you `await` outside an `async` function? When? — 1m
133. What is a Promise's three states? — 1m
134. What does `Promise.all([])` return? — 1m
135. Difference between `Promise.all` and `Promise.allSettled`. — 2m
136. What does `Promise.race` do? — 1m
137. What is a Symbol and what is it useful for? — 2m
138. What is `Object.freeze` and is it deep? — 2m
139. Difference between shallow copy and deep copy. — 2m
140. How do you shallow-copy an object? Give two ways. — 2m
141. What is destructuring? Give an example for arrays and objects. — 2m
142. What is the spread operator and what does it do? — 1m
143. What is the rest parameter? — 1m
144. What does `Array.prototype.map` return? — 1m
145. Difference between `map` and `forEach`. — 1m
146. What does `Array.prototype.reduce` do? — 2m
147. Difference between `find` and `filter`. — 1m
148. What does `Array.prototype.flat()` do? — 1m
149. What does `Array.prototype.flatMap()` do? — 1m
150. What does `Array.from` do? — 1m
151. What is the difference between `Array.isArray` and `typeof` for arrays? — 1m
152. What is template literal syntax? — 1m
153. What is a tagged template literal? — 2m
154. What does `Object.keys()` return? — 1m
155. Difference between `for...in` and `for...of`. — 2m
156. What is an iterator? — 2m
157. What is a generator function (`function*`)? — 2m
158. What does `Set` data structure do? — 1m
159. What does `Map` data structure do? — 1m
160. Difference between `Map` and a plain object. — 2m
161. What is `WeakMap` and why is it "weak"? — 2m
162. What is the difference between deep and shallow equality? — 2m
163. What does `JSON.stringify` do with `undefined` values? — 1m
164. What does `try / catch / finally` do? — 1m
165. What does `throw` do? — 1m
166. What is event delegation? — 3m
167. What is `event.stopPropagation()`? — 1m
168. Difference between `event.preventDefault()` and `return false`. — 2m
169. What is the difference between `addEventListener` and `onclick`? — 2m
170. What is the difference between `localStorage` and `sessionStorage`? — 2m
171. How much data can `localStorage` typically hold? — 1m
172. What is a cookie and what attribute makes it HTTP-only? — 2m
173. What is CORS in one sentence? — 2m
174. What is JSON Web Token (JWT) in one sentence? — 2m
175. What does `fetch` return? — 1m
176. How do you read a JSON response from `fetch`? — 1m
177. What does `AbortController` do? — 2m
178. What is a "thenable"? — 1m
179. What is `Symbol.iterator`? — 2m
180. What is the prototype chain? — 3m
181. What does `Object.create(null)` produce? — 1m
182. What is a "pure function"? — 1m
183. Difference between mutating and non-mutating array methods. — 2m
184. What does `Array.prototype.sort` do by default? — 1m
185. What is the difference between `concat` and the spread operator for arrays? — 1m
186. What does `Array.prototype.includes` do? — 1m
187. What does `Number.isInteger` check? — 1m
188. What is `BigInt`? — 1m
189. What is `globalThis`? — 1m
190. What is "use strict" and what does it change? — 2m

## TypeScript Fundamentals (191–240)

191. What is TypeScript and how does it relate to JavaScript? — 1m
192. Difference between `any` and `unknown`. — 2m
193. What is `never` and when does it appear? — 2m
194. Difference between `interface` and `type`. — 2m
195. Can you extend an `interface`? Can you extend a `type`? — 2m
196. What is a union type? Give an example. — 1m
197. What is an intersection type? — 1m
198. What is a literal type? — 1m
199. What is a discriminated (tagged) union? — 3m
200. What does the `readonly` modifier do on a property? — 1m
201. What does `as const` do? — 2m
202. What is type narrowing? Give one example. — 2m
203. What is the `keyof` operator? — 2m
204. What is `typeof` in TypeScript? — 1m
205. What is a generic? Show a generic function signature. — 2m
206. What does `extends` mean in a generic constraint? — 2m
207. What is `Partial<T>`? — 1m
208. What is `Required<T>`? — 1m
209. What is `Pick<T, K>`? — 1m
210. What is `Omit<T, K>`? — 1m
211. What is `Record<K, V>`? — 1m
212. What is `Readonly<T>`? — 1m
213. What is `ReturnType<T>`? — 1m
214. What does the non-null assertion `!` do? — 2m
215. Difference between `as Type` cast and `<Type>` cast. — 1m
216. What is a tuple? — 1m
217. What is the difference between `void` and `undefined` as return types? — 2m
218. What does `enum` do? — 1m
219. Difference between numeric and string enums. — 2m
220. What is `const enum`? — 2m
221. What is module augmentation? — 2m
222. What is a declaration file (`.d.ts`)? — 1m
223. What does `strict: true` enable in `tsconfig`? — 2m
224. What is `noImplicitAny`? — 1m
225. What is `strictNullChecks`? — 2m
226. What is the difference between `interface` merging and `type` alias re-declaration? — 2m
227. What is a mapped type? — 2m
228. What is a conditional type? — 3m
229. What does the `infer` keyword do? — 3m
230. What is a "branded" or "nominal" type pattern? — 2m
231. What is `unknown` better than `any` for catch clause variables? — 2m
232. What does `satisfies` do? — 2m
233. What is optional chaining `?.`? — 1m
234. What is nullish coalescing `??`? — 1m
235. Difference between `??` and `||`. — 2m
236. What is a function overload? — 2m
237. How do you type a function that accepts a callback? — 2m
238. What is `void` as a parameter type in a callback? — 2m
239. What does the `?` modifier on a parameter do? — 1m
240. How do you type the rest parameters `(...args: ...)`? — 1m

## DOM & Browser APIs (241–280)

241. What is the DOM? — 1m
242. What is the difference between `getElementById` and `querySelector`? — 2m
243. What does `querySelectorAll` return? — 1m
244. Is the return of `querySelectorAll` live or static? — 1m
245. What is the difference between `innerHTML` and `textContent`? — 2m
246. Why is `innerHTML` a security risk? — 2m
247. How do you create a new element programmatically? — 1m
248. What does `appendChild` vs `append` differ in? — 2m
249. What is event bubbling? — 2m
250. What is event capturing? — 2m
251. What is the `passive` listener option used for? — 2m
252. What is the difference between `MouseEvent` and `PointerEvent`? — 2m
253. What is the `IntersectionObserver` API used for? — 2m
254. What does `MutationObserver` do? — 2m
255. What does `ResizeObserver` do? — 2m
256. What is `requestAnimationFrame`? — 2m
257. Difference between `setTimeout(fn,0)` and `requestAnimationFrame(fn)`. — 2m
258. What is a `MediaQueryList` and how do you listen for changes? — 2m
259. What is the `History` API? — 2m
260. What does `history.pushState` do? — 2m
261. What is the difference between `pushState` and `replaceState`? — 1m
262. What event fires when the user clicks the browser back button? — 1m
263. What does `window.matchMedia` do? — 2m
264. What is `navigator.clipboard.writeText` used for? — 1m
265. What permissions are required to read the clipboard? — 2m
266. What is the `Notification` API? — 1m
267. What is a service worker? — 2m
268. What is the difference between a service worker and a web worker? — 2m
269. What runs first: `DOMContentLoaded` or `load`? — 1m
270. What is `document.readyState`? — 1m
271. What does `requestIdleCallback` do? — 2m
272. What is the `URL` class and what does `new URL(href, base)` give you? — 1m
273. What is `URLSearchParams` for? — 1m
274. What is a `FormData` object? — 1m
275. What does `structuredClone` do? — 1m
276. What is a `Blob` vs a `File`? — 2m
277. What is `IndexedDB` in one sentence? — 2m
278. What is the `BroadcastChannel` API? — 2m
279. What is the difference between `scrollIntoView` options `smooth` vs `instant`? — 1m
280. What is `dataset` on an HTMLElement? — 1m

## Angular CLI & Setup (281–320)

281. What command creates a new Angular project? — 1m
282. What command serves an app locally? — 1m
283. What is the default port for `ng serve`? — 1m
284. What command runs unit tests? — 1m
285. What command generates a new standalone component? — 1m
286. What command generates a new service? — 1m
287. What command updates Angular and its packages? — 1m
288. What is `angular.json` in one sentence? — 1m
289. What is `package.json` vs `angular.json`? — 2m
290. What is the difference between `ng build` and `ng build --configuration=production`? — 2m
291. Where does `ng build` output by default? — 1m
292. What does the `--prerender` flag do on `ng build`? — 2m
293. What is the difference between `ng add` and `npm install`? — 2m
294. What does `ng update --next` do? — 1m
295. What is a workspace vs a project in Angular CLI terms? — 2m
296. What is the purpose of `tsconfig.app.json` vs `tsconfig.json`? — 2m
297. What does `ng generate config` do? — 2m
298. What is the default build tool used by Angular 21? — 1m
299. What is the default dev-server tool used by Angular 21? — 1m
300. What is `provideRouter` and where is it typically called? — 2m
301. What is `bootstrapApplication` and how does it differ from `platformBrowserDynamic().bootstrapModule`? — 2m
302. What does `ng deploy` do? — 1m
303. What is the purpose of a workspace's `schematics`? — 2m
304. How do you generate a component with a specific change-detection strategy via CLI? — 2m
305. What does `ng lint` do? — 1m
306. What is the role of `eslint.config.js` in an Angular project? — 1m
307. What does `ng e2e` do? — 1m
308. How do you skip generating tests when scaffolding a component? — 1m
309. What does `--standalone` mean when generating? — 1m
310. What is the difference between `--inline-template` and `--inline-style`? — 1m
311. What does the `polyfills` build option do? — 2m
312. What environment files exist by default and what are they for? — 2m
313. How do you add a new build configuration? — 2m
314. What is the difference between `assets` and `styles` in `angular.json`? — 2m
315. What is `ngHttpServer` or `ng serve --ssr`? — 2m
316. What does the SSR builder add to your project? — 2m
317. What is `angular.json`'s `optimization` field for? — 2m
318. What is `aot` and is it the default in production? — 1m
319. What does `ng cache` do? — 1m
320. What does `ng analytics` control? — 1m

## Standalone Components & Architecture (321–360)

321. What is a standalone component? — 2m
322. What property identifies a component as standalone? — 1m
323. Are NgModules required in Angular 21? — 1m
324. What is `bootstrapApplication` and what does its `providers` array hold? — 2m
325. What does the `imports` array on a component contain? — 1m
326. Can a standalone component import another standalone component? — 1m
327. Can a standalone component import a directive without an NgModule? — 1m
328. How do you provide HttpClient in a standalone app? — 2m
329. How do you provide the Router in a standalone app? — 1m
330. How do you import a third-party module into a standalone component? — 2m
331. What is `provideHttpClient(withInterceptors([...]))`? — 2m
332. What does `provideZonelessChangeDetection()` do? — 2m
333. What does `provideClientHydration()` do? — 2m
334. What is the difference between `providers` on a component and a route's `providers`? — 2m
335. What is `EnvironmentInjector`? — 2m
336. What is `ElementInjector`? — 2m
337. What is the role of `@Injectable({ providedIn: 'root' })`? — 2m
338. Is `providedIn: 'root'` tree-shakeable? — 1m
339. What is the difference between `providedIn: 'root'` and providing in `bootstrapApplication`? — 2m
340. What is a feature provider (e.g., `withFetch`)? — 2m
341. What is `loadComponent` in routing? — 1m
342. What is `loadChildren` in routing? — 1m
343. Can a standalone component declare `selector: 'app-foo'`? — 1m
344. Where do you put global styles in a standalone-only app? — 1m
345. What is `@defer` and where do you use it? — 1m
346. What is a "host component" in routing terms? — 2m
347. Can a standalone component still be lazy-loaded? — 1m
348. What does `RouterOutlet` need to be imported by? — 1m
349. What is the purpose of `inject()` over constructor injection? — 2m
350. Where can `inject()` be called? — 2m
351. What is `runInInjectionContext`? — 2m
352. What is `assertInInjectionContext`? — 1m
353. What does `inject(ChangeDetectorRef)` give you? — 1m
354. What does `inject(ElementRef)` give you? — 1m
355. What is the role of `DOCUMENT` injection token? — 2m
356. What is the purpose of `PLATFORM_ID` and `isPlatformBrowser`? — 2m
357. What is the difference between providing at root vs at a component vs at a route? — 3m
358. Why prefer standalone over NgModules in new code? — 2m
359. What is a `provideExperimentalZonelessChangeDetection`-style API used for historically? — 1m
360. What does `provideAnimationsAsync()` do? — 2m

## Templates, Interpolation & Bindings (361–420)

361. What is interpolation syntax in an Angular template? — 1m
362. Can interpolation contain function calls? Should it? — 2m
363. What is property binding syntax `[prop]="expr"`? — 1m
364. What is event binding syntax `(event)="handler($event)"`? — 1m
365. What is two-way binding `[(ngModel)]`? — 1m
366. What is the "banana in a box" syntax and what does it desugar to? — 2m
367. What is the difference between `{{ x }}` and `[innerText]="x"`? — 2m
368. Why does `[disabled]` work but `disabled=""` not toggle dynamically? — 2m
369. What is attribute binding `[attr.aria-label]="..."`? — 2m
370. Why use attribute binding instead of property binding for `aria-*`? — 2m
371. What is class binding `[class.active]="x"`? — 1m
372. What is `[class]="expr"` with an object or string used for? — 2m
373. What is style binding `[style.color]="x"`? — 1m
374. What is `[style.width.px]="w"` for? — 1m
375. What is `[ngStyle]` and is it still recommended? — 2m
376. What is `[ngClass]` and is it still recommended? — 2m
377. What is the syntax for an event handler with `$event`? — 1m
378. Can a template event handler return a value used by Angular? — 1m
379. What is `keydown.enter` pseudo-event? — 1m
380. What is `keydown.control.enter` for? — 1m
381. What does `$event.preventDefault()` do in a template handler? — 1m
382. What does `(click)="onClick(); $event.stopPropagation()"` do? — 1m
383. What is template reference variable syntax `#name`? — 1m
384. What can you do with a template reference variable? — 2m
385. What is `@let` in a template? — 1m
386. Why is `@let` preferable to repeated expression evaluation? — 2m
387. What is the syntax of `@if` and `@else if` and `@else`? — 1m
388. What is the syntax of `@for` and what does `track` do? — 2m
389. Why is `track` required on `@for`? — 2m
390. What is `$index` in `@for`? — 1m
391. What other implicit variables does `@for` expose? — 2m
392. What is `@empty` used for inside `@for`? — 1m
393. What is the syntax of `@switch`, `@case`, `@default`? — 1m
394. What is the difference between `@if` and `*ngIf`? — 1m
395. Why is `@if` preferred over `*ngIf` in v21? — 2m
396. What is `@defer` block syntax? — 2m
397. Name three triggers for `@defer`. — 1m
398. What does `@placeholder` do inside a `@defer`? — 1m
399. What does `@loading` do inside a `@defer`? — 1m
400. What does `@error` do inside a `@defer`? — 1m
401. What is the difference between `@defer (on idle)` and `@defer (on viewport)`? — 2m
402. What does `@defer (when expr)` mean? — 2m
403. What is `@defer (on interaction)` and how does it know which element to listen on? — 2m
404. What is `@defer (on hover)`? — 1m
405. What is `@defer (on immediate)`? — 1m
406. What is `@defer (on timer(2s))`? — 1m
407. Can you nest `@defer` blocks? — 1m
408. What is `*ngTemplateOutlet`? — 2m
409. What is `<ng-template>`? — 2m
410. What is `<ng-container>` used for? — 2m
411. Difference between `<ng-template>` and `<ng-container>`. — 2m
412. What is structural directive syntax `*directive`? — 2m
413. What does the `*` prefix desugar to? — 2m
414. What is template-level `let-name="value"` for? — 2m
415. Can you have multiple `<router-outlet>` in one template? — 1m
416. Can a template call a component method on every change detection? Why is that bad? — 2m
417. What is a "pure pipe" vs an "impure pipe" effect on the template? — 2m
418. What does the `async` pipe do? — 2m
419. What does the `async` pipe do on component destroy? — 1m
420. Can you bind to a signal in a template by writing `{{ count() }}`? — 1m

## Built-in Directives (421–460)

421. List the built-in structural directives still available pre-v17. — 1m
422. What replaced `*ngIf` in modern Angular? — 1m
423. What replaced `*ngFor` in modern Angular? — 1m
424. What replaced `*ngSwitch` in modern Angular? — 1m
425. Is `*ngIf` still functional in v21? — 1m
426. What is `NgClass` and is there a `[class]` equivalent? — 2m
427. What is `NgStyle` and is there a `[style]` equivalent? — 2m
428. What is `NgPlural` used for? — 2m
429. What is `NgComponentOutlet`? — 2m
430. What does `NgTemplateOutlet` accept? — 2m
431. What is the purpose of `RouterLink`? — 1m
432. What is `RouterLinkActive` and how do you toggle a class with it? — 2m
433. What is `routerLinkActiveOptions` for? — 2m
434. What is `FormsModule` for and what directive does it bring? — 2m
435. What is `ReactiveFormsModule` for (legacy)? — 1m
436. What is the `FormField` directive in Signal Forms? — 1m
437. Difference between `[formField]` and `[formControl]`. — 2m
438. What is the `ngModel` directive doing under the hood? — 2m
439. What is `ngForm` for? — 2m
440. How do you import a single directive without its whole module in v21? — 2m
441. What is `[hidden]` and how is it different from `@if`? — 2m
442. What does `[innerHTML]` do, and what sanitization happens? — 2m
443. What is `attr` binding for booleans like `aria-expanded`? — 2m
444. What does `[draggable]` binding do? — 1m
445. What is `RouterOutlet` and what classes does it add? — 2m
446. Can directives have inputs? — 1m
447. Can directives have outputs? — 1m
448. What is the difference between a structural and an attribute directive? — 2m
449. Can a directive have a selector like `[appHighlight]`? — 1m
450. What is `exportAs` on a directive? — 2m
451. How do you reference an exported directive in a template? — 2m
452. What is `HostBinding` and its modern `host` equivalent? — 2m
453. What is `HostListener` and its modern `host` equivalent? — 2m
454. What does the `host` metadata object on a component support? — 2m
455. What is `:host` in component styles? — 1m
456. What is `:host-context` in component styles? — 2m
457. What is view encapsulation? — 2m
458. Name the three view encapsulation modes. — 1m
459. What is `ViewEncapsulation.None` and the risk? — 2m
460. What is `ViewEncapsulation.ShadowDom`? — 2m

## Built-in Pipes (461–500)

461. What is a pipe? — 1m
462. What pipe converts a Date object to a string? — 1m
463. What is the default `DatePipe` format? — 1m
464. What does the `UpperCasePipe` do? — 1m
465. What does the `LowerCasePipe` do? — 1m
466. What does the `TitleCasePipe` do? — 1m
467. What does the `CurrencyPipe` do? — 1m
468. What does the `DecimalPipe` do? — 1m
469. What is the `PercentPipe`? — 1m
470. What does the `JsonPipe` do and when is it useful? — 1m
471. What is the `SlicePipe`? — 1m
472. What is the `KeyValuePipe`? — 1m
473. What is the `I18nPluralPipe`? — 1m
474. What is the `I18nSelectPipe`? — 1m
475. What is the `AsyncPipe`? — 1m
476. What does `AsyncPipe` do with Observables vs Promises? — 2m
477. Does `AsyncPipe` work with signals? — 1m
478. How do you read a signal in a template — pipe or call? — 1m
479. Can you chain pipes? Give syntax. — 1m
480. Can you pass arguments to a pipe? Give syntax. — 1m
481. How do you make a custom pipe? — 2m
482. What property on `@Pipe` enables impure behavior? — 1m
483. What is the cost of an impure pipe? — 2m
484. Why is `JsonPipe` impure? — 1m
485. What is the import path for `CommonModule` pipes in standalone components? — 2m
486. How do you import `DatePipe` into a standalone component? — 1m
487. Can you use a pipe in component code (not template)? How? — 2m
488. Why is `new DatePipe(...).transform()` discouraged? — 2m
489. What does `formatDate` from `@angular/common` do? — 1m
490. What is the difference between `currency` and `number` pipes? — 1m
491. What does `'1.2-2'` mean as a digit-info argument? — 2m
492. How does locale affect the `DatePipe`? — 2m
493. How do you register additional locale data? — 2m
494. What pipe formats file sizes (built-in)? — 1m
495. Does Angular ship a "truncate" pipe? — 1m
496. Does Angular ship a "sort" pipe? — 1m
497. Why doesn't Angular ship a "sort" pipe? — 2m
498. What is `LowerCasePipe` vs `String.prototype.toLowerCase()` in templates? — 2m
499. Why prefer a pipe over a method call in templates? — 2m
500. What is the difference between pure pipes and `computed()` signals? — 2m

## Parent-Child Communication (501–560)

501. Name three ways a parent passes data to a child. — 2m
502. What is `input()` in v21? — 1m
503. Difference between `@Input()` decorator and `input()` signal. — 2m
504. How do you mark an input as required? — 1m
505. How do you provide a default value for an input? — 1m
506. What is an input `transform` function? — 2m
507. Give an example of a boolean-attribute transform. — 2m
508. What is `output()` in v21? — 1m
509. How do you emit a value via `output()`? — 1m
510. Difference between `@Output()` `EventEmitter` and `output()`. — 2m
511. What is `model()` and what does it give you? — 2m
512. What is the difference between `input()`, `output()`, and `model()`? — 2m
513. How does the parent two-way bind to a `model()` input? — 2m
514. What is the alias parameter on `input` / `output`? — 1m
515. Can a parent pass a function as an input? When is that a smell? — 2m
516. Can a child call a parent method directly? How? — 2m
517. What is `viewChild()` in v21? — 1m
518. What is `viewChildren()` in v21? — 1m
519. What is `contentChild()` in v21? — 1m
520. What is `contentChildren()` in v21? — 1m
521. What is the difference between `viewChild` and `contentChild`? — 2m
522. Are signal queries available synchronously in the constructor? — 1m
523. When are signal queries first populated? — 2m
524. What does `{ read: ElementRef }` option on a query do? — 2m
525. What does content projection do? — 2m
526. What is `<ng-content>`? — 1m
527. What is the `select` attribute on `<ng-content>`? — 2m
528. Give an example of multi-slot projection. — 2m
529. Can you project nothing into a slot? What happens? — 1m
530. What is fallback content in `<ng-content>` (v18+)? — 2m
531. How does content projection interact with `ng-template`? — 2m
532. Can a child component read what was projected into it? — 1m
533. What is the difference between a service-based parent-child communication and inputs/outputs? — 3m
534. What is a "shared service" pattern? — 2m
535. Why prefer signals over BehaviorSubject for sharing state? — 2m
536. How does change detection flow between parent and child? — 2m
537. If a parent updates an input, when does the child re-render? — 2m
538. What is the OnPush change detection strategy? — 2m
539. Why pair OnPush with signals or async pipe? — 2m
540. What is the difference between `Output<T>` and `EventEmitter<T>`? — 2m
541. Can `output()` be `void`? — 1m
542. What is `subscribe` doing on an `EventEmitter`? — 1m
543. What is the lifecycle order of parent-child component creation? — 2m
544. What is `AfterViewInit` for? — 1m
545. What is `AfterContentInit` for? — 1m
546. When does `OnChanges` fire for an `input()` signal? — 2m
547. What is the v21-preferred alternative to `ngOnChanges` for tracking input changes? — 2m
548. What is the cost of passing a new object identity to a child every CD cycle? — 2m
549. Why does passing a new array reference to a child invalidate OnPush? — 2m
550. What is the recommended way to deeply update a model input? — 2m
551. Can a parent style a child? How? — 2m
552. What is the `::part` CSS selector and when is it useful? — 2m
553. What is `attr.aria-labelledby` and how do parents propagate it? — 2m
554. What is the recommended way to call a child method from a parent? — 2m
555. Should you use `@ViewChild(SomeService)`? — 1m
556. What is the difference between `viewChild.required` and `viewChild`? — 2m
557. Can content children be queried across multiple projected slots? — 2m
558. What is "host-controlled state" anti-pattern? — 2m
559. How does input binding interact with route parameters via `withComponentInputBinding()`? — 2m
560. How do you handle bidirectional data flow without `model()`? — 2m

## Content Projection (561–590)

561. What is the purpose of content projection? — 1m
562. Where does projected content live in the DOM? — 2m
563. What is single-slot projection? — 1m
564. What is multi-slot projection? — 1m
565. What CSS selector form works in `<ng-content select>`? — 2m
566. Can you project structural directives like `@if`? — 2m
567. What is the difference between projection and dynamic components? — 2m
568. Can projected content reference parent context? — 2m
569. What is the difference between "transcluded" content and child views? — 2m
570. What is `@ContentChild()` and its signal equivalent? — 2m
571. Can you have nested `<ng-content>` elements? — 1m
572. What is a "card" component a good example of for projection? — 2m
573. How do you provide default content when nothing is projected? — 1m
574. What is `ng-content` `*ngIf` interaction? Is that allowed? — 2m
575. What happens to projected content if the host removes its `<ng-content>`? — 2m
576. Does projected content count for `viewChild` queries? — 2m
577. Does projected content count for `contentChild` queries? — 2m
578. How do you style projected content from a host? — 2m
579. What does `::ng-deep` do and why is it discouraged? — 2m
580. What are CSS Custom Properties as the modern replacement for `::ng-deep`? — 2m
581. Can `ng-content select="[slot=foo]"` match elements with a `slot` attribute? — 2m
582. What is "named slot" projection by attribute? — 2m
583. How do you project a list of children into an enumerated layout? — 2m
584. Can the host component reorder projected content? — 2m
585. Can you conditionally project content using `@if` around `<ng-content>`? — 2m
586. What is `<ng-template>` plus `ngTemplateOutlet` versus projection? — 2m
587. When should you prefer `<ng-template>` over projection? — 2m
588. What is a "templated component" pattern? — 2m
589. What is the v21-preferred way to forward attributes to projected children? — 2m
590. Why does projecting form controls require care with `FormField`? — 2m

## Signals Basics (591–650)

591. What is a signal? — 1m
592. How do you create a writable signal? — 1m
593. How do you read a signal's value? — 1m
594. How do you set a signal's value? — 1m
595. What is `.update()` on a signal? — 1m
596. What is `.asReadonly()`? — 2m
597. What is a `computed()` signal? — 1m
598. Is `computed()` lazy or eager? — 2m
599. Is `computed()` memoized? — 1m
600. What is a "reactive context"? — 2m
601. What contexts does Angular consider reactive? — 2m
602. What is `untracked()`? — 2m
603. When would you use `untracked()`? — 2m
604. What is `effect()`? — 1m
605. When does an `effect()` first run? — 1m
606. What is the lifecycle of an `effect()`? — 2m
607. Can you write to a signal inside an `effect()`? — 2m
608. What is the `allowSignalWrites` option? — 2m
609. Why is writing to signals in an effect generally an anti-pattern? — 3m
610. What is `linkedSignal()`? — 1m
611. When does `linkedSignal()` reset? — 2m
612. What is the difference between `computed()` and `linkedSignal()`? — 2m
613. What is the `{ source, computation }` form of `linkedSignal()`? — 2m
614. What is the `previous` argument inside `linkedSignal` computation? — 2m
615. When would you use `linkedSignal` over a plain `signal`? — 2m
616. What is `resource()` in v21? — 1m
617. What are the two main `resource()` options? — 1m
618. What is the difference between `resource` and `httpResource`? — 1m
619. What does `resource.value()` return when loading? — 1m
620. What does `resource.hasValue()` mean? — 1m
621. What does `resource.isLoading()` mean? — 1m
622. What does `resource.error()` return? — 1m
623. List the possible values of `resource.status()`. — 2m
624. What is `resource.reload()` for? — 1m
625. What is `abortSignal` in a `resource` loader? — 2m
626. How do you do optimistic updates with a `resource`? — 2m
627. What is `afterRenderEffect()` for? — 2m
628. Difference between `effect()` and `afterRenderEffect()`. — 2m
629. What is `afterNextRender()`? — 2m
630. What is `afterEveryRender()`? — 2m
631. Are signals tracked across `await` boundaries? — 2m
632. What is `signal({ a: 1 })` equality based on? — 2m
633. What is the `equal` option on `signal()` for? — 2m
634. How do you make a signal use deep equality? — 2m
635. What is a `Signal<T>` type vs `WritableSignal<T>`? — 1m
636. How do you type a signal initialized to `[]`? — 1m
637. How do you type a signal that can hold `null`? — 1m
638. What is the difference between a signal and an observable? — 3m
639. When would you still prefer an observable? — 2m
640. How do you convert a signal to an observable? — 1m
641. How do you convert an observable to a signal? — 1m
642. What is `toSignal()`? — 1m
643. What is `toObservable()`? — 1m
644. What is the default initial value of `toSignal(obs$)`? — 1m
645. How do you give `toSignal` a default value? — 1m
646. What does `toSignal({ requireSync: true })` do? — 2m
647. What is the relationship between signals and change detection? — 2m
648. Do signals require zone.js? — 1m
649. How do signals interact with OnPush? — 2m
650. What is the recommended state primitive for new Angular code? — 1m

## Computed & Effect (651–690)

651. What does `computed()` accept? — 1m
652. What does `computed()` return? — 1m
653. Can a computed depend on multiple signals? — 1m
654. What does it mean that computed dependencies are "dynamic"? — 2m
655. How is a computed signal recalculated? — 2m
656. Can you write to a `computed()`? — 1m
657. What error occurs if a computed creates an infinite loop? — 2m
658. What is glitch-free propagation? — 3m
659. What does `effect()` accept? — 1m
660. Does `effect()` return a cleanup function? — 1m
661. How do you register a cleanup inside an `effect()`? — 2m
662. What is `onCleanup` callback inside an effect? — 2m
663. When does an effect stop running? — 2m
664. What is `injector` option on `effect()` for? — 2m
665. What is `manualCleanup` option on `effect()` for? — 2m
666. Why is "syncing one signal to another" with an effect bad? — 2m
667. What pattern replaces the above anti-pattern? — 2m
668. How do you debounce side effects without RxJS? — 2m
669. What's a good use case for `effect()`? — 2m
670. What's a good use case for `afterRenderEffect()`? — 2m
671. When is `afterNextRender()` preferred? — 2m
672. Can effects run on the server (SSR)? — 1m
673. How do you guard an effect to browser-only? — 2m
674. What is the difference between `effect()` and `subscribe()`? — 2m
675. What is `runInInjectionContext`? — 2m
676. Why might you need `runInInjectionContext` around `effect()`? — 2m
677. What happens if you call `effect()` outside an injection context? — 2m
678. What is `DestroyRef`? — 1m
679. How do you register a destroy callback with `DestroyRef`? — 1m
680. What replaces `ngOnDestroy` for a simple cleanup? — 2m
681. What is `takeUntilDestroyed()`? — 1m
682. What does `takeUntilDestroyed()` need to be called within? — 1m
683. What is `OutputRef.subscribe()` vs `output()` consumer-side? — 2m
684. How do you read a signal once without subscribing? — 1m
685. How do you peek a computed without tracking it? — 1m
686. What is "stale closure" risk inside a signal computation? — 2m
687. What happens if a computed depends on `Date.now()`? — 2m
688. How do you make a clock signal that updates every second? — 2m
689. What's wrong with reading `Math.random()` inside a computed? — 2m
690. Why are signals "push" but computed reads are "pull"? — 3m

## Signal Forms Basics (691–750)

691. What package exports Signal Forms? — 1m
692. What function creates a Signal Form? — 1m
693. Does Signal Form structure derive from the model? — 1m
694. What is the safest initial value for a string field — `''`, `null`, or `undefined`? — 1m
695. What is the safest initial value for a number field? — 1m
696. What is the safest initial value for an array field? — 1m
697. What directive binds a field to an input element? — 1m
698. What does `[formField]` automatically handle? — 2m
699. List three forbidden HTML attributes when using `[formField]`. — 2m
700. Where do you place validation rules in Signal Forms? — 1m
701. How do you mark a field required? — 1m
702. How do you conditionally require a field based on another? — 2m
703. What option on `required` enables conditional behavior? — 1m
704. Can the `when` option be used with `pattern()`? — 1m
705. What helper enables conditional non-required rules? — 1m
706. What is `applyEach` for? — 2m
707. How many arguments does the `applyEach` callback take? — 1m
708. How do you iterate a Signal Form array in a template? — 1m
709. What is special about accessing `.length` on a Signal Form array? — 2m
710. Why do you say `form.field()` and not `form.field`? — 2m
711. What does calling a field as a function return? — 1m
712. Why is `form.field.touched()` wrong? — 2m
713. What does `form().valid()` return? — 1m
714. What does `form().invalid()` return? — 1m
715. What does `form().errors()` return? — 1m
716. What is the shape of a `ValidationError`? — 2m
717. What should a synchronous validator return on success? — 1m
718. Why must validators not return `null`? — 1m
719. What is `validate()` used for? — 1m
720. What is `validateAsync()` used for? — 1m
721. What is required (not optional) in `validateAsync()`? — 1m
722. What does `validateAsync` `params` need to be? — 1m
723. What does `validateAsync` `factory` return? — 1m
724. What is `validateHttp()` for? — 1m
725. What is `validateStandardSchema()` for? — 1m
726. How do you mark a field as `disabled` reactively? — 1m
727. How do you mark a field as `readonly` reactively? — 1m
728. How do you mark a field as `hidden` reactively? — 1m
729. Does `hidden()` remove the field from the model? — 1m
730. What does `debounce()` do on a field? — 1m
731. What is `submit(form, async () => {...})`? — 1m
732. Why must the `submit` callback be `async`? — 2m
733. What does `submit` do before the action runs? — 2m
734. Does `submit` run if the form is invalid? — 1m
735. How do you disable the submit button while the form is pending? — 1m
736. Why is `<button [disabled]="form.invalid()">` wrong? — 1m
737. What is the correct expression for disabling submit while pending? — 1m
738. How do you reset a Signal Form? — 1m
739. How do you imperatively update a field's value? — 2m
740. Why is `form.field.set(x)` wrong? — 1m
741. How do you remove an item from an array field? — 2m
742. How do you add an item to an array field? — 2m
743. Can you use `FormBuilder` with Signal Forms? — 1m
744. Can you mix Reactive Forms and Signal Forms in the same component? — 1m
745. Why are checkboxes restricted to boolean fields with `[formField]`? — 2m
746. How do you bind a multi-value array to a `<select>`? — 1m
747. How do you nest sub-forms? — 2m
748. What is `applyWhen(path, cond, schemaFn)`? — 2m
749. Why must `applyWhen` use `valueOf`/`stateOf` instead of calling the path? — 2m
750. What is the `metadata()` helper for? — 2m

## Reactive Forms (Legacy) Basics (751–780)

751. What module exposes Reactive Forms? — 1m
752. What is a `FormControl`? — 1m
753. What is a `FormGroup`? — 1m
754. What is a `FormArray`? — 1m
755. What is `FormBuilder`? — 1m
756. How do you create a control with a default value and a validator? — 2m
757. How do you patch only some values of a group? — 2m
758. Difference between `setValue` and `patchValue`. — 2m
759. How do you subscribe to value changes of a control? — 1m
760. How do you subscribe to status changes of a control? — 1m
761. How do you mark a control as touched? — 1m
762. How do you mark all descendants touched? — 1m
763. What is `markAsPristine` for? — 1m
764. What is `updateValueAndValidity`? — 2m
765. How do you add a validator dynamically? — 2m
766. What is a sync validator's signature? — 1m
767. What is an async validator's signature? — 1m
768. How do you bind a `FormControl` in a template? — 1m
769. What directive is needed for a `FormGroup` in a template? — 1m
770. What is `formControlName`? — 1m
771. What is `formArrayName`? — 1m
772. How do you iterate a `FormArray`'s controls in a template? — 2m
773. What is the difference between `reset()` and `setValue({})`? — 2m
774. What is `disable()` vs `enable()` on a control? — 1m
775. What is the gotcha with disabled controls and `value`? — 2m
776. How do you get the raw value including disabled controls? — 1m
777. How does Reactive Forms compare to Signal Forms in v21? — 2m
778. When would you still pick Reactive Forms in v21? — 2m
779. Why are Reactive Forms not preferred for *new* code in v21? — 2m
780. Can you migrate a Reactive Form to a Signal Form gradually? — 2m

## Services & Dependency Injection (781–830)

781. What is a service in Angular? — 1m
782. How do you make a class injectable? — 1m
783. What does `providedIn: 'root'` do? — 1m
784. What does `providedIn: 'platform'` do? — 2m
785. What is the difference between `providedIn` and providers array? — 2m
786. How do you inject a service into a component? — 1m
787. What is the modern way to inject (function vs constructor)? — 1m
788. What does `inject()` return? — 1m
789. Where can you call `inject()`? — 2m
790. What is `injection context`? — 2m
791. What is `runInInjectionContext` for? — 2m
792. What is the difference between class and factory providers? — 2m
793. What is `useClass`? — 1m
794. What is `useValue`? — 1m
795. What is `useFactory`? — 1m
796. What is `useExisting`? — 2m
797. What is an `InjectionToken`? — 2m
798. Why prefer `InjectionToken` over a string token? — 2m
799. What is `multi: true` on a provider? — 2m
800. Give an example of a multi-provider used in Angular (`HTTP_INTERCEPTORS`). — 2m
801. What is the difference between `providers` and `viewProviders`? — 2m
802. What is `EnvironmentInjector`? — 2m
803. What is `ElementInjector`? — 2m
804. What is the resolution order between Environment and Element injectors? — 3m
805. What is `@Optional()` / `inject(X, { optional: true })`? — 1m
806. What is `@SkipSelf()` / `inject(X, { skipSelf: true })`? — 2m
807. What is `@Self()` / `inject(X, { self: true })`? — 2m
808. What is `@Host()` / `inject(X, { host: true })`? — 2m
809. What is the singleton lifetime of `providedIn: 'root'`? — 2m
810. Can a service depend on another service? — 1m
811. Can a service inject a component? — 1m
812. Can a component inject a child component? — 1m
813. What is `forwardRef`? — 2m
814. When would you need `forwardRef`? — 2m
815. What is a "circular dependency" error in Angular DI? — 2m
816. How do you provide HttpClient? — 1m
817. How do you provide the Router? — 1m
818. How do you provide animations? — 1m
819. What does `provideEnvironmentInitializer` do? — 2m
820. What replaced `APP_INITIALIZER`? — 1m
821. What is a route-level provider? — 2m
822. What is the scope of a route-level provider? — 2m
823. Can a lazy-loaded route have its own providers? — 1m
824. What is `EnvironmentProviders`? — 2m
825. What is the difference between `Provider` and `EnvironmentProviders` types? — 2m
826. How do you provide a value tied to the current locale? — 2m
827. How do you provide a different service in test vs prod? — 2m
828. What is `TestBed.overrideProvider`? — 1m
829. What is `TestBed.inject`? — 1m
830. What is the difference between `inject()` in a service vs in a component? — 2m

## Routing (831–880)

831. What package exports the router? — 1m
832. How do you define a route in standalone? — 1m
833. What is the shape of a `Route`? — 2m
834. What does `path: ''` match? — 1m
835. What does `path: '**'` match? — 1m
836. What is `pathMatch: 'full'`? — 2m
837. What is the default `pathMatch`? — 1m
838. What is `redirectTo`? — 1m
839. What is `component` vs `loadComponent`? — 2m
840. What is `loadChildren`? — 2m
841. What is `children` in a route config? — 2m
842. What is `RouterLink` and how do you bind dynamic segments? — 2m
843. What is `[queryParams]` on `RouterLink`? — 1m
844. What is `[fragment]` on `RouterLink`? — 1m
845. What is `routerLinkActive`? — 1m
846. What is `withComponentInputBinding()` and what does it enable? — 2m
847. With component input binding, how does a route parameter reach a component? — 2m
848. How do you read a route param without input binding? — 2m
849. What is `ActivatedRoute`? — 1m
850. What is `ActivatedRouteSnapshot` vs `ActivatedRoute`? — 2m
851. What does `Router.navigate()` accept? — 2m
852. What does `Router.navigateByUrl()` accept? — 2m
853. Difference between `navigate(['/foo'])` and `navigateByUrl('/foo')`. — 2m
854. What is the `RouterOutlet` directive? — 1m
855. What is a "named outlet" and the URL syntax for it? — 2m
856. What is a route guard? — 1m
857. What is `CanActivateFn`? — 1m
858. What is `CanMatchFn` and why is it preferred for lazy loads? — 2m
859. What is `CanDeactivateFn` for? — 2m
860. What is `ResolveFn` for? — 2m
861. Are class-based guards still supported? Preferred? — 2m
862. What does `provideRouter(routes, withDebugTracing())` do? — 2m
863. What is `withViewTransitions()`? — 2m
864. What is `withInMemoryScrolling()`? — 2m
865. What is `withPreloading(PreloadAllModules)`? — 2m
866. What is the difference between lazy and eager loading? — 2m
867. What is "preloading"? — 2m
868. What is `scrollPositionRestoration`? — 1m
869. What is `anchorScrolling`? — 1m
870. What is `Router.events` and one event you'd subscribe to? — 2m
871. What is `NavigationStart` vs `NavigationEnd`? — 1m
872. What is `RouteReuseStrategy`? — 2m
873. What does `runGuardsAndResolvers: 'always'` do? — 2m
874. What is a `data` property on a route? — 1m
875. What is a `title` property on a route? — 1m
876. How does Angular set the document `<title>` from routes? — 2m
877. How do you redirect with query params preserved? — 2m
878. How do you build a URL programmatically? — 2m
879. What does `relativeTo: this.route` do in `navigate`? — 2m
880. What is the route lifecycle (events order high level)? — 3m

## HttpClient (881–920)

881. What package exports `HttpClient`? — 1m
882. How do you provide `HttpClient` in standalone? — 1m
883. How do you make a GET request? — 1m
884. Does `HttpClient.get` return a Promise or Observable? — 1m
885. How do you parse JSON automatically? — 1m
886. How do you set query parameters? — 2m
887. How do you set headers? — 2m
888. What is `HttpParams`? — 1m
889. What is `HttpHeaders`? — 1m
890. How do you post a JSON body? — 1m
891. How do you upload a file with `HttpClient`? — 2m
892. What does `responseType: 'blob'` give you? — 1m
893. What does `observe: 'response'` give you? — 2m
894. What does `observe: 'events'` give you? — 2m
895. What is an `HttpEvent`? — 2m
896. What is a functional interceptor? — 2m
897. How do you provide interceptors in standalone? — 2m
898. What is `withFetch()`? — 2m
899. What is the difference between XHR-backed and fetch-backed `HttpClient`? — 2m
900. What is `HttpContext`? — 2m
901. What is `HttpContextToken` for? — 2m
902. How do you cancel an HTTP request? — 2m
903. What does `firstValueFrom` do with an HTTP observable? — 2m
904. How do you handle errors from `HttpClient.get`? — 2m
905. What is the difference between `catchError` and `throwError`? — 2m
906. What is `retry()` operator and when to use it? — 2m
907. How do you add a Bearer token via interceptor? — 2m
908. How do you avoid leaking tokens to third-party origins? — 2m
909. What is `HttpClientTestingModule` (legacy) — what replaces it? — 2m
910. What is `HttpTestingController`? — 2m
911. How does `httpResource` differ from calling `HttpClient.get` and wrapping in a `toSignal`? — 2m
912. How do you read query params from a typed object with `HttpParams`? — 2m
913. What does `withCredentials: true` do? — 2m
914. What is a CORS preflight and which HTTP verbs trigger it? — 3m
915. What is the difference between 401 and 403? — 1m
916. What is the difference between 404 and 410? — 1m
917. What status codes mean "success"? — 1m
918. What status code means "no content"? — 1m
919. What status code means "rate limited"? — 1m
920. What status code means "service unavailable"? — 1m

## Lifecycle & Change Detection (921–950)

921. List the classic lifecycle hooks. — 2m
922. When does `ngOnInit` fire relative to constructor? — 2m
923. What is the difference between constructor and `ngOnInit`? — 2m
924. When does `ngOnChanges` fire? — 1m
925. Does `ngOnChanges` fire for signal inputs? — 2m
926. What replaces `ngOnChanges` for signal inputs? — 2m
927. What is `ngAfterViewInit`? — 1m
928. What is `ngAfterContentInit`? — 1m
929. What is `ngDoCheck` and why is it dangerous? — 2m
930. What is `ngOnDestroy`? — 1m
931. What replaces `ngOnDestroy` for simple cleanup? — 1m
932. What is `afterNextRender`? — 2m
933. What is `afterEveryRender`? — 2m
934. Does `afterNextRender` run on the server? — 1m
935. What is the default change detection strategy? — 1m
936. What does `ChangeDetectionStrategy.OnPush` skip? — 2m
937. Name three triggers that re-run CD with OnPush. — 2m
938. What is `ChangeDetectorRef.markForCheck`? — 1m
939. What is `ChangeDetectorRef.detectChanges`? — 1m
940. What is the difference between `markForCheck` and `detectChanges`? — 2m
941. What is "ExpressionChangedAfterItHasBeenChecked" error? — 3m
942. How do you fix the above error (one common way)? — 2m
943. What is the role of `NgZone`? — 2m
944. What does `runOutsideAngular` do? — 2m
945. When is zoneless CD preferable? — 2m
946. Do signals trigger CD in zoneless apps? — 1m
947. Do async pipes trigger CD in zoneless apps? — 1m
948. Does `setTimeout` trigger CD in a zoneless app? — 2m
949. What's a "zone-coupled" library? Example. — 2m
950. How do signals avoid the cost of zone-based CD? — 2m

## Custom Directives & Pipes (951–980)

951. How do you create a custom attribute directive? — 1m
952. What is the selector syntax for an attribute directive? — 1m
953. How do you inject the host element? — 1m
954. How do you bind a class from a directive? — 2m
955. How do you listen to a host event from a directive? — 2m
956. What is the `host` metadata block for in a directive? — 2m
957. What is a structural directive's required template constructor injection? — 2m
958. How does a structural directive show/hide content? — 2m
959. What does `*foo="value"` desugar to? — 2m
960. What is a directive `output()`? — 1m
961. Can a directive have a `model()`? — 1m
962. What is a custom pipe class signature? — 2m
963. What method does a pipe implement? — 1m
964. Is a pipe pure by default? — 1m
965. How do you opt into impure behavior? — 1m
966. How do you parameterize a custom pipe? — 1m
967. How do you inject a service into a custom pipe? — 1m
968. How do you locale-aware-format inside a pipe? — 2m
969. What is the trade-off of doing logic in a pipe vs a `computed()`? — 2m
970. When should a pipe be impure (a real example)? — 2m
971. How do you test a pure pipe? — 2m
972. How do you write a "truncate" pipe? — 2m
973. How do you write a "highlight" attribute directive? — 2m
974. How do you write a "click-outside" directive? — 2m
975. How do you write an "auto-focus" directive? — 2m
976. What is the difference between writing it as a directive vs a component? — 2m
977. Where do you declare custom directives in a standalone setup? — 1m
978. Can a directive be standalone? — 1m
979. Can a pipe be standalone? — 1m
980. What is the import path conventionally used for shared directives? — 1m

## RxJS, Testing, Tooling & Misc (981–1000)

981. What is an Observable in one sentence? — 1m
982. Difference between Subject and BehaviorSubject. — 2m
983. What does `map` operator do? — 1m
984. What does `switchMap` do? — 2m
985. Difference between `switchMap`, `mergeMap`, `concatMap`, `exhaustMap`. — 3m
986. What does `takeUntil` do? — 1m
987. What is `takeUntilDestroyed()` used for? — 1m
988. Why are observables not always needed in v21? — 2m
989. What is the recommended unit test runner for Angular 21? — 1m
990. What is `TestBed.configureTestingModule({...})`? — 2m
991. What is a `ComponentFixture`? — 1m
992. What is `fixture.detectChanges()`? — 1m
993. What is a Component Harness? — 2m
994. What is `RouterTestingHarness`? — 2m
995. Name two E2E test frameworks commonly used with Angular. — 1m
996. What is the difference between unit, integration, and E2E tests? — 2m
997. What command runs Angular migrations? — 1m
998. Name two automated migrations in v21. — 2m
999. What is the Angular DevTools browser extension and what does it show? — 2m
1000. Where do you go for the official Angular docs and what is the URL? — 1m
