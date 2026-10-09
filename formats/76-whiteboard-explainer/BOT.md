# BOT.md · generate a "Whiteboard explainer (marker diagram of the mechanism, static or video)"

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
5. Name every asset `F76-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F76
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

A hand-drawn whiteboard diagram explaining why the usual fix fails and how the product works (layers, timelines, cost math). Shown as a photo of the whiteboard or a 30s marker-drawing video with a person addressing the viewer by name ("Hey Priya, you need this").

### Why it works

- Teacher framing creates authority without claiming credentials.
- A marker drawing feels homemade and honest.
- Simplifies LC's real edge (bonded PVD vs plating) into one picture.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static | Whiteboard photo: two drawn layers "plating (wears off)" vs "PVD (bonded)" + arrows + LC necklace taped on | Headline: "whiteboard alert ✏️" |
| Video 30s | Hand draws the diagram, VO explains | "Before you buy another gold chain…" |

### Hooks

- "Whiteboard alert ✏️ why plating wears off"
- "Before you buy another gold chain, look at this"
- "The 2-layer drawing every jewelry buyer should see"

### Production recipe

1. Use a real whiteboard and the founder's handwriting.
2. One idea per board: layers, cost per wear, care.
3. Shoot the static and a 30s time-lapse.

### Existing bot prompt

```
Write 4 whiteboard explainers for LC: what to draw (labels, arrows), 60-word VO, headline. Use only {{PDP_FACTS}}.
```

### Variants to test

- Static vs time-lapse
- Named-address hook vs generic

## Reference examples

See [examples/README.md](examples/README.md) (6 posts). Top 5:

- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @artfully_amberr (9L/0BM/252V): Here's a #UGCexample I made for Stasis. This whiteboard explainer concept has generated revenue for the client. For this creative, I leaned into my background a — https://x.com/artfully_amberr/status/2100249277029126306
- @0xROAS (213L/357BM/24kV): here's another BANGER ai ad style you can use in your ads it's called BRB Whiteboard Explainer style (my fav) there's infinite ways you can scale your creative  — https://x.com/0xROAS/status/2094086530973229173
- @raph_guilhem (55L/105BM/7kV): 30 Meta ad formats folder tree (hooks, founder content, etc.). — https://x.com/raph_guilhem/status/2083288607062732816
- @Ecombos_Ai (28L/26BM/2kV): 10 AI UGC styles: talking-head testimonial, product-in-hand, first-try reaction, fake podcast, street interview, comment reply, unboxing, DITL/GRWM, before/afte — https://x.com/Ecombos_Ai/status/2103180929057407425
