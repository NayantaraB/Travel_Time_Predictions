# **Travel Time Predictions using Ubers and OSM in Kolkata**
This is my final project for IDCE 30274: Programming for GIS where I use a tutorial to predict travel times in my home town, Kolkata in India. 

I use aggreagted travel time data  for the first quarter from the first quarter of 2020 from the [Uber Movement](https://movement.uber.com/?lang=en-US).  

### To complete this assignment you will need:
- A Google account or a Python IDE. I use Colab, but this project uses a LOT of ram on your google drive, so it would be better to use a [Jupyter Notebook] (https://jupyter.org/). 

### What you will submit:
A link to your Github repo. The repo must contain your Python code (either as script in `.py` or a notebook in `.ipynb` format). There are four code challenges here, so be sure your code is well documented and shows us how you are solving each challenge! The `README` of your repo should briefly summarize the project (in your own words) and contain an embdded image of your final output. You do not need to include the data files you downloaded (as I have here), but can if you like. If you're going to use this repo as part of your portfolio I suggest that you include a "data" section in your readme that explains what data you've used and links to the pages where it can be downloaded (in fact, you can just copy that text from this repo!).

## Why is this lab important?
Up to now, we've been learning about the basics of Python and have done work manipulating strings, lists, dictionaries, and have started importing files such as `.txt` files. In this lab, we're going to be working with multiple files in `.csv` format. Spreadsheets are, for better or worse, the _lingua franca_ of humanitarian and international development data. As [Sarah Telford of the UN's Humanitarian Data Exchange platform tells it](https://www.devex.com/news/opinion-humanitarian-world-is-full-of-data-myths-here-are-the-most-popular-91959), "Big data is promising, but the challenge in the humanitarian sector is bringing together small amounts of non-standardized data, mostly stored in spreadsheets, from dozens of organizations to create a common picture of needs and response."

The ability to find tabular (ie. spreadsheet) data; explore it; manipulate it; and analyze it is a critical skill. Not only that, but just being able to provide basic graphical representation of quantitative information (our histogram of flight distances) to help decision makers understand the basics of data, is important. Again, to cite the article above, "...cleaning and combing data and making choices about how data will be presented... is different than drawing conclusions from the data to understand why a crisis is deteriorating, or to decide whether to prioritize a cash response rather than food distribution. Data experts create the visuals; subject matter experts do the analysis." It's important to understand that, sometimes, your role as a GIS analyst may be to prepare and display data for decision makers or subject matter experts (and [there are a LOT of them](https://blog.veritythink.com/post/60157407408/these-are-the-humanitarian-decision-makers)) for them to interpret.  

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

