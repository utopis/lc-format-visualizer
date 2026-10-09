# BOT.md · generate a "Shock & gross visual (the problem in close-up)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: Static 1080x1350, or a 10-15s video), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@FedotOff90](https://x.com/FedotOff90/status/2099967483071582480) · A woman in a robe and headband doing a close-up demo of a gross-but-satisfying product, with captions, filmed in one take in her bathroom.
- Example: [@jadorz](https://x.com/jadorz/status/2100011962352513295) · tried $2 ring gimmick and it turned my finger green
- Example: [@Nerdspringbreak](https://x.com/Nerdspringbreak/status/1919742776255635591) · Worst birthday is when my boyfriend bought me ring that turned my finger green and a man's size trench coat from Rt 18 flea market. I still miss the U
- Example: [@huntingbygones](https://x.com/huntingbygones/status/1948169528703398314) · me at the doctor showing them how my cheap ring turned my finger green
- Example: [@drebabys](https://x.com/drebabys/status/1819923093139165232) · my TikTok ring turned my finger green….

### Live paid ads in this format (2 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Male Health Tips: Elder "ancient remedy" doctor (men's health, gut-blood-flow claim)** (222 days live): A grey-bearded man in a suit vest holds a dropper bottle; captions read "Dr. Sebi exposed how to increase size QUICKLY". Script: "Most men don't realize… It all comes down to blood flow and what's happening in your gut… berberine and sodium alginate…". 41 s, 2
- **Resilia · Natural Defense Report: “This is what crawls out of you when you Carve a crawl in Time-o-o-o-one…”**: Opens: “This is what crawls out of you when you Carve a crawl in Time-o-o-o-one for two weeks straight Day one you swallow two soft gels Nothing dramatic By evening a faint gurgling Something's waking up in…”

**Do not copy (seen in these live ads):** Parasite "crawls out of you" claims are unsupported and misleading.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-2s (or main image) | Harsh macro of the problem: a green ring mark on a finger, a flaking chain on a neck. Shot with side light so the texture shows | Text: "This is what $20 'gold' does." |
| 2-5s | Same finger, now wearing the PVD ring, clean skin, natural light | "This is 6 months of showers in Louise Carter." |
| 5-9s | Quick proof: ring under the tap, then wiped dry, still bright | "14K PVD. Doesn't turn green." |
| End | Offer card | "Any 7 for $85." |

### Prompts

**Shoot**

```
Macro lens or iPhone macro mode, a single hard side light for the "before" (texture), soft window light for the "after". Same hand, same angle, same framing.
```

**Sourcing the problem shot**

```
Use a real photo from a team member or customer (with permission); never fake the discolouration with makeup or editing.
```

**Copy (Claude)**

```
Write 10 one-line captions that name the problem bluntly without insulting the viewer, max 8 words each.
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
- [ ] Files named `F83-<concept>-<variant>`; tracking tag `utm_content=F83-<concept>-<variant>`.
- [ ] Avoid: Only show real problems; faked damage breaks ad rules and trust.
- [ ] Avoid: Meta restricts "shocking" or body-focused imagery; keep it to jewellery and skin marks, never wounds.
- [ ] Avoid: Don't shame the viewer ("you're wearing junk"); shame the cheap product.

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
5. Name every asset `F83-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F83
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

The opening image is the ugliest, most specific version of the problem: a green ring mark on a finger, black flakes of plating, a discoloured line on the neck. The shock stops the scroll; the solution follows.

### Why it works

- Disgust and recognition are strong stop signals.
- A specific problem visual beats an abstract claim (7 Trends #1).
- The viewer self-identifies instantly.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | Macro: green band on a finger | "This is what cheap gold does to your skin." |
| 2-10s | Flaking chain under a loupe | — |
| 10-20s | LC piece, same finger after 3 months | "14K PVD. Bonded." |

### Hooks

- "This is what cheap gold does to your finger"
- "Zoom in on your plated necklace"

### Production recipe

1. Shoot real green-stain marks (own tests); no customer photos without consent.
2. Keep it tasteful: no medical skin conditions.
3. Static + 15s video.

### Existing bot prompt

```
Write 4 shock-visual openers for LC (what the macro shot shows, first line), each followed by a 15s solution arc. No medical claims.
```

### Variants to test

- Static vs video
- Shock level

## Reference examples

See [examples/README.md](examples/README.md) (3 posts). Top 5:

- @FedotOff90 (238L/632BM/20kV): 7,500+ winning Meta ads sorted by format across public boards (top-50 DTC, beauty, natives, listicles, shock & gross, BOFU). — https://x.com/FedotOff90/status/2093350155751924213
- @FedotOff90 (30L/31BM/3kV): Dog joint pain 4 formats, all 200+ days: "SCAM ALERT… turns out it works?" static, brace carousel, sticky-note UGC, quote carousel — format | lander | offer | d — https://x.com/FedotOff90/status/2097694037050642468
- @FedotOff90 (3L/7BM/2kV): Gross ads get banned in every "clean creative" guide. They keep making money anyway. A gross picture (the parasite, the plaque, the gunk in your pillow) stops t — https://x.com/FedotOff90/status/2099967483071582480
