# BOT.md · generate a "Founder walk-and-talk / founder-story ad (incl. host interview)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 45s-4min, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@luisfelipebfr2](https://x.com/luisfelipebfr2/status/2101018997508669891) · A founder mini-documentary of almost 4 minutes for Eskiin (shower filters): the founder walking the factory floor ("showerhead company"), a junk-filled showerhead, the filter cartridge, packing orders ("every order"), staff ("Take care of family") and a customer washing her hair ("for a full refund").
- Example: [@ecomrudolfs](https://x.com/ecomrudolfs/status/2059559665520795790) · Out of 997 active ads, this founder led ad is CRUSHING it Break it down and use the same winning format
- Example: [@LachezarVoynov](https://x.com/LachezarVoynov/status/2057488725769163085) · This ad combines 2 of the top-performing ad creative elements in 2026: > AI-generated clips > Founder-led content Here’s why you should re-create it f
- Example: [@JoeJMarston](https://x.com/JoeJMarston/status/2007102582058340515) · Here’s how we’ve been reskinning our existing, top-performing founder ads. Founder ads still work. But when performance softens, it’s rarely because t
- Example: [@LoukasHambi](https://x.com/LoukasHambi/status/1978090871296782364) · We know Founders ads crush, but if yours are starting to fatigue, here’s a few quick-win format adaptations you can make: (These are flying for us rig
- Example: [@metaadsatscale](https://x.com/metaadsatscale/status/2093049398024384915) · New brands face a trust gap. A founder story ad flips that. Face, voice, real skin in the game. People buy from people they relate to, not logos.
- Example: [@strikerecom](https://x.com/strikerecom/status/2106092593511837880) · the amount of directions u can take a native is STUPIDDD if a video concept already works just turn that shit into a native founder ads have been crus
- Example: [@ecom_cork](https://x.com/ecom_cork/status/2098433621077983648) · Few million more founder ads https://t.co/IKeYhoxbMc

### Live paid ads in this format (2 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Rachel's Tea: Co-founder spouse explains the new product line** (481 days live): Plain kitchen talking head: "Hi, this is Mike. Rachel has asked me to explain why she has a new product line." No hook graphics, no music; he explains that the brand now has its own manufactured line and why the labels changed. Cut-ins of the product row on th
- **BioRoot Labs: "A message from our founder" scarcity text static** (378 days live): A white text static: "A MESSAGE FROM OUR FOUNDER 💔 We never expected this. Thousands of people are turning to BioRoot Labs' Doctor-Formulated Turmeric daily, and our limited Buy Two, Get One Free offer is about to expire… our stock is dangerously low… Sale end

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-5s | Founder walking toward camera (street, studio, warehouse), gimbal or handheld | Open loop: "I started this because my mom's chain turned her neck green" |
| 5-60s | Walking cutaways: workshop, packing orders, the product being tested | Why it exists, the problem, what she refused to compromise on |
| 60-120s | Customers / reviews on screen | Proof |
| End | Founder stops, looks at camera | Guarantee + offer |

### Prompts

**Shoot**

```
Gimbal (DJI Osmo Mobile), 4K 30fps, wireless lav (Rode Wireless GO), walk slowly toward the camera, record 3 full takes, cut to the best lines.
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
- [ ] Files named `F27-<concept>-<variant>`; tracking tag `utm_content=F27-<concept>-<variant>`.
- [ ] Avoid: ONE topic per video; founders try to say everything.
- [ ] Avoid: Hook in the first sentence, not after the intro.
- [ ] Avoid: All claims (warranty, materials) must match the product page.

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
5. Name every asset `F27-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F27
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

The founder walks (street, studio, warehouse) and talks to camera — or is interviewed by a handheld-mic host — about ONE thing: why the product exists, the problem she hated, or the mechanism. Unscripted, raw, one idea per ad. Long version = founder-story mini-VSL (personal open loop → problem → failed solutions → mechanism → product → mission → payoff).

### Why it works

- The founder conveys the most conviction and is "impossible to copy" (@williamkast_).
- Looks like an organic interview, so it humanises before it sells (@joshsuggss).
- Founder story sells two things: the product and the people you trust to make it — every feature becomes a character trait (Eskiin breakdown).
- Unscripted, single-claim founder ads beat polished scripted ones, which have become wallpaper (@KanishDigital quoting @ujjawalasthana).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-3s | Walking shot, Qirra mid-sentence (start in motion) + text hook | "I started Louise Carter because I was sick of taking my jewelry off." |
| 3-15s | Keep walking; problem in her words (green necks, tarnish, losing earrings at the gym) | Ambient street sound, lav mic |
| 15-30s | Cut to hands: dunk the Chelsea Herringbone in a glass of water / show 6-month-old piece | "This is 14K PVD — here is why it doesn't do that." |
| 30-45s | Back to walk: one belief/mission line ("jewelry you never take off") | Natural pace, jump cuts allowed |
| 45-55s | CTA beat: "any 7 for $85" card over her walking away | Soft music under |

### Hooks

- "I'm the founder, and I need to tell you why I made jewelry you can shower in."
- "Every jewelry brand told me 'just take it off before you shower.' So I made my own."
- Host: "What's the one thing people get wrong about gold jewelry?" Qirra: "That it has to be fragile."
- "This necklace is 6 months old. I have never taken it off."
- "I'm not supposed to tell you this as a jewelry founder, but…"
- (Story VSL) "This picture was on my vision board for ten years."

### Production recipe

1. Write 15 one-line "beliefs" Qirra actually holds (from interviews, reviews, DMs); each = one ad.
2. Shoot 2-hour block: 10 walk-and-talk takes + 5 host-interview questions (host off-camera, handheld mic on Qirra).
3. Lav mic (Rode Wireless), phone 4K 30fps, 0.5x lens for one variant (see F45).
4. Edit 20-45s cuts; captions; never add music over first 3s.
5. Long version (60-120s) uses the Eskiin sequence: open loop → problem → failed fixes → mechanism (PVD) → product → mission → payoff + guarantee.
6. Run as Partnership ad from Qirra's personal IG if she has one.

### Existing bot prompt

```
You are writing founder walk-and-talk ad beats for Louise Carter (waterproof 14K PVD jewelry, founder Qirra). Input: {{QIRRA_INTERVIEW_TRANSCRIPT}} + {{TOP_20_REVIEWS}}. Output 12 single-idea ads. For each: belief line (≤12 words, in her phrasing), problem in customer words (quote the review), one proof beat she can do with her hands on camera, a 9-word on-screen hook, and length (20/35/50s). Then outline ONE 90s founder-story mini-VSL using: open loop → problem → failed solutions → mechanism → product → mission → payoff → guarantee. No claims beyond the PDP.
```

### Variants to test

- Walk vs seated vs car (F14)
- Host-interview vs solo
- One claim (waterproof) vs origin story
- 20s vs 90s

## Reference examples

See [examples/README.md](examples/README.md) (27 posts). Top 5:

- @williamkast_ (227L/549BM/17kV): 5 formats that win in every account, each with a live Atria ad link: founder, yapper, AI educator, B-roll text overlay, long VSL. — https://x.com/williamkast_/status/2084298521251860579
- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @williamkast_ (28L/34BM/3kV): 5 formats to test: founder talking head, voiceless B-roll text overlay, yapper (uncut), AI educational, camouflage static + long copy. — https://x.com/williamkast_/status/2078179704050246125
- @joshsuggss (38L/11BM/7kV): 105 founder interviews in 16 weeks; "founder ads" = walk-and-talk about your brand (agency pitch). — https://x.com/joshsuggss/status/2091887902137454922
- @alexpagepilot (11L/19BM/1kV): Top 5 dropship formats: UGC problem/solution, "TikTok made me buy it", us vs them split, founder talking head (retargets 2-3x), text-overlay slideshow. — https://x.com/alexpagepilot/status/2099438014456045990
