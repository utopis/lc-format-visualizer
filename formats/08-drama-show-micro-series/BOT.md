# BOT.md · generate a "Drama "show" micro-series (product as a prop, entertainment first)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 45-120s episode, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@JUSTCHAEL_](https://x.com/JUSTCHAEL_/status/2098373776828256595) · A short AI-made soap-opera scene for a handbag brand (Outlash): three women in a boutique, a tense confrontation, close-ups of the brown purse, then a cut to a living-room fallout. Shot and paced like an episode of a drama series, with the bag as a plot device.
- Example: [@frankyecom](https://x.com/frankyecom/status/2106833649970684195) · Women want shows: characters, drama, payoff; build entertainment first, slot product in.
- Example: [@frankyecom](https://x.com/frankyecom/status/2108308896813326775) · Best drama ads let viewer see the version of herself she wants to become.
- Example: [@adamtaylorl](https://x.com/adamtaylorl/status/2099815494434099379) · Resilia mastered storytelling ads -> $100M/yr.
- Example: [@frankyecom](https://x.com/frankyecom/status/2105732607208026318) · Cinematic realistic AI ads in scrutinized categories (GLP).
- Example: [@SGradon](https://x.com/SGradon/status/2101705439565979947) · In 2026 creative strategists should steal from screenwriters AI drama ads are becoming a trend, and everyone's about to copy the same 5 stories. Here'
- Example: [@zedmadeit](https://x.com/zedmadeit/status/2102176819709673703) · heres how to make ai drama ads for your brand ai dramas are the new trend and theyre great for engagement but you want the right kind the kind that ac
- Example: [@david_attisaas](https://x.com/david_attisaas/status/2108195582607081720) · I'm running short drama ads for a few apps right now, and every one of them started as a copy of something a dropshipper ran first. I went looking aft
- Example: [@ViralOps_](https://x.com/ViralOps_/status/2108255353016406383) · Koriderm is absolutely CRUSHING with these DRAMA ads rn. they're literally making mini movies just to sell skincare products 😭 and i think this could 

### Live paid ads in this format (1 in [adlibrary/](adlibrary/README.md), longest-running first)

- **PopDrama 02: Long-form short-drama episode ad (PopDrama, 19:41)** (406 days live): A full episode of a ReelShort-style drama (a boardroom, a betrayed heroine, a CEO), running 958-1,181 s, used as a Meta ad by the drama app.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-5s | Cold open mid-conflict: two women, one accusing the other | First line is drama, not product: "You wore MY necklace to her wedding?" |
| 5-30s | Shot-reverse-shot dialogue, medium close-ups, warm interior | Escalation, a secret revealed |
| 30-60s | Twist: the necklace matters to the plot (it was a gift, it survived something) | Product appears as a prop, never pitched |
| 60-90s | Payoff + cliffhanger for episode 2 | "Part 2 tomorrow" caption |
| End card (2s) | Product + brand, quiet | "[Brand] · waterproof 14K" + AI label if generated |

### Prompts

**Script (Claude)**

```
Write a 90-second soap-opera episode with 3 women, one location, one secret and a cliffhanger. A gold necklace from [brand] is the object the conflict is about. No product claims in dialogue except one natural line ("I literally swim in it").
```

**Veo 3 / Seedance (dialogue scenes)**

```
cinematic medium close-up, two women in a boutique arguing, dramatic soft lighting, 35mm, natural lip-sync with dialogue "[line]", 8s, 9:16
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
- [ ] Files named `F08-<concept>-<variant>`; tracking tag `utm_content=F08-<concept>-<variant>`.
- [ ] Avoid: Entertainment first: if the product is pitched in the first 30s it becomes an ad and drops retention.
- [ ] Avoid: Keep the same faces across episodes (character reference images), or the series feels fake.
- [ ] Avoid: Long dialogue AI scenes break; keep each generated shot under 8s and cut between them.

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
5. Name every asset `F08-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F08
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

A 45-120s mini-episode with characters, conflict, tension and payoff; product enters late as the thing that changes the scene. "Women wanna watch shows… They don't wanna get 8 seconds into their scroll and suddenly feel ambushed by an ad. So give them the show" ([@frankyecom](https://x.com/frankyecom/status/2106833649970684195)). Best drama ads let the viewer "experience a version of themselves they secretly want to become" ([@frankyecom](https://x.com/frankyecom/status/2108308896813326775)).

Beat sheet (60-90s): cold open mid-conflict (line of dialogue) · setup (who, what's at stake) · escalation (embarrassment/rival/ex) · turn (friend/mother/stranger offers the product) · payoff (status reversal, compliment, confidence) · tag: product + offer. Series: Episode 2 continues the same characters (recurring cast lowers cost and raises recall).

### Why it works

Retention (people want the payoff), comments ("I need part 2"), shares among friends; avoids ad-blindness.

### Hooks

"My husband's 'work wife' came to our anniversary…", "My ex showed up to the wedding with…", "She borrowed my necklace and never gave it back", "I found my mom's jewelry box after…".

### Production recipe

Claude writes 10 episode outlines from LC personas; AI video (Seedance/Veo/Kling) with locked cast reference sheets, or real actors on a 1-day shoot for 6 episodes; VO + captions; real product close-ups.

## Reference examples

See [examples/README.md](examples/README.md) (15 posts). Top 5:

- @adamtaylorl (381L/593BM/77kV): Resilia mastered storytelling ads -> $100M/yr. — https://x.com/adamtaylorl/status/2099815494434099379
- @frankyecom (282L/437BM/67kV): Women want shows: characters, drama, payoff; build entertainment first, slot product in. — https://x.com/frankyecom/status/2106833649970684195
- @frankyecom (344L/248BM/54kV): AI UGC dominating; women consume ads differently (story/drama) - creative strategist takeaway. — https://x.com/frankyecom/status/2105377535345258584
- @frankyecom (206L/182BM/11kV): Best drama ads let viewer see the version of herself she wants to become. — https://x.com/frankyecom/status/2108308896813326775
- @frankyecom (215L/116BM/22kV): Cinematic realistic AI ads in scrutinized categories (GLP). — https://x.com/frankyecom/status/2105732607208026318
