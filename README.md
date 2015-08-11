# Data Visualization Project - Nanodegree
by Saad Khan, [Data Analyst Nanodegree](https://www.udacity.com/course/nd002) Nov '14

## Project Deliverables

1. The original index.html file for the first version of your graphic **[Full Artice: index_final_V1.html | Html Code: index_final_V1.html]**
2. The final index.html file for the final version of your graphic **[index_final.html]**
3. The README.md file with the sections Summary, Design, Feedback, and Resources **[This file]**
4. The final data set file used for the graphic **[parkdata_final.tsv]** This file is in the Project6_ND/index_files/data/ location
5. A list of Web sites, books, forums, blog posts, github repositories, etc. that you referred to or used in creating your submission **[At the end of this README file in Resources section]**
6. Additional versions of your index.html as you iterated on your visualization based on feedback (index1.html, index2.html, index3.html, ... , index_final.html)

## Summary

The visualization illustrates annual visitor trend for the top 5 most visited National Parks in the US. The top 5 parks chosen for the visualization are based on National Geographic article [Top 10 Most Visited National Parks](http://travel.nationalgeographic.com/travel/national-parks/most-visited-parks-photos/) and the [National Park Service website](www.nps.gov). Data used to create the visualization was, taken for the past 20 years, from the National Parks website [National Park Service - Park Reports](https://irma.nps.gov/Stats/) and the focus was specifically on recreation visitors as they take the major percentage chunk of the total visitors, visiting a National Park.

## Design

### Goal

The initial goal before I started was to display the information either in some sort of bar, line or bubble charts. I started of by considering the top 10 parks and later on decided to stick with the top 5. Initial rough plot/sketch was using line charts in MS Excel so I decide to keep line chart as my mode of presentation.

### Initial Design Process

##### Data Collection/Extraction and Sketching

The raw data was extracted from the National Parks website for each of the parks - example: [Grand Canyon National Park](https://irma.nps.gov/Stats/SSRSReports/Park%20Specific%20Reports/Recreation%20Visitors%20By%20Month%20(1979%20-%20Last%20Calendar%20Year)?Park=GRCA). Some Park related information was included from wikipedia (such as Area, and States). Then basic MS Excel manipulation was performed to combine all the Top 10 Parks data into a tsv file.

Initial sketch of what I wanted to visualize was created in MS Excel, which is illustrated in the image below .![Initial DataVis Parks MSExcel](https://github.com/saadkhan321/Project6_ND/blob/master/images/Initial_DataVis_Parks_MSExcel.PNG)

### Initial Design Process

##### Struggles [Starting with D3.js]

For the actual visualization, I started off by creating a basic multiple-line chart in D3 using the example: [Multi-Series Line Chart](http://bl.ocks.org/mbostock/3884955). This initial plot as shown below had no interactive element along with overlapping labels. Data considered for this visualization was only taken for 10 years [2005 - 2014]. Code and data files for this particular visualization are in the index_files folder:

##### **[html file: index_initial_V1.html / data file: parkdata_initial_1.tsv]** 

![Initial DataVis Parks D3 v1](https://github.com/saadkhan321/Project6_ND/blob/master/images/Initial_DataVis_Parks_D3_v1.PNG)

Next, a slightly imporoved version of the chart was created where font for the charts was adjusted, y-axis values were displayed using appropriate axis customization according to [the link](http://curran.github.io/screencasts/introToD3/examples/viewer/#/103). Domain for y-axis was set at 0 to better visualize the visitation per park. Legend was added to the plot using [the link](http://bl.ocks.org/weiglemc/6185069). The image of the visualization is shown below. Code and data files for this improved version are in the index_files folder:

##### **[html file: index_initial_V2.html / data file: parkdata_initial_1.tsv]** 

![Initial DataVis Parks D3 v2](https://github.com/saadkhan321/Project6_ND/blob/master/images/Initial_DataVis_Parks_D3_v2.PNG)

### Intermediate Design Process

In order to add interaction/animation to the visualization I decided to switch to dimple.js and use its already built in features to enhance my visualization.

##### Initial Visualization with Interaction [ moving on to Dimple.js]

To create the visualization using dimple.js I gathered some additional information pertaining to the parks and created a more detailed version of the data file. This data file is in the index_files/data folder [parkdata_initial_2.tsv].

Using the newly created data file I created the initial visualization in dimple.js. Interactivity was added to the visualization in form of filtering the line charts on park basis. The code for this visualization is in the index_files folder:

##### **[html file: index_initial_V3.html / data file: parkdata_initial_2.tsv]** 

![Initial DataVis Parks Dimple v1](https://github.com/saadkhan321/Project6_ND/blob/master/images/Initial_DataVis_Parks_Dimple_v1.PNG)

##### Wider Visual Display

Little enhancement in the code helped in improving the visualization display, making it more wider. The code for this visualization is in the index_files folder:

##### **[html file: index_initial_V4.html / data file: parkdata_initial_2.tsv]** 

![Initial DataVis Parks Dimple v2](https://github.com/saadkhan321/Project6_ND/blob/master/images/Initial_DataVis_Parks_Dimple_v2.png)

##### Addition of Tooltip Animation

To enhance the data representation of the visualization, I added useful information such as park name, park area and monthly visitation (without axis labels) in the tooltips for each data point. The version of the code with enhancements in the visualization are in the index_files folder:

##### **[html file: index_initial_V5.html / data file: parkdata_initial_3.tsv]** 

![Initial DataVis Parks Dimple v3](https://github.com/saadkhan321/Project6_ND/blob/master/images/Initial_DataVis_Parks_Dimple_v3.png)

##### Enhancing the Tooltip [without feedback]

This version of the data visualization included enhanced interactivity of the charts and animation of the tooltip with detailed tooltip chart displaying monthly visitor information. Code for this version is also in the index_files folder **[html file: index6.html / data file: parkdata_final.tsv]** 

![Initial DataVis Parks Dimple Final](https://github.com/saadkhan321/Project6_ND/blob/master/images/Initial_DataVis_Parks_Dimple_v4.png)

##### Final Version 1 [without feedback]

The final version of the code was used as part of a narrative/story to show the comparison of the top most visited National Parks in the US. The html file pertaining to the full article and the associated data file are in the index_files folder. Following is the first iteration of the full article without any feedback. Subsequent version have the feedback incorporated **[html file: index_final_V1.html / data file: parkdata_final.tsv]**

bl.ocks code version 1 is at [this link](http://bl.ocks.org/saadkhan321/ffa7663330bb317bea19)

##### Final Version 2 [incorporating 1st feedback]

After the 1st feedback, an updated version of the data visualization was created and uploaded on to bl.ocks.org. The associated .html files are int he index_files folder **[html file: index_final_V2.html / data file: parkdata_final.tsv]**

The code version 2 for the visualization after 1st feedback is at [this link](http://bl.ocks.org/saadkhan321/3afb4229b42e81dfcace)

##### Final Version 3 [incorporating 2nd feedback]

Index_final_V3.html was generated which incorporated the 2nd feedback. The code was uploaded on to bl.ocks.org and associated .html files are uploaded are in the index_files folder **[html file: index_final_V3.html / data file: parkdata_final.tsv]**

Code version after the 2nd feedback for the visualization is at [this link](http://bl.ocks.org/saadkhan321/af2604432728503f60a7)



Article itself is at [this link](http://saadkhan321.github.io/)

Code view version is at [this link](http://bl.ocks.org/saadkhan321/4d8a10332f67f59cde6f)


## Feedback

**NO FEEDBACK RECEIVED**

## Resources

#### National Parks Information

National Geographic Article: http://travel.nationalgeographic.com/travel/national-parks/most-visited-parks-photos/

National Park Service website link 1: https://irma.nps.gov/Stats/Reports/National

National Park Service website link 2: https://irma.nps.gov/Stats/Reports/Park/

National Park Service website link 3: https://irma.nps.gov/Stats/Reports/Park/ACAD

National Park Service website link 4: https://irma.nps.gov/Stats/SSRSReports/Park%20Specific%20Reports/Recreation%20Visitors%20By%20Month%20(1979%20-%20Last%20Calendar%20Year)?Park=ACAD

Wikipedia Resource: https://en.wikipedia.org/wiki/List_of_national_parks_of_the_United_States

##### http://news.discovery.com/adventure/everything-you-need-to-know-about-national-parks.htm
##### http://www.nationalparkstraveler.com/parks/great-smoky-mountains-national-park/park-history-great-smoky-mountains
##### http://www.livescience.com/39515-yosemite-national-park-facts-information-lodging.html 
##### http://wikitravel.org/en/Rocky_Mountain_National_Park

#### Javascript, HTML, CSS, D3, Dimple.js

##### http://webdesign.about.com/od/html5tags/fl/div-vs-section.htm
##### http://bl.ocks.org/weiglemc/6185069
##### https://www.youtube.com/watch?v=8jvoTV54nXw
##### http://bl.ocks.org/weiglemc/6185069
##### http://bl.ocks.org/mbostock/9764126
##### http://stackoverflow.com/questions/8639383/how-do-i-center-an-svg-in-a-div
##### http://bost.ocks.org/mike/selection/
##### http://blog.fullstackacademy.com/post/100672562966/d3-js-in-10-minutes
##### http://bost.ocks.org/mike/nest/
##### https://robot.bolink.org/ebooks/Interactive%20Data%20Visualization%20For%20The%20Web.pdf
##### http://bl.ocks.org/mbostock/3883245
##### http://bl.ocks.org/mbostock/3884955
##### http://www.d3noob.org/2013/07/arranging-more-than-one-d3js-graph-on.html
##### http://115.28.34.34/wp-content/uploads/2015/01/d3cookbook.pdf
##### https://leanpub.com/D3-Tips-and-Tricks/read
##### http://dc-js.github.io/dc.js/
##### https://github.com/mbostock/d3/wiki/SVG-Shapes#line
##### http://stackoverflow.com/questions/15288850/font-size-is-not-working-in-my-d3-js-code
##### http://stackoverflow.com/questions/12057145/d3-js-axis-labels-color-not-changing
##### http://dimplejs.org/advanced_examples_viewer.html?id=advanced_interactive_legends
##### http://dimplejs.org/advanced_examples_viewer.html?id=advanced_trellis_bar
##### https://github.com/PMSI-AlignAlytics/dimple/wiki/dimple.chart#legends
##### https://github.com/PMSI-AlignAlytics/dimple/wiki/dimple.series
##### http://annapawlicka.com/pretty-charts-with-dimple-js/
##### https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toFixed
##### http://stackoverflow.com/questions/5012111/how-to-position-a-div-in-the-middle-of-the-screen-when-the-page-is-bigger-than-t
##### http://www.sitepoint.com/create-data-visualizations-javascript-dimple-d3/
##### http://www.w3.org/Style/Examples/007/center.en.html
##### http://www.w3schools.com/tags/tag_ol.asp
##### http://www.w3schools.com/cssref/playit.asp?filename=playcss_font-size&preval=xx-small
##### https://css-tricks.com/almanac/properties/b/background-image/
##### https://github.com/mbostock/d3/wiki/Time-Formatting
##### http://stackoverflow.com/questions/30945581/change-axis-color-dimple

## Data

Final .tsv file used for data visualization is \index_files\data\parkdata_final.tsv
