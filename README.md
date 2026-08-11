## Subnational Vulnerability and Multidimensional Poverty in Kenya: Mapping County-Level Inequality.

---

## Project Description.
National averages often mask regional inequalities. While Kenya has made progress in overall economic growth and energy expansion, access to essential public goods such as safe drinking water, grid electricity and basic education remains unevenly distributed across its 47 counties.
This project evaluates subnational infrastructure deprivations using official statistics from the Kenya National Bureau of Statistics (KNBS) paired with geographic boundary datasets from Humanitarian Data Exchange (HDX). By combining Pandas, NumPy, Seaborn, GeoPandas, and Matplotlib. This analysis constructs a normalized Composite Basic Needs Index (CBNI) to identify spatial clusters of infrastructure vulnerability and evaluate relationships between household utilities and educational outcomes. 

---

## Project Objectives.
Evaluating poverty through income metrics alone fails to capture non-monetary deprivations. This project focuses on a simple but critical idea that poverty is more than just a lack of money. Looking at income only makes people miss the full picture while factors such as clean drinking water, no electricity, no schools for children and poor sanitation are still indicators of poverty. This is called Multidimensional Poverty-looking at multiple dimensions of a person's life at the same time-because a household might fall above the monetary poverty line yet lack clean water, sanitation, electricity, or access to schooling.

Key Project Goal:
> - Provide actionable insights by delivering clear, evidence-based recommendations that pinpoint which specific counties require priority resource allocation for basic infrastructure.

--- 

## Research Questions
Primary research question - How do basic infrastructure deprivations (access to clean water, electricity and education) vary geographically across Kenya's 47 counties and which region exhibits the highest composite vulnerability?!

Secondary Research questions:-

A. County Rankings and Mapping (GeoPandas and Matplotlib)
> - 1. Which counties fall into the highest and lowest quintiles of basic needs deprivation across Kenya?! (Answered by creating a top/bottom 10 ranking table and a color-coded 47-county map).

>   3. Are there distinct regional or spatial clusters (e.g., Northern/Arid counties vs. Central/Urban counties) where basic needs deprivations are consistently low?!   (Answered by observing regional patterns on the map, such as Northern/Arid counties vs. Urban/Central counties).

[-] B. Infrastructure Relationships (Seaborn)
> - 3. How strongly correlated is electricity access with clean drinking water availability across Kenya's counties?!  (Answered using a correlation heatmap and scatter plot).

>   5. Is there a significant relationship between household infrastructure access (water/power) and education completion rates at the county level?! (Answered using regression trendlines to see if lack of home utilities connects to lower school completion).

[-] C. Multi-Metric vs. Single-Metric Comparison (NumPy and Pandas)
> - 5. How does ranking counties using a multidimensional composite index like combining water, power and education differ from ranking them using single metric alone like electricity access only?!
(Answered by comparing rank differences between single-indicator lists and the combined index).

>   7. Which specific basic needs indicator contributes the highest weight to overall county vulnerability in the top 10 most deprived counties?!

---

## Tech Stack and Libraries.
> - Pandas: Merging county datasets and cleaning strings.
> - NumPy: Normalizing metrics to build the index.
> - Seaborn: Plotting correlations and distribution curves.
> - GeoPandas: Creating county choropleth maps.
> - Matplotlib: Arranging the final multi-chart dashboard.

---

## Dataset Sources.
> - Kenya National Bureau of Standards (2019 Kenya Population and Housing Census Volume IV: Distribution of Population by Socio-Economic Characteristics). 
> - HDX Kenya Boundaries Dataset - for geospatial boundaries.

---

## Key Methodology and Pipeline.
> - Data Cleaning - gathering county data from Kenya National Bureau of Statistics and using Pandas to clean up messy county names, fill in numbers and organize stats on water, electricity, sanitation and education for all 47 counties. 
> - Composite Index Normalization - using NumPy to combine water access, electricity, sanitation and education into one clear score (eg., from 0.0 for low poverty to 1.0 for extreme poverty).
> - Exploratory Data Analysis - using seaborn charts to answer key research questions.
> - Choropleth Mapping and Spatial Analysis- using GeoPandas and Matplotlib to attach pandas calculations with geographic shapefiles to create an easy to read, color-coded map of Kenya.
