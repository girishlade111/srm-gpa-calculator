# SRM GPA Calculator

A pair of free, offline, client-side grade calculators for students of **SRM Institute of Science and Technology** (and anyone using a 10-point grading scale): compute your **semester GPA** from course grades and credits, and your **cumulative CGPA** across semesters. No sign-up, no server, no data leaves your browser.

## What It Does

- **Semester GPA calculator** (`srm-gpa-calculator.html`) — add courses with their grade and credit value; it totals grade points and credits and computes the semester GPA on SRM's 10-point scale.
- **CGPA calculator** (`srm-cgpa-calculator.html`) — add as many semesters as you like with each semester's GPA (and credits); it rolls them up into your cumulative CGPA.
- Everything runs locally in a single HTML file — works offline once loaded.

## Tech Stack

- Plain HTML, CSS, and vanilla JavaScript (no frameworks, no build step, no dependencies)
- Each calculator is one self-contained `.html` file with inline styles and scripts

## Quick Start

No installation needed. Either:

1. Open `index.html` (landing page) in any browser and pick a calculator, or
2. Open `srm-gpa-calculator.html` / `srm-cgpa-calculator.html` directly.

### Run a local server (optional)

```bash
# Python
python3 -m http.server 8000
# then visit http://localhost:8000

# Node
npx serve .
```

## Project Structure

```
├── index.html                  # Landing page linking both calculators
├── srm-gpa-calculator.html     # Semester GPA calculator (grades × credits)
├── srm-cgpa-calculator.html    # CGPA calculator (multi-semester rollup)
└── LICENSE                     # MIT
```

## Grading Reference (SRM 10-point scale)

| Grade | Points |
|-------|--------|
| S     | 10     |
| A     | 9      |
| B     | 8      |
| C     | 7      |
| D     | 6      |
| E     | 5      |
| F     | 0      |

> GPA = Σ (grade points × credits) ÷ Σ credits. CGPA is the credit-weighted average across semesters.

## Deploy Notes

Static site with zero build — deploy anywhere:

- **GitHub Pages:** Settings → Pages → Deploy from branch → `main` / root. Served as `https://<user>.github.io/srm-gpa-calculator/`.
- **Cloudflare Pages / Netlify / Vercel:** drag-and-drop the folder or connect the repo; no build command, publish directory = repo root.

## License

MIT — see [LICENSE](LICENSE).

---

Built by Girish Lade — https://ladestack.in
