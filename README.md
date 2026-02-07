# Football Premier League Analysis (2008–2025) — Power BI Dashboard

Interactive Power BI dashboard that explores whether Manchester City have been the Premier League’s “best” club in the post‑2008 era by comparing clubs across results, attacking output, defensive control, and discipline.

The report is “definition-driven”: instead of one score, you can switch seasons/windows and see which clubs lead under different metric definitions.

## Project format (PBIP)
This repository stores the report as a **Power BI Project (.pbip)**, which splits the semantic model and report into text-based files that work well with Git version control. [web:1124]

Main folders/files:
- `pl_09_25.pbip` (project entry point)
- `pl_09_25.Report/` (report definition)
- `pl_09_25.SemanticModel/` (dataset / model definition)
- `datapackage.json`, `schema.json` (data package metadata)

## Data
**Source:** football-data.co.uk match-level CSVs. The dataset includes results and (where available) match statistics such as shots, corners, fouls, bookings/cards, and referees. [web:978][web:1159]

**Scope used in the report**
- Seasons: **2008/09 → 2024/25**
- League: English Premier League
- Data type: results + event counts (no xG / tracking)

### Where are the CSV files?
This GitHub repository does **not** include the raw CSV files (they are ignored via `.gitignore`).  
To reproduce the report locally, download the required Premier League season CSVs from football-data.co.uk and place them in a local data folder (see setup below). [web:978]

## Report pages (what you’ll find)
- **Index / Navigation:** Landing page to navigate the report.
- **Team Performance Summary:** Points, wins, home/away splits, basic context counters.
- **Offensive Analysis:** Goals, shots, shots on target, accuracy-style indicators.
- **Defensive Analysis:** Clean sheets, shots on target conceded, goals conceded, Big 6 trend.
- **Aggression / Discipline:** Fouls/cards and custom aggression views.

## Model & key design choices
- Star-style modeling with a Team dimension filtering match facts.
- Includes a “Top 6” slicer option (Arsenal, Chelsea, Liverpool, Man City, Man United, Tottenham) implemented via a bridge-style pattern (may require careful relationship filtering depending on your model design). [web:1058]

## Run it locally (Power BI Desktop)
### Prerequisites
- Power BI Desktop

### Steps
1. Download the Premier League season CSV files from football-data.co.uk. [web:978]
2. Create a local folder (example): `data/raw/` and put the CSVs there.
3. Open `pl_09_25.pbip` in Power BI Desktop. [web:1124]
4. In Power BI Desktop: **Transform data** → update the source paths/parameters (first time only) so they point to your local `data/raw/`.
5. Click **Refresh**.

## Notes / limitations
- This is a results/statistics dashboard (no xG, no tracking), so it reflects outputs and event counts rather than chance quality.
- Some match-stat columns can vary by season/source; visuals depending on missing fields may be incomplete. [web:1159]

## Credits
- Data: football-data.co.uk [web:978]
- Built with: Microsoft Power BI

## Author
Mahdi Ben Jemaa
