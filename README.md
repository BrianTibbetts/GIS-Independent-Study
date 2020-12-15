# GIS-Independent-Study: Geographic data analysis using Jupyter Notebooks

## Software Design Notes

#### Data Design

Python's Pandas and Geopandas libraries are used to manage most of the data. Most of the data retrieved from each database is managed with Pandas dataframes.
Geopandas is used for GIS-specific data, including latitude and longitude points and any lines or polygons made up of connected points.
Matplotlib handles objects representing static maps, and Folium is used to create objects related to Leaflet.js interactive maps.

#### Architecture Design

Once the data for each project is available, it's transformed to meet the needs of the project.
Pandas and Geopandas functions are used to narrow down the data to relevant information.
Project 1 counts events by latitude and longitude and filters out data below the top 100 locations for events.
In project 2, the data is aggregated by a map of U.S. climate divisions defined by the NOAA.
Project 3 transforms several data sets, the most major example being that traffic data and population data are combined to form a per capita data set.
Project 4 uses Pandas to filter out unnecessary data and aggregate data by state.

Each project makes a final transformation to display the data as a map. Usually this is with a function of Matplotlib or Folium. For example, in projects 3 and 4, Folium's Circle function draws bubbles centered on latitude and longitude points.

#### Interface Design

Pandas functions are used to read in data from csv files in most cases.
Project 1 uses Google BigQuery to access data archived by GDELT without reading a specific file.
Kaggle's API is called in projects 2, 3, and 4 to download specific data sets relevant to those projects.

#### Procedural Design

Project 2 used Python's built in functions the most, with Math.sqrt to help calculate the z-score and a filename made using os.path.
The bubble maps in project 4 used a custom function made to pick colors.


## Links to Jupyter Notebooks pages:

- [Project 1: Tracking conflict related to the 2011 East African drought](https://nbviewer.jupyter.org/github/BrianTibbetts/Africa-GIS-Project/blob/master/Africa-GIS-Project/East-African-2011-Drought-Conflict.ipynb)

- [Project 2: A time series of NOAA Climate data focused on temperatures outside the norm](https://nbviewer.jupyter.org/github/BrianTibbetts/US-Climate-Time-Series/blob/main/US-Avg-Temp-Shift.ipynb)

- [Project 3: Analysis of traffic accidents in the UK](https://nbviewer.jupyter.org/github/BrianTibbetts/UK-Traffic-Accidents/blob/main/UK-Per-Capita-Traffic.ipynb)

- [Project 4: U.S. Greenhouse Gas Emissions by State in 2014](https://nbviewer.jupyter.org/github/BrianTibbetts/EPA-Air-Pollution/blob/main/EPA-Air-Pollution.ipynb)


## Data Sources
- [Google BigQuery GDELT Event data](https://cloud.google.com/bigquery)
- [Google BigQuery in-depth documentation for the GDELT data set](https://cloud.google.com/bigquery/docs/reference)

- [NOAA Climate At a Glance (CAG) data set by climate division](https://www.ncdc.noaa.gov/cag/divisional/mapping)

- [UK Road Safety data](https://www.kaggle.com/bluehorseshoe/uk-2016-road-safety-data)

- [EPA Air Pollution Monitoring data](https://www.kaggle.com/jaseibert/us-facilitylevel-air-pollution-20102014)


## Other Resources and Guides


#### Intro to GIS

- https://docs.qgis.org/3.10/en/docs/gentle_gis_introduction/index.html
- [A practice Jupyter Notebook page](https://nbviewer.jupyter.org/github/BrianTibbetts/Jupyter-Notebook-Test/blob/master/hello_world_binder.ipynb)

#### Kaggle guide on Geospatial Analysis

- https://www.kaggle.com/learn/geospatial-analysis

#### QGIS Training Manual

- https://docs.qgis.org/3.10/en/docs/training_manual/index.html

#### Python library documentation

- https://scitools.org.uk/cartopy/docs/latest/
- https://matplotlib.org/3.3.1/contents.html
- https://pandas.pydata.org/docs/
- https://python-visualization.github.io/folium/
