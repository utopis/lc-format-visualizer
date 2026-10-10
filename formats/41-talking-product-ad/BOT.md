# BOT.md · generate a "Talking product (AI-animated product as narrator)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 15-30s, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@koloveski](https://x.com/koloveski/status/2076868032002150833) · A fully animated product video: an Amazon logo, "ONLY ONE CLICK", a parcel dropping in, an object rising out of a box, then the Amazon logo again. The product animates itself with no presenter.
- Example: [@adamtaylorl](https://x.com/adamtaylorl/status/2105251325130739743) · 1. The talking dog The whole story is told by the dog and the timeline tells the owner exactly when to expect results. Tell your story from the view o
- Example: [@rirahcreates](https://x.com/rirahcreates/status/2092163067073241239) · We're entering an era where your marketing doesn't have to look ordinary. With AI, your ideas can literally come to life. Join AI Content Lab and lear
- Example: [@DBackendBesties](https://x.com/DBackendBesties/status/2105653073276207449) · Day 1/30 of creating AI-powered ads for brands. I created this 3D animated product ad for @oraimomate to show how AI can help e-commerce brands turn t
- Example: [@AgentOpusAI](https://x.com/AgentOpusAI/status/2082224622255374394) · Making an animated product ad used to be a project. Making them at scale used to take a month. We took down both. Full tutorial 👇 https://t.co/6pMG6df

### Live paid ads in this format (2 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Hemios: Talking-product CGI skit (Hemios, "I'm not an accessory, Karen")** (254 days live): A Pixar-style couple in bed talk to an animated hematite ring: "I have to apologize… I thought you were a scam… I'm not an accessory, Karen. I'm 2,000 years of natural hematite. I was fixing men before pills existed." 32 s.
- **Penrose Skin: Talking-jar CGI rivalry ("You copied me! That's theft!")** (89 days live): A CGI designer-cologne bottle argues with the Penrose jar: "You copied me! That's theft!" / "Can't copyright a scent, babe… And I've got your exact same scent. Plus pheromones. For $220 less." 43 s.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-2s | The product with animated eyes and mouth, close-up on a bathroom shelf | "I'm the necklace she wore in the ocean 47 times." |
| 2-15s | Product "remembers" moments (shower, sea, a date) as quick cutaways | Speaks in first person |
| 15-25s | Product winks | "Still gold. Get me at [brand]." |

### Prompts

**Kling / Pika (image-to-video)**

```
animate the gold necklace in this photo with small expressive cartoon eyes and a mouth, it talks to camera, keep the jewelry design identical, soft bathroom light, 5s
```

**Voice (ElevenLabs)**

```
Warm, witty, female, 30s, slight smile in the voice; stability 40, similarity 75.
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
- [ ] Files named `F41-<concept>-<variant>`; tracking tag `utm_content=F41-<concept>-<variant>`.
- [ ] Avoid: Keep the product recognisable; eyes and mouth only, no redesign.
- [ ] Avoid: Claims spoken by the product are still ad claims.

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
5. Name every asset `F41-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F41
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

The product itself gets eyes/mouth (AI animation) and speaks to camera: "I'm the necklace she wore in the ocean 47 times." Personification makes the mechanism a story.

### Why it works

- Novelty stops the scroll; product is literally the protagonist.
- Ran 183 days for a hair brand (@FedotOff90).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-3s | Animated LC necklace on vanity | "Hi. I'm the necklace she refuses to take off." |
| 3-15s | Cuts to necklace "experiencing" shower, pool | "Shampoo? Fine. Chlorine? Fine. 14K PVD, baby." |
| 15-20s | Stack of friends | "Bring my friends. Any 7 for $85." |

### Hooks

- "I'm the necklace she never takes off"
- "Day 180 on her neck. Still gold."

### Production recipe

1. Generate base product shots; animate with an image-to-video model + lip-sync voice.
2. Keep voice consistent (persona); label as AI animation.
3. 15-25s.

### Existing bot prompt

```
Write 5 first-person scripts (≤55 words) for an animated LC necklace/ring narrator with a witty, warm persona; include one PDP fact each.
```

### Variants to test

- Character voice
- Product

## Reference examples

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @FedotOff90 (25L/20BM/3kV): Hair-thinning ads 180+ days: persona page with AI-animated shampoo bottle (199 ads, 183d), pool side-by-side test (215d), "don't put this on your face" UGC (309 — https://x.com/FedotOff90/status/2097761790621057320
- @Ecombos_Ai (22L/14BM/793V): AI ecom format tiers: S = AI animation, AI singing, AI native statics → advertorial; A = AI before/after, AI podcast, talking product; F = AI avatar reading scr — https://x.com/Ecombos_Ai/status/2107157131010965744
- @koloveski (183L/112BM/191kV): 🚨 I made a fully animated product video for Amazon without touching a traditional editing workflow. I used Dreamina Octo as my AI creative partner, and it took  — https://x.com/koloveski/status/2076868032002150833
- @AgentOpusAI (16L/22BM/6kV): Making an animated product ad used to be a project. Making them at scale used to take a month. We took down both. Full tutorial 👇 https://t.co/6pMG6dfEhs https: — https://x.com/AgentOpusAI/status/2082224622255374394
- @raph_guilhem (8L/5BM/1kV): Our best clients are generating their highest performing Meta ads with one format: animated product videos. Origami style. Voxel. Minecraft. Pixar. Paper craft. — https://x.com/raph_guilhem/status/2076713068982100369
