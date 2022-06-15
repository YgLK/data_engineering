# I03. Speed limit compliance in San Francisco

Here is our **Data Engineering** project.

We will work with the **[Speed limit compliance in San Francisco](https://data.sfgov.org/Public-Safety/San-Francisco-Speed-Limit-Compliance/mfjz-pnye)** dataset, we are going to analyze and process the data.

Explore the repo in the following order:

[ 2.1 Obtaining road data in San Francisco (OSMNX data set)](2.Data&#32;processing.ipynb#2.1_obtaining_road_data_in_san_francisco_(osmnx_data_set))

[ 2.2 Data cleaning and preparing for ML model (OSMNX data set)](2.Data&#32;processing.ipynb#2.2_data_cleaning_and_preparing_for_ML_model_(osmnx_data_set))

##### Example machine learning usage:

[3. Creating machine learning model](#3)  
- [3.1.1 Load dataset prepared previousl](#3_1_1)  
- [3.1.2 Split into training and testing sets](#3_1_2)  

[3.2 Scalling values](#3_2)  

[3.3 Building deep learning model model](#3_3)  
- [3.3.1 Finding the best parameters](#3_3_1)  

[3.4 Predictions for all streets in San Francisco](#3_4)  
- [3.4.1 Load all streets (saved previously)](#3_4_1)  
- [3.4.2 Scale - exactly like we did it before with training dataset](#3_4_2)  
- [3.4.3 Make prediction](#3_4_3)  

[4. Result visualisation by coloring map](#4)  
- [4.1 Precentage of cars moving too fast - Over_pct](#4_1)  
- [4.2 Precentage of cars exceeding speed limit more than 5 mph - O5mph_pct](#4_2)  
- [4.3 Average speed - Speed_avg](#4_3)  
- [4.4 Average speed ovet speed limit - SpeedO_avg](#4_4)  
- [4.5 Average speed of cars exceeding speed limit for more than 5 mph - Spd5O_avg](#4_5)  

You can install all needed libraries (and propably a few needless) using conda and [requirements file](requirements.txt)

Unfortunately we can't link to specific header inside jupyter file - this is a bug which has not been resolved for 5 years - [see the issue thread](https://gitlab.com/gitlab-org/gitlab/-/issues/18269)

Team members:
- Bartosz Sambór
- Jakub Szpunar
- Daniel Henel
