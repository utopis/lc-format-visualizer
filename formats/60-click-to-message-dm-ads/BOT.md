# BOT.md · generate a "Click-to-message ads (Messenger / IG DM / TikTok Instant Messaging) — 'stylist in your DMs'"

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
5. Name every asset `F60-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F60
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

Ads whose CTA opens a chat instead of a landing page. The creative promises a concrete service ("send us who it's for + budget → we'll build her stack in 2 minutes"); an automated welcome flow qualifies (recipient, style, budget) and a human or bot replies with 3 picks + checkout link.

### Why it works

- Optimises for conversations, routing ads to people willing to talk.
- Gift buyers are unsure — a stylist chat removes the decision barrier.
- Captures zero-party data (recipient, occasion) for Omnisend/OneText.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Ad 0-3s | Creator: "Don't know what to get her? DM us 'STACK'" | — |
| Ad 3-10s | Screen-record of a real chat: 3 picks appear | — |
| Chat 1 | Welcome: "Who's it for? Mom / Partner / Friend / Me" | Buttons |
| Chat 2 | "Gold or mixed? Dainty or bold?" | Buttons |
| Chat 3 | 3 picks + "any 7 for $85" link + human handoff | — |

### Hooks

- "Tell us who it's for. We'll build the stack."
- "DM 'STACK' and a real stylist picks 7 for you"
- "Gift panic? Message us."

### Production recipe

1. Build welcome flow (Meta inbox automations / ManyChat) with 3 qualifying questions.
2. Staff replies within minutes during peak gifting weeks; after-hours auto-reply with picks.
3. Send picks with UTM links (utm_content=F60-*) so Omni attributes revenue.
4. Ask opt-in for SMS/email (OneText/Omnisend) inside the chat.

### Existing bot prompt

```
Write a click-to-message ad (15s script + primary text) and a 4-step welcome flow for LC gifting: recipient, style, budget, occasion date; output 3 SKU picks logic from {{CATALOG}} and the handoff message.
```

### Variants to test

- Bot-only vs human handoff
- Platform (IG DM vs Messenger vs TikTok IMA)

## Reference examples

See [examples/README.md](examples/README.md) (0 posts). Top 5:

