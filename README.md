# JNTUA SGPA / CGPA Calculator (R23)

A web app for JNTUACEA B.Tech students to calculate their **SGPA** and **CGPA** based on expected marks, following the official **R23 Academic Regulations**.

**Live demo:** https://asifshaiks531-crypto.github.io/SGPA-calculator-for-JNTUA-R23/

## Deployment (GitHub Pages)

This repo auto-deploys to GitHub Pages via GitHub Actions on every push to `main`.

**One-time setup** (only needed once per repo):
1. Go to your repo → **Settings → Pages**
2. Under "Build and deployment", set **Source** to **GitHub Actions**
3. Push to `main` — the workflow in `.github/workflows/deploy.yml` builds and deploys automatically
4. Your site will be live at `https://<username>.github.io/<repo-name>/`

If you rename the repo, update `base` in `vite.config.js` to match the new repo name exactly (with leading and trailing slashes), or assets won't load.

## Features

- Select your **branch** (CSE, AI&ML, ECE, EEE, ME, Civil, Chemical) and **semester** — subjects load automatically from the official R23 course structure
- Enter expected marks per subject; grades and SGPA calculate instantly
- Non-credit / audit courses (Environmental Science, Technical Paper Writing & IPR, Gender Sensitization, etc.) are handled correctly — marks out of 30, Satisfactory/Unsatisfactory status, excluded from SGPA/CGPA as per regulations
- Save multiple semesters to track cumulative **CGPA**
- Shows projected class of degree (First Class with Distinction / First Class / Second Class / Pass Class) and CGPA-to-percentage conversion

## Grading reference (R23)

| Marks | Grade | Points |
|---|---|---|
| 90–100 | A+ | 10 |
| 80–89 | A | 9 |
| 70–79 | B | 8 |
| 60–69 | C | 7 |
| 50–59 | D | 6 |
| 40–49 | E | 5 |
| Below 40 | F | 0 |

SGPA = Σ(Credits × Grade Points) / ΣCredits per semester
CGPA = weighted average of SGPA across semesters by credits

## Tech stack

- React 18
- Vite

## Running locally

```bash
npm install
npm run dev
```

## Building for production

```bash
npm run build
npm run preview
```

## Data source & known gaps

Subject lists and credit structures were extracted from the official JNTUACEA R23 course structure & syllabus documents and the R23 Academic Regulations document.

- Chemical Engineering: only I & II Year data available (III/IV Year syllabus document wasn't available at time of building — contributions welcome)
- If you spot an incorrect subject, code, or credit value, please open an issue or PR

## Disclaimer

This is an unofficial, student-built tool. Always verify your official SGPA/CGPA against your college's results portal or examination branch. This calculator is for planning and estimation purposes only.

## Author

Built by Asif Shaik — B.Tech CSE, JNTUACEA.
