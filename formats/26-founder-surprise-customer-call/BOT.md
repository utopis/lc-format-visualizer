# BOT.md · generate a "Founder surprise customer call (+ customer-service call variant)"

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
5. Name every asset `F26-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F26
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

The founder phones a real repeat customer who does not know the call is coming, asks normal questions ("why do you keep ordering?"), and the recorded, unscripted conversation IS the ad. Variant: a real customer-SERVICE call where a shopper asks the 5-6 pre-purchase questions and support answers them.

### Why it works

- It is a testimonial that does not look like one — you overhear a conversation instead of watching an actor (@antonioventre_).
- Surprise cannot be faked; viewers have learned to spot coached answers and AI voices.
- The CS-call variant removes objections instead of piling on claims: the viewer hears their own doubt asked and answered before the PDP.
- Founder + customer in one asset = two trust signals; works cold (TOF story) and warm (MOF objection handling).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | Split screen: Qirra at desk with phone on speaker + caption "Calling a customer who has ordered 6 times (she has no idea)" | Ringtone SFX |
| 2-6s | Customer picks up, confused/laughs — keep the real reaction | "Hello?… wait, THE Qirra?" |
| 6-20s | Q1 "Why do you keep ordering?" → answer in her words; waveform + live captions | Unedited audio, light noise reduction only |
| 20-35s | Q2 "What changed since you started wearing it?" → story (swims, showers, compliments, a gift) | B-roll of the pieces she names (LC footage) |
| 35-45s | Q3 "Would you tell a friend?" / she asks Qirra a question back | Genuine laugh/emotion moment |
| 45-55s | End card: piece names + "any 7 for $85" + review count | VO or text CTA |

### Hooks

- "I called a customer who has bought from us 6 times. She had no idea."
- "POV: the founder calls you at 9am to ask why you keep buying necklaces"
- "I asked our most loyal customer one question…"
- "She thought this was a scam call 😂"
- (CS variant) "The 5 questions everyone asks before buying waterproof jewelry — answered on a real call"
- "We called the customer who left this review →" (review card on screen)

### Production recipe

1. Pull 30 repeat customers (3+ orders) and 20 recent 5-star reviewers from Shopify/Omni; email first asking permission "to maybe give you a quick call from our founder" WITHOUT saying when (consent to call + record; surprise = timing).
2. Record with a call app that announces recording (or get verbal consent on tape at the start and keep it in the raw).
3. Qirra asks only 3-4 open questions; never leads ("isn't it amazing that…").
4. Edit: keep ums and laughs; captions word-for-word; cut to 30-60s for Meta, 20-35s for TikTok; 3 hook variants per call (different opening line or on-screen text).
5. CS variant: export the top 6 pre-purchase questions from Gorgias/inbox + ad comments; record a real support call (or a real customer who agreed to ask them) — never script fake customers.
6. Bot prompt for picking cuts: see below.

### Existing bot prompt

```
You are an LC ad editor. Here is the transcript of a recorded founder→customer call with timestamps: {{TRANSCRIPT}}. 1) Mark the 3 most emotional or surprising 5-12s moments. 2) Mark every objection answered (waterproof, tarnish, real gold?, gift, price). 3) Propose 3 cuts (20s / 35s / 55s) with in/out timestamps, an on-screen hook line (≤9 words) for each, and a caption plan. Never change her words; never add claims she did not make; flag any claim that is not on the LC PDP.
```

### Variants to test

- Founder vs support agent as caller
- Audio-only waterfall + captions vs split-screen video
- Customer on video (FaceTime, with consent) vs audio
- Hook = customer's first reaction vs on-screen stat ("6 orders")

## Reference examples

See [examples/README.md](examples/README.md) (12 posts). Top 5:

- @williamkast_ (38L/46BM/3kV): Turn 1 winning ad into 5: same message, different frameworks (DITL, 3 reasons, old me/new me, phone call). — https://x.com/williamkast_/status/2086835243474985414
- @antonioventre_ (37L/34BM/2kV): Surprise founder→customer call ad: customer doesn't know the call is coming; ad-manager screenshot shows it as top ROAS (4.80 on $20.9k) in a $112k set. — https://x.com/antonioventre_/status/2084767090116837682
- @antonioventre_ (12L/13BM/995V): Customer-SERVICE call ad: record a real pre-purchase support call answering the 5-6 questions buyers actually ask. — https://x.com/antonioventre_/status/2091592059517837677
- @therahulissar (12L/7BM/1kV): Trends beyond AI: greenscreen personal story with no product until late; natives → quiz funnel; founder calling customers. — https://x.com/therahulissar/status/2103485927528009820
- @antonioventre_ (8L/4BM/693V): Production rule: reaction can't be scripted — founder-customer call + POV reaction ads with live unscripted reaction. — https://x.com/antonioventre_/status/2091895054755373116
