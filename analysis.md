# Analysis — Anderssons VVS (Borås)

Run mode: **full-build**
Pipeline: V11 full
Brief date: 2026-04-23

---

## 1. Industry Analyzer

Business type: **VVS / rörmokeri / installation & service** — local technical trade.

Sub-classification: **Hybrid quote + service trade**, not pure emergency. Work is mixed:
- planned installation (badrum, värmepump, stambyte-adjacent) — high-ticket, quote-led
- service & reparation (läckage, rördragning, mindre jobb) — phone-led
- BRF & företag (löpande serviceavtal) — relationship-led

The business is NOT an emergency dispatch operator. Treating it as one would misrepresent the offering and push the site toward the generic "akut rörmokare" template the client explicitly wants to avoid.

Audience breakdown:
- Primary: villaägare in Borås and närområde — renovation + service + heat-pump decisions
- Secondary: bostadsrättsföreningar — service agreements, scheduled maintenance, badrumsstambyte cycles
- Tertiary: företag — office / lokal-related VVS, minor commercial work

Conversion logic:
- Primary goal: få offert (form or email)
- Secondary goal: ring direkt (high-intent calls)
- The site must make both paths obvious without shouting

Reference category: this is a **premium local trade firm** positioned as the thoughtful, technical choice — not the cheapest, not the loudest, not the 24/7 dispatcher.

---

## 2. Strategy Brain

Strategic positioning: **"Tekniskt VVS-arbete, utfört med omsorg."**

Hypothesis: the Borås VVS market is saturated with indistinguishable emergency-style sites (orange bars, 24/7 claims, van photos). A calm, editorial, architecturally confident presence will be materially more memorable and will convert better among homeowners planning a badrumsrenovering or värmepump — exactly the high-value work the firm wants more of.

Three strategic bets:
1. **Lead with craft, not panic.** No "AKUT" vocabulary, no red/orange colour cues. Calm petrol + brass + sand reads as considered rather than reactive.
2. **Editorial hierarchy.** Serif display + asymmetric composition signals care — the same signal the customer is trying to find in a tradesperson.
3. **Quiet CTA rhythm.** One primary CTA (Begär offert), one secondary (phone). No CTA spam. Premium trust comes from confidence, not aggression.

Risks managed:
- Risk of looking "spa-like" → avoided by keeping petrol as the dominant colour, using technical vocabulary, and photographing fixtures/water/installation rather than candles/towels/plants.
- Risk of looking "luxury brand" → avoided by keeping copy grounded (local, hantverk, process), avoiding gold foil treatments, and using brass as a thin rule accent only.
- Risk of looking corporate/sterile → avoided by warm sand tones, handcrafted section numbering, and imagery of real work and hands.

---

## 3. Brand Identity

**Brand personality**
- Precise — technically competent without being cold
- Locally grounded — Sjuhärad, not "rikstäckande"
- Considered — slow-speaking, unhurried
- Crafted — the work is the marketing

**Emotional direction**
- Calm confidence, not reassurance theatre
- The quiet pride of a tradesperson who respects their trade
- The same trust signal a well-made tool transmits

**Verbal tone**
- Swedish, natural, direct
- Short sentences
- No exclamation marks
- No superlatives unless factual
- No "we are your experts" posture — instead, "vi arbetar så här"

**Visual personality**
- Editorial, architectural, restrained
- Display serif (Fraunces) paired with technical grotesk (Inter)
- Thin brass rules as the only true decorative element
- Large numbered section markers (01, 02, 03) as editorial scaffolding

**Audience impression goal**
When someone lands on the site, they should think: "*Those people seem to know what they're doing. I'd trust them in my home.*"

---

## 4. Reference Analysis (Vola / Dornbracht / Axor)

The three reference brands are premium fixture manufacturers, not service firms. We borrow attitude, not artefacts.

What to **take** (attitude):
- Confident whitespace — content is not crammed
- Display typography with narrow tracking and quiet hierarchy
- Product-focused photography (fixtures, water, surfaces) over lifestyle photography (people smiling)
- Editorial section rhythm — short paragraphs of positioning text between imagery
- Calm, considered colour palettes with warm neutrals

What to **leave behind** (would misrepresent a local VVS firm):
- Minimalist-to-sterile whitespace (these sites sell €3,000 taps; ours sells a badrumsrenovering)
- Art-direction-driven storytelling with abstract product shots
- Global navigation patterns (language switchers, distributor locators)
- Product-catalogue scale

What to **never copy**:
- Specific layouts, exact typographic scales, specific video compositions, specific copy lines.

---

## 5. Implementation Architect

Selected path: **static-premium-multipage**.

Reasoning:
- Scope is homepage + 3 SEO service pages — no need for React.
- SEO benefits from clean static HTML with full markup control.
- Hero video + mild reveal-on-scroll motion are trivial in vanilla JS.
- Lead-capture form is a single preview form until a real endpoint is wired up (see `build-notes.md`).
- Easier for the client to host and edit later.

Shared technical patterns:
- Single `styles.css` for site-wide system
- Per-page inline `<script>` kept minimal
- Reused header / footer markup across pages (static include via duplicated HTML — acceptable for 4 pages; if the site grows, migrate to a template engine)

Out of scope for this build:
- CMS integration
- Real form backend
- Image CDN
- Analytics
- Cookie banner (should be added when site goes live if tracking is added)

---

## Summary for downstream agents

Industry: VVS, premium local trade (not emergency).
Audience: villaägare + BRF + företag in Sjuhärad.
Primary conversion: offertförfrågan.
Design family: Trade Showcase — Editorial Precision variant.
Brand posture: calm, precise, architecturally restrained, locally grounded.
Implementation: static-premium-multipage.
