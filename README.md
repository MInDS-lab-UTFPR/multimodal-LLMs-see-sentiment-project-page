# Multimodal LLMs See Sentiment — project page

Project page for **[Multimodal LLMs See Sentiment](https://arxiv.org/abs/2508.16873)**
(da Silva, Harrison, Minetto, Delgado, Nassu, Silva).

| | |
|---|---|
| Paper | [arXiv:2508.16873](https://arxiv.org/abs/2508.16873) |
| Code | https://github.com/neemiasbsilva/multimodal-LLMs-see-sentiment |
| Dataset | https://huggingface.co/datasets/Neemias/multimodal-LLMs-See-Sentiment |
| Models | https://huggingface.co/Neemias/multimodal-LLMs-See-Sentiment |

## Develop

```bash
npm install
npm run dev      # http://localhost:4321
npm run build    # astro check && astro build -> dist/
npm run preview  # serve the production build
npm run all:fix  # astro check + eslint --fix + prettier --write
```

## Where things live

| Path | What it is |
|---|---|
| `src/paper.mdx` | **All page content.** Front matter sets the tab title, description, favicon and link-preview thumbnail; the body is the page. |
| `src/pages/index.astro` | The HTML shell — `<head>`, meta tags, typography classes. |
| `src/components/` | Content components used from the MDX. |
| `src/assets/` | Figures and images, optimised at build time. |
| `public/` | Files served as-is: `favicon.svg`, `thumbnail.png`. |
| `src/styles/global.css` | Tailwind entry, theme tokens, column-width variables. |

### Components written for this page

| Component | Use |
|---|---|
| `BaselineChart.astro` | The four-panel F-score comparison against VADER / ResNet / Swin. Pass `panels`; bars with `ours: true` get the accent colour. |
| `CueRow.astro` | One interpretability example — thumbnail, description excerpt, semantic cues, human perception tags, ground truth vs prediction. |
| `CaseCard.astro` | One cross-dataset qualitative case — image with ground truth, baseline prediction and ours. |
| `Stats.astro` | The headline number tiles under the intro. |

The rest (`Header`, `Figure`, `Picture`, `Wide`, `Table`, `HighlightedSection`,
`TwoColumns`, `Carousel`, `Video`, `SmallCaps`, `starwind/tabs`) come from the template.

## Deploying

`.github/workflows/astro.yml` builds and deploys to GitHub Pages on every push to `main`.
Enable Pages for the repository with **Source: GitHub Actions** and it works with no further
configuration — the workflow passes `--site` and `--base` for you.

## Credits

Built with [Roman Hauksson-Neill's academic project page template](https://research-template.roman.technology).
