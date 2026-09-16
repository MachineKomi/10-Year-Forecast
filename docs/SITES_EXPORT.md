# The Next Ten Years

An interactive editorial forecast for 2027–2036, comparing Astra, Fable, Grok and Gemini against a dated evidence snapshot.

- Plain static HTML, CSS and ES modules. No dependency installation or compilation is required.
- `dist/data.js` contains 30 forecast entries, 40 model/year summaries, nine thematic comparisons and 18 evidence records.
- `dist/app.js` renders year navigation, inline evidence disclosures, accessible year/art dialogs, comparisons and data visualisations.
- `dist/styles.css` includes desktop/mobile layouts, keyboard focus states and reduced-motion handling.
- Each of the ten years has a unique OpenAI-generated illustration with a coordinated accent and motif. Full-size WebP scenes and small responsive/navigation variants live in `dist/art/`. These are imagined scenes, not evidence or technical diagrams.
- Timeline, Compare, Evidence and About are distinct navigable views. Year/mode deep links, Back/Forward reading positions, per-year disclosure memory, keyboard focus and reduced-motion preferences are supported.
- Generation prompts and a provenance manifest are retained in `art-provenance/`. The available ImageGen tool did not expose a model-version selector; no specific version is asserted.

## Provenance

Forecast inputs: https://github.com/MachineKomi/10-Year-Forecast/tree/cc6c7ce283124bd8351565ebd0b75d49289cb2c7

Evidence snapshot: 16 September 2026. Model labels follow the supplied repository. Primary evidence is linked at the claim level and in the evidence catalogue. Data-centre demand uses the IEA 2026 update (485 TWh estimated for 2025; 950 TWh projected for 2030), rather than mixing editions.

Forecasts are qualitative editorial judgements. Agreement is not a calibrated probability. Timing windows distinguish programme targets, institutional projections and speculative milestones. GLM/DeepSeek non-response is recorded as a user report; its cause is not asserted.

## Validation

JavaScript syntax; ten year templates; ten four-model year comparisons; nine topic comparisons; all 30 inline evidence entries; source/model referential integrity; invalid query-parameter handling; view selection, history and focus logic; dialog templates; generated HTML structure; local asset references and WebP dimensions. All ten illustrations were visually inspected. A separate static UX review identified and resolved route validation and history/disclosure persistence issues. No live browser rendering was performed in this redesign flow.

Original deployment used OpenAI Sites. This portable copy uses `vercel.json`; the original account-specific hosting manifest is intentionally excluded. Runtime files match the deployed Sites source.
