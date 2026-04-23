# AI Image & Video Prompts — Anderssons VVS

Generation-ready prompts for every visual referenced in `image-plan.md`. Each prompt is self-contained and does not assume a specific generator — they should work with Midjourney v6+, SDXL, Flux, Runway, Luma, or Veo with light adaptation.

Global style tokens to append to any prompt when the generator allows it:

> *editorial, architectural, cinematic still, natural diffused daylight, low saturation, warm neutrals (deep petrol, warm sand, muted brass, off-white), medium-format feel, prime lens, shallow to moderate depth of field, no text, no watermark, no stock photography look*

Global **negative prompt** (for generators that support it):

> *stock photography, uniformed tradespeople posing, fake smiles, over-bright interior, red, orange, neon, cheesy, clip art, fisheye, oversharpened, hdr, tacky, candles, bouquet, towels folded into swan, low-budget brochure, clutter, plastic props, cartoon*

---

## HERO VIDEO

### `/assets/placeholders/hero-vvs-video-loop.mp4`

**Format**: video, 6–8s seamless loop, 1920×1080 (master 3840×2160), 30fps, no audio, h.264 or av1.

**Prompt**:
> Extreme close-up, cinematic slow-motion shot of clear water flowing from a brushed brass mixer tap into a shallow off-white stone basin. The water forms a smooth, glassy column before it breaks into a quiet splash. Warm diffused daylight from a window camera-left casts a soft highlight on the brass. Background is a blurred warm-sand interior wall with a hint of petrol-blue shadow. Gentle, unhurried pace. No people. No text. No music cues. Short, seamlessly loopable 6-second passage. Photographed feel, not CGI. Neutral colour grade, warm midtones, protected highlights.

**Direction notes for the generator / editor**:
- Water must feel controlled, not a gush. Turn pressure down mentally.
- The tap must read as a *quality* fixture — brushed brass, not chrome, not gold-plated. Avoid any visible brand marks.
- Loop point should be where the water stream is at a steady state so the splice is invisible.
- Avoid macro extremes that become abstract — viewer should still read "tap + water + basin".

### `/assets/placeholders/hero-vvs-poster.jpg`

**Format**: JPG, 1920×1080.

**Prompt**:
> Single still frame from the hero video above, captured at the moment the water column is steady and the splash is small. Same composition, same light, same palette. No motion blur. Editorial photograph feel.

---

## STILL IMAGERY

### `/assets/placeholders/service-badrum.jpg`

**Format**: JPG, 1600×2000 (4:5).

**Prompt**:
> Editorial detail photograph of a finished contemporary Swedish bathroom. Warm off-white microcement wall, sand-toned limestone floor, a brushed brass rain shower head and matching valve trim. Soft diffused daylight from a tall window outside frame. One corner composition, not centered. Quiet, uncluttered. No products on display, no bottles, no towels. Shallow depth of field with the brass fixture in sharp focus.

### `/assets/placeholders/service-varmepump.jpg`

**Format**: JPG, 1600×2000 (4:5).

**Prompt**:
> Exterior mid-distance photograph of a modern outdoor air-to-water heat pump unit installed against a vertical Nordic wood-clad house wall. Overcast morning light, muted colour palette, grass and gravel at base, neat copper line-set running along the wall. Architectural photography feel, not product photography. No people. No brand markings visible on the unit.

### `/assets/placeholders/service-service.jpg`

**Format**: JPG, 1600×2000 (4:5).

**Prompt**:
> Close-up photograph of a tradesperson's hands tightening a brass compression fitting under a kitchen sink. Warm task light from the right, shadowed cabinetry in the background. Clean hands, worn but cared-for tools, a wrench and a small water level visible. Focus on craft and precision. No face visible. Neutral warm palette.

### `/assets/placeholders/service-brf.jpg`

**Format**: JPG, 1600×2000 (4:5).

**Prompt**:
> Interior photograph of a well-organised multi-unit building utility room: neatly run insulated hot and cold water pipes, a hydronic manifold with individual circuit ports, colour-coded insulation, clean concrete floor, cool diffused daylight from a small high window. No clutter, no people. Architectural-documentary mood, restrained palette.

### `/assets/placeholders/badrum-highlight.jpg`

**Format**: JPG, 1500×2000 (3:4 portrait).

**Prompt**:
> Full-height editorial portrait photograph of a warm-neutral bathroom in a private home. Microcement walls in warm off-white, sand limestone flooring, a single freestanding warm-toned vanity with a brushed brass tap, soft natural light from a slim floor-to-ceiling window at the far end. Subtle atmosphere, no people, no toiletries. Feels lived-in but composed. Shallow depth of field.

### `/assets/placeholders/craft-signature.jpg`

**Format**: JPG, 2000×1333 (3:2).

**Prompt**:
> Tactile close-up of two hands holding a brushed metal pipe fitting against a dark warm-grey background. Slight motion at the fingers suggesting work in progress. Single directional warm light from the upper left. Skin tone natural, hands lived-in but clean. Minimal props — just the fitting and the hands. Moody, quiet, editorial.

### `/assets/placeholders/og-image.jpg`

**Format**: JPG, 1200×630.

**Prompt**:
> Cropped and recomposed frame of the hero image, tightened to 1200×630 with the brass tap and water column positioned on the left third. Small, restrained "Anderssons VVS · Borås" wordmark in thin brass-toned letters in the lower left corner, safely inside a 48px margin. The right side intentionally left with quiet negative space.

### `/assets/placeholders/service-badrum-hero.jpg`

**Format**: JPG, 2400×1350 (16:9).

**Prompt**:
> Wide editorial photograph of a bathroom mid-renovation: bare substrate walls with visible tätskikt layer applied, studs and pipe rough-in still exposed on one wall, a stack of new brass fixtures laid out on a protective cloth on the floor, soft north-facing daylight. Controlled mess, not chaos. No people.

### `/assets/placeholders/service-varmepump-hero.jpg`

**Format**: JPG, 2400×1350 (16:9).

**Prompt**:
> Indoor photograph of an installer in focused profile close-up, mid-task on an indoor värmepump module in a laundry/utility space. Hands in foreground, face softly out of focus. Tools on a cloth nearby. Warm task light mixing with cool daylight. Architectural documentary feel, not corporate.

### `/assets/placeholders/service-rormokare-hero.jpg`

**Format**: JPG, 2400×1350 (16:9).

**Prompt**:
> Top-down photograph of a clean work surface: a pipe cutter, four copper elbow fittings neatly arranged, a small spirit level, a measuring tape partly extended, a leather-covered notebook with handwritten measurements. Warm diffused daylight. Deep petrol-blue workbench surface. Subtle brushed-brass accents on the tools. Quiet, intentional composition.

---

## USAGE NOTES

- All prompts are written in English because image generators parse English more reliably; the resulting visuals are palette-neutral and fit the Swedish copy.
- For any generator run, produce at least 4 variations and select the one closest to the palette token set.
- Resize / crop to the stated aspect ratio after generation; do not rely on the generator's native ratio alone.
- Export JPGs at quality 82–86, mozjpeg if available. Strip metadata before upload.
- Video should be encoded both as MP4 (h.264) and WebM (vp9) for broad browser support; the HTML currently references the MP4 only and can be extended to a `<source>`-based fallback in a follow-up revision.
