# BOT.md · generate a "Click-to-message ads (Messenger / IG DM / TikTok Instant Messaging) — 'stylist in your DMs'"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: Ad 1080x1350/1080x1920 + DM flow), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@aura_alloy](https://x.com/aura_alloy/status/1982632501110812979) · A small jewellery seller's post: a 30-second clip of a moissanite pendant necklace turning slowly on a black velvet display card, with three more clips of other pieces. The whole sales path is in the caption: what comes in the box, the price, and "to place an order, send us a DM or message us on WhatsApp". It shows the selling-in-DMs behaviour that click-to-message ads are built for; it is an orga
- Example: [@tajaccesories](https://x.com/tajaccesories/status/1726896564520845767) · The “Cupid” love necklace Price: N5,500 Please send us a DM to order Jewelry in Lagos. Delivery available Nationwide @HafeezAkanni_
- Example: [@3sixfivepro](https://x.com/3sixfivepro/status/1968749907600105843) · Click-to-message ads on @WhatsApp are a simple way to move people from scrolling to starting a conversation. ✅ Instead of sending them to a landing pa

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Creative | Product + concrete promise | "Send us who it's for + budget, we'll build her stack in 2 minutes" |
| CTA | Send message button | - |
| DM flow | Auto-greeting with 3 quick replies (gift / for me / help me choose) | Then a human or a bot recommends 3 pieces |
| Close | Checkout link in the chat | - |

### Prompts

**Meta setup**

```
Objective: Engagement or Sales with "Message destination" (Messenger + IG + WhatsApp). Greeting template with quick replies; route to a person within 5 minutes during business hours.
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
- [ ] Files named `F60-<concept>-<variant>`; tracking tag `utm_content=F60-<concept>-<variant>`.
- [ ] Avoid: A slow reply kills it; staff it or use a bot with a handoff.
- [ ] Avoid: No clean public example; visual is a mock.

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

See [examples/README.md](examples/README.md) (1 posts). Top 5:

- @aura_alloy (0L/0BM/0V):  — https://x.com/aura_alloy/status/1982632501110812979
