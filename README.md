# **Travel Time Predictions using Ubers and OSM in Kolkata**
This is my final project for IDCE 30274: Programming for GIS where I use a tutorial to predict travel times in my home town, Kolkata in India. 

I use aggreagted travel time data  for the first quarter from the first quarter of 2020 from the [Uber Movement](https://movement.uber.com/?lang=en-US).  


## Python pacakages used
- [Pandas](https://pandas.pydata.org/): To read the `.csv` file containing travel time data.
- [Geopandas](https://geopandas.org/): To read the `.json` file containing data on city boundaries. 
- [Shapely](https://pypi.org/project/Shapely/): To analyze city boundaries. 
- [Matplotlib](https://matplotlib.org/): To display city boundaries.


### To code along you will need:
- A Google account or a Python IDE. I use Colab, but this project uses a LOT of ram on your google drive, so it would be better to use a [Jupyter Notebook](https://jupyter.org/). 
- Travel time data and city boundaries from the city of your choice using [Uber Movement](https://movement.uber.com/?lang=en-US). The city boundary for Kolkata is avaialble 

# Getting started
Before we get to the data, let's briefly touch on reading and writing comma-separated data, or data from `.csv` files. Comma-separated values is a way of expressing structured data in flat text files like this:

```
"Refugee_Camp_Name","Country","Population2006","Population2014"
"Kakuma","Kenya","90457","153959"
"Hagadera","Kenya","59185","106968"
"Adjumani","Uganda","54051","96926"
"Dagahaley","Kenya","39526","88486"
"Zaatari","Jordan","0","84773"
```
This is a commonly used format to get data in and out of programs like spreadsheet software, where the data are tabular. [Python comes with a CSV module](https://docs.python.org/3/library/csv.html) that provides one way to easily work with CSV-delimited data: Try downloading the `Camp_stats.csv` file, wihch is previewed above and [can be accessed in the data folder](data/Camp_stats.csv), to your desktop or local working environment. Then run the following code in Colab to choose it as a file:
```python
# Upload local script to Colab here.
from google.colab import files
uploaded = files.upload()
```

