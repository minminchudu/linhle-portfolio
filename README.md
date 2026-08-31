# Portfolio site

Source for the analyst portfolio of Linh Le. Case studies across healthcare finance,
payments, e-commerce, retail and product research, plus the work behind them.

Astro, static output, plain CSS. No framework runtime ships to the browser.

## Running it

```sh
npm install
npm run dev      # localhost:4321
npm run build    # static output to dist/
npm run preview  # serve the built output
```

Requires Node 22.12 or newer.

## Where things are

| Path | What it holds |
| :--- | :--- |
| `src/pages/index.astro` | The single-page front: hero, narrative, projects, experience, education, toolkit, contact |
| `src/pages/work/` | One case study per project |
| `src/pages/beyond.astro` | Rough to Cut, the personal page |
| `src/pages/writing/` | Essay reading pages, generated from `src/content/essays.json` |
| `src/components/` | Work cards, role diagrams, figures, the header mark |
| `src/layouts/` | `Base.astro` for the shell, `CaseStudy.astro` for the case study frame |
| `src/styles/tokens.css` | Colour, type scale and spacing tokens, light and dark |
| `public/media/` | Decks, dashboards, resume, certification badges |
| `public/figures/` | Charts used inside case studies |

## Adding a case study

Copy an existing file in `src/pages/work/`, change the `CaseStudy` props, and add a
matching `WorkCard` to the projects section of `src/pages/index.astro`. The route comes
from the filename.

Every figure quoted on a page traces to a source deliverable: a notebook, a workbook, or
a report. Nothing is estimated for effect.
