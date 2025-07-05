# Fuzzy-Logic Early Warning System for Small-Scale Fisheries Using BMKG Marine Weather Forecasts

A web-based Decision Support System (DSS) that integrates **BMKG marine weather forecasts** with **rule-based** and **fuzzy-logic** risk assessments to provide clear, actionable safety advisories for **small-scale fisheries** in Indonesia.

---

## Overview

This project addresses the challenge of providing **interpretable, practical, and locally relevant marine weather safety guidance** to coastal and artisanal fishers. Tropical weather variability—strong winds, heavy rainfall, high waves—poses significant navigation risks, particularly for small-scale fishers who often lack structured early warning systems.

The system automatically **fetches BMKG forecast data** (including wind speeds, wave categories, rainfall descriptions, and official warnings) and evaluates maritime safety risk using:

- **Rule-based thresholds** aligned with BMKG advisories
- **Mamdani-style fuzzy logic** for nuanced, expert-like reasoning
- **Dual evaluation strategy** (expected conditions vs. worst-case wind scenarios)

---

## Features

-Real-time integration with **BMKG** marine weather forecast API  
-Rule-based risk assessment with explainable thresholds  
-Fuzzy-logic risk assessment with Mamdani inference and defuzzification  
-Dual evaluation: expected conditions (average wind) and caution (maximum wind)  
-User-friendly web interface with theme toggle  
-Official BMKG warning integration  
-Supports safer decision-making for small-scale fishers  

---

## Live Demo

[https://sl.unsrat.ac.id/fuzzy](https://sl.unsrat.ac.id/fuzzy)

> Try the full interactive system online!

---

## Data Source

This system uses public forecast data from the **BMKG Indonesia** Maritime Weather API:

- Official website: [https://peta-maritim.bmkg.go.id/public_api/perairan](https://peta-maritim.bmkg.go.id/public_api/perairan)

---

## How It Works

1. **Fetches BMKG JSON Forecast Data**  
   - Wind speed (min/max)
   - Wave category and description
   - Rainfall description
   - Official BMKG warnings

2. **Rule-Based Assessment**  
   - Assigns risk points per parameter
   - Sum of points mapped to Safe / Caution / Dangerous

3. **Fuzzy-Logic Assessment**  
   - Fuzzifies inputs (wind, wave, rainfall) using membership functions
   - Mamdani-style rule base to evaluate risk activations
   - Defuzzification to single risk score (0–1)
   - Categorizes as Safe / Caution / Dangerous

4. **Dual Evaluation Strategy**  
   - Expected Conditions: average wind speed
   - Worst-Case Scenario: maximum wind speed

5. **User Interface**  
   - Interactive selection of Indonesian maritime areas
   - Displays BMKG warnings, risk assessment results, and detail toggles

---

## Feel Free to Install on your own.

Clone this repo and serve the files locally:

```bash
git clone https://sl.unsrat.ac.id/fuzzy-repo
cd fuzzy-repo
