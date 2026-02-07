# Football Premier League Analysis (2008–2025) — Power BI Dashboard

Interactive Power BI report that explores whether Manchester City have been the Premier League’s “best” club in the post‑2008 era by comparing clubs across results, attacking output, defensive control, and discipline.

The dashboard is intentionally definition-driven: instead of one score, it lets you switch seasons/windows and see which clubs lead under different metric definitions.

## Download & open (recommended)
The easiest way to view the dashboard is to download the **PBIX** from the latest GitHub Release:

- Latest release page: [sha256:c5d0f001ba2a95f3c12482aa04eba6639c8bba5225ce82ea22321eb6dd4ab95c](https://github.com/Mahdibenj22/PL_2008_2025_Analysis/releases/tag/v1.0.0)

Download the `.pbix` asset from that page, then open it in **Power BI Desktop**.

## Data (included in this repo)
This repository includes the match-level Premier League CSV files under:

- `PL_2008_2025/`

If your PBIX prompts “can’t find file / credentials”, it’s usually because Power BI still points to the original file path from the author’s computer.

### Fix data paths (first time only)
After cloning/downloading this repo:

1. Open the PBIX (or the PBIP project) in Power BI Desktop.
2. Go to **Transform data** (Power Query).
3. Find the query step that references the folder/file path and update it to your local path, pointing to this repo’s `PL_2008_2025/` folder.
4. Click **Close & Apply**, then **Refresh**.

Tip: If you downloaded the repo as ZIP, make sure you **extract** it first (don’t open from inside the ZIP). [web:1252]

## Quick start (no Git)
1. GitHub repo page → click **Code → Download ZIP**, then unzip. [web:1252]
2. Open the PBIX from the Release (section above).
3. If prompted, set the data path to: `<unzipped-folder>\PL_2008_2025\`, then Refresh.

## Quick start (with Git)
```bash
git clone https://github.com/Mahdibenj22/PL_2008_2025_Analysisis.git
Then:

Open the PBIX from Releases (recommended), or open the PBIP project (below).

Update the data path to: <cloned-folder>\PL_2008_2025\, then Refresh.

Project format (PBIP) — for developers
This repository also contains a Power BI Project (.pbip) version for source control and collaboration:

pl_09_25.pbip

pl_09_25.Report/

pl_09_25.SemanticModel/

PBIP stores the report and semantic model as text-based definitions, which works well with Git workflows. [web:1124]

Report pages (what you’ll find)
Index / Navigation: Landing page to navigate the report.

Team Performance Summary: Points, wins, home/away splits, and context counters.

Offensive Analysis: Goals, shots, shots on target, accuracy-style indicators.

Defensive Analysis: Clean sheets, shots on target conceded, goals conceded, Big 6 trend.

Aggression / Discipline: Fouls/cards and custom aggression views.

Scope used in the report
Seasons: 2008/09 → 2024/25

League: English Premier League

Data type: results + match statistics counts (no xG / tracking)

Notes / limitations
Match-stat fields can vary by season/source; if a season has missing stats, visuals depending on those fields may be incomplete.

Credits
Data: football-data.co.uk (historical results + match stats CSVs) [web:978][web:1159]

Built with: Microsoft Power BI

Author
Mahdi Ben Jemaa
