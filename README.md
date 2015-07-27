# Data Visualization: Top 10 U.S. National Parks Visitation, 1995-2014
by Saad Khan, Data Analyst Nanodegree Nov '14 [Data Analyst Nanodegree](https://www.udacity.com/course/nd002)

## Summary

The intent was to analyze the distribution of visitors visiting the top 10 most visited National Parks in the US during the last 20 years. The data visualization displays comparison of the most visited National Parks in the US. The top 10 parks chosen for the visualization are based on National Geographic article [Top 10 Most Visited National Parks](http://travel.nationalgeographic.com/travel/national-parks/most-visited-parks-photos/). Data used to create the visualization was taken from the National Parks website [National Park Service - Park Reports] (https://irma.nps.gov/Stats/Reports/Park/).

## Design

### Initial Design Process - Data Collection/Extraction

The raw data was extracted from the National Parks website for each of the parks - example: [Acadia National Park](https://irma.nps.gov/Stats/SSRSReports/Park%20Specific%20Reports/Recreation%20Visitors%20By%20Month%20(1979%20-%20Last%20Calendar%20Year)?Park=ACAD). Some Park related information was included from wikipedia (such as Area, and States). After that basic MS Excel manipulation was performed to combine all the Top 10 Parks data into a tsv file.

Initial sketch of what I wanted to visualize was created in MS Excel, which is illustrated in the image below [Initial DataVis Parks MSExcel].

### Initial Design Process - Struggles

I started off by creating a basic multiple-line chart in D3 using the example: [Multi-Series Line Chart](http://bl.ocks.org/mbostock/3884955). This initial plot as shown below had no interactive element and also had improper/chopped off labels and was only plotted using visitation data for 10 years [2005 - 2014] [html file: index1.html / data file: parkdata_initial_1.tsv] [Initial DataVis Parks D3].

Next version of the chart was created in which, font for the charts was adjusted, y-axis values were displayed using appropriate axis customization according to [the link](http://curran.github.io/screencasts/introToD3/examples/viewer/#/103). Domain for y-axis was set at 0 to better visualize the visitation per park. Legend was added to the plot using [the link](http://bl.ocks.org/weiglemc/6185069). The image of the visualization is shown below [html file: index2.html / data file: parkdata_initial_1.tsv]


## Feedback

## Resources
