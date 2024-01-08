# SeattleCrimeAnalysis

This report presents a comprehensive analysis of crime distribution and trends in the city of Seattle for the years 2008 to 2022, emphasizing year 2022 to understand the present crime dynamics in Seattle, by utilizing a robust dataset obtained from the Seattle Police Department. The dataset is a rich amalgamation of information, detailing the types of offenses, the locations where they occurred, the times at which they took place, and other critical variables that give a multi-dimensional view of criminal activity within the city.

The objective of this analysis is to derive meaningful insights that can aid in the enhancement of public safety and the optimization of law enforcement resources. By dissecting the datasets, we aim to identify patterns in the prevalence of various types of crimes in multi-level areas, pinpoint neighborhoods that are disproportionately affected by criminal activities as well as the localization of crime.

Our approach involves a granular examination of the data to reveal the intricate dynamics of crime in Seattle. The spatial distribution that may suggest geographically concentrated pockets of high criminal activity that provide an understanding of the city's crime landscape.

As we proceed, we will explore the methodology behind our analysis, present our findings in a series of visualizations and narratives, and conclude with recommendations based on our study. This report is not the culmination but a continuous effort towards understanding and reducing crime in Seattle.


## Table of Contents
- [Table of Contents](#table-of-contents)
- [Requirements](#requirements)
- [Dataset](#dataset)
- [References](#references)
- [Authors](#authors)


## Requirements
[(Back to top)](#table-of-contents)  
Make sure you have the following Python libraries installed:

```bash
pip install pandas altair
```

## Dataset
[(Back to top)](#table-of-contents)  
About Dataset
The analysis utilizes crime data sourced from the Seattle Police Department spanning the years 2008 to 2022, available at https://data.seattle.gov/Public-Safety/SPD-Crime-Data-2008-Present/tazs-3rd5. The dataset encompasses a comprehensive array of information crucial for understanding and analyzing criminal activities. Each crime report is uniquely identified by a Report Number, facilitating tracking and reference, while the Offense ID serves as an added unique identifier for individual offenses. The temporal aspects of the offenses are detailed through Offense Start date and end date, providing insights into the duration of events. 

The dataset obtained from SPD contained longitude and latitude coordinates which doesn’t provide any higher level meaning in terms of geographic crime pattern. These coordinates were transformed into Geometry point objects, then employing a spatial join technique, each point was linked to its respective Census Block using Seattle's 2020 Census Block geometry data.  Leveraging the hierarchical structure of Census Blocks and Tracts within larger areas, the data was further contextualized within Community Reporting Areas (CRAs) in Seattle. CRAs, resembling neighborhood and neighborhood districts, provide a localized community-level perspective, aligning with familiar terminology for Seattle residents. Additionally, Seattle's neighborhoods and neighborhood districts are aligned with census tracts borders, ensuring a non-overlapping dataset for accuracy. Subsequently, a merger with "Selected Demographic and Housing Estimates (DP05)" data for the 2020 population was executed, contributing to a more nuanced analysis of normalization by population or by areas. This integrated approach offers valuable insights into the interplay between crime patterns and demographic factors, enhancing the overall understanding of the socio-economic landscape.

The rationale behind aggregating points into larger areas is twofold: it provides a summarized view of crime patterns in multi-level while retaining the localization of incidents. Additionally, employing familiar terms caters to the understanding and engagement of our Seattle audience. 


## References:
[(Back to top)](#table-of-contents)  
Seattle Police Department Crime Data: https://data.seattle.gov/Public-Safety/SPD-Crime-Data-2008-Present/tazs-3rd5  
Seattle Geographic Data: https://data-seattlecitygis.opendata.arcgis.com/datasets/SeattleCityGIS::selected-demographic-and-housing-estimates-dp05/explore  
Seattle GIS: https://data-seattlecitygis.opendata.arcgis.com/datasets/SeattleCityGIS::community-reporting-areas-3/about  
Seattle Census Dataset: https://data.seattle.gov/dataset/2020-Census-Blocks-Seattle/rg9f-z788/data  


## Authors
[(Back to top)](#table-of-contents)

- [@Kewal Tadas ]
    [![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kewaltadas/)
