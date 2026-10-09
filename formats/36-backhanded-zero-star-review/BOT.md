# BOT.md · generate a "Backhanded / 'bad review' ad (complaint that is secretly a benefit)"

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
5. Name every asset `F36-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F36
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

A review-card or creator reading a "1-star review" whose complaint is actually a benefit ("1 star: I can't find a reason to take it off"), or a brand "we're sorry" apology for a positive problem ("we're sorry the herringbone sold out again"). Must use real reviews or be clearly the brand's own joke.

### Why it works

- Negative stars stop the scroll (loss-aversion).
- The twist makes it shareable; humour lowers ad resistance.
- Real backhanded reviews are common in LC's review base (compliments, "addicted").

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | 1-star review card on screen, creator reacting | "We got a 1-star review…" |
| 2-8s | Zoom on text: "Ruined my life. Everyone asks where it's from and I have to keep sending the link." | Creator deadpan |
| 8-15s | Product shots | "We're so sorry. Any 7 for $85." |

### Hooks

- "Our worst review ever:"
- "We're sorry. (Not really.)"
- "1 star: now my sister wants one too"
- "Complaint received: I forgot I was wearing it in the ocean"

### Production recipe

1. Search LC reviews for backhanded phrases ("addicted", "everyone asks", "husband", "can't stop").
2. Use real review text (with reviewer first name/initial per review-platform rules); if invented for comedy, frame as brand's own joke, never as a customer review.
3. Static review card + 10-15s creator/Qirra read version.

### Existing bot prompt

```
From these real LC reviews {{REVIEWS}}, find 10 that read like complaints but are benefits. For each: on-image quote (verbatim), 1-line brand "apology", 80-word primary text. Do NOT edit review wording.
```

### Variants to test

- Review card vs founder read
- Apology vs 1-star frame

## Reference examples

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @ads4apps (412L/930BM/27kV): 39 Meta formats that convert (930 bookmarks): X reasons, IG story, us vs them, Venn, don't buy this, iPhone notes, text message, low stock, we're sorry, breakin — https://x.com/ads4apps/status/2081785032679518490
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @KanishDigital (13L/13BM/824V): Negative hooks ("this product should be banned", "don't buy this…") — for one baby brand the best ad is a fully negative ad. — https://x.com/KanishDigital/status/2101549415467213023
- @Yannlce (3L/2BM/1kV): Same 40-format list (adds claymation, AI podcast). — https://x.com/Yannlce/status/2085017654364958737
- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
