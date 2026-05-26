# Scenario-Based — 500 Questions

Real-world situations: production incidents, user complaints, architecture forks, team disagreements, migration crises, security events. Answer with what you'd ask, what you'd do next, and the trade-offs. Times follow the legend in the [root README](../README.md): Easy 1–3m, Medium 3–7m, Hard 7–15m, Extreme 15–30m, Legends 30–90m.

---

## Easy (1–100)

1. A user says "the search box feels laggy". What's your first hypothesis and quickest test? — 3m
2. The login button works but nothing happens for ~2s after clicking. Where do you look first? — 3m
3. A page shows "undefined" briefly before content appears. Most likely cause? — 2m
4. The app builds fine locally but fails on CI with "out of memory". First two things to try? — 3m
5. A teammate asks "should we use signals or RxJS for this new feature?" — your one-line answer? — 2m
6. PM wants to add a "dark mode toggle". You have 1 day. What's the minimum viable plan? — 3m
7. A new junior asks where to put a service used by two features. What do you say? — 2m
8. Designer hands you a 1MB hero PNG. What do you do before merging? — 2m
9. A page is missing a `<title>` per route. What's the Angular 21 idiomatic fix? — 2m
10. QA says tab order is broken on the contact form. First thing to check? — 2m
11. A new endpoint returns dates as ISO strings. Where do you convert to `Date`? — 3m
12. A request fails with CORS error in dev but not prod. Why and what to do? — 3m
13. A user complains "the page jumps when images load". One-line fix? — 2m
14. The CSS file is 600KB. Where do you start trimming? — 3m
15. A teammate copy-pastes the same component for the third time. What do you suggest? — 3m
16. The bundle grew 50KB after adding `moment.js`. Alternatives? — 2m
17. A button is `<div onclick>` for "styling reasons". What's the right answer? — 2m
18. The router shows a flash of empty content during navigation. Why and quick fix? — 3m
19. A `@for` loop misses the `track` expression. What does the linter say and what's the fix? — 2m
20. The form's submit button stays clickable while submitting. Quick fix? — 2m
21. A network panel shows 10 identical GET requests on page load. Likely cause? — 3m
22. The page works on localhost but throws on Vercel. First check? — 3m
23. The CI pipeline takes 25 minutes; tests are 18 of those. First action? — 3m
24. A teammate's PR adds 3 inline `<style>` tags. What's the convention? — 2m
25. The footer overlaps the modal when the modal is open. Likely cause? — 2m
26. Screen reader reads "button button button" — why and quick fix? — 3m
27. A user reports the form clears when they switch tabs and come back. Why and fix? — 3m
28. A new lib needs `provideX()` at root. Where in the code? — 2m
29. The chart re-renders every keystroke in an unrelated input. Why? — 3m
30. The lazy chunk loads 3 seconds after route nav. Quick check? — 3m
31. A user's password input shows the password by default. Why? — 2m
32. Mobile users can't tap a tiny "X" close button. What's the rule? — 2m
33. A new feature flag is on for one user but off for everyone else. How was it set? — 3m
34. The console shows a deprecation warning for `@Input()`. What do you do? — 2m
35. A teammate asks why `*ngIf` still works. Your reply? — 2m
36. A PR removes `ngOnDestroy` from a class. Should it? — 3m
37. A form's date input shows MM/DD/YYYY for European users. Why? — 3m
38. The page works for English but breaks for Arabic. First check? — 3m
39. A teammate wants to disable a built-in form button via `[disabled]` on an `<input>` with `[formField]`. Why is that wrong? — 2m
40. The dropdown opens but doesn't close on outside click. Quick approach? — 3m
41. A user reports double submission of the form. Quick fix? — 3m
42. The modal traps focus, but Tab cycles to the page behind. Why? — 3m
43. A teammate added `any` to silence a TS error. Your response? — 2m
44. A library was added via `npm install` not `ng add`. What might be missing? — 3m
45. A page's LCP is the hero image but it loads after the JS. Quick fix? — 3m
46. The skeleton flickers visible-invisible during data load. Why? — 3m
47. The animation is laggy on mobile. First properties to check? — 3m
48. The 401 interceptor refreshes the token but doesn't retry the original request. Why? — 3m
49. A request is sent on every keystroke. Quickest operator? — 2m
50. The toast appears twice for one event. Likely cause? — 2m
51. A user logs out but their data is still in the URL. Quick fix? — 3m
52. The router shows `/items/123?from=cart`. How do you read `from`? — 2m
53. A new route doesn't show in the navbar. Where do you check first? — 2m
54. The test passes locally but fails in CI with "ChromeHeadless timeout". First action? — 3m
55. The component uses `@Input()` but the test passes a `signal()`. What's wrong? — 3m
56. A PR replaces `ngClass` object with `[class.x]`. Should you approve? — 2m
57. A teammate uses `setTimeout(..., 0)` to fix CD. What's the better approach? — 3m
58. A user reports a typo in the email subject template. Where's that source? — 2m
59. The new lib requires `provideAnimations()`. Where? — 2m
60. The customer wants a print-friendly view. Quick approach? — 3m
61. The header logo doesn't show on `/login`. Why? — 3m
62. The 500 errors page is missing for SSR. Quick approach? — 3m
63. A user reports horizontal scroll on mobile. First CSS suspect? — 2m
64. The dev server reloads but state is lost. Why? — 2m
65. The chart resizes after rotation but is squished. Why? — 3m
66. The text on a button is 9px. What's the rule? — 2m
67. The form's validation message disappears on blur. Why? — 3m
68. The user can't paste a phone number with hyphens. Why? — 3m
69. The currency shows "USD 1,000.00" but users expect "$1,000.00". Where to change? — 3m
70. The date pipe shows GMT instead of local. Why? — 3m
71. The avatar image has no alt text. What's the rule? — 2m
72. The link looks like a button. Should it be a `<button>`? — 3m
73. The page returns 200 OK for a missing item. Why does SEO suffer? — 3m
74. A teammate added a custom router. Why is that almost always wrong? — 3m
75. The form posts as multipart but server expects JSON. Quick fix? — 3m
76. A nav drawer animation is 600ms — too slow. What's the convention? — 2m
77. The login button shows "Sign In" but should be "Sign in". Where's the catalog? — 2m
78. The error reads "an unexpected error occurred". Where's the better source of truth? — 3m
79. The user's clicked element loses focus after action. Why? — 3m
80. The fade-in animation runs even with `prefers-reduced-motion`. Why? — 3m
81. The new design uses 12 fonts. What's the constraint? — 2m
82. The viewport doesn't fit the content on small screens. CSS rule to add? — 2m
83. The toggle saves to server on every change. Quick UX fix? — 3m
84. The "remember me" checkbox isn't remembered. Why? — 3m
85. The page reloads on every form submit. Why? — 2m
86. The list shows 100 items but only 10 visible. Why is scroll slow? — 3m
87. The chart legend overflows the container. Quick fix? — 3m
88. The button click triggers two analytics events. Why? — 3m
89. The new lib's CSS overrides our theme. Why and quick fix? — 3m
90. The route guard returns `Promise<boolean>` but redirect doesn't happen. Why? — 3m
91. The PWA install prompt doesn't show. First check? — 3m
92. The offline page is white. Why? — 3m
93. The screenshot in the README is outdated. Whose responsibility? — 2m
94. The teammate wants to disable a CI gate to merge. Your response? — 3m
95. The new feature requires a 3rd-party CDN script. What to add to CSP? — 3m
96. The customer wants WhatsApp notifications. What's the design starter? — 3m
97. The new analytics needs consent. Where in the flow? — 3m
98. The CMS preview shows draft content publicly. Why? — 3m
99. The launch is tomorrow and bug XYZ is open. What questions to ask? — 3m
100. The retrospective asks "what would you do differently"? Frame an answer. — 3m

## Medium (101–200)

101. A page's LCP regressed from 2.1s to 3.5s in the last release. How do you bisect? — 7m
102. A user reports the cart shows the wrong total intermittently. Where do you start? — 7m
103. A teammate wants to introduce NgRx. Make the case for or against. — 6m
104. The CTO wants you to "move everything to signals". Where do you push back? — 6m
105. A senior engineer says "don't use SSR, just CSR." Why might they be right or wrong? — 6m
106. The QA team finds an a11y issue per release. Design a prevention plan. — 6m
107. The product team wants experiments on every page. Design a sane integration. — 7m
108. The data team wants to track every user click. What's the privacy/perf framing? — 6m
109. A junior asks "should this be a directive or a component?". Walk them through it. — 5m
110. A 3rd-party library breaks under zoneless. Decide whether to keep zoneless or drop. — 7m
111. The team wants to migrate from Karma to Vitest. Plan the rollout. — 6m
112. The team wants to migrate from RxJS-heavy services to signal stores. Plan the rollout. — 7m
113. A PR introduces a custom HTTP fetcher bypassing `HttpClient`. Why is that a smell? — 5m
114. The design system team ships a breaking change. What's your rollout plan? — 7m
115. A new API uses GraphQL. Should you switch your HTTP layer entirely? — 7m
116. The PM wants offline mode for the dashboard. What questions do you ask first? — 6m
117. A page works in Chrome but breaks in Safari. Triage steps? — 6m
118. The hero animation drops frames on iPhone SE. Strategy? — 6m
119. The Lighthouse score is 65 — what are the top 3 likely culprits? — 6m
120. The CSS bundle grew 200KB after adding Tailwind. Why and how to control it? — 6m
121. A teammate's PR adds 5 levels of `@Input` chain. What pattern would simplify? — 6m
122. A page has 12 different loading spinners. How do you converge? — 5m
123. The dashboard reloads every 30 seconds because of WS reconnect. Fix? — 7m
124. The error monitoring shows 10k errors a day but no fix prioritization. Plan? — 7m
125. The customer asks "why is our app slower than competitor X's?". Framework for answering? — 7m
126. The team wants to ship Edge SSR but lacks experience. Risk plan? — 7m
127. A feature behind a flag has 10x bugs of others. What's the systemic cause? — 6m
128. The migration to standalone is stalled at 60%. Re-engagement plan? — 7m
129. The team is split on Tailwind vs CSS Modules. How to decide? — 6m
130. The product wants to A/B the entire homepage. Plan with SSR. — 7m
131. The page state is in 4 different places (URL, signal, localStorage, server). Plan a refactor. — 7m
132. The team writes E2E tests but skips unit tests for "speed". Push back? — 6m
133. The design system has 200 components, 30 are duplicates. Cleanup plan? — 7m
134. A "white screen" bug only repros on Firefox + Adblock. Triage? — 6m
135. The team's bundle grew 1MB after a quarterly cleanup. Forensics? — 7m
136. The CMS preview leaks staging URLs to prod. Plan? — 6m
137. A PR proposes hand-rolling a date picker. Encourage or discourage? — 5m
138. A teammate's `effect()` triggers HTTP storms. Refactor to what? — 6m
139. A signal store grows to 2000 lines. Split strategy? — 6m
140. The team wants a "no any" lint rule. Risks and rollout? — 6m
141. The team wants 100% test coverage. Where do you push back? — 5m
142. The CTO asks "are we Angular-only or polyglot?". Frame the answer. — 7m
143. A new feature requires WebRTC. Time to first call < 5s. Architecture? — 7m
144. A feature requires offline PDF generation. Architecture? — 7m
145. A user complains "the page works once, then it's broken forever" — Service Worker? — 6m
146. The app uses cookies for auth but breaks in Safari ITP. Plan? — 7m
147. The app's 3rd-party tracker is blocked by 30% of users. Replacement plan? — 6m
148. The marketing team wants a static blog inside the app. Plan? — 6m
149. The marketing team wants a 100ms TTFB. Plan? — 7m
150. The team is split on monorepo vs polyrepo. Frame the decision. — 7m
151. The team's PR review takes 3 days on average. Reduce to 1. — 6m
152. The team ships on Fridays and breaks on Mondays. Process change? — 6m
153. A new hire joins next week. What do you have them do first? — 5m
154. A senior is leaving in 2 weeks. Knowledge transfer plan? — 6m
155. The roadmap has 5 priorities. How do you sequence them? — 6m
156. The customer asks for a "no-code editor". Sane scope? — 7m
157. The customer asks for "AI features". Sane scope and risks? — 7m
158. The customer asks for a "dashboard builder". Sane scope? — 7m
159. The customer asks for "real-time everywhere". Sane scope? — 7m
160. The customer asks for "white-labeling". Sane scope and risks? — 7m
161. The customer asks for "multi-tenant". Plan? — 7m
162. The customer asks for "BYO-domain". Plan? — 6m
163. The customer asks for "embeddable widgets". Plan? — 7m
164. The customer asks for "marketplace plugins". Plan? — 7m
165. The customer asks for "white-label theme editor". Plan? — 7m
166. The customer asks for "schedule reports by email". Plan? — 6m
167. The customer asks for "export to PDF/Excel". Plan? — 6m
168. The customer asks for "bulk import via CSV". Plan? — 6m
169. The customer asks for "SSO with Okta/Azure/Google". Plan? — 7m
170. The customer asks for "SCIM provisioning". Plan? — 6m
171. The customer asks for "audit log of every action". Plan? — 7m
172. The customer asks for "rollback any change". Plan? — 7m
173. The customer asks for "compare two versions". Plan? — 7m
174. The customer asks for "GDPR delete me". Plan? — 7m
175. The customer asks for "GDPR export my data". Plan? — 6m
176. The customer asks for "HIPAA compliance". Plan? — 7m
177. The customer asks for "WCAG 2.2 AAA". Plan? — 7m
178. The customer asks for "100ms search". Plan? — 7m
179. The customer asks for "100k concurrent users". Plan? — 7m
180. The customer asks for "ship to China". Plan considerations? — 7m
181. The customer asks for "ship to EU under DMA". Considerations? — 7m
182. The customer asks for "voice-only UI". Considerations? — 7m
183. The customer asks for "kiosk mode". Considerations? — 6m
184. The customer asks for "in-store tablet experience". Plan? — 6m
185. The customer asks for "watch-OS companion". Plan? — 7m
186. The customer asks for "AR overlay". Plan? — 7m
187. The customer asks for "AI chatbot". Plan? — 7m
188. The customer asks for "live customer support inside the app". Plan? — 7m
189. The customer asks for "spam protection on forms". Plan? — 6m
190. The customer asks for "bot detection". Plan? — 6m
191. The customer asks for "fraud detection". Plan? — 7m
192. The customer asks for "credit card capture". Plan? — 7m
193. The customer asks for "Apple Pay / Google Pay". Plan? — 7m
194. The customer asks for "Stripe Connect onboarding". Plan? — 6m
195. The customer asks for "subscription upgrade/downgrade flow". Plan? — 7m
196. The customer asks for "invoice download". Plan? — 5m
197. The customer asks for "refund flow with approval". Plan? — 6m
198. The customer asks for "discount codes". Plan? — 6m
199. The customer asks for "abandoned cart email". Plan? — 6m
200. The customer asks for "live chat for support". Plan? — 6m

## Hard (201–300)

201. Production incident: every user sees a blank page for 30s before content appears. RCA approach? — 12m
202. Production incident: 5% of users see a 500 on `/checkout`. RCA approach? — 12m
203. Production incident: SSR cache poisoning leaks one tenant's data to another. Immediate + long-term? — 15m
204. Production incident: third-party script breaks our CSP, half of users see broken UI. Decision tree? — 12m
205. Production incident: a deploy doubled bundle size and LCP. Rollback or roll-forward? — 12m
206. Production incident: feature flag stuck on for 100% of users instead of 10%. Containment? — 12m
207. Production incident: WebSocket reconnect storm after our LB restart. Mitigation? — 15m
208. Production incident: SW caches old `index.html`; users stuck for hours. Plan? — 15m
209. Production incident: refresh-token flow looping for 10% of users. Triage? — 15m
210. Production incident: payment retry doubles charges. Containment? — 15m
211. Production incident: image CDN down; site readable but ugly. Communicate? — 10m
212. Production incident: analytics is logging PII (full email in URL). Remediation? — 15m
213. Production incident: SEO traffic dropped 40% after migration. Hypotheses? — 15m
214. Production incident: A/B test variant breaks for screen readers only. Plan? — 12m
215. Production incident: Cloudflare cache invalidation lagging by 5min. Mitigation? — 12m
216. Production incident: cookies invalidated after deploy because of `SameSite` change. Plan? — 12m
217. Production incident: SSR error rate spiked from 0.1% to 5%. Diagnostic plan? — 15m
218. Production incident: hydration mismatch on a /pricing page only for paying users. Hypothesis? — 12m
219. Production incident: WS disconnect every 30s for users behind corporate firewall. Plan? — 12m
220. Production incident: search relevance dropped after backend change; FE looks fine. Coordination? — 12m
221. Architecture decision: convert 3 internal apps to one app. Plan? — 15m
222. Architecture decision: switch from REST to GraphQL for new features only. Risks? — 15m
223. Architecture decision: move from cookies-only auth to JWT. Trade-offs? — 15m
224. Architecture decision: move from CSR-only to SSR for SEO benefit. Plan? — 15m
225. Architecture decision: adopt module federation for shared design system. Trade-offs? — 15m
226. Architecture decision: replace Akita with signal store. Plan? — 15m
227. Architecture decision: split a 1M-LOC monolith into 3 SPAs. Strategy? — 15m
228. Architecture decision: keep Reactive Forms in legacy, Signal Forms in new code. Long-term? — 12m
229. Architecture decision: ship a public component lib outside the company. Plan? — 15m
230. Architecture decision: replace Mapbox with Maplibre. Trade-offs? — 12m
231. Architecture decision: replace Stripe with two payment providers (region). Plan? — 15m
232. Architecture decision: replace REST with tRPC for internal services. Trade-offs? — 12m
233. Architecture decision: replace cookies with localStorage for auth. Why not? — 10m
234. Architecture decision: replace third-party analytics with first-party. Plan? — 15m
235. Architecture decision: replace third-party CMS with in-house. Plan? — 15m
236. Architecture decision: ship feature behind paid plan. Plan? — 12m
237. Architecture decision: ship feature with 1-day TTL preview. Plan? — 10m
238. Architecture decision: ship feature with 30-day open beta. Plan? — 12m
239. Architecture decision: rename the product mid-app. Plan? — 10m
240. Architecture decision: convert from sub-domain to path-based tenant routing. Plan? — 15m
241. Migration: switch CSS from SCSS to Tailwind across 300 components. Plan and risks. — 15m
242. Migration: switch from Material to a custom design system across 500 components. Plan. — 15m
243. Migration: switch from Karma + Jasmine to Vitest. Plan. — 12m
244. Migration: switch from Protractor to Playwright. Plan. — 12m
245. Migration: switch from Cypress to Playwright. Plan. — 12m
246. Migration: switch from Webpack to esbuild. Plan. — 12m
247. Migration: switch from NgModules to standalone. Plan. — 15m
248. Migration: switch from `*ngIf` to `@if`. Plan. — 10m
249. Migration: switch from `@Input()` to `input()`. Plan. — 10m
250. Migration: switch from `RouterModule.forRoot` to `provideRouter`. Plan. — 10m
251. Migration: switch from `HttpClientModule` to `provideHttpClient`. Plan. — 10m
252. Migration: switch from Reactive Forms to Signal Forms. Plan. — 15m
253. Migration: switch from NgRx classic to signal store. Plan. — 15m
254. Migration: switch from `@angular/animations` to CSS-only. Plan. — 12m
255. Migration: switch from server cookies to header tokens. Plan. — 12m
256. Migration: switch from Mocha to Vitest. Plan. — 10m
257. Migration: switch from a self-hosted CDN to a managed CDN. Plan. — 12m
258. Migration: switch from a managed CDN to multi-CDN. Plan. — 15m
259. Migration: switch DBs (Postgres → DynamoDB) impacts FE — plan. — 15m
260. Migration: from monolith to micro-frontends. Plan. — 15m
261. Team decision: senior wants RxJS-everywhere; junior wants signals-everywhere. Mediate. — 12m
262. Team decision: which framework to teach new hires first? — 8m
263. Team decision: own design system or fork an open-source one? — 12m
264. Team decision: code freeze before holidays — what's the policy? — 8m
265. Team decision: who owns SSR? FE team or platform team? — 12m
266. Team decision: who owns hydration bugs? — 8m
267. Team decision: who owns CSP violations? — 8m
268. Team decision: who owns SEO regressions? — 8m
269. Team decision: who owns perf budgets? — 10m
270. Team decision: who owns a11y compliance? — 10m
271. Team decision: who owns i18n? — 10m
272. Team decision: who owns analytics quality? — 10m
273. Team decision: who owns dependency updates? — 10m
274. Team decision: who owns security reviews? — 10m
275. Team decision: who owns release notes? — 8m
276. Team decision: who owns user-facing copy? — 8m
277. Team decision: who owns design tokens? — 10m
278. Team decision: who owns CI maintenance? — 10m
279. Team decision: who owns flaky tests? — 10m
280. Team decision: who is on-call for FE? — 10m
281. Process: design a "first incident response" playbook for FE. — 15m
282. Process: design a "perf regression" review process. — 15m
283. Process: design a "deprecation" policy for shared libs. — 12m
284. Process: design a "feature flag retirement" policy. — 12m
285. Process: design a "post-mortem" template. — 12m
286. Process: design a "release notes" template. — 10m
287. Process: design a "PR review checklist" for FE. — 12m
288. Process: design a "PR template" for FE. — 10m
289. Process: design a "design review" template. — 12m
290. Process: design a "tech debt log" workflow. — 12m
291. Stakeholder: PM wants to ship MVP in 1 sprint. Triage what's cut. — 15m
292. Stakeholder: legal wants consent banner; design wants minimal UI. Negotiate. — 12m
293. Stakeholder: security wants strict CSP; analytics wants 3rd-party scripts. Negotiate. — 12m
294. Stakeholder: marketing wants pixel-perfect; engineering wants responsive. Negotiate. — 10m
295. Stakeholder: support wants more in-app help; product wants a clean UI. Negotiate. — 10m
296. Stakeholder: data wants more tracking; users complain about consent fatigue. Negotiate. — 12m
297. Stakeholder: ops wants observability everywhere; bundle budget shrinks. Negotiate. — 12m
298. Stakeholder: HR wants accessibility done by EOY; team's busy. Negotiate. — 12m
299. Stakeholder: finance wants per-tenant billing dashboards; ETA unclear. Negotiate. — 12m
300. Stakeholder: legal wants audit logs of every UI action. Negotiate scope. — 12m

## Extreme (301–400)

301. The CTO walks in: "Why is our app slower than competitor X's?". You have 30 minutes to present a plan. — 30m
302. The board asks: "Should we adopt AI in our app?". Frame the answer in product, perf, and security. — 30m
303. The lead designer wants every screen to have view-transitions. Frame the perf and a11y trade-offs. — 25m
304. The customer demands "100ms response on every action". Frame the system-level approach. — 30m
305. The customer demands "no third-party libraries". Frame the trade-offs and roadmap. — 30m
306. The customer demands "no analytics". Frame impact on product, marketing, and engineering. — 25m
307. The customer demands "AGPL-free dependencies only". Plan a sweep + replacement. — 25m
308. The customer demands "no CDN" (on-prem). Frame the trade-offs. — 25m
309. The customer demands "no service worker" (security policy). Frame alternatives. — 25m
310. The customer demands "no cookies". Frame alternatives. — 25m
311. The customer demands "no JS" (NoScript profile). Frame what survives. — 25m
312. The customer demands "no JS for first paint". Plan with SSR/streaming. — 25m
313. The customer demands "no third-party fonts". Frame the system. — 20m
314. The customer demands "no Google services". Frame replacements. — 25m
315. The customer demands "no AWS". Frame deployment alternatives. — 25m
316. The customer demands "no telemetry phoning home". Frame replacements. — 25m
317. The customer demands "no remote anything". Frame what's possible. — 25m
318. The customer demands "100% on-device LLM". Frame UX trade-offs. — 25m
319. The customer demands "real-time everything". Frame the architecture. — 30m
320. The customer demands "offline everything". Frame the architecture. — 30m
321. The PR review surfaces 5 architectural issues at once. Triage approach. — 25m
322. The team disagrees on a state management library. Run a decision meeting. — 25m
323. The team disagrees on testing strategy. Run a decision meeting. — 25m
324. The team disagrees on monorepo tool (Nx vs Turbo vs vanilla). Run a decision meeting. — 25m
325. The team disagrees on CSS approach (Tailwind vs CSS Modules vs vanilla). Run a decision meeting. — 25m
326. The team disagrees on form library (Reactive vs Signal vs custom). Run a decision meeting. — 25m
327. The team disagrees on auth library (in-house vs Auth0 vs WorkOS). Run a decision meeting. — 25m
328. The team disagrees on observability (Sentry vs Datadog vs in-house). Run a decision meeting. — 25m
329. The team disagrees on i18n approach ($localize vs lib). Run a decision meeting. — 25m
330. The team disagrees on perf budget (strict vs loose). Run a decision meeting. — 25m
331. A v22 RC is out. Plan the team's upgrade timeline. — 25m
332. A new framework (FrameworkX) is gaining traction. Should we evaluate? When? — 25m
333. The team's bus factor is 1 for SSR. Knowledge transfer plan. — 25m
334. The team's senior is leaving. Plan succession. — 25m
335. The team's PM is leaving. Plan continuity for product decisions. — 20m
336. The team needs to hire two seniors. Frame the interview signal. — 25m
337. The team needs to ramp 5 new hires. Frame the onboarding plan. — 25m
338. The team needs to launch a public OSS library. Plan. — 30m
339. The team needs to write an RFC for upstream Angular. Plan. — 25m
340. The team needs to host a public workshop on Angular 21. Plan. — 25m
341. The customer demands a SLA: 99.99% FE uptime. Frame the architecture and ops. — 30m
342. The customer demands: zero CLS. Frame how. — 25m
343. The customer demands: zero hydration errors. Frame how. — 25m
344. The customer demands: zero a11y violations. Frame how. — 25m
345. The customer demands: zero CSP violations. Frame how. — 25m
346. The customer demands: zero JS errors in 30 days. Frame how. — 25m
347. The customer demands: zero secrets in client bundle. Frame how. — 20m
348. The customer demands: zero PII in logs. Frame how. — 25m
349. The customer demands: zero downtime deploys. Frame how. — 25m
350. The customer demands: zero cookies for guest users. Frame how. — 25m
351. The customer demands: zero third-party requests on landing page. Frame how. — 25m
352. The customer demands: zero data leaving the EU. Frame how. — 25m
353. The customer demands: < 100kB total page weight. Frame how. — 30m
354. The customer demands: < 1s LCP globally. Frame how. — 30m
355. The customer demands: works in IE11. Frame the answer politely. — 20m
356. The customer demands: works on a 2010 Android phone. Frame the answer. — 25m
357. The customer demands: same UX in browser, iOS, Android. Frame the architecture. — 30m
358. The customer demands: same UX in mobile and desktop. Frame the trade-offs. — 25m
359. The customer demands: native-app feel from web. Frame how. — 25m
360. The customer demands: web-app feel from native. Frame how. — 25m
361. M&A: integrate an acquired app into our shell. Frame timeline. — 30m
362. M&A: integrate an acquired team into ours. Frame onboarding. — 25m
363. M&A: shut down our app, keep theirs. Frame migration. — 30m
364. M&A: shut down their app, keep ours. Frame migration. — 30m
365. M&A: merge backends, FEs stay separate. Frame integration. — 30m
366. Crisis: prod is down. CTO is yelling. Frame the next 10 minutes. — 25m
367. Crisis: data breach. Frame the next 1 hour. — 30m
368. Crisis: SLA breached. Frame the comms. — 25m
369. Crisis: vendor outage. Frame the failover. — 25m
370. Crisis: PR fire from a customer tweet. Frame the response. — 25m
371. Crisis: regulatory request arrives. Frame the response. — 30m
372. Crisis: critical CVE in our framework. Frame the response. — 30m
373. Crisis: critical CVE in our dep. Frame the response. — 30m
374. Crisis: critical CVE in our CDN. Frame the response. — 25m
375. Crisis: critical CVE in our browser baseline. Frame the response. — 25m
376. Crisis: misconfigured CSP blocks 100% of users. Frame the rollback. — 25m
377. Crisis: misconfigured CORS blocks 100% of API. Frame the rollback. — 25m
378. Crisis: misconfigured robots.txt blocks SEO. Frame the rollback. — 25m
379. Crisis: misconfigured analytics double-counts revenue. Frame the comms. — 25m
380. Crisis: misconfigured experiment shows wrong UI to 100% of users. Frame the rollback. — 25m
381. Roadmap: design the next quarter for FE platform team. — 30m
382. Roadmap: design the next year for FE platform team. — 30m
383. Roadmap: design the next 3 years for FE platform team. — 30m
384. Roadmap: align FE roadmap with product roadmap. Frame the process. — 25m
385. Roadmap: align FE roadmap with platform roadmap. Frame the process. — 25m
386. Roadmap: communicate FE roadmap to non-engineers. Frame the doc. — 25m
387. Roadmap: justify a "tech debt" sprint. Frame the pitch. — 25m
388. Roadmap: justify a "FE perf" sprint. Frame the pitch. — 25m
389. Roadmap: justify a "FE a11y" sprint. Frame the pitch. — 25m
390. Roadmap: justify a "FE security" sprint. Frame the pitch. — 25m
391. Hiring: design the FE interview loop. — 30m
392. Hiring: design the FE technical screen. — 25m
393. Hiring: design the FE system-design interview. — 30m
394. Hiring: design the FE coding interview. — 25m
395. Hiring: design the FE leadership interview. — 25m
396. Promotions: design the senior → staff bar for FE. — 30m
397. Promotions: design the staff → principal bar for FE. — 30m
398. Promotions: design the FE IC ladder. — 30m
399. Promotions: design the FE manager ladder. — 30m
400. Promotions: design the FE platform vs product split. — 30m

## Legends (401–500)

401. You are CTO. The org has 200 FE engineers and 4 apps on Angular 21. Design the next 3-year platform roadmap including framework upgrades, hiring, tooling, observability, and OKRs. — 90m
402. You are head of platform. Design a "golden path" for new Angular 21 apps including auth, observability, design system, CI/CD, deployment, perf budgets, a11y, security, i18n. — 75m
403. You are head of platform. Design a "deprecation pipeline" for shared libs (versioning, communication, codemods, sunsetting, support). — 75m
404. You are head of platform. Design an "FE observability" plane that captures RUM, errors, perf, a11y, security, and feature usage. — 75m
405. You are head of platform. Design an "FE perf budget" system across 50 apps with automated enforcement. — 75m
406. You are head of platform. Design an "FE a11y compliance" system across 50 apps with automated enforcement. — 75m
407. You are head of platform. Design an "FE security review" pipeline integrating CSP, SRI, Trusted Types, secrets, third-party audit. — 75m
408. You are head of platform. Design an "FE i18n compliance" system across 50 apps. — 75m
409. You are head of platform. Design a "feature flag" platform powering 50 apps with audit, rollouts, and kill switches. — 75m
410. You are head of platform. Design an "experimentation" platform with SSR-safe variant assignment and analytics integration. — 75m
411. You are head of platform. Design a "design system" team operating model serving 50 apps. — 75m
412. You are head of platform. Design an "FE on-call" rotation across 50 apps. — 60m
413. You are head of platform. Design an "FE incident command" structure. — 60m
414. You are head of platform. Design an "FE post-mortem" culture. — 60m
415. You are head of platform. Design an "FE roadmap review" cadence. — 60m
416. You are head of platform. Design a "shared component" governance model. — 60m
417. You are head of platform. Design a "shared style" governance model. — 60m
418. You are head of platform. Design a "shared token" governance model. — 60m
419. You are head of platform. Design a "shared API" governance model. — 60m
420. You are head of platform. Design a "shared identity" governance model. — 60m
421. You are head of platform. Design a "browser support" matrix and review cadence. — 60m
422. You are head of platform. Design a "device support" matrix and review cadence. — 60m
423. You are head of platform. Design a "third-party dependency" review process. — 60m
424. You are head of platform. Design a "third-party script" review process. — 60m
425. You are head of platform. Design an "ML/AI feature" review process. — 60m
426. You are head of platform. Design a "PR review" calibration across 200 engineers. — 60m
427. You are head of platform. Design a "code style" governance model. — 60m
428. You are head of platform. Design a "test strategy" governance model. — 60m
429. You are head of platform. Design a "deploy strategy" governance model. — 60m
430. You are head of platform. Design an "FE security training" program. — 60m
431. You are head of platform. Design an "FE a11y training" program. — 60m
432. You are head of platform. Design an "FE perf training" program. — 60m
433. You are head of platform. Design an "FE i18n training" program. — 60m
434. You are head of platform. Design an "FE oncall training" program. — 60m
435. You are head of platform. Design an "FE leveling" rubric. — 60m
436. You are head of platform. Design an "FE promo packet" template. — 60m
437. You are head of platform. Design an "FE engineering principles" doc. — 60m
438. You are head of platform. Design an "FE hiring rubric" doc. — 60m
439. You are head of platform. Design an "FE org chart" for 200 engineers. — 75m
440. You are head of platform. Design an "FE budget" for the year (people + tools + cloud). — 75m
441. You are CEO. The company is 5 years old. Should we keep Angular for the next 5 years? Defend with criteria. — 90m
442. You are CEO. The board wants to replace the FE stack. Decision-making framework? — 75m
443. You are CEO. The CTO wants to fork the framework. Decision-making framework? — 75m
444. You are CEO. The customer wants white-label embedded experience. Strategic plan? — 75m
445. You are CEO. The customer wants AI integration. Strategic plan? — 75m
446. You are founder. You're building a new FE-heavy startup. Choose Angular vs alternatives. Defend. — 75m
447. You are founder. You're building a real-time collaboration product. Choose architecture. — 90m
448. You are founder. You're building a creator tools product. Choose architecture. — 90m
449. You are founder. You're building an internal admin tool. Choose architecture. — 60m
450. You are founder. You're building a regulated FinTech app. Choose architecture. — 90m
451. You are founder. You're building a B2B SaaS dashboard. Choose architecture. — 75m
452. You are founder. You're building a media streaming app. Choose architecture. — 90m
453. You are founder. You're building a healthcare app. Choose architecture. — 90m
454. You are founder. You're building an e-commerce app. Choose architecture. — 90m
455. You are founder. You're building a marketplace. Choose architecture. — 90m
456. You are founder. You're building a social network. Choose architecture. — 90m
457. You are founder. You're building a developer tool. Choose architecture. — 75m
458. You are founder. You're building a no-code platform. Choose architecture. — 90m
459. You are founder. You're building an OS-like web platform. Choose architecture. — 90m
460. You are founder. You're building a metaverse experience. Choose architecture. — 90m
461. You are framework author. Design a backwards-compatible RFC for Angular 22. — 90m
462. You are framework author. Design a deprecation policy for v22 → v25. — 75m
463. You are framework author. Design a contribution guide for v22. — 75m
464. You are framework author. Design an RFC for "Resumability" in Angular. — 90m
465. You are framework author. Design an RFC for "Server Components" in Angular. — 90m
466. You are framework author. Design an RFC for "Server Actions" in Angular. — 90m
467. You are framework author. Design an RFC for "Islands" in Angular. — 90m
468. You are framework author. Design an RFC for "type-safe templates" in Angular. — 90m
469. You are framework author. Design an RFC for "compile-time signal deps" in Angular. — 90m
470. You are framework author. Design an RFC for "compile-time effect-write detection" in Angular. — 75m
471. You are framework author. Design an RFC for "compile-time CSS encapsulation" in Angular. — 75m
472. You are framework author. Design an RFC for "compile-time SSR safety" in Angular. — 75m
473. You are framework author. Design an RFC for "compile-time hydration mismatch detection" in Angular. — 75m
474. You are framework author. Design an RFC for "compile-time `@defer` deps". — 75m
475. You are framework author. Design an RFC for "compile-time route guards". — 75m
476. You are framework author. Design an RFC for "compile-time form schema". — 75m
477. You are framework author. Design an RFC for "compile-time i18n keys". — 75m
478. You are framework author. Design an RFC for "compile-time a11y violations". — 75m
479. You are framework author. Design an RFC for "compile-time perf budgets". — 75m
480. You are framework author. Design an RFC for "compile-time security checks". — 75m
481. You are open-source maintainer. Design a release cadence for a popular lib. — 75m
482. You are open-source maintainer. Design a triage process for issues. — 60m
483. You are open-source maintainer. Design a triage process for PRs. — 60m
484. You are open-source maintainer. Design a deprecation policy for the lib. — 60m
485. You are open-source maintainer. Design a "v2.0" launch plan. — 75m
486. You are open-source maintainer. Design a "sponsorship" model. — 60m
487. You are open-source maintainer. Design a "governance" model. — 60m
488. You are open-source maintainer. Design a "contributor recognition" model. — 60m
489. You are open-source maintainer. Design a "docs site" v2. — 75m
490. You are open-source maintainer. Design a "playground" feature. — 60m
491. You are conference organizer. Design a "best of Angular 21" track. — 60m
492. You are conference organizer. Design a "Angular vs React" panel. — 60m
493. You are conference organizer. Design a "FE perf" workshop. — 75m
494. You are conference organizer. Design a "FE a11y" workshop. — 75m
495. You are conference organizer. Design a "FE security" workshop. — 75m
496. You are educator. Design a 12-week "Angular 21" course. — 90m
497. You are educator. Design a 12-week "FE platform" course. — 90m
498. You are educator. Design a 12-week "FE leadership" course. — 90m
499. You are educator. Design a "self-taught FE engineer" learning path. — 90m
500. Reflect on this entire problem set. If you could keep only 10 questions across all 7,000, which ones, and why? — 90m
