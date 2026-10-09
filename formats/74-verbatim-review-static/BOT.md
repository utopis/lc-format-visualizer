# BOT.md · generate a "'The Verbatim': one raw customer review as the whole creative"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 1 static 1080x1350), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@CreatorSaad](https://x.com/CreatorSaad/status/2107818233302528335) · A spec static built from a single verbatim review: "Your customers already wrote it." over the quoted line "Most of the time you don't even know it's on." (a GEEKOM owner, 5-star review) with the mini PC on a desk.
- Example: [@PhilKiel](https://x.com/PhilKiel/status/1842707896443732362) · Customer review static. Who thinks a customer actually wrote this? Stellar copywriting if they did 😂
- Example: [@ariesnotebook](https://x.com/ariesnotebook/status/1857792129004675247) · Simple but effective testimonial static. Stats: 4.8M likes
- Example: [@helloitsdrew_](https://x.com/helloitsdrew_/status/2000557038682706000) · Keys to an effective review/testimonial static: - Review that highlights a specific product benefit - Review shown in an authentic way (social media U
- Example: [@FedotOff90](https://x.com/FedotOff90/status/2108212319113412929) · Complete breakdown of 420 gut health ads winning on Meta (save this). Gut health is one of the biggest money printers on Meta right now. Bloating, dig

### Live paid ads in this format (2 in [adlibrary/](adlibrary/README.md), longest-running first)

- **BioRoot Labs: "We don't trick you into taking turmeric" retention-claim static** (481 days live): A beige static: "We don't trick you into taking turmeric. Your body convinces you to keep going. After one bottle, most people don't cancel. They stock up." Bottle and capsules, "Trusted by thousands" with Trustpilot stars.
- **Amy: Verified-buyer review card over car selfie (Amy, beef liver)** (382 days live): "GREAT ENERGY BOOSTER!" headline; a 5-star "Verified Buyer" review card floats over a man's car selfie holding the bottle; an arrow links the two.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Main | One real customer review, verbatim (typos kept), set very large | e.g. "Most of the time you don't even know it's on." |
| Attribution | First name + "verified buyer" + stars | "Jess R., verified buyer ★★★★★" |
| Corner | Small product photo + logo | - |
| Primary text | - | "We didn't write this. Jess did." |

### Prompts

**Review mining (Claude)**

```
From these 200 reviews [paste], pick the 10 that read most like something a friend would text. Keep them verbatim, do not fix typos. Explain why each one sells.
```

**Figma**

```
Review 72-88px serif, oversized quote marks in brand gold, attribution 28px grey, product 220px bottom-right.
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
- [ ] Files named `F74-<concept>-<variant>`; tracking tag `utm_content=F74-<concept>-<variant>`.
- [ ] Avoid: Real reviews only, verbatim, with permission; never edit a review to make it stronger.
- [ ] Avoid: The featured example is a spec ad built from a real review; the format works best when the review is specific.

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
5. Name every asset `F74-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F74
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

One unedited customer review, typos and all, set in large type (or as a screenshot of the review), with only a small logo and product photo. The brand steps back: "this review says it better than we could."

### Why it works

- Raw voice is more believable than polished copy.
- One specific story beats a star average.
- Fastest possible production: choose a review, set the type.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static | Big serif quote from a real verified review about months of ocean wear | Primary: "This review says it better than we can." |

### Hooks

- "This review says it better than we could"
- "Read what Jess wrote after 4 months"
- "We didn't write this. Jess did."

### Production recipe

1. Export the top 50 reviews; tag them by theme (ocean, shower, gift, compliments).
2. Get consent if a name or photo is used; keep spelling as written.
3. Make 10 statics; rotate themes.

### Existing bot prompt

```
From {{REVIEWS}}, pick the 10 most specific reviews (time worn, situation, emotion). For each: verbatim quote (unaltered), visual idea, 1-line primary text.
```

### Variants to test

- Typeset vs screenshot
- Short vs long review

## Reference examples

See [examples/README.md](examples/README.md) (7 posts). Top 5:

- @FedotOff90 (17L/18BM/3kV): Rebuilt the formats list with proof: 30-day survival column = "this works" bar; copy the structure, not the words. — https://x.com/FedotOff90/status/2100948331136782532
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @FedotOff90 (20L/24BM/1kV): Complete breakdown of 420 gut health ads winning on Meta (save this). Gut health is one of the biggest money printers on Meta right now. Bloating, digestion, pr — https://x.com/FedotOff90/status/2108212319113412929
- @CreatorSaad (0L/0BM/0V):  — https://x.com/CreatorSaad/status/2107818233302528335
- @williamkast_ (252L/400BM/13kV): Formats by funnel: TOF founder/yapper/AI animation/natives/3 reasons/voiceless overlay; MOF comment reply/testimonial mashup/text wall; BOF urgency statics. — https://x.com/williamkast_/status/2103910235005935644
