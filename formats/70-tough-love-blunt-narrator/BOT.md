# BOT.md · generate a "Tough Love: blunt, scolding narrator ad ('stop doing this to yourself')"

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
5. Name every asset `F70-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F70
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

A narrator who talks to the viewer like a blunt friend or older sister: "Stop buying jewelry you have to take off." The tone is affectionate scolding, followed by a practical fix. Works as a static with long copy or as a talking-head video.

### Why it works

- Directness stands out in a feed full of polite ads.
- Scolding makes it a rescue story, with the viewer in it.
- It pairs naturally with an older, experienced narrator.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-3s | Narrator to camera, arms crossed | "Stop buying necklaces you have to take off." |
| 3-25s | Tray of green-stained jewelry | "You've spent $200 on stuff that died in a month." |
| 25-45s | LC stack, in the shower | "Buy once. 14K PVD. Any 7 for $85." |

### Hooks

- "Stop buying jewelry you have to babysit"
- "Honey, that chain is not real gold"
- "I'm going to be blunt about your jewelry drawer"

### Production recipe

1. Cast a real customer or staff member as the "blunt friend"; no invented personas.
2. Keep it affectionate, never shaming bodies or money.
3. Test as static with long copy and as a 30s video.

### Existing bot prompt

```
Write 4 tough-love scripts (30s) and 2 long-copy statics for LC in a blunt older-sister voice, warm not insulting. Proof only from {{PDP_FACTS}}.
```

### Variants to test

- Narrator age
- Static vs video

## Reference examples

See [examples/README.md](examples/README.md) (7 posts). Top 5:

- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @0xROAS (104L/139BM/9kV): 100% AI Drama Ad with Seedance 2.5... module is live inside ai ads community here’s how to make sure your dramas hit: - start with a very aggressive hook - make — https://x.com/0xROAS/status/2107188290264740348
- @mannybarbas_ (57L/28BM/6kV): Regarding turning off ads: Stop doing this constantly every single day. Sometimes an ad with a higher CPA is actually doing an important job: bringing fresh peo — https://x.com/mannybarbas_/status/2093433523906773248
- @Bobbyy_V (40L/9BM/11kV): Every player with a brain just going flats and ultra aggressive hook curls + switch stick because they know you have 1.5 seconds before Myles Garrett and Aaron  — https://x.com/Bobbyy_V/status/2096365154011074617
- @ZedNilm1 (3L/9BM/655V): this parasite ad looks like something made in 10 minutes which is exactly why i’d pay attention to it ugly animation aggressive hook zero concern for looking “p — https://x.com/ZedNilm1/status/2098017463195553912
