# BOT.md · generate a "The Cross-Out static (strike through the failed fixes and leave the one that works)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

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
5. Name every asset `F67-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F67
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

A plain static listing the fixes the viewer has already tried, each one struck through, with the product as the last line, not crossed out. The primary text repeats the list ("Olive oil. Apple cider vinegar. Honey masks…") before naming the mechanism.

### Why it works

- The viewer recognises their own failed attempts, which reads as "this brand gets it".
- The strikethrough is a visual pattern-break and makes the argument without copy.
- Works as a pure static, so it is cheap to test 10 versions.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static | Kraft/white background: "~~clear nail polish~~ / ~~taking it off to shower~~ / ~~gold-tone~~ / 14K PVD ✓" next to a necklace on wet skin | Headline: "Done taking it off every night?" |
| Primary text | List of failed fixes → why plating fails → bonded PVD | "Any 7 for $85" |

### Hooks

- "Done trying everything else?"
- "~~Take it off before the shower~~"
- "Things I tried before I found waterproof gold"

### Production recipe

1. Collect 5 failed fixes from LC reviews and support tickets.
2. Make 4 designs: handwritten marker, typed list, Notes-app screenshot (F32), sticky note.
3. Primary text 120-250 words: failed fixes → mechanism → offer.

### Existing bot prompt

```
From {{REVIEWS}}, list the fixes customers tried before LC (polish, removing jewelry, cheap plated pieces). Write 5 cross-out statics (≤5 struck lines + 1 winner line) and a 150-word primary text for each.
```

### Variants to test

- Problem list vs gift list vs price list
- Handwritten vs typed

## Reference examples

See [examples/README.md](examples/README.md) (5 posts). Top 5:

- @FedotOff90 (17L/18BM/3kV): Rebuilt the formats list with proof: 30-day survival column = "this works" bar; copy the structure, not the words. — https://x.com/FedotOff90/status/2100948331136782532
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @aashishilla170 (1L/0BM/35V): Breaking down an ad a day. Day 1 3 things that work, 3 that don't, how I'd fix it. What's working: &gt;Strikethrough sells freedom, not price, which is the real — https://x.com/aashishilla170/status/2105999366104444944
- @antonioventre_ (7L/6BM/790V): Three static concepts from one angle (energy), none of them showing the product: 1. The calendar. A week view with "gym", "dinner with friends", "hike" all cros — https://x.com/antonioventre_/status/2085397746660278559
- @principles0618 (4L/1BM/2kV): GTM, ADS, Web traffic tracking - It all starts to merge and you better build your stack in one big monorepo to give your clankers full access to the context. To — https://x.com/principles0618/status/2105476261619339387
