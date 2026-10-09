# BOT.md · generate a "Recurring (AI or illustrated) character / mascot page"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 10-30s per bit, 1080x1920, same character every post), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@rewind02](https://x.com/rewind02/status/2107211233405325547) · A recurring AI character (a duck-headed "AI influencer" in a leather jacket) walking through a store aisle and showing a drink to camera. The same character appears in every post, so the audience follows the character.
- Example: [@ErnestoSOFTWARE](https://x.com/ErnestoSOFTWARE/status/2103534688048414959) · 11.5M views one faceless account; pitches Arcads automating carousels; 3-4 accounts.
- Example: [@MuteeAutomation](https://x.com/MuteeAutomation/status/2107022363313279044) · This channel found a crazy content loophole: Take a familiar news format → add satire → create a recurring character → keep the format consistent. The
- Example: [@YouTubeAut3538](https://x.com/YouTubeAut3538/status/2107104155831546119) · This channel found a crazy content loophole: Take a familiar news format → add satire → create a recurring character → keep the format consistent. The
- Example: [@AdebayoYTA](https://x.com/AdebayoYTA/status/2107147460443275590) · Familiar news format. Satire on top. One recurring character. Same shape every upload. 60–90 seconds. Millions of views across the catalog. The videos
- Example: [@Automation94453](https://x.com/Automation94453/status/2107048376558567547) · This channel found a crazy content loophole: Take a familiar news format → add satire → create a recurring character → keep the format consistent. The

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-2s | The character (odd, recognisable: a talking duck in a leather jacket, a grumpy gold chain) in a real-looking place | Catchphrase or a trending audio line |
| 2-15s | One bit borrowed from a trending format (POV, "tell me without telling me", store walk) | Character delivers the joke in its voice |
| 15-25s | Product appears as part of the bit, never pitched | One natural mention |
| Series rule | Same look, voice and framing every time | Pin a "who is this?" intro post |

### Prompts

**Character sheet (Midjourney)**

```
character design sheet, a small anthropomorphic gold necklace with expressive eyes and tiny arms, sassy personality, Pixar style, front/side/back views, white background --ar 16:9
```

**Kling / Seedance**

```
the same character [ref image] walking down a supermarket aisle holding a drink, handheld phone footage, realistic store, 5s, 9:16
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
- [ ] Files named `F21-<concept>-<variant>`; tracking tag `utm_content=F21-<concept>-<variant>`.
- [ ] Avoid: A new character every week builds nothing; the repeat is the asset.
- [ ] Avoid: Do not copy an existing IP character's look.
- [ ] Avoid: Post 3-5 times a week for a month before judging.

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
5. Name every asset `F21-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F21
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

One distinctive character (odd, recognisable — accent, look, catchphrase) in short repeatable bits; motion borrowed from trending formats; same character every post builds a following ([@sairahul1](https://x.com/sairahul1/status/2107172215586513360)).

## Reference examples

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @ErnestoSOFTWARE (941L/1533BM/95kV): 11.5M views one faceless account; pitches Arcads automating carousels; 3-4 accounts. — https://x.com/ErnestoSOFTWARE/status/2103534688048414959
- @sairahul1 (237L/329BM/23kV): GaryVee: make AI influencers; 'jean phil' 100M views in 1 week (recognizable odd character). — https://x.com/sairahul1/status/2107172215586513360
- @rewind02 (108L/56BM/4kV): AI influencer: treat character as a service, sell ads to brands. — https://x.com/rewind02/status/2107211233405325547
- @MuteeAutomation (43L/39BM/3kV): This channel found a crazy content loophole: Take a familiar news format → add satire → create a recurring character → keep the format consistent. The result? M — https://x.com/MuteeAutomation/status/2107022363313279044
- @BTCTanAces1 (18L/0BM/343V): Research on brand characters consistently shows measurable effects: higher recall, stronger emotional response, better long-term brand equity, and improved mark — https://x.com/BTCTanAces1/status/2082833207402057894
