# SyntheticSnow results

SyntheticSnow is a physics snow model (CryoGARS, Boise State University). It simulates a whole winter of mountain snow on
a 30 m grid from the terrain, the trees and the daily weather: snowfall, trees catching snow, wind moving snow,
compaction, melt and sublimation. It will make realistic training data for a neural network that maps snow from radar.
These pages compare the model with measurements it never saw; nothing in the model is tuned to them.

## Pages (interactive 3D, needs a browser with WebGL2)

- **Start here:** https://anantgahlaut.github.io/syntheticSnow/
- **LiDAR map test (30 m):** https://anantgahlaut.github.io/syntheticSnow/lidar/
  model snow depth vs airborne LiDAR at 9 SnowEx site-dates (Idaho, Colorado, Utah; 2020-2021) and at every NIVAL flight
  over Mores Creek, Idaho, in winter 2026, plus a 12-day forecast test
- **SNOTEL station test:** https://anantgahlaut.github.io/syntheticSnow/snotel/
  the model through the whole winter at 16 SNOTEL station-winters on each station's own weather, compared every day with
  the snow pillow (SWE) and the sonic depth sensor

## Model version

V5.2 (5 November 2026): energy-balance melt, ageing albedo, meltwater drains once the pack has warmed (5-day running
air temperature), wind-shifted snowfall onto lee slopes. New in V5.2: snow blown by the wind settles downwind over about
150 m instead of in the next cell, each wind step's change is smoothed over 3 x 3 cells (no snow lost or made), and
snowfall stops increasing with height 300 m above the weather's reference height (snow levels off near the crests).

## Data

NASA SnowEx and NIVAL airborne LiDAR (NSIDC DAAC), USDA NRCS SNOTEL, gridMET. This repository holds only the pages and
their data. MIT License (see LICENSE).
