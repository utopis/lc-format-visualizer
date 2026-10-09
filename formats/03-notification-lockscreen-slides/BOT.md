# BOT.md · generate a "Notification / lock-screen 2-slide slideshow"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 2 slides, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@brainextends](https://x.com/brainextends/status/2099496707209994736) · A short slideshow built from big stat cards and phone UI: "#00", "4.8", "<$5K" tiles over lifestyle photos, then an iPhone lock screen at 9:41 with notification bubbles ("Follow your routine"). Two slides, phone-native look, no talking.
- Example: [@simonecanciello](https://x.com/simonecanciello/status/2035079759588163995) · brooo WHAT is this strategy? 3 pics slideshow, fake notification (curiosity = comments) and show your app. 1M views. $160k/month app.
- Example: [@enzoxmotion](https://x.com/enzoxmotion/status/2099622190970712321) · this app went from $1k to FUCKING $10k mrr in a WEEK. all it took was one slideshow, two slides total, that ended up crossing a million views nothing 
- Example: [@marcospb_](https://x.com/marcospb_/status/2010412391037878286) · 1M likes New TikTok slideshow banger found “Four years of a relationship and out of nowhere she sent me this.” Next slide: the breakup text. Right und

### Live paid ads in this format (1 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Japanese Taste: iPhone Notes checklist static (Japanese Taste)** (238 days live): An iPhone Notes screen: "Weekly Japanese Taste Checklist: Snacks for Friday night ✓, Matcha for Monday mornings ✓, J-Beauty for your nightly reset ✓" with product photos.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Slide 1 | Aesthetic lifestyle photo (beach towel, bathroom shelf, a hand in water) with an iPhone lock screen overlaid: time 9:41, date, 2-4 notification bubbles | Notifications in a brutal/witty brand voice: "[Brand]: you took it off again?" / "Reminder: it's waterproof. stop." |
| Slide 2 | Product worn in the same scene, or a clean stat card | Payoff line: "14K PVD. Shower, sea, sleep. Never take it off." Optional price. |

### Prompts

**Figma**

```
Use an iOS 17 lock-screen kit: SF Pro Display 96pt time, notification card 32px radius, 70% white blur, app icon 38px. Place over the photo, centred upper third.
```

**Nano Banana / Midjourney (background)**

```
flat lay of a wet beach towel, sunglasses and a gold necklace on warm sand, top-down, late afternoon light, vertical 9:16, photoreal
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
- [ ] Files named `F03-<concept>-<variant>`; tracking tag `utm_content=F03-<concept>-<variant>`.
- [ ] Avoid: More than 4 notifications becomes unreadable at scroll speed.
- [ ] Avoid: Do not fake notifications from real apps or people (no fake bank alerts or texts from named people); use the brand as the sender.
- [ ] Avoid: Slide 1 must make sense on its own; most viewers never swipe.

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
5. Name every asset `F03-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F03
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

2 slides. Slide 1: aesthetic AI/lifestyle visual with an iPhone lock screen overlay showing 2-4 push notifications written in a witty/brutal brand voice ("Right now is another chance to become who you want to be"). Slide 2: the "app comes in naturally" — product/app screenshot or a single line. ([@brainextends](https://x.com/brainextends/status/2099496707209994736), [@enzoxmotion](https://x.com/enzoxmotion/status/2099622190970712321)).

### Why it works

Feels like a meme/screenshot, instantly readable, relatable voice; 2 slides = high completion.

### Hooks

Lock-screen time + 3 notifications from the brand: affirmation, call-out, joke. "your necklace texted you", "notifications from your jewelry box".

### Production recipe

Figma/Canva lock-screen template (generic iOS-style, no Apple logos), AI background (consistent palette), copy generated in batches of 50 by Claude in LC voice, human-edited. 
Prompt: *"Write 30 sets of 3 lock-screen notifications from 'Louise Carter' (jewelry) to its owner. Voice: warm, teasing best friend. Themes: showering with jewelry on, beach days, compliments, stacking, Monday. Max 70 chars each. No false claims; jewelry is 14K PVD waterproof."*

## Reference examples

See [examples/README.md](examples/README.md) (9 posts). Top 5:

- @brainextends (265L/497BM/16kV): 2-slide slideshow, AI visuals + phone-notification copy -> 1M views, app $1k->$5k/mo. — https://x.com/brainextends/status/2099496707209994736
- @enzoxmotion (208L/378BM/13kV): Same 2-slide notification-style slideshow case ($1k->$10k MRR claim). — https://x.com/enzoxmotion/status/2099622190970712321
- @Just_sharon7 (339L/8BM/38kV): This is the slideshow system people keep skipping. Don’t start from “give me 20 viral ideas.” Start from a format that’s already winning, then let ChatGPT Astra — https://x.com/Just_sharon7/status/2098089273123848524
- @defileo (27L/34BM/6kV): I CAN'T F*CKN BELIEVE SOMEONE LEAKED FULL TIK-TOK AUTOMATION STACK 20M views across six videos, one of them did 7.5M and pulled 3.3K followers, and the whole th — https://x.com/defileo/status/2103190977678877006
- @Voxyz_ai (15L/34BM/4kV): > someone built an AI marketing team for their app with 𝟱 𝗚𝗿𝗼𝗸 𝗕𝗼𝘁𝘀. the content playbook behind it had already pulled 𝟮𝟬𝗠+ 𝘃𝗶𝗲𝘄𝘀 across six videos. now the who — https://x.com/Voxyz_ai/status/2103144930655051824
