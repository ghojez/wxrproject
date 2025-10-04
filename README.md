# WXR Project
![alt text](https://github.com/ghojez/wxrproject/blob/main/WXR.png?raw=true)
Historical weather data based on real Doppler radar depictions. The main goal of this project is to provide easy access to historical weather across many regions in ID. The radar generates precipitation images every 10 minutes, helping audiences understand how weather develops over time and how it correlates with business metrics

The workflow leverages Python, Pandas, and GitHub Actions to run on a scheduled basis (cron jobs), ensuring the data stays up to date without manual intervention

Radar Image: https://ghojez.github.io/wxrproject/index.html

## Features

- Cloudflare R2 Backbone
- Multi-station coverage
- Automated scheduling using GitHub Actions
- Data normalization to consistent 10-minute intervals
- HTML export for visualization
- Continuous updates committed back to the repository

---

## Data Flow

1. **Fetch Data**  
   Pulls raster files from the corresponding national agency API based on station codes.

2. **Normalize Time**  
   Adjusts timestamps to UTC+7 and aligns them with 10-minute intervals.

3. **Aggregate and Export**  
   Builds a combined HTML dashboard per station.

## Data Update Interval
Data will be updated daily. The availability of historical data depends on maximum storage and bandwidth limits

## Usage Permit
Access is limited to selected audiences. Please refrain from sharing or endorsing this tool outside the selected audiences defined by the project owner

---

[![Daily Update](https://github.com/ghojez/rainproject/actions/workflows/main.yml/badge.svg?branch=main)](https://github.com/ghojez/rainproject/actions/workflows/main.yml)


---

