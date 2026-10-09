# BOT.md · generate a "Drama "show" micro-series (product as a prop, entertainment first)"

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
- @frankyecom (281L/437BM/66kV): Women want shows: characters, drama, payoff; build entertainment first, slot product in. — https://x.com/frankyecom/status/2106833649970684195
- @frankyecom (344L/248BM/54kV): AI UGC dominating; women consume ads differently (story/drama) - creative strategist takeaway. — https://x.com/frankyecom/status/2105377535345258584
- @frankyecom (206L/182BM/11kV): Best drama ads let viewer see the version of herself she wants to become. — https://x.com/frankyecom/status/2108308896813326775
- @frankyecom (215L/116BM/22kV): Cinematic realistic AI ads in scrutinized categories (GLP). — https://x.com/frankyecom/status/2105732607208026318
