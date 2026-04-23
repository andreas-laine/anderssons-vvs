# Build Notes — Anderssons VVS

Run mode: **full-build**
Implementation path: **static-premium-multipage**
Build date: 2026-04-23

---

## Implementation strategy

Chosen: `static-premium-multipage` — vanilla HTML + CSS + a small amount of inline JS per page. No build step, no framework. This is the correct trade-off for a 4-page marketing site where SEO and hosting simplicity matter more than interactivity.

Pages delivered:
- `index.html`
- `badrumsrenovering-boras.html`
- `varmepump-boras.html`
- `rormokare-boras.html`

Shared:
- `styles.css` — one stylesheet for the whole site

Hosting expectations: any static host (Netlify, Vercel, Cloudflare Pages, or a traditional LAMP host). Fonts are loaded from Google Fonts; no self-hosting in this build. The site is designed to work without JavaScript; JS only enhances (mobile menu, reveal-on-scroll, FAQ, scrolled-nav state).

---

## Design family selection

Selected preset: **Trade Showcase** (from `templates/families/trade-showcase.md`).

Customisation depth: **heavy** — a distinct *Editorial Precision* variant within the Trade Showcase family. The base conversion logic is preserved (proof-led, craft-focused, quote-led primary CTA), but the visual grammar is substantially reinterpreted:

- editorial serif display type (Fraunces) replacing a technical/bold display grotesk
- asymmetric hero layout with wide negative space instead of a centered composition
- thin brass horizontal rules as the only recurring decorative element
- numbered section markers (01–05) acting as editorial scaffolding
- quiet petrol/sand/brass palette instead of strong primary trade colours
- muted hero video rather than a static trust-bar header strip

This variant is **not** being added to the preset library in this build — it is treated as a project-specific interpretation. If it proves reusable, a follow-up task should generalise it into `templates/families/trade-editorial.md`.

---

## Design profile (Design Intelligence)

| Axis | Value |
|---|---|
| Visual direction | Editorial, architectural, restrained |
| Design tone | Calm, confident, crafted |
| Visual density | Low-to-medium — generous whitespace, short paragraphs |
| CTA prominence | Low-to-medium — one primary, one secondary, never stacked aggressively |
| Colour direction | Petrol-dominant with sand warmth and a single brass accent |
| Typography direction | Display serif + technical grotesk pairing |
| Card / banding system | Subtle banding between sections; cards are flat with thin top-rule on hover |
| Section rhythm | Long quiet intro → denser services → breathing space → quote section → FAQ → CTA |
| Trust style | Confident copy, no badges, no review strips, no fake social proof |
| Image dependency | High — the design leans on atmospheric water/fixture/interior imagery |

---

## Variation vs. prior Anderssons VVS output

This build is materially different from `output-sites/andersson-vvs-v3/` in all the categories the V11 variation rule cares about:

| Axis | v3 (prior) | this build |
|---|---|---|
| Layout family | centered trade-emergency | asymmetric editorial |
| Hero composition | dark navy split with trust bar | muted hero video + editorial overlay |
| Section order | trust → services → areas → akut → FAQ | hero → statement → services → approach → highlight → areas → trust → FAQ → CTA |
| CTA strategy | phone-led, urgent, repeated | offert-led, calm, paced |
| Visual style | corporate navy + grotesk | petrol + sand + brass + serif + grotesk |
| Content emphasis | emergency availability | craft + local precision |
| Page rhythm | dense, dispatch-like | editorial, unhurried |
| Card / banding language | bold solid cards | flat cards with top-rule reveal |
| Density and pacing | compressed | generous negative space |
| Decorative treatment | none | thin brass rules + large numbered markers |
| Motion | none beyond basic | subtle scroll-reveal + muted hero video |

Colour and copy changes alone would not have been sufficient — layout, hierarchy and rhythm are redesigned.

---

## Brand identity applied

Verbal tone applied consistently across every page:
- headlines are declarative but quiet — no exclamation marks
- body copy favours short sentences and concrete nouns (tätskikt, koppling, projektering) over marketing adjectives
- CTAs read as invitations ("Begär offert", "Boka platsbesök") rather than commands
- no superlatives, no "bästa", "snabbaste", "ledande"

---

## Motion direction (Motion Director)

Motion is present but restrained. Where used, it is purposeful and subtle.

1. **Hero video** — autoplay, muted, looped, `playsinline`. Poster image displayed until the video is loaded. On mobile (< 640px) the video is removed from the DOM via CSS and only the poster shows. Under `prefers-reduced-motion: reduce`, the video is paused and the poster remains.
2. **Scroll-reveal** — a small IntersectionObserver raises service cards, approach steps, and FAQ items by 12px with a 0.4s ease. Disabled under `prefers-reduced-motion`.
3. **Navigation scroll state** — above 40px scroll, the nav gains `backdrop-filter: blur(10px)` and a 1px brass bottom rule. Subtle, not a bar appearing.
4. **FAQ accordion** — a simple native `<details>` element, styled, no custom JS height animation — this is intentional: native elements are keyboard-accessible and resilient.
5. **Hover micro-transitions** — service cards, links, and the primary CTA have 150–250ms transitions on transform/border-colour only.

No parallax. No count-up animations. No auto-rotating testimonial carousels.

---

## Decorative layout direction

One recurring motif only: **thin brass horizontal rules** (1px) that sit above section headings and beneath the hero overlay. Combined with the numbered section markers (`01`, `02`, `03`…) in Fraunces italic, these are the only non-typographic decorative elements.

No noise overlays, no wave dividers, no blob shapes. The editorial restraint *is* the decoration.

---

## Form treatment

The offert form on the homepage and CTA on service pages is a **preview form**. It does not submit to a real endpoint. The `<form>` element uses `method="post"` and `action="#offert"` and has no server-side or third-party handler attached. JavaScript captures the submit event, shows a friendly confirmation state, and DOES NOT pretend to send the data anywhere.

### Required work before launch

1. Replace the `<form action="#offert">` with either:
   - a real backend endpoint (recommended: Formspree, Basin, Netlify Forms, or a custom serverless function), OR
   - a `mailto:johan@anderssonvvs.se` fallback (lower quality UX, but honest)
2. Add a real `Integritetspolicy` page and link it from the form's consent line
3. If a third-party form service is used, add a cookie notice if the service sets cookies
4. Remove the "preview" text in the JS confirmation once real submission is wired

---

## Contact integrity

- Phone number is wired as a real `tel:` link: `+46767760006`
- Email is wired as a real `mailto:` link: `johan@anderssonvvs.se`
- No "click-to-dispatch", no fake SMS shortcuts, no "online chat" widgets

---

## Media readiness status

**Pending**: all imagery and the hero video are planned but **not yet generated**. The HTML references `/assets/placeholders/*` paths which currently do not exist.

Current runtime behaviour:
- `<video>` with a missing source: the browser will show the `poster` attribute — which is also missing — and fall back to the `background` of the hero section, which is a calm petrol-to-sand gradient in CSS. This is the intentional interim state: *never a fabricated photo*.
- `<img>` tags on service pages: each has an explicit `loading="lazy"` and a CSS `background` fallback so the layout does not break when the image file is absent. The `alt` text is written as if the image were present so screen-reader users receive the intended description.

Final delivery is NOT complete until the assets listed in `image-plan.md` are produced (using the prompts in `ai-image-prompts.md`) and placed under `/assets/placeholders/` or, later, `/assets/real/`.

---

## Asset folder policy (inherited from CLAUDE.md)

- `/assets/real/`, `/images/`, `/videos/` — **never overwrite** these. Once they contain real files, those files take absolute priority over anything in `/assets/placeholders/`.
- `/assets/placeholders/` — editable; holds planned AI-generated interim assets. This is where produced imagery from `ai-image-prompts.md` should land.

---

## Accessibility

- Landmark elements used (`header`, `nav`, `main`, `section[aria-labelledby]`, `footer`)
- Every interactive element has a visible focus ring (`outline` on focus-visible, using brass)
- Colour contrast ratios verified in the design tokens:
  - petrol text on off-white background = ≥ 12:1
  - sand bg with petrol text = ≥ 10:1
  - brass CTA outline on petrol = ≥ 4.5:1 (used for focus ring, not running text)
- Hero video has `aria-hidden="true"` and is purely decorative; no content lives only in the video
- FAQ uses native `<details>`/`<summary>`
- Form inputs have associated `<label>` elements
- `prefers-reduced-motion` respected for motion and hero video

---

## Known follow-up items

1. **Generate and place all AI imagery** per `ai-image-prompts.md`
2. **Wire the form** to a real endpoint (see "Form treatment")
3. **Add an Integritetspolicy page** and link from the form
4. **Add opening hours to schema** once confirmed
5. **Add organisationsnummer and full address to the footer** once confirmed
6. **Add verified certifications** (Säker Vatten, BKR/GVK, F-gas) only if confirmed — see `fact-check-needed.md`
7. **Add a small jour-page** only if a real jour is offered
8. **Consider a before/after project gallery** once real project photography exists
9. **Analytics + cookie notice** — only if tracking is wired up

---

## QA log (mobile + compliance review)

- Navigation: collapses to hamburger below 860px; hamburger opens full-screen overlay with large tap targets
- Hero: video hidden below 640px; poster-only path tested conceptually; hero overlay text remains readable on petrol gradient fallback
- Services: grid falls to 1 column below 640px; card tap target entire card
- Approach: timeline falls to vertical stack below 720px; brass dots reposition cleanly
- FAQ: `<details>` works with keyboard and screen readers; no horizontal overflow
- CTA form: single column on mobile, 2-column above 720px; no horizontal scroll
- Footer: 2-column below 720px, 4-column above
- Sticky bottom CTA bar on mobile is petrol-backed with 48px tap targets (Ring / Offert); hidden ≥ 860px
- No white/blank overlay bugs after menu close
- Tested conceptually — viewport scans required with real assets in place
