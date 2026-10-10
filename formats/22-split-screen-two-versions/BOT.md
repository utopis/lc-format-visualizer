# BOT.md · generate a "Split-screen "two versions of the same person" day"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 15-30s, 1080x1920, left/right split), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@Charconsults](https://x.com/Charconsults/status/2081629763882430905) · Fast UGC cuts for an herb-keeper product: wilted herbs ("HERBS SAY GOODBYE"), the creator smiling with the product, adding water, fresh mint and rosemary in the tubes ("THAT FITS PERFECTLY"), a finished salad and "STOP WASTING HERBS". The before and after sit next to each other.
- Example: [@adamtaylorl](https://x.com/adamtaylorl/status/2102759898391920860) · 5. Choose your own adventure Handing the viewer the decision turns a 2-minute ad into a game they want to finish. Give them two paths, and let the bad
- Example: [@creativesbycare](https://x.com/creativesbycare/status/2099292610175361351) · If you're a smart brand... Here is one of the formats you'll start testing now, to avoid scrambling in Q4! (part 1/4) ⭐️ READING REVIEWS ⭐️ Social pro
- Example: [@DailyYTNiches](https://x.com/DailyYTNiches/status/2096979805346673029) · This channel hasn't even had a single flop video 👀 ~ 1.86k subscribers ~ 547,079 total views ~ $875 in the 30 days alone (assuming a $2.59 RPM) Format
- Example: [@YouTubeAut3538](https://x.com/YouTubeAut3538/status/2097064734474256890) · This channel hasn't even had a single flop video. ~ 1.86k subs ~ 547,079 total views ~ $875 in the 30 days alone (assume $2.59 RPM) Format &gt; Split 
- Example: [@ytaeliteacademy](https://x.com/ytaeliteacademy/status/2096998590971269290) · This channel hasn't even had a single flop video 👀 ~ 1.86k subscribers ~ 547,079 total views ~ $875 in the 30 days alone (assuming a $2.59 RPM) Format

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-2s | Split screen, same person twice, timestamps top ("7:00 AM") | Hook: "same girl, two jewelry boxes" |
| 2-20s | Synced timelines: left takes jewelry off to shower/swim, loses an earring; right keeps it on | Time captions advance together (7:00 / 12:30 / 18:00) |
| 20-30s | End: left frustrated, right getting compliments | Product + offer on the right side |

### Prompts

**Shoot**

```
Tripod, locked camera, shoot both versions with the same framing and light, edit side by side in CapCut (Layout > Split), 2px white divider.
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
- [ ] Files named `F22-<concept>-<variant>`; tracking tag `utm_content=F22-<concept>-<variant>`.
- [ ] Avoid: Unsynced timing between halves confuses viewers; keep the beats aligned.
- [ ] Avoid: Do not exaggerate the "without" side into a false claim about other products.

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
5. Name every asset `F22-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F22
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

Left: version A of a person's day; right: version B (with product), synced timelines, captions with times.

## Reference examples

See [examples/README.md](examples/README.md) (10 posts). Top 5:

- @CEO_Vlad (88L/169BM/5kV): AI UGC formats tiered: S = podcast, talking head, in-car... — https://x.com/CEO_Vlad/status/2096569603761827953
- @thankyouecom (78L/133BM/6kV): Almost every winner in our scaling CBO this month is AI debate Here’s our method for generating these bangers 1. Not an interview Debate formats are arguments a — https://x.com/thankyouecom/status/2093386984349700402
- @Charconsults (3L/0BM/172V): Day 7/14 This one is an oldie, brief show the product in use and the pay off for using. This ad was very visual use before after/split screen pacing and brolls. — https://x.com/Charconsults/status/2081629763882430905
- @adamtaylorl (0L/0BM/0V):  — https://x.com/adamtaylorl/status/2102759898391920860
- @DailyYTNiches (158L/96BM/7kV): This channel hasn't even had a single flop video 👀 ~ 1.86k subscribers ~ 547,079 total views ~ $875 in the 30 days alone (assuming a $2.59 RPM) Format > Split s — https://x.com/DailyYTNiches/status/2096979805346673029
