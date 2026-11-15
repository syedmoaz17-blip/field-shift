# Field Shift: Crop Rotation Planner

Team Indus Orbit (Syed Moaz Altaf, Sana Rasheed). NASA Space Apps Challenge 2026, Sahiwal, Pakistan.
Challenge: Field Shift: Adapting Farms with NASA Data.

Field Shift helps farmers choose which crops to grow over the next two years. It combines NASA POWER climate data for the farm's exact location with the farmer's soil, water and priorities, then ranks 20 crop plans for Punjab against what the farmer grows now.

- App: [index.html](index.html)
- Demo slides (7): [slides.html](slides.html), also as [PDF](FieldShift_Demo_Slides.pdf)

## How it works
1. Tap a field on the map. The app loads NASA POWER data for that point: temperature, rainfall, sunlight and root-zone moisture, plus monthly records from 2001 to 2024.
2. NASA sunlight and temperature give the daily water loss from a field (Hargreaves method). FAO-56 crop coefficients turn that into each crop's monthly water use, and NASA rainfall is subtracted to find the irrigation needed.
3. NASA temperatures are checked against each crop's heat-sensitive weeks.
4. Soil type, pH, salt and organic matter change how well each crop fits and how each plan affects soil health.
5. Five scores (water, soil, income, heat and drought, fodder) are weighted by the farmer's sliders to rank the plans.

## Run it
Open `index.html` in a browser. Nothing to install. Live NASA data needs an internet connection; without one, the app uses saved NASA data for Sahiwal.

## Data and credits
- NASA POWER Project, NASA Langley Research Center: https://power.larc.nasa.gov (MERRA-2, CERES).
- FAO Irrigation and Drainage Paper 56: crop coefficients.
- Leaflet and © OpenStreetMap contributors, Chart.js, Google Fonts.

## AI disclosure
The code for the app and the slides was written with help from an AI coding assistant (Claude, by Anthropic) and checked by the team. The team chose the problem, the approach and the crop plans. No AI-generated images, audio or video are used.

## Limits
Scores are planning estimates, not yield forecasts. Check varieties, sowing dates and fertilizer with your local agriculture extension office.
