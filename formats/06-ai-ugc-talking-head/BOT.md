# BOT.md · generate a "AI UGC talking-head (avatar) — and its realism stack"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 15-45s, 1080x1920, 30fps), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@frankyecom](https://x.com/frankyecom/status/2105377535345258584) · A run of AI-made and real beauty talking heads: a TV-shopping set ("LIVE MASCARA DEMO"), tight face close-ups that read like UGC, a before/after face and a mannequin head. The speaker talks straight to camera with captions.
- Example: [@kristian_jennin](https://x.com/kristian_jennin/status/2101352217089282066) · AI UGC looks fake because of a missing step (realism workflow video).
- Example: [@zedmadeit](https://x.com/zedmadeit/status/2107552798842003488) · Intentional AI ad system starting from brand/product/customer, visuals matched to script.
- Example: [@eliasrrecom](https://x.com/eliasrrecom/status/2092612451623694388) · Realistic AI UGC ads tutorial.
- Example: [@ladprofit](https://x.com/ladprofit/status/2100960479577362499) · Seedance AI UGC page for Veterans Day: same B-roll, new hook each post, trending audio, comment-keyword link (comment-gated teardown).
- Example: [@adamtaylorl](https://x.com/adamtaylorl/status/2089713928511345017) · Hike Footwear ad 100% AI.
- Example: [@CEO_Vlad](https://x.com/CEO_Vlad/status/2108405736245952955) · Audio is what makes AI UGC feel real; one robotic sentence kills it.
- Example: [@Mho_23](https://x.com/Mho_23/status/2085374858267857069) · Realistic AI UGC with Seedance 2.0 full breakdown (mho_23).
- Example: [@oliverxmedia](https://x.com/oliverxmedia/status/2104954498565464350) · Realistic AI = reference images + precise prompts + consistent characters + guided motion.

### Live paid ads in this format (2 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Khazanay Pakistan: Clinic presenter in scrubs (orthopedic shoes)** (338 days live): A woman in navy scrubs in a clinic corridor: "Let me tell you that you don't need a new body. You just need better support… it's not always an injury… unsupported shoes… plantar fasciitis". 70 s, run as 2 near-identical ads.
- **Blossom Essentials Skin: Short AI-UGC "only balm I'll ever buy" (Blossom Essentials, 3 variants)** (213 days live): Three 24-33 s UGC cuts: "This is the only skin balm I will ever spend money on… I've tried everything, from prescription to specialist." Different women, same script skeleton.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-2s | Avatar holding the product up close to a phone camera in a real-looking room (bathroom mirror, car, kitchen) | Hook from a real review: "okay I need to talk about this necklace because I literally sleep in it" |
| 2-10s | Medium selfie, natural hand movement, slight handheld wobble | Problem in her words: "every gold necklace I owned turned green or snapped" |
| 10-25s | Cutaways: REAL product B-roll (shower, sea, close-up of clasp) | Proof beats: "I showered, I swam, it looks the same" |
| 25-35s | Back to avatar, smiling, touching the piece | Offer + CTA: "they do any 7 for $85, link's below" |

### Prompts

**Arcads / HeyGen / Creatify (avatar)**

```
Choose a 25-40 female avatar filmed in a bathroom or car, natural lighting, casual clothes. Script: [paste]. Settings: "casual" tone, add 2-3 natural pauses, slight pitch variation, 9:16.
```

**Realism stack**

```
Add background room tone, a 3-5% handheld shake, auto-captions in TikTok style, cut every 2-4s, cover the mouth area with B-roll at least 40% of the time.
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
- [ ] Files named `F06-<concept>-<variant>`; tracking tag `utm_content=F06-<concept>-<variant>`.
- [ ] Avoid: Avatars reading a script word-perfect look fake; add fillers ("like", "honestly") and a stumble.
- [ ] Avoid: Avatars may not claim a personal experience they did not have in places where that is regulated; label AI and keep claims to product facts.
- [ ] Avoid: Never show the avatar "wearing" AI jewelry; cut to real product footage.
- [ ] Avoid: Ranked by researchers: avatar reading a script = F tier; avatar inside a story or skit performs better.

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
5. Name every asset `F06-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F06
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

A phone-selfie video of a "creator" talking to camera — bedroom, bathroom, car, kitchen — holding/wearing the product, 15-45s, casual captions. Sub-formats ranked by @CEO_Vlad: **S** podcast ad, talking head ("cleanest test of whether your angle works"), in-car ("reads private, cheapest to render well"); **A** street interview, multi-scene demo; **B** reply-to-comment overlay, split-screen day.
Example (jewelry): GIVA collection "I'm obsessed with these tiny little things and I've been stacking them like this…" (Arcads promo, [@SparkifyAI](https://x.com/SparkifyAI/status/2101869170937958407)).

Script skeleton (30s): 0-3s hook line + gesture ("I don't usually film unboxings but…") · 3-15s problem/story · 15-25s product proof (close-up, real product footage cut-in) · 25-30s CTA.

### Production recipe

Angles from real reviews (Claude: cluster LC reviews into motivators: shower-proof, gifting, compliments, sensitive skin feel, value of stack) → script per motivator → avatar (Arcads/HeyGen/Higgsfield; or Seedance/Veo with reference image) → voice (ElevenLabs, matched) → **real LC product B-roll cut-ins** (never render the jewelry with AI in close-up) → CapCut captions.

## Reference examples

See [examples/README.md](examples/README.md) (37 posts). Top 5:

- @jakecastilloooo (984L/3090BM/290kV): Ex-Cal AI UGC lead's full AI UGC workflow (article): customer context → outlier videos vs creator baseline → reverse-engineer → believable first frame → test ta — https://x.com/jakecastilloooo/status/2107873317369581751
- @kristian_jennin (1124L/3024BM/231kV): AI UGC looks fake because of a missing step (realism workflow video). — https://x.com/kristian_jennin/status/2101352217089282066
- @eliasrrecom (266L/548BM/54kV): Realistic AI UGC ads tutorial. — https://x.com/eliasrrecom/status/2092612451623694388
- @zedmadeit (348L/473BM/20kV): Intentional AI ad system starting from brand/product/customer, visuals matched to script. — https://x.com/zedmadeit/status/2107552798842003488
- @adamtaylorl (266L/426BM/22kV): Hike Footwear ad 100% AI. — https://x.com/adamtaylorl/status/2089713928511345017
