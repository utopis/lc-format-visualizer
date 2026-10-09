# BOT.md · generate a "'3 reasons why' / X reasons listicle ad"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 20-40s video, carousel or static), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@lorenzo_pravata](https://x.com/lorenzo_pravata/status/2090384597737508973) · A doctor in a white coat talking to camera, intercut with CGI of a bone breaking down and microscopic cells. Each "reason why" gets its own visual, then it cuts back to the doctor.
- Example: [@FomoAiCommunity](https://x.com/FomoAiCommunity/status/2045575780831514799) · 3 Reasons Why You Need InkJoy at Home 1. Stop wasting time on static art 2. Never miss family moments 3. Become the house everyone talks about InkJoy 
- Example: [@ZedNilm1](https://x.com/ZedNilm1/status/2054297982577901656) · "5 science-backed reasons why an award-winning German scientist recommends complete gut repair for men struggling with dad bods." Every word in that h
- Example: [@Ubaidullah_llc](https://x.com/Ubaidullah_llc/status/2103025457876836606) · A couple months ago, I got the lowest CPA of $49.22 for my client on a product with a $500 AOV through a listicle static. My biggest takeaway was that
- Example: [@DalyDee___](https://x.com/DalyDee___/status/2040779950085595240) · Big day for my client: One AI animation listicle ad. £20,268 in spend. 501 purchases. 17,676 clicks. £1.15 CPC. That's what one well built creative ca
- Example: [@Bogzabs96](https://x.com/Bogzabs96/status/2092929767993471081) · This ad is CRAZY from the team: The 3 reasons why: 1. Script is crazy good 2. Format includes an authority figure and looks like nothing in the ad acc
- Example: [@SeanKim436](https://x.com/SeanKim436/status/2102890739432566805) · Here are 3 reasons why the biggest consumer tech startups are POURING money into Canvas UGC over traditional influencer marketing in 2026 1. More volu

### Live paid ads in this format (3 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Rachel's Tea: Animated numbered-benefit product spec video** (424 days live): Motion-graphic: bottle on orange/white, '100 BILLION PROBIOTICS' supers, numbered 01 / 02 benefit callouts sliding in, ORDER NOW end card; music only.
- **Resilia · Resilia: “The parasite causing your ITCHY ANUS”** (1 days live): "The parasite causing your ITCHY ANUS": 01/02/03 numbered reasons with the pouch.
- **Resilia · Resilia: A landscape variant of the 01/02/03 numbered-reasons card** (1 days live): A landscape variant of the 01/02/03 numbered-reasons card.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-2s | Creator holds up 3 fingers + product | "3 reasons I stopped buying gold-plated jewelry" |
| 2-8s | Shower shot | "1: I shower in this." |
| 8-14s | Gift box | "2: it comes ready to gift." |
| 14-20s | Stack on wrist | "3: any 7 for $85." |
| End | Product | CTA |

### Prompts

**Claude**

```
From these reviews [paste], extract the 6 most-mentioned reasons. Write 3 listicles (3, 5, 7 reasons) as a 20s talking-head script, 8 carousel slides (max 10 words each) and one static headline.
```

### QA checklist (all must pass before hand-off)

- [ ] Hook lands in the first 1.5 s (video) or is readable at thumbnail size (static / slide 1).
- [ ] Removal test: delete the product from the script. If it still makes sense, rewrite so the product is the payoff.
- [ ] Matches the reference structure (same beat order and length band) before any creative twist.
- [ ] Uses only real product imagery for the product; AI is for backgrounds, characters or b-roll, and is disclosed where required.
- [ ] Every claim is on the brand's approved-claims list (PDP); no invented stats, reviews, doctors or customers.
- [ ] Captions burned in and inside the safe zone; sound-off still understandable.
- [ ] One clear CTA that matches the landing page offer.
- [ ] Three hook variants delivered for the same body (test hooks, not whole new ads).
- [ ] Files named `F39-<concept>-<variant>`; tracking tag `utm_content=F39-<concept>-<variant>`.
- [ ] Avoid: Each reason must be true and checkable.
- [ ] Avoid: Package the same reasons 4 ways (talking head, overlay, carousel, static) before changing the reasons.

<!-- QUICKSTART:END -->

## Inputs you need

- `BRAND`: name, product, price, offer, audience, 3-5 proof points, claims you may NOT make
- `REVIEWS`: 20+ customer reviews or comments (voice of customer)
- `ASSETS`: real product photos / video, logo, fonts, colors
- `CHANNEL`: organic (TikTok/IG/Shorts) or paid (Meta/TikTok/YouTube)

## Steps

1. Read **Format DNA** below and 3-5 files in `examples/` (prefer `curated`). Note the hook, the beat structure and the length.
2. Mine `REVIEWS` for the 3 strongest angles (problem, desire, objection) in the customer's words.
3. Write 3 concepts. For each: title, angle, hook (first line / first 2 seconds), full script or slide-by-slide copy, shot list or layout, on-screen text, CTA, caption.
4. Follow the **Production recipe** below for tools and prompts. Use real product imagery for the product itself; never invent product features or results.
5. Name every asset `F39-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F39
concept: <short name>
angle: <problem | desire | objection>
hook: "<first line / first 2s>"
beats:
  - t: "0-2s"
    visual: "..."
    text: "..."
    audio: "..."
caption: "..."
cta: "..."
production: {tools: [...], prompts: [...], est_cost: "...", est_time: "..."}
test: {channel: "...", budget: "...", success_metric: "..."}
```

## Guardrails

- No fake reviews, fake customers, undisclosed AI people presented as real customers, or invented stats. Disclose AI where the platform requires it.
- Follow `../_COMPLIANCE.md` and the brand's claim rules.

## Format DNA (from the playbook)

### What it is

A numbered listicle — "3 reasons I only wear 14K PVD", "5 reasons this is the best gift under $100" — delivered as talking head, voiceless overlay, carousel or static. Same message, packaged as a list.

### Why it works

- Numbers promise a finite, skimmable payoff → watch-through.
- Converts any winning message into a new framework (Entity ID) per @williamkast_.
- Easy for creators and AI to produce at volume.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | Creator holds up 3 fingers + necklace | "3 reasons I stopped buying gold-plated jewelry" |
| 2-8s | Shower shot | "1: I shower in this." |
| 8-14s | Gift box | "2: it comes ready to gift." |
| 14-20s | Stack | "3: any 7 for $85." |

### Hooks

- "3 reasons this is the only necklace I wear"
- "5 reasons it's the easiest gift this year"
- "3 reasons your jewelry turns green (and the fix)"

### Production recipe

1. Pull reasons from reviews (angle bank).
2. Produce 4 packagings: talking head, F30 overlay, carousel, static.
3. Hook variants: number (3 vs 5) and subject.

### Existing bot prompt

```
From {{REVIEWS}} extract the 6 most-mentioned reasons customers love LC. Write 3 listicles (3, 5, 7 reasons) as: 20s talking-head script, carousel slides (≤10 words each), static headline.
```

### Variants to test

- Number of reasons
- Packaging (video/carousel/static)

## Reference examples

See [examples/README.md](examples/README.md) (20 posts). Top 5:

- @ads4apps (412L/930BM/27kV): 39 Meta formats that convert (930 bookmarks): X reasons, IG story, us vs them, Venn, don't buy this, iPhone notes, text message, low stock, we're sorry, breakin — https://x.com/ads4apps/status/2081785032679518490
- @williamkast_ (252L/400BM/13kV): Formats by funnel: TOF founder/yapper/AI animation/natives/3 reasons/voiceless overlay; MOF comment reply/testimonial mashup/text wall; BOF urgency statics. — https://x.com/williamkast_/status/2103910235005935644
- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @williamkast_ (38L/46BM/3kV): Turn 1 winning ad into 5: same message, different frameworks (DITL, 3 reasons, old me/new me, phone call). — https://x.com/williamkast_/status/2086835243474985414
- @rirahcreates (12L/17BM/1kV): 20 UGC types: talking head, review, unboxing, testimonial, demo, problem/solution, before/after, GRWM, DITL, voiceover, routine, how-to, FAQ, 3 reasons why, POV — https://x.com/rirahcreates/status/2089827933561016787
