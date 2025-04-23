# The Incumbent's Shadow: Analyzing Strategic Positioning in the 2024 GOP Primary

![0000d10](https://github.com/user-attachments/assets/4a473db0-6ee1-4f44-9021-f0412545c278)

## Project Overview

This repository contains an analysis of campaign event data from the 2024 Republican primary season. The project investigates whether candidates strategically positioned themselves in relation to Donald Trump's campaign events using a novel "shadow zone" concept.

## Research Question

Did Republican primary candidates systematically avoid or deliberately follow Donald Trump on the campaign trail? 

The analysis examines if candidates were statistically more or less likely to appear in the same locations as Trump within a defined time window (3 days before/after).

## Data Source

The data comes from FiveThirtyEight's tracking of GOP candidate campaign visits throughout the 2024 primary season:
- 1,741 campaign events
- Tracking period: January 2023 through early March 2024
- Data includes: candidate name, date, location (city and state), and event type

Source: [FiveThirtyEight GitHub Repository](https://github.com/fivethirtyeight/data/tree/master/gop-candidate-visits-2024)

## Methodology

The analysis follows these steps:

1. **Define "Shadow Zone"**: Events occurring in the same state as a Trump event within ±3 days
2. **Create Shadow Zone Variable**: For each non-Trump event, determine if it falls in a shadow zone
3. **Statistical Analysis**: Chi-square test to determine if candidates' presence in shadow zones differs from random chance
4. **Examine Residuals**: Identify which candidates significantly avoided or followed Trump
5. **Additional Analysis**: Explore patterns by state, time period, and event type

## Key Files

- `incumbent_shadow_analysis.Rmd`: Main R Markdown file containing all analysis code
- `candidate_visits.csv`: FiveThirtyEight dataset of GOP campaign events
- `shadow_zone_functions.R`: Helper functions for shadow zone calculations
- `visualizations/`: Directory containing generated plots and charts

## Required Packages

```r
library(tidyverse)
library(lubridate)
library(ggplot2)
library(scales)
library(knitr)
library(DT)
```

## Key Findings

1. **Statistical Evidence**: Chi-square test (χ² = 45.229, df = 9, p-value < 0.001) confirms candidates' positioning relative to Trump was not random
2. **Candidate Strategies**:
   - "Avoiders": Chris Christie and Tim Scott showed statistically significant patterns of avoiding Trump
   - "Followers": Vivek Ramaswamy and Mike Pence exhibited patterns of appearing in Trump's shadow
3. **Temporal Patterns**: Events in Trump's shadow increased dramatically as the Iowa caucuses approached (87% in January 2024)
4. **Geographic Patterns**: Early primary states showed different patterns (Iowa: 62.5% in shadow; New Hampshire: 25.8%)
5. **Event Types**: Different campaign activities showed varying likelihood of occurring in Trump's shadow

## How to Run

1. Clone this repository
2. Open `incumbent_shadow_analysis.Rmd` in RStudio
3. Install required packages if needed
4. Run all chunks to reproduce the analysis

## Visualization Highlights

The repository includes several key visualizations:

1. Shadow Zone Percentages by Candidate
2. Shadow Zone Events Over Time
3. Chi-Square Residuals Visualization
4. State-Level Shadow Analysis
5. Event Type Analysis
![0000f10](https://github.com/user-attachments/assets/feccafc3-be5b-42d2-8afc-a2fb6938a06c)
![000012](https://github.com/user-attachments/assets/dba821c6-c35f-44eb-9772-761ad82a334d)
![000010](https://github.com/user-attachments/assets/a3e25590-894e-4575-be50-ac599e87048f)

## Limitations

- Definition of "shadow zone" is somewhat arbitrary (±3 days, state-level)
- Analysis establishes correlation but not causation
- Does not account for other factors that might influence scheduling (e.g., external events)
- Limited to publicly available event data

## Future Work

- Test different shadow zone definitions (city-level, different time windows)
- Incorporate polling data to examine relationship between shadow behavior and performance
- Apply methodology to previous primary contests for comparison
- Develop real-time tracking of shadow zone behavior for future primaries

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- FiveThirtyEight for collecting and providing the campaign event data
- R community for developing the tools that made this analysis possible

## Author

Emmanuel Olimi Kasigazi

## Contact

https://www.linkedin.com/in/olimiemma/ 

![Evemt shadow](https://github.com/user-attachments/assets/349346c2-068d-450d-80bd-59b57671e44c)
![state shadow](https://github.com/user-attachments/assets/6883cc61-4af8-48ca-af17-0b24e0690adc)
![Chi residuals](https://github.com/user-attachments/assets/ab446803-e93f-44f6-bf1d-06570207b295)
![chi test](https://github.com/user-attachments/assets/0fbba983-d2ee-4728-b87b-f4375853e62d)
![monthly shadow](https://github.com/user-attachments/assets/bb66ff9e-5073-454f-b5d2-d1606d5d3b6e)
![shadow summary](https://github.com/user-attachments/assets/7074b124-f845-4cf6-97d1-28680371da33)


