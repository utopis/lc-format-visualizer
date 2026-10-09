# BOT.md · generate a "Whiteboard explainer (marker diagram of the mechanism, static or video)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: Photo of a whiteboard (static) or a 30-60s drawing video), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@artfully_amberr](https://x.com/artfully_amberr/status/2100249277029126306) · A creator drawing on a whiteboard while explaining ("that nobody talks about", "these dopamine levels"), with a graph curve, then the product page and a woman relaxing. It is a teacher-style explainer with a marker.
- Example: [@0xROAS](https://x.com/0xROAS/status/2086523553717883287) · we finally cracked whiteboard ads inside ai ads community. this is extremely engaging and you can use it for whatever use case you want: - ecom - saas
- Example: [@adswithcami](https://x.com/adswithcami/status/2057020088457277861) · You don't need UGC creators for whiteboard ads now??
- Example: [@mattepstein](https://x.com/mattepstein/status/1998112905410318548) · 🚨 New ad type Whiteboard ads. We're seeing these CRUSH in ad accounts.
- Example: [@Ajain112](https://x.com/Ajain112/status/2102383908344193207) · India’s first fashion whiteboard ad. // needs minor editing. This is raw.
- Example: [@DavidRunsAds](https://x.com/DavidRunsAds/status/2093266262335909916) · Whiteboard ADS might be one of my favorite AI UGC formats yet. instead of just talking at the camera, you can actually explain the idea visually draw 
- Example: [@mattepstein](https://x.com/mattepstein/status/2006398516093153407) · 5. Authority whiteboard ad
- Example: [@oliverwhudson](https://x.com/oliverwhudson/status/2049158983106081277) · Whiteboard ads are still flying for us. We launched one for a supplement brand targeting a HRT angle that surfaced in research. First 7 days, top spen
- Example: [@navneet_214](https://x.com/navneet_214/status/2053875278691070165) · Whiteboard ad format still works in 2026 and this one for a teen body soap brand proves it raw. readable. relatable. converts. want static ads like th

### Live paid ads in this format (3 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Rachel's Tea: Animated numbered-benefit product spec video** (424 days live): Motion-graphic: bottle on orange/white, '100 BILLION PROBIOTICS' supers, numbered 01 / 02 benefit callouts sliding in, ORDER NOW end card; music only.
- **Pinch Magic Fiber: Presenter explainer with 'this is what 30 g of fiber looks like'** (288 days live): Bearded presenter talks fiber science over b-roll (poop-shape hook, psyllium close-ups, comparison chart 'Premium Psyllium / 0 g sugar / Bromelain') and the key visual: a table of whole foods = 30 g fiber, 'if you can't eat this every day, here's this'. Ends o
- **Smooche · Smooche: A whiteboard sketch** (20 days live): A whiteboard sketch: "GLP-1 alone | GLP-1 + peptides. YOU LOSE THE WEIGHT. YOU GAIN THE LINES."

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | Hand starts drawing on a whiteboard, top-down or straight-on | "why your gold jewelry turns green (nobody tells you this)" |
| 3-25s | Diagram: a thin plating layer wearing off vs a bonded PVD layer | Marker labels, narrator explains |
| 25-40s | Cost math: "$20 x 6 replacements vs one $85 stack" | Simple numbers |
| 40-50s | Product placed on the board | CTA |

### Prompts

**Shoot**

```
Whiteboard + black and gold markers, ring light from the side to avoid glare, phone on an overhead arm, record at 1x then speed up to 2x.
```

**Script (Claude)**

```
Write a 45-second whiteboard explainer: problem, why the usual fix fails, how [product] works, cost comparison, CTA. Each line must correspond to something drawn.
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
- [ ] Files named `F76-<concept>-<variant>`; tracking tag `utm_content=F76-<concept>-<variant>`.
- [ ] Avoid: The diagram must be technically correct.
- [ ] Avoid: Cost math must use real prices.

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
5. Name every asset `F76-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F76
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

A hand-drawn whiteboard diagram explaining why the usual fix fails and how the product works (layers, timelines, cost math). Shown as a photo of the whiteboard or a 30s marker-drawing video with a person addressing the viewer by name ("Hey Priya, you need this").

### Why it works

- Teacher framing creates authority without claiming credentials.
- A marker drawing feels homemade and honest.
- Simplifies LC's real edge (bonded PVD vs plating) into one picture.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static | Whiteboard photo: two drawn layers "plating (wears off)" vs "PVD (bonded)" + arrows + LC necklace taped on | Headline: "whiteboard alert ✏️" |
| Video 30s | Hand draws the diagram, VO explains | "Before you buy another gold chain…" |

### Hooks

- "Whiteboard alert ✏️ why plating wears off"
- "Before you buy another gold chain, look at this"
- "The 2-layer drawing every jewelry buyer should see"

### Production recipe

1. Use a real whiteboard and the founder's handwriting.
2. One idea per board: layers, cost per wear, care.
3. Shoot the static and a 30s time-lapse.

### Existing bot prompt

```
Write 4 whiteboard explainers for LC: what to draw (labels, arrows), 60-word VO, headline. Use only {{PDP_FACTS}}.
```

### Variants to test

- Static vs time-lapse
- Named-address hook vs generic

## Reference examples

See [examples/README.md](examples/README.md) (6 posts). Top 5:

- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @artfully_amberr (9L/0BM/252V): Here's a #UGCexample I made for Stasis. This whiteboard explainer concept has generated revenue for the client. For this creative, I leaned into my background a — https://x.com/artfully_amberr/status/2100249277029126306
- @0xROAS (213L/357BM/24kV): here's another BANGER ai ad style you can use in your ads it's called BRB Whiteboard Explainer style (my fav) there's infinite ways you can scale your creative  — https://x.com/0xROAS/status/2094086530973229173
- @raph_guilhem (55L/105BM/7kV): 30 Meta ad formats folder tree (hooks, founder content, etc.). — https://x.com/raph_guilhem/status/2083288607062732816
- @Ecombos_Ai (28L/26BM/2kV): 10 AI UGC styles: talking-head testimonial, product-in-hand, first-try reaction, fake podcast, street interview, comment reply, unboxing, DITL/GRWM, before/afte — https://x.com/Ecombos_Ai/status/2103180929057407425
