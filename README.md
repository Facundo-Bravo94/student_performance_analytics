# Student Performance Analytics 📚

**[Live demo →](https://facundo-bravo94.github.io/student_performance_analytics/)**

Interactive dashboard exploring how study habits, sleep, stress and screen time relate to academic performance, built on a Kaggle dataset of ~3,000 students. It's a standalone web version of the same analysis originally built in Power BI — same underlying insights, delivered as a dependency-free dashboard anyone can open straight in a browser.

## Problem

Dashboards are often locked behind BI tools that require a license or desktop app to view. This project asks: can the same interactive, filterable experience be rebuilt as a single static HTML file — with real-time filtering and custom charts — using nothing but HTML, CSS and vanilla JavaScript?

## Methodology

- **Data**: Kaggle dataset on student habits vs. academic performance (~3,000 students), pre-aggregated client-side into KPI and segment summary tables (performance tier × city type).
- **Charts built from scratch** — no charting library: bar charts and KPI cards in CSS, the donut chart drawn directly with the Canvas API, and a scatter plot rendered on canvas as well.
- **Interactivity**: filtering by performance tier (Low / Medium / High) and city type (Rural / Semi-Urban / Urban) recomputes every KPI and chart in real time from precomputed lookup tables — no server, no build step.

## Tools

HTML5 · CSS3 · JavaScript (vanilla) · Canvas API

## What it shows

- KPI row — average exam score, average study hours/day, % high burnout risk, doomscrolling impact on score, % focused students.
- Study time vs. exam score scatter, segmented by performance tier and filterable by city type.
- Average exam score by career goal, stress vs. motivation by performance tier, mental-state distribution (donut), learning style comparison, and doomscrolling-before-sleep impact.

## Key findings

- Higher performers study more (4.7h/day vs. 3.5h for the lowest tier), but hours alone don't explain the gap — stress drops (6.1 → 4.7) and motivation rises (4.9 → 6.6) as performance improves.
- Doomscrolling before sleep is associated with a ~5-point drop in average exam score across every segment.
- Burnout risk falls sharply with performance: **39% (Low) → 26% (Medium) → 17% (High)**.

## Repo contents

- [`index.html`](index.html) — full dashboard, self-contained, no build step required
