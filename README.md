# Project: AgroRadar

**Voice-first, evidence-backed crop rotation advice for Bangladeshi farmers, powered by NASA Earth observation data.**

Team **AstroAlgo** | NASA Space Apps Challenge 2026 | Challenge: *Field Shift: Adapting Farms with NASA Data*

---

## Problem

Bangladeshi farmers face early flash floods in the Haor basin, drought in the Barind Tract, and salinity along the coast. The rainy season has also shifted, so the planting calendar passed down from their parents no longer matches the weather.

Most existing tools do not help enough:
- Forecasts are written for experts, not for farmers who cannot read them.
- Many apps give a whole district the same advice.
- They show an answer but not the evidence behind it.
- They pick one crop and ignore rotation and soil health.

One wrong planting decision can cost a family a whole year of income.

## Our solution

**AgroRadar** turns NASA satellite data into one clear decision: **"What should I plant next on my own field, and why?"**

1. **Pin your field.** The farmer drags a pin onto his own land on a satellite map. No typing.
2. **See how your season has moved.** NASA rainfall records show how many days the rains now arrive earlier or later than before.
3. **Get three rotation options.** Each is shown in pictures with expected yield, risk level and soil-health benefit (for example lentil, mustard, mung bean), and can be spoken aloud in Bangla.
4. **Read the receipt.** A "Why" screen shows: satellite signal, then field condition, then recommendation.
5. **Check the history.** The app shows the past year this season most resembles and what worked then.

AgroRadar does **not** claim to forecast daily weather months ahead. It says "risk is elevated" and backs its advice with real past years.

## NASA data

| Dataset | Use |
|---|---|
| NASA POWER | 20+ years of rainfall and temperature, used to measure the season shift and compute anomalies |
| SMAP | Soil moisture, used as a field-condition signal |
| GPM IMERG | Finer rainfall data, including upstream rain that drives Haor flash floods |

**How we use it:** we pull daily data for the pinned location, build a long-term climatology, compare the current season with it, match it to the closest past years, rank rotations with crop rules, and explain the result in simple spoken Bangla.

NASA POWER is gridded at about 50 km, so nearby districts can share a cell. We cross-check with finer layers (SMAP, IMERG) and state this limit openly.

## What makes it stand out

- **Rotation-first**, not just a single crop pick
- **Evidence, not a black box:** real NASA records and real past years
- **Honest uncertainty:** no fake exact dates
- **A "receipt" for every answer,** so farmers can question it
- **Built for farmers who cannot read:** voice, icons and Bangla on every screen
- **Field-level advice,** not district-level
- **Upstream-aware flood risk** for the Haor

## The six screens

1. Opening page: asks "Where is your land?"
2. Select field: satellite map with a draggable pin
3. Shifting details: old vs. current season
4. Three rotations: options with yield, risk and soil benefit
5. Why: the reasoning behind each recommendation
6. History: the closest-matching past year

## Current status

- **Built:** The full six-screen Bangla UI/UX prototype and user flow on [Figma](https://www.figma.com/design/8rgrDhdDOjZLYgbe6G9ZlS/Field-Shift-%25E2%2580%2594-NASA-Space-Apps-2026?node-id=1-6&p=f&t=SF2SnhCz8i6DdUFb-0).
- **Illustrative data:** numbers shown in the prototype, such as the 11-day shift and the matching year, are **placeholders**, not final results from NASA data.
- **Next:** real NASA data analysis, the rotation rules engine, and a historical backtest.

## Roadmap

- Replace placeholder values with real NASA-derived results
- Backtest against past floods and droughts, reporting hits and false alarms honestly
- Flood and drought risk alerts
- Finer-resolution data to reduce the 50 km grid problem
- Offline mode and a full Bangla voice interface
- Pilot with farmers and agricultural extension officers


## Team AstroAlgo

| Name | Role |
|---|---|
| Md. Mahabubar Rahman | Management and Communication Lead |
| Mehedi Hasan Moon | AI/ML and Backend Lead |
| Maisha | UI/UX and Frontend Lead |
| Nahul Vaia | AI/ML Researcher and Presentation Lead |
| Zunayed Rahman | AI/ML Dataset Collector |
| Asikur Rahman Rohan | AI/ML Research Assistant |

## Data credits

- NASA POWER: https://power.larc.nasa.gov/
- SMAP: https://smap.jpl.nasa.gov/
- GPM IMERG: https://gpm.nasa.gov/data/imerg

---
