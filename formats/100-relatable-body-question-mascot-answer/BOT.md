# BOT.md · generate a "Relatable body question + in-app answer (\"at what age did you find out…\" reaction, mascot explains)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 12-17s, 1080x1920, creator selfie + answer card; works muted), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@jasonugc](https://x.com/jasonugc/status/2108273335314641352) · A creator walking outside at sunset. The on-screen text says "Be honest.. is your September period late??" and she gives the camera a knowing look (0:00-0:03). At 0:05 it hard-cuts to the app: a cute white dragon mascot ("Earth Realm"), "Day 33 | 5 days longer than your usual cycle, Period delayed". Under it is a Luteal-phase card: "Women's health fact they don't teach you in school: if your perio
- Example: [@leonclipping](https://x.com/leonclipping/status/2107903429490135362) · this app spams ONE format and pulled 522M views with organic UGC a 4 sec shocked reaction to a period fact nobody told you, then the dragon in the app
- Example: [@consumerxai](https://x.com/consumerxai/status/2107834606368293123) · 121M views lost to 9.6M on the number that matters more for engagement saves -> a save means "i'm going to do this later" and has high intent -> calor
- Example: [@guillemcraft](https://x.com/guillemcraft/status/2075221274591101354) · 50k+ views on insta in just ONE HOUR i posted a video while waiting for my flight to Menorca and went viral i found a format that works and i just rep

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-1s | Front camera, chest-up, bathroom/bedroom, natural light. Eyes widen, hand to mouth. No product visible. | Caption (top third, 64px white, black stroke): "at what age did you find out 'gold tone' means there's no gold in it??" |
| 1-4s | Hold the reaction; slow head shake, mouths "what". Do NOT talk. | Trending sound at -20 dB, or silence + one word "what??" |
| 4-9s | Hard cut to 9:16 answer card: brand character/avatar top-left, 2 chat bubbles typing in (CapCut "typewriter" 0.6s each) | Bubble 1 (≤22 words): "Gold tone = colour only. Most of it is brass with a thin plate that wears off with water and sweat." |
| 9-14s | Hands-only macro: LC necklace under a running tap, then on a towel, still bright | Bubble 2: "14K PVD bonds the gold to steel. Shower, swim, sleep in it." |
| 14-17s | End card: product grid on warm beige | "any 7 for $85" + "which fact next? 👇" |

### Prompts

**Fact bank (Claude)**

```
Give me 60 true, surprising facts about gold jewelry, plating, sweat, water and skin that women 25-45 often learn late. Phrase each as "at what age did you find out ...?". Then mark which ones are supported by these product facts: {{PDP_FACTS}}. Drop anything medical.
```

**Answer card (Canva/Figma)**

```
1080x1920, background #F6EFE6, avatar circle 160px top-left, chat bubbles 900px wide, 44px Hanken Grotesk, max 2 bubbles, 22 words each. Duplicate the page per fact.
```

**Creator brief**

```
Film 10 reactions in one session: front camera, 4K 30fps, window light, neutral top, no jewelry visible. React to reading the fact for the first time; 3-5 s each; no speaking.
```

**Spanish version**

```
Translate the hook as a native Mexican-Spanish speaker would say it on TikTok, keep "¿a qué edad te enteraste...?" structure; ≤14 words.
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
- [ ] Files named `F100-<concept>-<variant>`; tracking tag `utm_content=F100-<concept>-<variant>`.
- [ ] Avoid: The reaction must happen before any product appears; product in the first second kills it.
- [ ] Avoid: One fact per video. Two facts = no one remembers either.
- [ ] Avoid: Facts must be true and checkable; a wrong fact in the comments sinks the account.
- [ ] Avoid: Keep the answer card short enough to read twice in 5 seconds.

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
5. Name every asset `F100-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F100
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

A 3-5 second selfie of a creator reacting to a **body fact nobody told her** (caption: *"at what age did you find out that [surprising body fact]?"* or *"why did nobody tell me [fact]"*), then a cut to the app screen where the app's character (Musa uses a cute dragon) **answers the question** in 2-3 chat bubbles. The question is the content; the app is the place the answer lives. One hook, hundreds of creators, two languages.

It is different from F28 (reaction + demo) because the viewer is not watching a feature: they are getting an answer to a question they also never asked. The comment section becomes "I'm 34 and just found out", which is what pushes it.

### Why it works

- Taboo-adjacent body questions (period, discharge, cycle, skin) are things women google privately and never see discussed; seeing a peer react gives permission to watch and comment.
- "At what age did you find out…" is a participation prompt: every comment is someone's age, so comments explode.
- The app is framed as the friend who explains, not a product pitch; the mascot makes it soft and screenshot-able.
- One template, infinite facts: a fact bank of 200 questions = 200 videos per creator, no new concept work.
- Language-agnostic: Musa runs English and Spanish creators on the same template.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-1s | Selfie, eyes wide / hand over mouth, bathroom or bedroom | Caption top: "at what age did you find out that gold-plated jewelry is basically a thin coat over brass??" |
| 1-4s | Creator slowly shakes head, mouths "what" | Trending audio low; no voice or one word ("what??") |
| 4-9s | Screen recording: LC "Ask Goldie" Q&A card / PDP FAQ or a simple branded explainer card | Bubble 1: "Most cheap gold jewelry = brass + a micro-layer of gold. Water and sweat wear it off → green skin." |
| 9-14s | Hands: 14K PVD necklace under the tap, still gold | Bubble 2: "PVD bonds the gold at a molecular level. That's why ours can go in the shower." |
| 14-17s | End card | "any 7 for $85 · link in bio" (organic) / CTA button (paid) |

### Hooks

- "at what age did you find out your necklace turning green isn't your skin's fault?"
- "at what age did you find out 'gold tone' means zero gold?"
- "why did nobody tell me you can shower in real gold jewelry"
- "I'm 31 and just found out what 'vermeil' actually means"
- "at what age did you find out sweat is why your earrings itch?"

### Production recipe

1. **Fact bank (1 h):** 100 true, surprising, PDP-backed facts about gold jewelry, skin, plating, sweat, water, allergies. Each one phrased as "at what age did you find out…". Verify each against the PDP / supplier spec.
2. **Answer cards:** design one reusable 9:16 answer template (character or brand avatar + 2-3 chat bubbles). Make it in Figma/Canva; swap text per video.
3. **Creator brief:** 3-5 s silent reaction, filmed front camera, natural light, no product in the first shot. Creators pick facts from the bank.
4. **Edit (CapCut):** caption 60-70 px white with black stroke, top third; hard cut at 4 s to the answer card; product shot; end card. 12-17 s total.
5. **Volume:** 10-30 creators × 1/day for 3 weeks; Spanish creators on the same bank.
6. **Promote:** top 3 by saves → Spark/Partnership ads; keep the question as the ad's primary text.

### Existing bot prompt

```
You are writing for Louise Carter (14K PVD gold jewelry you can shower, swim and sleep in; any 7 for $85).
Write 30 hooks in the exact pattern "at what age did you find out [true surprising fact about gold jewelry, plating, skin reactions, water or sweat]?"
Rules: every fact must be supported by {{PDP_FACTS}}; no medical claims; no competitor names.
For the best 10, write: (a) a 2-bubble answer the brand character gives (max 22 words per bubble), (b) the product shot that proves it, (c) a Spanish version of the hook.
```

### Variants to test

- Question wording ("at what age" vs "why did nobody tell me")
- Answer card: mascot vs plain brand avatar vs creator voiceover
- Reaction intensity (shock vs laugh vs facepalm)
- Language (EN vs ES)
- Fact category (plating vs skin vs care)

## Reference examples

See [examples/README.md](examples/README.md) (4 posts). Top 5:

- @leonclipping (44L/66BM/3kV): Musa app: ONE format (4-sec shocked reaction to a body fact → mascot explains) = 522M views, 930 videos >100K, 100+ creators. — https://x.com/leonclipping/status/2107903429490135362
- @guillemcraft (28L/29BM/11kV): 50k+ views on insta in just ONE HOUR i posted a video while waiting for my flight to Menorca and went viral i found a format that works and i just repeat it ove — https://x.com/guillemcraft/status/2075221274591101354
- @jasonugc (12L/6BM/652V): this period app quietly did 522M views 930 videos past 100k 100 creators one format every clip is a relatable body question "at what age did you find out..." th — https://x.com/jasonugc/status/2108273335314641352
- @consumerxai (3L/1BM/293V): 121M views lost to 9.6M on the number that matters more for engagement saves -&gt; a save means "i'm going to do this later" and has high intent -&gt; calorie a — https://x.com/consumerxai/status/2107834606368293123
