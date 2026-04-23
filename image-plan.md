# Image & Video Plan — Anderssons VVS

All visuals are planned as **AI-generated assets**. No real photography has been supplied and no real photos are claimed to exist. The HTML references local asset paths that will resolve once the planned assets are produced. Until then, `styles.css` provides restrained neutral backgrounds so the page never looks broken, but also never fabricates fake imagery.

See `ai-image-prompts.md` for generation-ready prompts for each entry below.

---

## Visual direction summary

Overall mood: *architectural, technical, crafted, warm neutral.* Water, brushed metal, interior light, close-up hands-on work. No lifestyle/family imagery. No stock-photo vans or uniformed tradespeople posing. No candles, flowers, towels — this is a VVS firm, not a spa.

Palette to bias prompts toward:
- deep petrol (shadows / water highlights)
- warm sand (walls / interiors / ambient light)
- muted brass (fixtures / fittings)
- off-white (surfaces / tiles / concrete plaster)

Photographic language:
- close-up or mid-distance — never overview
- natural diffused daylight preferred
- slight cinematographic warmth, low saturation
- medium format / prime lens feel, shallow-to-moderate depth of field
- never glossy / commercial / stock

---

## Hero video (homepage)

Justification: hero video is justified for the homepage because (a) the client's positioning requires a premium visual identity and a still image cannot deliver the same atmosphere, (b) water + fixture cinematography is thematically aligned with VVS, and (c) Vola/Dornbracht-referenced attitudes favour motion over stills. Downgrades gracefully to a poster image on mobile and under `prefers-reduced-motion`.

| Field | Value |
|---|---|
| Purpose | Establish premium, technical, calm atmosphere from the first second |
| Subject | Close-up of water flowing from a brushed brass / polished chrome tap into a sand-toned stone basin |
| Emotional goal | Quiet craft, controlled technique, domestic warmth |
| Media type | Video (looped, 6–8s, muted, autoplay) |
| Aspect ratio | 16:9 (also 21:9 master if produced) |
| Resolution | 1920×1080 (master 3840×2160) |
| Local file path | `/assets/placeholders/hero-vvs-video-loop.mp4` |
| Poster fallback | `/assets/placeholders/hero-vvs-poster.jpg` (1920×1080) |
| Loop length | 6–8 seconds, seamless |
| Sound | None — video must be silent by design (autoplay requires muted) |

Mobile behaviour: `<video>` is hidden via CSS below `≤ 640px` and replaced by the poster image, to respect mobile data budgets.

---

## Key still imagery

### 1. Services section — Badrumsrenovering
| Field | Value |
|---|---|
| Purpose | Illustrate the flagship service visually |
| Subject | Detail shot of a finished badroom corner: brushed brass rain shower, off-white microcement wall, warm sand floor, soft window light |
| Emotional goal | Warmth + precision |
| Media type | Image |
| Aspect ratio | 4:5 |
| Local file path | `/assets/placeholders/service-badrum.jpg` |

### 2. Services section — Värmepump
| Field | Value |
|---|---|
| Purpose | Visualise heat-pump install without stock imagery |
| Subject | Exterior close-up of a modern outdoor värmepump unit against a calm wood-clad house wall, grey morning light |
| Emotional goal | Considered installation, real residential context |
| Media type | Image |
| Aspect ratio | 4:5 |
| Local file path | `/assets/placeholders/service-varmepump.jpg` |

### 3. Services section — Service & läckage
| Field | Value |
|---|---|
| Purpose | Signal hands-on technical care |
| Subject | Hands working on a copper / brass fitting under a sink, wrench visible, warm task light |
| Emotional goal | Capable, patient, careful |
| Media type | Image |
| Aspect ratio | 4:5 |
| Local file path | `/assets/placeholders/service-service.jpg` |

### 4. Services section — BRF & företag
| Field | Value |
|---|---|
| Purpose | Establish commercial/BRF scope without corporate cliché |
| Subject | Clean utility room with pipework, manifold, insulated pipes, muted cool light |
| Emotional goal | Organised, professional, reassuring |
| Media type | Image |
| Aspect ratio | 4:5 |
| Local file path | `/assets/placeholders/service-brf.jpg` |

### 5. Badrum highlight (homepage mid-section)
| Field | Value |
|---|---|
| Purpose | Showcase flagship renovation as editorial spread |
| Subject | Full-height photograph of a finished warm-neutral bathroom with brass fittings, microcement, soft window light |
| Emotional goal | Quiet pride in the result |
| Media type | Image |
| Aspect ratio | 3:4 (portrait) |
| Local file path | `/assets/placeholders/badrum-highlight.jpg` |

### 6. Craft / approach signature
| Field | Value |
|---|---|
| Purpose | Human, tactile proof of care |
| Subject | Hands holding a brushed-metal fitting, slight motion blur, dark moody background |
| Emotional goal | Precision, craft |
| Media type | Image |
| Aspect ratio | 3:2 |
| Local file path | `/assets/placeholders/craft-signature.jpg` |

### 7. Open Graph / social share
| Field | Value |
|---|---|
| Purpose | Link preview across social and messaging |
| Subject | Cropped frame from the hero video poster, with small brass wordmark bottom-left |
| Media type | Image |
| Aspect ratio | 1200×630 |
| Local file path | `/assets/placeholders/og-image.jpg` |

### 8. Service page — Badrumsrenovering hero
| Field | Value |
|---|---|
| Subject | Wide angle of a badroom mid-installation: bare tile substrate, tätskikt visible, fixtures laid out carefully |
| Aspect ratio | 16:9 |
| Local file path | `/assets/placeholders/service-badrum-hero.jpg` |

### 9. Service page — Värmepump hero
| Field | Value |
|---|---|
| Subject | Installer in focused close-up working on indoor värmepump unit, soft natural light |
| Aspect ratio | 16:9 |
| Local file path | `/assets/placeholders/service-varmepump-hero.jpg` |

### 10. Service page — Rörmokare hero
| Field | Value |
|---|---|
| Subject | Worktop detail — pipe cutter, copper fittings, notebook with measurements, warm diffused light |
| Aspect ratio | 16:9 |
| Local file path | `/assets/placeholders/service-rormokare-hero.jpg` |

---

## Design dependency on strong imagery

This design **relies** on imagery for its premium effect. Without the planned assets produced, the site reads as structurally strong but atmospherically thin. The CSS interim state is intentionally neutral (petrol/sand gradients, never fake photographs) so the build never deceives — but final delivery is not complete until the above assets are generated and placed.

See `build-notes.md` → "Media readiness status" for the current state.

---

## Real asset override rule

Per `/.claude/CLAUDE.md` asset-protection rule: once real files exist in `/assets/real/`, `/images/`, or `/videos/`, the HTML should be updated (via a targeted-revision run) to reference them, and the placeholder paths should be retired. The placeholder paths under `/assets/placeholders/` are editable; the real-asset folders are NOT to be overwritten.
