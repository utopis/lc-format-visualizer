# BOT.md · generate a "AI character motion-swap reel (one striking AI character swapped into a dance, stage or crowd clip; hashtag-only or one-line ego caption)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 10-15s, 1080x1920, one AI character, one motion clip, hashtag-only caption), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@kelmruns](https://x.com/kelmruns/status/2107508612058747114) · A 9-second vertical reel of an AI-generated gym bro with a giant blonde two-foot quiff, swapped with Seedance 2.5 into crowded real-world clips (a cowboy bar, a bowling alley, riding a lawn mower) with a hype soundtrack. The caption is one ego line: "ladies you all look lovely tonight, but i look better". The poster claims the 2-day-old account reached 26K followers and 2.2M likes in 48 hours and 
- Example: [@k4zxbt](https://x.com/k4zxbt/status/2108240597421084694) · your local pub is an AI influencer now a small-town US bar made $16,720 off one AI trickshot clip > ask ChatGPT for the most impossible pool shot it c
- Example: [@k4zxbt](https://x.com/k4zxbt/status/2106342154452779278) · this giant Tokyo girl made with ChatGPT got 23.6M views and $11,200 on one clip > generate tall girl character with ChatGPT > pick spots built for sho
- Example: [@k4zxbt](https://x.com/k4zxbt/status/2108659775206756837) · real or AI, nobody can tell anymore these twins got 2.5M likes and $14,339 remaking the creepiest meme online > generate two identical girls in long b
- Example: [@kelmruns](https://x.com/kelmruns/status/2108656084890349694) · the internet is so cooked this AI wednedsay made with GPT Astra 6 got 67.4M views and $27,433 on one clip > generate a pale girl with two black braids
- Example: [@kelmruns](https://x.com/kelmruns/status/2108258506801299744) · influencers are dead this AI freak DJ made with GPT Astra 6 got 9.9M views and $19,433 on one clip > generate a guy in a grey suit with a mushroom bow
- Example: [@k4zxbt](https://x.com/k4zxbt/status/2106690716109885936) · dead internet theory is real AI conjoined twins made with ChatGPT got 125k likes and $7,800 on one clip > generate one body with two faces in ChatGPT 
- Example: [@kelmruns](https://x.com/kelmruns/status/2107886356496097561) · is this a f*cking joke? this AI short king made with ChatGPT got 3.9M views and $17,339 on 1 week from tiktok > generate a short chubby guy with a bow

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-1s | Goldie (an original disclosed LC AI muse: sleek platinum bob, oversized gold hoops, the same 7-piece LC stack) mid-move in a plain white room | Licensed trending sound |
| 1-10s | She performs a trend dance recorded by our own consenting LC creator, swapped in with Seedance 2.5; the stack catches the light on every arm move | - |
| 10-12s | Ends on a wrist-to-camera beat; small corner label "AI character" | Caption: "#goldie #7for85 #waterproofjewelry" |

### Prompts

**Character (GPT Image / Nano Banana)**

```
"Original fashion character, not resembling any real person or franchise: sleek platinum bob, oversized gold hoop earrings, a stack of 7 dainty gold pieces (2 chains, 2 bracelets, 3 rings), black ribbed tank, full body, neutral white room, photoreal, 9:16, consistent face sheet front/3-4/profile."
```

**Motion swap (Seedance 2.5 / Kling motion control)**

```
Reference video = our own creator dancing in a white room (signed release covering AI motion transfer). Replace the performer with the character image; keep camera and timing; preserve jewelry count and gold tone.
```

**Caption (in character)**

```
Hashtags only, or one deadpan line: "quick swim set", "she never takes it off 💧". Turn on the AI-generated label.
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
- [ ] Files named `F112-<concept>-<variant>`; tracking tag `utm_content=F112-<concept>-<variant>`.
- [ ] Avoid: Lookalikes of franchise characters or real people = IP and likeness risk (the Wednesday example).
- [ ] Avoid: Never swap into someone else's viral video: their motion, face and audio are not licensed.
- [ ] Avoid: Jewelry distorts in video models: count pieces and check links every frame; composite the real product if needed.
- [ ] Avoid: Undisclosed AI persona selling subscriptions or brand deals breaks platform rules: label it and say it in the bio.
- [ ] Avoid: Earnings screenshots in the source posts are unverified; judge on follows per 10K views and link clicks.

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
5. Name every asset `F112-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F112
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

A 10-15 second vertical reel of **one instantly recognisable AI character** (an exaggerated silhouette: two black braids and blunt bangs, a two-foot blonde quiff, a mushroom bowl cut in a grey suit, a short guy with a huge moustache) **dropped into motion that already went viral**: a known dance in a plain white room, a DJ booth at a sold-out show, a cowboy bar, a parking-lot dance between two tall creators. The motion comes from a reference clip and the character is swapped in with a video model (Seedance 2.5 in every example). The caption is either **hashtags only** or **one ego line** ("quick DJ set", "ladies you all look lovely tonight, but i look better", "praise your short king", "same soul, upgraded version"). The account posts the same character every day, so it becomes a recurring character page (F21) built at AI speed.

The pipeline @kelmruns lists, five times over:
1. Generate the character in ChatGPT image ("GPT Astra 6" in his posts): one exaggerated, readable feature.
2. Pick the stage: a dance everyone knows, the biggest stage you can find, or a crowd that reacts.
3. Swap the character into the clip with Seedance 2.5 (motion and camera stay, the person changes).
4. Caption it as the character: hashtags only, or one deadpan line.

### Why it works

- **Proven motion, new face.** The dance or stage already earned retention, and the novelty of the character resets pattern recognition (Voynov's "odd visuals" hook, Adam Taylor's subconscious filter: movement + face + broken pattern).
- **A silhouette you can read on mute in 0.5 s.** Every winner has one absurd feature (braids, quiff, bowl cut, height gap).
- **Same character daily = a parasocial page.** People follow a character, not a video, which lets the pages sell "talk with me" subscriptions, courses or brand deals.
- **Cost per post is near zero**, so pages can test 5-10 characters a week.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time | Visual | Audio / copy |
|---|---|---|
| 0-1 s | Goldie (original character: sleek platinum bob, oversized gold hoops, a stack of 7 LC pieces) in a plain white room, mid-move | Trending sound (licensed in-app) |
| 1-10 s | She performs a trend dance recorded **by our own LC creator** (consented, paid) and swapped with Seedance; the stack catches the light on every arm move | — |
| 10-12 s | She ends on a wrist shot to camera; small corner label "AI character" | Caption: "#goldie #7for85 #waterproofjewelry" or "she never takes it off 💧" |

### Hooks

- A trend dance everyone already knows (motion reference you own or licensed)
- "Quick [shower / swim / gym] set" with the character wearing the stack through it
- "same soul, upgraded version" glow-up with the character's own fictional backstory (disclosed)
- The character between two of **your own** creators (height or style contrast)

### Production recipe

1. **Character bible:** one original character (never a lookalike of a real person or a franchise character) with one absurd, readable feature, plus how she wears LC (always the same 7-piece stack).
2. **Motion library:** film your own creators doing 10 trend dances and moves in a white room (paid, signed release that covers AI motion transfer). Don't take motion from other people's videos.
3. **Swap:** character image + your motion clip → Seedance 2.5 (or Kling motion control); check that the jewelry renders accurately (count the pieces, gold tone, no melting links).
4. **Caption:** hashtags only or one deadpan line in the character's voice; turn on the platform's AI-generated label.
5. **Post daily** from one brand-owned, disclosed account; reply in character.

### Existing bot prompt

```
Design an ORIGINAL AI character for <BRAND> (not resembling any real person, celebrity or franchise character). Give: name, one exaggerated readable feature, outfit, and exactly how the product appears in every shot. Then plan 10 reels: for each, the motion reference (from our own consented creator library), setting (plain white room / big stage / crowd), a 10-15 s beat sheet, the caption (hashtags only or one deadpan line in character), and an AI-disclosure label. Flag any shot where the product could render inaccurately.
```

### Variants to test

- Hashtag-only versus one-line ego caption
- White room versus big stage versus crowd reaction
- Character alone versus character between two real LC creators
- Organic page only versus Spark-boosting the top reel to a TOF audience

## Reference examples

See [examples/README.md](examples/README.md) (5 posts). Top 5:

- @kelmruns (0L/0BM/0V):  — https://x.com/kelmruns/status/2108258506801299744
- @kelmruns (0L/0BM/0V):  — https://x.com/kelmruns/status/2107886356496097561
- @kelmruns (0L/0BM/0V):  — https://x.com/kelmruns/status/2107508612058747114
- @kelmruns (0L/0BM/0V):  — https://x.com/kelmruns/status/2107165250868937035
- @kelmruns (0L/0BM/0V):  — https://x.com/kelmruns/status/2108656084890349694
