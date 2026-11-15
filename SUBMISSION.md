# Field Shift: text for the Space Apps Project page

Team: Indus Orbit. Local event: Sahiwal, Pakistan. Challenge: Field Shift: Adapting Farms with NASA Data.
Copy each section into the matching box on the Project page.

---

## Project Name
Field Shift: Crop Rotation Planner

## High-Level Project Summary
Field Shift is a free web tool that helps farmers decide which crops to grow over the next two years. The farmer taps their field on a map, and Field Shift loads NASA POWER climate data for that exact point: temperature, rainfall, sunlight and root-zone moisture. The farmer then adds their soil type, pH, salt level, organic matter and how much irrigation water they have, and says what matters most: saving water, healthier soil, income, safety from heat and drought, or fodder for animals.

Field Shift uses the NASA data to work out how much water each crop needs month by month and when heat could damage it. It then ranks 20 realistic two-year crop plans for Punjab against what the farmer grows now. For a typical loam field in Sahiwal, the best plans need 560 to 690 mm less irrigation a year than rice and wheat, and lift the soil-health score from 28 to over 70.

This matters because Punjab's groundwater is falling, Sahiwal gets only about 293 mm of rain in an average year, and most farmers grow the same two cereals every year on tired soil. Field Shift gives them a simple, data-based way to ask, "What if I rotate differently?"

## Link to Project Demo
https://syedmoaz17-blip.github.io/field-shift/slides.html

## Link to Final Project
https://syedmoaz17-blip.github.io/field-shift/

## Detailed Project Description

**What it does**

Field Shift answers one question for a farmer: which crop plan suits my field best? It works in three steps.

1. Your farm. Tap the map or pick a district. NASA climate data for that point loads in a few seconds.
2. Soil and water. Choose soil type, pH, salt, organic matter, irrigation water and tube-well quality, and say what you grow now.
3. What matters to you. Five sliders: save water, healthier soil, income, safety from heat and drought, and fodder for animals.

Field Shift then shows:
- The best plan for the field, with the water it saves and the change in soil health compared with what the farmer grows now.
- All plans ranked, each with five 0 to 100 scores and a 24-month crop calendar.
- Plain-language notes, such as free nitrogen from pulses (shown as bags of urea saved), heat warnings for sensitive crop stages, crops that don't suit the soil, and late sowing.
- A month-by-month water chart showing how much rain covers and how much must come from irrigation.
- The farm's climate from NASA: average rain, the driest and wettest years since 2001, the hottest month and root-zone moisture.
- A "hotter future" test that adds 1 °C or 2 °C to see which plans still hold up.

**How it works**

- Climate data: the app calls the NASA POWER API directly from the browser for the chosen point. It uses long-term monthly averages plus monthly records from 2001 to 2024.
- Water use: daily water loss from a green field (reference evapotranspiration, ET0) is calculated from NASA temperature and sunlight using the Hargreaves radiation method: ET0 = 0.0135 × (T + 17.8) × Rs / 2.45. Each crop's FAO-56 crop coefficient turns this into its monthly water use. Rain that crops can use (70% of NASA rainfall, up to the crop's need) is subtracted to get the irrigation needed. Rice also gets an allowance for water lost through puddled fields.
- Heat risk: NASA monthly temperatures are compared with the danger temperatures for each crop's sensitive weeks, for example wheat grain filling in March and April, cotton flowering in July and August, and potato planting in October and November.
- Soil fit: soil type, pH, salt and tube-well water quality change how well each crop is expected to grow.
- Soil health: pulses, berseem, green manure (sesbania), more crop variety and crop residues raise the score. Puddled rice, potato tillage and growing cereal after cereal lower it. Soils low in organic matter gain the most.
- Ranking: the five scores are combined using the farmer's own slider settings.
- If the NASA server can't be reached, the app uses saved NASA data for Sahiwal so it still works.

**Benefits**

- Saves water: 560 to 690 mm less irrigation a year compared with rice and wheat in our Sahiwal example. That is about 5,600 to 6,900 cubic metres per hectare.
- Builds soil and cuts fertilizer costs: pulses and clover add nitrogen, which saves about 1 to 1.5 bags of urea per hectare a year.
- Lowers climate risk by flagging heat-sensitive crop stages and testing plans against a hotter future.
- Helps dairy farmers: Sahiwal is home to the Sahiwal cattle breed, and plans like sorghum and berseem, then maize and oats, give green fodder all year.
- Free, with no login or install. Works on a phone and shows crop names in English and Urdu.

**What we hope to achieve**

We want to test Field Shift with agriculture extension officers and dairy farmers around Sahiwal. Next we plan to add NASA SMAP soil moisture and Landsat and MODIS images to detect each field's real crop history, an Urdu and Punjabi voice version for farmers who don't read, and market prices in the income score.

**Tools we used**

HTML, CSS and JavaScript (a single web page, no server needed). Leaflet with OpenStreetMap for the map, Chart.js for the charts, the NASA POWER API for climate data, FAO-56 crop coefficients, and GitHub Pages for hosting.

## Use of Super Intelligence (SI)
Yes. We used an AI coding assistant (Claude, by Anthropic) to write the HTML, CSS and JavaScript of the web app and the slide layout, and to help edit the English text of this submission. Our team chose the challenge and the approach, picked the crops and rotations that fit Punjab, and checked the farming assumptions. All climate data comes straight from NASA POWER. We used no AI-generated images, video or audio. The AI help is stated in the code comments, the page metadata, the app footer, the README and the last slide.

## NASA Data
- NASA POWER (Prediction Of Worldwide Energy Resources), NASA Langley Research Center, Agroclimatology community, via the API at https://power.larc.nasa.gov:
  - Climatology (long-term monthly averages): T2M (air temperature at 2 m), T2M_MAX (highest temperature), PRECTOTCORR (rainfall), ALLSKY_SFC_SW_DWN (sunlight reaching the ground, from CERES), RH2M (humidity) and GWETROOT (root-zone soil moisture, from MERRA-2).
  - Monthly data from 2001 to 2024: T2M and PRECTOTCORR, used for year-to-year rainfall and the driest and wettest years.
- These come from NASA's MERRA-2 model (GMAO) and the CERES radiation products.
- How we used them: temperature and sunlight give crop water use, rainfall gives the irrigation needed, temperature gives heat risk, and the 2001 to 2024 record shows how unreliable rain is.

## Space Agency Partner Data and Other References
- FAO Irrigation and Drainage Paper No. 56, "Crop Evapotranspiration" (Allen et al., 1998): crop coefficients and the Hargreaves method.
- Public crop calendars and crop guidance from the Punjab Agriculture Department and the Ayub Agricultural Research Institute, used as background.
- Leaflet 1.9.4 (BSD-2 licence) and OpenStreetMap map tiles (© OpenStreetMap contributors, ODbL).
- Chart.js 4.4.1 (MIT licence).
- Google Fonts: Bricolage Grotesque, Inter and Noto Nastaliq Urdu (SIL Open Font License).
- Photos from Unsplash, used under the free Unsplash License (free to use, credit given): mustard field by William Jones, cracked soil by Mike Erskine, canal through fields by Bernd Dittrich, farmer in a green field by Muhammad Sohail Arif Moeeni.
- The other screenshots in the slides are of our own app. We used no other copyrighted images.
- We did not use Space Agency Partner data in this version. We plan to add ESA Sentinel-2 images later.
