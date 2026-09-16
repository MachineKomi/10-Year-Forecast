# HORIZON — The Next Ten Years

An illustrated, evidence-led exploration of 2027–2036, comparing the Astra, Fable, Grok and Gemini forecasts in this repository. Includes the complete website originally built with OpenAI Sites, ten original annual illustrations, 30 editorial forecast entries, 40 model/year summaries, nine thematic comparisons and 18 evidence records.

[Current OpenAI Sites edition](https://the-next-ten-years.hawkinguniverse01.chatgpt.site) · [Deploy on Vercel](docs/DEPLOYMENT.md) · [Research and data guide](docs/RESEARCH.md)

## Run locally

From the repository root, with Python 3 installed:

```sh
python3 -m http.server 8000 --directory dist
```

On Windows, use `py -m http.server 8000 --directory dist` if `python3` is unavailable. Open **http://localhost:8000**. Serve the site over HTTP; opening `index.html` as a local file will not reliably load its JavaScript modules.

No dependency installation, compilation, API key, OpenAI account, database or backend is required to run the site. Google Fonts is an optional external font request; system fonts provide a fallback. Evidence and original-forecast links lead to external sources.

## Deploy on Vercel

Import **MachineKomi/10-Year-Forecast** into Vercel. Use the repository root, the **Other** framework preset and the committed `vercel.json`. It selects `dist` as the output directory and skips installation and building. See [deployment instructions](docs/DEPLOYMENT.md).

## Repository guide

| Path | Purpose |
| --- | --- |
| `2027-36-*.md` | The four original model forecast documents, preserved unchanged |
| `dist/index.html` | Page shell and navigation |
| `dist/app.js` | Interactive timeline, comparisons, citations, dialogs and history |
| `dist/data.js` | Canonical editorial dataset and source records |
| `dist/visuals.js` | Annual art descriptions, accents and interface motifs |
| `dist/styles.css` | Responsive layout, typography, colour and motion |
| `dist/art/` | Ten full-resolution WebP illustrations and ten thumbnail variants |
| `art-provenance/` | Image-generation prompts and portable asset manifest |
| `research/forecast-snapshot.json` | Machine-readable export for research tools |
| `scripts/export-data.mjs` | Regenerates the JSON export from the canonical dataset |
| `docs/` | Deployment, research methodology and original implementation notes |
| `vercel.json` | Portable static hosting configuration |

The files in `dist` are the authored source and deployable website, not disposable build output. Edit them directly and keep them committed. The dataset is a **16 September 2026 snapshot**, not a live research feed.

## Research reuse

Use the JSON snapshot directly in Python, R, notebooks or other systems. To refresh it after editing `dist/data.js`, with a modern Node.js installed:

```sh
npm run export:data
```

No `npm install` is needed. Preserve original model outputs, document your changes, distinguish observations from forecasts and define outcome criteria before scoring predictions. [Research guidance](docs/RESEARCH.md) explains the schema and limitations.

## Provenance and licence

The original inputs are pinned to revision `cc6c7ce283124bd8351565ebd0b75d49289cb2c7`. Model names and versions follow the supplied document labels; provider provenance has not been independently verified. The ten illustrations were generated with OpenAI's available image tool; its exact model version was not exposed. Artwork depicts imagined scenes rather than evidence or technical diagrams.

The existing [Apache 2.0 licence](LICENSE) is preserved. Linked third-party publications retain their own terms; this repository contains citations and editorial summaries, not copies of those publications.

This export captures the deployed Sites source revision `08f2518d52d8b07fb3347bb96b0cdfbd09d87064`. OpenAI hosting account identifiers and ephemeral execution paths are not needed for deployment and are omitted from this portable export. Future edits in GitHub and OpenAI Sites do not automatically synchronise.
