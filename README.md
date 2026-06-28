# OmniFusion — Landing Page

A single-file, dependency-free marketing landing page for
[OmniFusion](https://github.com/MaxiZm/OmniFusion), the self-hostable,
OpenAI-compatible council-of-models inference endpoint.

## What's here

| File | Purpose |
| --- | --- |
| `index.html` | The entire site — HTML, CSS, and JS inlined. No build step. |
| `favicon.svg` | The OmniFusion mark (warm graphite + molten amber). |

## Design language

The page extends OmniFusion's own admin-UI brand DNA rather than a generic dark
theme, and leans into the product's **judicial / deliberative** world — a
*council* convenes, a *judge* weighs consensus and dissent, a *verdict* is
synthesized.

- **Surfaces** — warm graphite (`#0e0d09` → `#28261d`), not cold black.
- **Accent** — a single *molten amber* (`#e8743b`). Depth comes from a deep
  ember + black, not a second hue (warm-monochrome discipline). Status colors
  (desaturated green / clay) are used only as semantics, never as brand accents.
- **Type** — Newsreader (editorial serif display, optical sizing), Archivo
  (technical grotesque body), Spline Sans Mono (data/labels). The verdict is set
  in serif against the mono machinery — the type contrast encodes meaning.
- **Texture** — ledger hairline grid + warm drifting aurora + film grain.
- **Structure** — `§` section marks for the one real sequence (the proceedings).

### The signature: *the council in session*

The hero centerpiece is a live, orchestrated deliberation that boots on load:
the prompt types in, three panelists move queued → calling → returned, a
consensus meter resolves, the judge marks agreement and one **dissent**, and a
synthesized **verdict** types out in serif. It loops gently and has a manual
**replay**. It is illustrative (labelled as such) — no live model calls, no
benchmark/accuracy claims.

Other elements: an orchestrated hero load sequence, a compatibility statement
(not a logo marquee), the §01–§03 proceedings with a connecting flow line,
tabbed code samples with copy-to-clipboard, a bento feature grid with cursor
spotlight, an instrument-grade spec ledger, scroll-reveal that is **fail-open**
(content is visible by default; JS only opts into the hidden-then-animate state),
visible keyboard focus, and a full `prefers-reduced-motion` path. Fully
responsive.

## Run it

No tooling required — open `index.html` directly, or serve the folder:

```bash
python3 -m http.server 4173
# then open http://127.0.0.1:4173
```

## Deploy

Live at **<https://maxizm.github.io/OmniFusionWEB/>**, served from the
`gh-pages` branch (a mirror of `main` plus a `.nojekyll` marker). To redeploy,
push your changes and re-sync `gh-pages` to `main`.

It's static, so any host works — GitHub Pages, Netlify, Vercel, Cloudflare
Pages, or an S3 bucket. Drop the folder in and point the root at `index.html`.

## Notes on copy

All OmniFusion product claims are drawn from the OmniFusion README. Per the
project's own benchmark-honesty rules, **no performance advantage is asserted for
OmniFusion itself.**

The **Benchmark** section makes the architectural case with third-party evidence:
[OpenRouter's published DRACO results](https://openrouter.ai/blog/announcements/fusion-beats-frontier/)
("Surpassing Frontier Performance with Fusion", Jun 12 2026) on Perplexity AI's
DRACO deep-research benchmark, where fusion panels outscore every frontier model
run solo. The numbers are charted verbatim from that post and are explicitly
attributed to **OpenRouter Fusion** — they validate the *architecture* OmniFusion
shares (panel → judge → synthesis), not OmniFusion's own runs. OmniFusion is not
affiliated with OpenRouter.
