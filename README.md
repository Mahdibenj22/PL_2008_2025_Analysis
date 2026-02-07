&nbsp;Football Premier League Analysis (2008–2025) — Power BI Dashboard



Interactive Power BI report that explores whether Manchester City have been the Premier League’s “best” club in the post‑2008 era by comparing clubs across results, attacking output, defensive control, and discipline.



The dashboard is intentionally “definition-driven”: instead of one score, it lets you switch seasons/windows and see which clubs lead under different metric definitions.





&nbsp;1) Data



\*\*Source:\*\* football-data.co.uk (match-level CSVs). The site provides computer-ready football results plus match statistics such as shots, fouls, cards, and referees (availability varies by season/league). \[page:1]



\*\*Scope used in the report\*\*

\- Seasons: \*\*2008/09 → 2024/25\*\*

\- League: English Premier League

\- Data type: results + event counts (no xG / tracking)



> Note: football-data.co.uk also includes betting odds fields; this report focuses on performance outcomes and match statistics. \[page:1]





&nbsp;2) Report pages (what you’ll find)



&nbsp;Index / Navigation

Landing page to navigate the report pages.



&nbsp;Team Performance Summary

High-level ranking and “who led what” views:

\- Total matches, goals, yellow/red cards (context counters)

\- Points per match + total points tables

\- Home/away points per match top lists

\- Matches won ranking



&nbsp;Offensive Analysis

Team attacking profile and style:

\- Goals (total + per match)

\- Shots vs Shots on Target per match (volume vs precision)

\- Shot accuracy + finishing/goal conversion style indicators

\- “Big win” / highest goal difference table (context / examples)



&nbsp;Defensive Analysis

Long-horizon defensive control + trend:

\- Clean sheet rate

\- Shots on target conceded per match

\- Goals conceded per match

\- Season trend line for Big 6 defensive goals conceded



&nbsp;Aggression / Discipline

Discipline and physicality patterns:

\- Team cards, fouls

\- Aggression index per match (custom)

\- Yellow \& red cards per match scatter





&nbsp;3) Model \& key design choices



\### Core model idea

A classic star approach: a \*\*Team\*\* dimension filters the match fact table(s), enabling consistent slicing across all pages.



\### “Top 6” single dropdown option (Big 6 selector)

The report supports a single slicer choice (“Top 6”) that filters the model to these clubs:

\- Arsenal, Chelsea, Liverpool, Man City, Man United, Tottenham





&nbsp;4) Reproduce the report (setup)



&nbsp;Prerequisites

\- Power BI Desktop (latest recommended)



&nbsp;Steps

1\. \*\*Get the CSVs\*\*

&nbsp;  - Download Premier League season CSV files from football-data.co.uk. \[page:1]

2\. \*\*Place files in your project folder\*\*

&nbsp;  - Keep a consistent structure (example):

&nbsp;    - `data/raw/` (downloaded CSVs)

&nbsp;    - `powerbi/` (PBIX)

3\. \*\*Open the PBIX\*\*

&nbsp;  - Open the report in Power BI Desktop.

4\. \*\*Fix file paths (first time only)\*\*

&nbsp;  - Go to \*\*Transform data\*\* → update source paths to point to your local `data/raw/` folder.

5\. \*\*Refresh\*\*

&nbsp;  - Click \*\*Refresh\*\* to load all seasons and rebuild model tables/measures.



&nbsp;Optional (recommended) UX additions

\- Add a “Reset filters” button (bookmark)

\- Add a minimum matches threshold to avoid small-sample extremes when filtering narrow windows







&nbsp;5) Notes, assumptions, limitations



\- This is a \*\*results/statistics\*\* dashboard (no xG, no tracking), so it measures outputs and repeatable tendencies rather than chance quality.

\- Match-stat fields can vary by season/source; if a season has missing stats, visuals depending on those fields may be incomplete.

\- Bi-directional filtering can be powerful but should be used carefully because it can affect performance/behavior; in this project it’s used to enable the bridge-table slicer behavior. \[page:2]







&nbsp;Credits

\- Data: football-data.co.uk \[page:1]

\- Built in: Microsoft Power BI



&nbsp;Author

Mahdi Ben Jemaa



