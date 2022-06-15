# I03. Speed limit compliance in San Francisco

Here is our **Data Engineering** project.

We will work with the **[Speed limit compliance in San Francisco](https://data.sfgov.org/Public-Safety/San-Francisco-Speed-Limit-Compliance/mfjz-pnye)** dataset, we are going to analyze and process the data.

Explore the repo in the following order:

You can install all needed libraries (and propably a few needless) using conda and [requirements file](requirements.txt)

Unfortunately we can't link to specific header inside jupyter file - this is a bug which has not been resolved for 5 years - [see the issue thread](https://gitlab.com/gitlab-org/gitlab/-/issues/18269)

Explore the repo in the following order:

[1.1 Load data from csv file](1.Data_exploration.ipynb#1.1-Load-data-from-csv-file) 

[1.2 Use `Shapely` to visualise LineStrings from `the_geom` column](1.Data_exploration.ipynb#1.2-Use-Shapely-to-visualise-LineStrings-from-the_geom-column)

[1.3 Visualize all values from the_geom column on one plot](1.Data_exploration.ipynb#1.3-Visualize-all-values-from-the_geom-column-on-one-plot)

[1.4 Create geometry column by loading LineStrings from the_geom column as Shapely objects](1.Data_exploration.ipynb#1.4-Create-geometry-column-by-loading-LineStrings-from-the_geom-column-as-Shapely-objects)
- [1.4.1 Plot the results](1.Data_exploration.ipynb#1.4.1-Plot-the-results)

[1.5 With the use of `osmnx` create visualisation of San Francisco](1.Data_exploration.ipynb#1.5-With-the-use-of-osmnx-create-visualisation-of-San-Francisco)
- [1.5.1 Load graph of the city fom `osmnx`](1.Data_exploration.ipynb#1.5.1-Load-graph-of-the-city-fom-osmnx)
- [1.5.2 Show city visualisation with the use of  `ox` graph](1.Data_exploration.ipynb#1.5.2-Show-city-visualisation-with-the-use-of--ox-graph)

[1.6 Retrieve nodes and edges from San Francisco graph](1.Data_exploration.ipynb#1.6-Retrieve-nodes-and-edges-from-San-Francisco-graph)
- [1.6.1 Visualize all nodes on the map](1.Data_exploration.ipynb#1.6.1-Visualize-all-nodes-on-the-map)
- [1.6.2 Analyse edges information](1.Data_exploration.ipynb#1.6.2-Analyse-edges-information)
- [1.6.3 Visualize San Francisco streets](1.Data_exploration.ipynb#1.6.3-Visualize-San-Francisco-streets)

[1.7 Plot `Speed limit compliance in San Francisco` data on San Francisco map](1.Data_exploration.ipynb#1.7-Plot-Speed-limit-compliance-in-San-Francisco-data-on-San-Francisco-map)

[1.8 Find a way to join edges with the `Speed limit compliance in SF` dataset](1.Data_exploration.ipynb#1.8-Find-a-way-to-join-edges-with-the-Speed-limit-compliance-in-SF-dataset)
- [1.8.1 Quick glimpse on the geometrical data](1.Data_exploration.ipynb#1.8.1-Quick-glimpse-on-the-geometrical-data)
- [1.8.2 Try to join speed limit compliance data with the edges data by performing spatial join](1.Data_exploration.ipynb#1.8.2-Try-to-join-speed-limit-compliance-data-with-the-edges-data-by-performing-spatial-join.)
- [1.8.3 Show joined data on the plot](1.Data_exploration.ipynb#1.8.3-Show-joined-data-on-the-plot.)

[1.9 Join osmnx edges with Speed compliance data by the street column](1.Data_exploration.ipynb#1.9-Join-osmnx-edges-with-Speed-compliance-data-by-the-street-column.)

[1.10 Next approach to data joining](1.Data_exploration.ipynb#1.10-Next-approach-to-data-joining)
- [1.10.1 Join attempt result](1.Data_exploration.ipynb#1.10.1-Join-attempt-result)

[1.11 Join data by name of the street](1.Data_exploration.ipynb#1.11-Join-data-by-name-of-the-street)
- [1.11.1 Further data matching](1.Data_exploration.ipynb#1.11.1-Further-data-matching)
- [1.11.2 Plot the result of joining by the streetname](1.Data_exploration.ipynb#1.11.2-Plot-the-result-of-joining-by-the-streetname)


[2.1 Obtaining road data in San Francisco (OSMNX data set)](2.Data processing.ipynb#2_1) 

[2.2 Data cleaning and preparing for ML model (OSMNX data set)](2.Data processing.ipynb#2_2) 
- [2.2.1 dropping unnecessary columns](2.Data processing.ipynb#2_2_1)
- [2.2.2 improving "maxspeed" column](2.Data processing.ipynb#2_2_2)
- [2.2.3 improving "oneway" column](2.Data processing.ipynb#2_2_3)
- [2.2.4 improving "lanes" column](2.Data processing.ipynb#2_2_4)
- [2.2.5 improving "highway" column](2.Data processing.ipynb#2_2_5)
- [2.2.5 improving "name" column](2.Data processing.ipynb#2_2_6)
- [2.2.6 summary](2.Data processing.ipynb#2_2_7)

[2.3 Obtaining speed limit data in San Francisco (SanFranciscoSpeedLimitCompliance data set)](2.Data processing.ipynb#2_3)

[2.4 Data cleaning and preparing for ML model (SanFranciscoSpeedLimitCompliance data set)](2.Data processing.ipynb#2_4)
- [2.4.1 Dropping unnecessary column](2.Data processing.ipynb#2_4_1)
- [2.4.2 improving "speedlimit" column](2.Data processing.ipynb#2_4_2)
- [2.4.2 improving "the_geom" column](2.Data processing.ipynb#2_4_3)

[2.5 Merging datasets](2.Data processing.ipynb#2_5)

[2.6 Preparing merged data for Machine Learning Model](2.Data processing.ipynb#2_6)
- [2.6.1 Data set for machine learning](2.Data processing.ipynb#2_6_1)
- [2.6.2 Data set for predictions](2.Data processing.ipynb#2_6_2)


##### Example machine learning usage:

[3. Creating machine learning model](3.Machine learning.ipynb#3)  
- [3.1.1 Load dataset prepared previousl](3.Machine learning.ipynb#3_1_1)  
- [3.1.2 Split into training and testing sets](3.Machine learning.ipynb#3_1_2)  

[3.2 Scalling values](3.Machine learning.ipynb#3_2)  

[3.3 Building deep learning model model](3.Machine learning.ipynb#3_3)  
- [3.3.1 Finding the best parameters](3.Machine learning.ipynb#3_3_1)  

[3.4 Predictions for all streets in San Francisco](3.Machine learning.ipynb#3_4)  
- [3.4.1 Load all streets (saved previously)](3.Machine learning.ipynb#3_4_1)  
- [3.4.2 Scale - exactly like we did it before with training dataset](3.Machine learning.ipynb#3_4_2)  
- [3.4.3 Make prediction](3.Machine learning.ipynb#3_4_3)  

[4. Result visualisation by coloring map](3.Machine learning.ipynb#4)  
- [4.1 Precentage of cars moving too fast - Over_pct](3.Machine learning.ipynb#4_1)  
- [4.2 Precentage of cars exceeding speed limit more than 5 mph - O5mph_pct](3.Machine learning.ipynb#4_2)  
- [4.3 Average speed - Speed_avg](3.Machine learning.ipynb#4_3)  
- [4.4 Average speed ovet speed limit - SpeedO_avg](3.Machine learning.ipynb#4_4)  
- [4.5 Average speed of cars exceeding speed limit for more than 5 mph - Spd5O_avg](3.Machine learning.ipynb#4_5)  

You can install all needed libraries (and propably a few needless) using conda and [requirements file](requirements.txt)

Team members:
- Bartosz Sambór
- Jakub Szpunar
- Daniel Henel
