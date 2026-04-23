# SEO Plan — Anderssons VVS

Local-intent SEO for Borås and Sjuhärad, across homepage + 3 service pages. Every page has a unique SEO purpose. No thin or duplicated service pages.

---

## Keyword map

### Homepage — brand + primary local term
- Primary: `VVS Borås`
- Secondary: `rörmokare Borås`, `VVS-service Borås`, `VVS-installation Borås`
- Tertiary / intent-adjacent: `badrumsrenovering Borås`, `värmepump Borås`, `läckage Borås`
- Navigational: `Anderssons VVS`, `Anderssons VVS Borås`

### /badrumsrenovering-boras.html
- Primary: `badrumsrenovering Borås`
- Secondary: `renovera badrum Borås`, `totalentreprenad badrum Borås`, `VVS badrum Borås`
- Long-tail: `pris badrumsrenovering Borås`, `badrum stambyte Borås`
- Informational: `vad kostar att renovera badrum`, `hur lång tid tar en badrumsrenovering`

### /varmepump-boras.html
- Primary: `värmepump Borås`
- Secondary: `luftvärmepump Borås`, `bergvärmepump Borås`, `installera värmepump Borås`
- Long-tail: `byta värmepump Borås`, `service värmepump Borås`
- Informational: `vilken värmepump passar villa`, `ROT-avdrag värmepump`

### /rormokare-boras.html
- Primary: `rörmokare Borås`
- Secondary: `rörmokeri Borås`, `VVS-firma Borås`, `rörarbete Borås`, `serviceavtal VVS BRF Borås`
- Long-tail: `hitta rörmokare Borås`, `lokal rörmokare Sjuhärad`

---

## Page-level SEO briefs

### Homepage (index.html)
- **Title tag** (≤ 60 chars): `Anderssons VVS Borås – Installation & service | Rörmokare i Sjuhärad`
- **Meta description** (≤ 155 chars): `Lokal VVS-firma i Borås för villaägare, BRF och företag. Badrumsrenovering, värmepumpar, service och rördragning. Begär offert eller ring 076-776 00 06.`
- **H1**: `Tekniskt VVS-arbete, utfört med omsorg.`
- **H2 pattern**: Arbetsområden · Så arbetar vi · Badrumsrenovering · Sjuhärad · Nära, noggrant, tekniskt förankrat · Vanliga frågor · Begär offert
- **Canonical**: `https://www.anderssonvvs.se/`
- **Schema**: `LocalBusiness` (type `Plumber`), `FAQPage`, `WebSite`. No `AggregateRating` (unverified). No reviews.

### /badrumsrenovering-boras.html
- **Title tag**: `Badrumsrenovering i Borås – projektering till färdigt rum | Anderssons VVS`
- **Meta description**: `Helhetslösning för badrumsrenovering i Borås: VVS-projektering, tätskikt, ytskikt och fixtures. Begär kostnadsförslag – lokalt utfört arbete.`
- **H1**: `Badrumsrenovering i Borås`
- **H2 pattern**: Vad en badrumsrenovering omfattar · Vår arbetsgång · Material & fixtures · Tidsplan · Vanliga frågor · Offertförfrågan
- **Schema**: `Service` under parent `LocalBusiness`, `FAQPage`, `BreadcrumbList`.

### /varmepump-boras.html
- **Title tag**: `Värmepump i Borås – rådgivning, installation, service | Anderssons VVS`
- **Meta description**: `Värmepump i Borås: luft/vatten, frånluft och bergvärme. Rådgivning, installation och service. Boka platsbesök eller ring 076-776 00 06.`
- **H1**: `Värmepump i Borås`
- **H2 pattern**: Typer av värmepump · Vår rådgivning · Installation · Service & underhåll · ROT & finansiering · Vanliga frågor · Boka platsbesök
- **Schema**: `Service`, `FAQPage`, `BreadcrumbList`.

### /rormokare-boras.html
- **Title tag**: `Rörmokare i Borås – service, installation, BRF & företag | Anderssons VVS`
- **Meta description**: `Rörmokare i Borås för villor, BRF och företag. Service, rördragning, läckage och installation. Begär offert eller ring 076-776 00 06.`
- **H1**: `Rörmokare i Borås`
- **H2 pattern**: Vad vi hjälper med · När du bör ringa · Serviceavtal för BRF & företag · Vårt arbetssätt · Vanliga frågor · Kontakt
- **Schema**: `Service`, `FAQPage`, `BreadcrumbList`.

---

## Internal linking plan

Homepage links **out** to:
- `/badrumsrenovering-boras.html` — from Arbetsområden card and from the Badrum highlight block
- `/varmepump-boras.html` — from Arbetsområden card
- `/rormokare-boras.html` — from Arbetsområden card and from "Service & läckage" card

Each service page links **laterally** to the other two service pages (under a "Relaterade arbetsområden" block) and **up** to the homepage (via nav and breadcrumb).

Footer on every page links to all three service pages + homepage + service-area list — establishing clean internal link equity flow.

---

## Structured data plan

Homepage:
- `LocalBusiness` → `Plumber`
  - name, url, telephone, email, areaServed (Borås, Dalsjöfors, Fristad, Sandared, Sjuhärad), address (locality only, no fake full address unless verified)
  - openingHours: commented out until verified; replaced by "After-hours availability is handled case-by-case" text rather than fake `24/7`
  - No `aggregateRating`, no `review` — flagged in `fact-check-needed.md`
- `WebSite` with `name` and `url`
- `FAQPage` with 5 grounded Q/A entries

Service pages:
- `Service` (provider: LocalBusiness stub referencing homepage URL)
- `BreadcrumbList` (Hem → Tjänster → <service>)
- `FAQPage` per page — 3–5 entries specific to that service

No schema is invented. Anything unverified is kept out of the schema.

---

## Content depth rules

- Every service page: ≥ 500 words of unique body copy, with 3 distinct H2 sections and a page-specific FAQ
- No boilerplate reuse between service pages — even the "vårt arbetssätt" sections must be written page-specific
- Every page ends with a conversion block that is page-relevant (offert vs. platsbesök)

---

## Local SEO supporting signals

- Consistent NAP (Namn + phone + email) on every page — footer + schema
- Location words naturally integrated in body copy, not stuffed
- Service-area list on homepage AND footer
- "Borås" in H1 of every service page
- Filenames use `-boras` suffix to reinforce local intent
