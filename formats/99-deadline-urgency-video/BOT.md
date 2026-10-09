# BOT.md · generate a "Deadline-urgency video (two-line sale-ends skit, 'don't say I didn't warn you', hands-only deal clip)"

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
5. Name every asset `F99-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F99
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

Short (10-30 s) bottom-of-funnel videos whose only job is the deadline: a two-person micro-skit ("Wait, the sale ends today?"), a hands-only product clip with "THIS DEAL WON'T LAST" text, or a blunt to-camera warning. They sit under the long-form story ads and close the people those ads warmed up.

### Why it works

- Long story ads create desire; these convert it before it fades.
- Ten seconds, one message, works muted.
- Skits make urgency feel like gossip instead of a banner.
- Strategists report BOF statics and deal videos now take top impression rank in these accounts.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0:00-0:03 | Two friends in a car, one scrolling | "Wait, what do you mean the sale ends tonight?" |
| 0:03-0:10 | Other friend holds up her stack | "Any 7 for $85 ends at midnight. I'm getting the gold huggies for Mom." |
| 0:10-0:15 | Hands-only end card, text "ENDS MIDNIGHT" | "Link below." |

### Hooks

- "Wait, what do you mean the sale ends tonight?"
- "Don't say I didn't warn you: last day for 7 for $85."
- "Restock is live. Last time it lasted 9 days."

### Production recipe

1. Build a calendar of REAL deadlines (BFCM, Mother's Day ship-by, restock windows).
2. Shoot 3 skits and 3 hands-only clips per deadline; swap only the date card.
3. Run only to warm audiences (video viewers 50%+, site visitors).

### Existing bot prompt

```
Write 6 deadline-urgency videos (≤15 s) for LC's real deadline {{DEADLINE}}: 2 two-person skits, 2 hands-only clips, 2 to-camera warnings. Each states the real end time and the offer (any 7 for $85). No fake stock counters.
```

### Variants to test

- Skit vs hands-only
- Gift vs self-purchase angle

## Reference examples

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @ErJithin (0L/0BM/0V): Story-song ads losing top impression rank to BOF statics in Koriderm/Resilia libraries. — https://x.com/ErJithin/status/2107419279872360910
- @MaximilianMoj (0L/0BM/0V): Resilia "$36M/month" (unverified) top 5 ads via Playhead teardowns: candida, aged garlic 4-week arteries, GLP-1, urgency (8 at once), animated explainer. — https://x.com/MaximilianMoj/status/2101002307160731848
- @jackolivieri_ (0L/0BM/0V): Smooche static "847 Orders in Last Hour, Almost Gone" / "LIVE UPDATE" stock copy (GetHookd share). — https://x.com/jackolivieri_/status/2097798592010547583
- @Counterprint (0L/0BM/0V):  — https://x.com/Counterprint/status/2107894146140631180
- @CityOfStonks (61L/1BM/3kV): LAST CHANCE TO GRAB SOME KEYS!!! @ccmweb3 has a GIVEAWAY for FIVE keys This is the creative agency that built City of Stonks, my personal media brand - show som — https://x.com/CityOfStonks/status/2093225775755657483
