# Fact-Check Needed — Anderssons VVS

Every item on this list is something the copy **does not claim specifically** and which the client must verify before it can be added. Where copy touches any of these areas, it has been deliberately written to be generically true for any professional Swedish VVS firm, without stating a number or a specific badge.

The generated site contains **no fabricated**:
- years in business
- ratings or stars
- review counts
- testimonial quotes
- staff size
- awards
- guarantees with a specific monetary or time value
- insurance amounts
- partnerships, memberships, or certifications
- municipality or BRF-client relationships
- response times
- pricing

---

## Items the client must verify before they can appear on the site

### Business & legal
- [ ] Full legal company name (the site currently uses the brand name "Anderssons VVS" in copy and leaves full corporate naming for the footer / impressum once confirmed)
- [ ] Organisationsnummer — NOT included in the build; add to footer once confirmed
- [ ] F-skatt registered? — referenced generically as "F-skatt" in trust language; confirm and keep, or remove
- [ ] Ansvarsförsäkring i kraft? — referenced generically; confirm the provider is current
- [ ] Momsregistrerad? — implicit if F-skatt, but confirm
- [ ] Business address / postal address — only locality ("Borås") is used; add full address to footer once confirmed
- [ ] Opening hours — intentionally omitted from schema and footer because it was not provided; the site uses the phrase "kontakta oss så återkopplar vi" rather than fake hours

### Qualifications & certifications
- [ ] Säker Vatten-auktoriserad? — not claimed on the site. If confirmed, add a dedicated trust line and, if a certification ID is issued, optional schema
- [ ] Kvalitets- och miljöansvar — any ISO 9001 / 14001? Not claimed on the site. Only add if confirmed and current
- [ ] Kylcertifikat / F-gas-certifikat for värmepump work — not claimed. The `varmepump-boras.html` page would benefit from this claim if confirmed
- [ ] BKR or other badrum-specific competences — not claimed. If the firm has a tätskikts-utbildning e.g. BKR/GVK, add a concrete line to `badrumsrenovering-boras.html`
- [ ] Nordic Swan / Svanen / other sustainability credentials — not claimed

### Track record & references
- [ ] Years the firm has been active — not claimed
- [ ] Number of completed projects — not claimed
- [ ] BRF references available on request? — the site currently says "Vi arbetar löpande med bostadsrättsföreningar och företag i Sjuhärad." This is true only if correct. Confirm.
- [ ] Named client references (companies, BRFs) — none are named on the site. Only add with explicit written consent from each client
- [ ] Photography of completed work — all photography is planned as AI-generated placeholder. Real project photography should replace placeholders wherever possible, with permission where homes are identifiable

### Commercial offering
- [ ] Ärligt pris-bedömning / kostnadsförslag without charge? — copy says "Vi ger ett kostnadsförslag innan arbetet startar." Confirm that is always true.
- [ ] Hembesök kostnadsfritt? — not claimed specifically. Confirm and add line if true.
- [ ] ROT-avdrag — written in the värmepump page as a generally true statement about the Swedish tax benefit (it exists, the site does not claim a specific amount). Confirm the firm handles ROT administration directly (most VVS firms do)
- [ ] Serviceavtal standard terms — site says "Vi erbjuder serviceavtal för BRF och företag." Confirm and clarify basic structure before adding detail
- [ ] Akutberedskap / jourtjänst — deliberately omitted. If a jour is offered and real, it should appear on a small dedicated page. Do NOT add a 24/7 claim unless it is literally true
- [ ] Garantitider — only referenced as "branschsedvanliga garantier". Confirm and optionally replace with specifics (e.g. konsumentens ångerrätt, materialgaranti enligt tillverkare)

### Geography
- [ ] Confirmed service area: currently "Borås, Dalsjöfors, Fristad, Sandared, Sjuhärad". Confirm correct and add or remove places
- [ ] Are there areas the firm explicitly does NOT cover? — worth stating as "Främst Sjuhärad" with a soft boundary

### Contact
- [x] Phone: 076-776 00 06 (from brief — treated as verified)
- [x] Email: johan@anderssonvvs.se (from brief — treated as verified)
- [x] Domain: https://www.anderssonvvs.se/ (from brief — treated as verified)
- [ ] Secondary phone or office number
- [ ] Preferred inbound channel during office hours (phone vs. offert-form)
- [ ] Instagram / Facebook handles — not linked on the site; add if relevant

### Social proof that is NOT on the site
- [ ] The site deliberately contains **zero** testimonials, star ratings, review badges, or "5.0 på Google"-style claims. These may only be added once (a) the firm has real reviews, (b) the review platform's terms allow display, and (c) the specific quotes / scores are current
- [ ] A JSON-LD `AggregateRating` block is **not** included. Add only when real data is current

---

## Copy lines that walk close to the line — confirm before launch

The following lines in the generated copy are written generically but could read as implied claims. The client should verify each is accurate:

| File | Line (paraphrased) | What must be true |
|---|---|---|
| index.html | "Lokal VVS-firma i Borås" | Correct |
| index.html | "F-skatt, ansvarsförsäkring och teknisk dokumentation enligt branschstandard" | Firm has F-skatt + ansvarsförsäkring; documentation refers to protokoll e.g. Säker Vatten-intyg if applicable |
| index.html | "Vi ger ett kostnadsförslag innan arbetet startar" | Actually true of how the firm works |
| index.html | "Vi arbetar löpande med bostadsrättsföreningar och företag" | There is at least ongoing BRF/företag work |
| badrumsrenovering-boras.html | "Tätskikt enligt branschregler" | Confirm BKR/GVK-trained installer |
| varmepump-boras.html | "Certifierad för ingrepp i köldmediesystem (F-gas)" | ONLY include if currently held. If not, remove before launch. |
| varmepump-boras.html | "ROT-avdrag administreras direkt på fakturan" | Standard for Swedish VVS firms but confirm |
| rormokare-boras.html | "Serviceavtal för BRF och företag" | Confirm the firm actively offers this product |

If any of these cannot be confirmed, the safe action is to remove or soften — NOT to rephrase them as stronger claims.

---

## Items intentionally left out

To preserve editorial restraint and commercial honesty, the following were deliberately NOT added, even though they would lift conversion:

- "15 år av erfarenhet" / any specific year count
- "Nöjda kunder i Borås sedan XXXX"
- "Hundratals badrum renoverade"
- "4,9 av 5 på Google"
- Named logotypes of BRFs or companies in a trust-bar
- Named manufacturer logos (Nibe, IVT, Vola, etc.)
- Generic fake testimonials

If the client provides verified versions of any of these, they can be added in a targeted-revision pass.
