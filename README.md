# Is the Planet Warming?

An interactive investigation for college general chemistry: students commit to a position, then
argue the side they do *not* hold using nothing but the data, stress test both arguments, and state
what actually stands.

**Live tool:** open `index.html`. All data is embedded in the page; no server needed.

## The question

Can the data support the premise that the average temperature of the planet is rising?

Temperature only. There are no greenhouse-gas columns in this tool, by design — the cause question
belongs to the companion tool, [Warming-vs-CO2](https://github.com/Lufox2021/Warming-vs-CO2), and
mixing them lets students answer "why" before they have settled "whether."

## The data

1,834 rows, one per place per year, 1895–2025.

| Column | Meaning |
| --- | --- |
| `year`, `decade` | The year of the reading |
| `location` | 14 regions, from one county to whole continents (below) |
| `temp_f` | Average temperature over the year, °F |
| `anomaly_f` | The same reading against that place's own 1901–2000 average |

Locations, in order of increasing area: Onslow County (NC) · North Carolina · California · Kansas ·
New Mexico · Contiguous U.S. · North America · South America · Europe · Africa · Asia · Oceania ·
Arctic · Antarctic.

The continental and polar series are NOAA Climate at a Glance Global, built from 5°×5° grid cells
and area-weighted; each region's coverage is stated in the tool. The U.S. series are the NOAA
U.S. Climate Divisional Database. Nothing is smoothed, interpolated or offset-corrected.

## What the tool does

Hypothesis lock-in, filters (including multi-select of up to five locations at once), a data table,
a plotting engine — response vs. a variable in four styles including a dot-per-reading strip plot,
distributions, main effects, interactions, 3D surfaces — with least-squares fitting and reported
standard errors, summary statistics, and a calculator for derived columns.

When a fit is run against a variable that closely tracks the calendar, the tool says so.

## What students find

Every one of the 14 regions warms, and every slope exceeds twice its own standard error. The size
varies enormously: Arctic +0.332 ± 0.025 °F/decade, California +0.234 ± 0.020, Onslow County
+0.105 ± 0.024, Antarctic +0.052 ± 0.007.

The cherry-pick is discoverable from inside the tool. Filter the contiguous U.S. to 1998–2012 and
the slope is −0.015 ± 0.046 °F/decade — a flat or cooling trend, from real NOAA data, honestly
plotted. Widen the window and it disappears. That asymmetry between a chosen interval and the full
record is the lesson: you cannot take a position and then go find the data that supports it.

Built by Tad Fox for general chemistry at Campbell University.
