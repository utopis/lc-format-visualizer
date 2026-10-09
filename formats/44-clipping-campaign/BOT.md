# BOT.md · generate a "Clipping campaign (pay-per-view clippers distribute founder/podcast content)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: System: a pool of clippers posting short clips from founder or podcast content, paid per 1,000 views), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@leonclipping](https://x.com/leonclipping/status/2107903429490135362) · A 4-second shocked-reaction hook (a woman covering her face and reading the fact on screen), then the app screen (a purple mascot with a body fact). It is one tiny format repeated across many clipping accounts.
- Example: [@alexzgirbu](https://x.com/alexzgirbu/status/2092441815739670637) · Clipper earns ~$3k per 1M views cutting streams/vlogs into short clips submitted to Content Rewards/Clipping Net/Clipster campaigns.
- Example: [@natiakourdadze](https://x.com/natiakourdadze/status/2107495566225834123) · The easiest way to get banned on Clip Brand? A bot score of 99. Don't submit videos with fake views. Content Rewards detects bots, and we can see it r
- Example: [@LinoLeighton](https://x.com/LinoLeighton/status/2077533819905744955) · Currently at 60 clippers now for side app. I’ve only spent $430 on this faceless clipping campaign so far and it’s currently on around 10X return. Ove
- Example: [@alexxgrowth](https://x.com/alexxgrowth/status/2085667455062389146) · doordash did $13.7 BILLION in revenue last year they have one of the best marketing teams on the planet and they just launched something called Cringe
- Example: [@savixbt](https://x.com/savixbt/status/2082914407567462902) · clippers in the house, @blknoiz06 just drop a clipping campaign for clippers there’s $10,000 in $ANSEM reward every month for clippers. requirements: 
- Example: [@Dkevs_](https://x.com/Dkevs_/status/2103032078514246093) · if you’re a founder and you haven’t launched your own clipping campaign yet just start. it’s one of the cheapest ways to distribute your content at sc
- Example: [@natiakourdadze](https://x.com/natiakourdadze/status/2101662430048735412) · Did I share my newest marketing obsession? Content Rewards by Whop 🥳 I just launched a campaign for Overglow AI, and clippers are already applying, po
- Example: [@LinoLeighton](https://x.com/LinoLeighton/status/2077532362842181898) · Currently at 60 clippers now for side app. I’ve only spent $430 on this faceless clipping campaign so far and it’s already generated $4K in Rev. Over 

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Source | A long founder video or podcast episode (20-60 min) | - |
| Brief | A shared folder with the source, the brand rules and 10 example clips | "Cut 15-45s moments; captions on; tag @louisecarter" |
| Clips | Clippers post on their own TikTok/IG/YT accounts | Hooks pulled from the best lines |
| Payout | Views tracked via platform (e.g. Whop/Clipping) and paid per 1,000 | - |
| Recycle | Best clips become paid ads (with rights) | - |

### Prompts

**Brief (Claude)**

```
Write a clipper brief: what to cut, what never to say, caption style, required disclosure (#ad / paid partnership), payout rate and rules.
```

**Platform**

```
Set up a campaign with a CPM cap, a view floor per clip, and manual approval of the first 20 clips.
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
- [ ] Files named `F44-<concept>-<variant>`; tracking tag `utm_content=F44-<concept>-<variant>`.
- [ ] Avoid: Clippers must disclose the paid relationship.
- [ ] Avoid: Approve early clips; one bad clip can misquote the founder.
- [ ] Avoid: Cap spend per clip to avoid paying for botted views.

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
5. Name every asset `F44-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F44
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

Post a campaign on a clipping marketplace (Content Rewards, Whop clipping, Sideshift-type) paying a fixed rate per 1k views; dozens of clippers cut your long-form (founder podcast, lives, interviews) or a template format into shorts on their own accounts.

### Why it works

- Pay only for views; massive account diversity.
- One proven format × 100 clippers = outlier scale (Musa 522M views).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Source | Qirra 30-60 min podcast/live with stories | — |
| Campaign | Rules: min length, must show product/name, disclosure, $ per 1k views, cap | — |
| Clips | Clippers post on own pages | — |
| Pay | Verified views only | — |

### Hooks

- Clip prompt: "the moment Qirra explains why she started LC"
- "Customer story that made Qirra cry"

### Production recipe

1. Need source content first (F27 founder content, podcast).
2. Pick reputable marketplace with view verification; set CPM cap and budget cap.
3. Require #ad disclosure and approved claims list.

### Existing bot prompt

```
From this transcript {{TRANSCRIPT}} of Qirra's long-form content, list 15 clip-worthy 20-45s moments with hook line, timestamp, and on-screen caption.
```

### Variants to test

- $/1k views
- Source type

## Reference examples

See [examples/README.md](examples/README.md) (14 posts). Top 5:

- @SeoulJosephK (720L/2243BM/98kV): App marketing reading list: paid (athcanft), organic UGC (Superwall pod), Sideshift/Posted/Noise view-based campaigns, Jake Castillo for influencers. — https://x.com/SeoulJosephK/status/2072291737536803119
- @alexzgirbu (39L/36BM/2kV): Clipper earns ~$3k per 1M views cutting streams/vlogs into short clips submitted to Content Rewards/Clipping Net/Clipster campaigns. — https://x.com/alexzgirbu/status/2092441815739670637
- @Dkevs_ (13L/9BM/1kV): App clipping campaign hit 140K+ views while still testing formats; trained teen clippers (agency pitch). — https://x.com/Dkevs_/status/2104045499208831116
- @leonclipping (44L/66BM/3kV): Musa app: ONE format (4-sec shocked reaction to a body fact → mascot explains) = 522M views, 930 videos >100K, 100+ creators. — https://x.com/leonclipping/status/2107903429490135362
- @LinoLeighton (82L/170BM/11kV): I ran a clipping campaign at 10X ROAS previously. Here’s exactly how I did it: • Paid anywhere from $0.20–$0.60 CPM depending on the country • Sourced clippers  — https://x.com/LinoLeighton/status/2096622664223707174
