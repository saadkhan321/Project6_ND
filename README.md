# Data Visualization Project - Nanodegree
by Saad Khan, [Data Analyst Nanodegree](https://www.udacity.com/course/nd002) Nov '14

## Project Deliverables

1. The original index.html file for the first version of your graphic **[index_initial_V1.html]**
2. The final index.html file for the final version of your graphic **[index.html]**
3. The README.md file with the sections Summary, Design, Feedback, and Resources **[This file]**
4. The final data set file used for the graphic **[parkdata_final.tsv]** This file is in the Project6_ND/index_files/data/ location
5. A list of Web sites, books, forums, blog posts, github repositories, etc. that you referred to or used in creating your submission **[At the end of this README file in Resources section]**
6. Additional versions of your index.html as you iterated on your visualization based on feedback (index1.html, index2.html, index3.html, ... , index_final.html) **[all files included in the index_files folder]**

## Summary

The visualization illustrates annual visitor comparison for the top 5 most visited National Parks in the US. The top 5 parks chosen for the visualization are based on National Geographic article [Top 10 Most Visited National Parks](http://travel.nationalgeographic.com/travel/national-parks/most-visited-parks-photos/) and the [National Park Service website](www.nps.gov). Data used to create the visualization was, taken for the past 20 years, from the National Parks website [National Park Service - Park Reports](https://irma.nps.gov/Stats/) and the focus was specifically on recreation visitors as they take the major percentage chunk of the total visitors, visiting a National Park.

## Design

### Goal

The initial goal before I started was to display the information either in some sort of bar, line or bubble charts. I started of by considering the top 10 parks and later on decided to stick with the top 5. Initial rough plot/sketch was using line charts in MS Excel so I decide to keep line chart as my mode of presentation.

### Initial Design Process

##### Data Collection/Extraction and Sketching

The raw data was extracted from the National Parks website for each of the parks - example: [Grand Canyon National Park](https://irma.nps.gov/Stats/SSRSReports/Park%20Specific%20Reports/Recreation%20Visitors%20By%20Month%20(1979%20-%20Last%20Calendar%20Year)?Park=GRCA). Some Park related information was included from wikipedia (such as Area, and States). Then basic MS Excel manipulation was performed to combine all the Top 10 Parks data into a tsv file.

Initial sketch of what I wanted to visualize was created in MS Excel, which is illustrated in the image below .![Initial DataVis Parks MSExcel](https://github.com/saadkhan321/Project6_ND/blob/master/images/Initial_DataVis_Parks_MSExcel.PNG)

### Initial Design Process [Starting with D3.js]

##### Struggles 

For the actual visualization, I started off by creating a basic multiple-line chart in D3 using the example: [Multi-Series Line Chart](http://bl.ocks.org/mbostock/3884955). This initial plot as shown below had no interactive element and also had overlapping labels. Data considered for this visualization was only taken for 10 years [2005 - 2014]. Code and data files for this particular visualization are in the index_files folder:

###### **[html file: index_initial_V1.html / data file: parkdata_initial_V1.tsv]** 

![Initial DataVis Parks D3 v1](https://github.com/saadkhan321/Project6_ND/blob/master/images/Initial_DataVis_Parks_D3_v1.PNG)

Next, a slightly improved version of the chart was created where font for the charts was adjusted, y-axis values were displayed using appropriate axis customization according to [the link](http://curran.github.io/screencasts/introToD3/examples/viewer/#/103). Domain for y-axis was set at 0 to better visualize the visitation per park. Legend was added to the plot using [the link](http://bl.ocks.org/weiglemc/6185069). The image of the visualization is shown below. Code and data files for this improved version are in the index_files folder:

###### **[html file: index_initial_V2.html / data file: parkdata_initial_V1.tsv]** 

![Initial DataVis Parks D3 v2](https://github.com/saadkhan321/Project6_ND/blob/master/images/Initial_DataVis_Parks_D3_v2.PNG)

### Initial Design Process [moving on to Dimple.js]

In order to add interaction/animation to the visualization I decided to switch to dimple.js and use its already built in features to enhance my visualization.

##### Initial Visualization with Interaction 

To create the visualization using dimple.js, I gathered some additional information pertaining to the parks and created a more detailed version of the data file. This data file is in the index_files/data folder [parkdata_initial_2.tsv].

Using the newly created data file I created the initial visualization in dimple.js. Interactivity was added to the visualization in form of filtering the line charts on park basis. The code for this visualization is in the index_files folder:

###### **[html file: index_initial_V3.html / data file: parkdata_initial_V2.tsv]** 

![Initial DataVis Parks Dimple v1](https://github.com/saadkhan321/Project6_ND/blob/master/images/Initial_DataVis_Parks_Dimple_v1.PNG)

##### Wider Visual Display

Little enhancement in the code helped in improving the visualization display, making it more wider. The code for this visualization is in the index_files folder:

###### **[html file: index_initial_V4.html / data file: parkdata_initial_V2.tsv]** 

![Initial DataVis Parks Dimple v2](https://github.com/saadkhan321/Project6_ND/blob/master/images/Initial_DataVis_Parks_Dimple_v2.png)

##### Addition of Tooltip Animation

To enhance the data representation of the visualization, I added useful information such as park name, park area and monthly visitation (without axis labels) in the tooltips for each data point. The version of the code with enhancements in the visualization are in the index_files folder:

###### **[html file: index_initial_V5.html / data file: parkdata_initial_V3.tsv]** 

![Initial DataVis Parks Dimple v3](https://github.com/saadkhan321/Project6_ND/blob/master/images/Initial_DataVis_Parks_Dimple_v3.png)

##### Enhancing the Tooltip

This version of the data visualization included animation of the tooltip with detailed tooltip chart displaying monthly visitor information. Code for this version is also in the index_files folder:

###### **[html file: index_initial_V6.html / data file: parkdata_initial_V4.tsv]** 

![Initial DataVis Parks Dimple Final](https://github.com/saadkhan321/Project6_ND/blob/master/images/Initial_DataVis_Parks_Dimple_v4.png)

### Intermediate Design Process [incorporating feedback]

##### 1. Intermediate V1 [without any feedback]

The intermediate version 1 of the code was used along with an introduction of the visualization to show the comparison of the top most visited National Parks in the US. The html file pertaining to the full article and the associated data file are in the index_files folder. This was the first iteration without any feedback. Subsequent version have the feedback incorporated 

###### **[html file: index_intermediate_V1.html / data file: parkdata_initial_V4.tsv]**

bl.ocks code version 1 is at [this link](http://bl.ocks.org/saadkhan321/ffa7663330bb317bea19)

##### 2. Intermediate V2 [incorporating 1st feedback]

The details of the 1st feedback are mentioned in the feedback section below. After the 1st feedback, an updated version of the data visualization was created and uploaded on to bl.ocks.org for further review. The associated .html files are in the index_files folder:

###### **[html file: index_intermediate_V2.html / data file: parkdata_initial_V4.tsv]**

The code version 2 for the visualization after 1st feedback is at [this link](http://bl.ocks.org/saadkhan321/3afb4229b42e81dfcace)

##### 3. Intermediate V3 [incorporating 2nd feedback]

Index_intermediate_V3.html was generated which incorporated the 2nd feedback. Details covered in the feedback section below. The code is on bl.ocks.org and associated .html files are uploaded are in the index_files folder 

###### **[html file: index_intermediate_V3.html / data file: parkdata_initial_V4.tsv]**

Code version after the 2nd feedback for the visualization is at [this link](http://bl.ocks.org/saadkhan321/af2604432728503f60a7)

##### 4. Intermediate V4 [incorporating 3rd feedback]

Some part of the 3rd feedback was incorporated in Index_intermediate_V4.html and rest was periodically implemented in the later versions as the visualization was being finalized. Also some additional enhancements such as inclusion of legend in the chart along with in chart notes were also added to the visualization. Html and data file are as follows:

###### **[html file: index_intermediate_V4.html / data file: parkdata_initial_V4.tsv]**

##### 5. Intermediate V5 [incorporating 4th feedback]

A mixture of 3rd and 4th feedback was incorporated in this version. On the suggestion of the Udacity Coach (Sheng-Kung), data was shifted from yearly to monthly format (details covered below in the feedback section). Doing so, popup chart stopped executing. Further enhancements in the visualization to bring back the popup chart were done in the subsequent versions. The monthly level data included was averaged over 10 years of visitation. Files for this version are as follows:

###### **[html file: index_intermediate_V5.html / data file: parkdata_initial_V4.tsv]**

##### 6. Intermediate V6 [Building up on all the feedbacks received]

In this version, bar chart was included in the popup chart showing year by year visitation for the month selected. Also inlcluded a rough draft for in-chart text block in the main chart. Related files are as follows:

###### **[html file: index_intermediate_V6.html / data file: parkdata_initial_V4.tsv]**


### Final Design

Final Design incorporated all feedbacks and some additional enhancements alongwith the story. Following are the additional enhancements I included on top of the feedback received:

1. Main change was to only focus on top 5 parks inorder to remove cluttering from the visualization.
2. Removed default axis labels and added visually attractive axis labels.
3. 5 In-chart text blocks with hover function to emphasize respective line charts were added. Text provided information pertaining to the main line charts.
4. Reverted back to 20 years of visitation data (main charts average over 20 years instead of 10 now)
5. Popup chart converted to line charts instead of bar charts (incorporating 20 year trend)
6. Changed the shape of the legend keys to be more viually appealing.

Related files pertaining to the final version are as follows:

###### **[html file: index.html / data file: parkdata_final.tsv]**

Visualization is at [this link](http://saadkhan321.github.io/)

Image below shows the snapshot of how the final visualization looks

![Final Visualization](https://github.com/saadkhan321/Project6_ND/blob/master/images/index_final.png)


## Feedback

The feedback was received via Udacity forums and email.

Link to [Udacity Forums feedback](https://discussions.udacity.com/t/project-feedback-required-top-10-most-visited-national-parks-in-us/27199)

### Feedback 1

##### Matthew Mucker (Fellow Nanodegree class mate) - Feedback via Udacity Forums

"Very nice!

The popup barcharts are a very nice touch. On my system, however, the title text of these charts is 'squished' vertically: the lines of text overlap each other and overlap the top border of the popup. This would be my primary feedback to you.

I'm not sure it's necessary to extend the y-axis down to zero. That leaves a lot of wasted space at the bottom of the plot, but in your defense, not extending the axis down to zero can lead to misinterpretation of the data.

I like the transitions when parks are added/removed from the chart".

### Response

###### Improved Version after feedback [html file: index_intermediate_V2.html]

Solution to the issue identified was given by modifying the code and impriving the tooltip chart. Before and after scenario is shown in the image below.

![After feedback 1](https://github.com/saadkhan321/Project6_ND/blob/master/images/improvemnt_after_feedback1.png)

###  Feedback 2

##### Susan Streisand (Fellow Nanodegree class mate) - Feedback via Udacity Forums

"I like this chart. The colors are pretty and the pop-up for each year is a nice way to show details. It might be nice to have the year on the pop-up as it's not easy to see exactly which year you are looking at. I am in chrome and it doesn't look squished. The pale yellow for Acadia is a little hard to read sometimes though".

### Response

###### Improved Version after feedback [html file: index_intermediate_V3.html]

Code was modified to incorporate the suggestions and the snapshots of the improvement made in the visualizaiton following this feedback is as follows:


![After feedback 2a](https://github.com/saadkhan321/Project6_ND/blob/master/images/improvemnt_after_feedback2a.png)
![After feedback 2b](https://github.com/saadkhan321/Project6_ND/blob/master/images/improvemnt_after_feedback2b.png)


### Feedback 3

##### Tyler Byers (Fellow Nanodegree class mate) - Feedback via email

"To me, 20 years seems to be maybe a little bit longer of a time-table than necessary, especially since there is relatively little year-to-year change (the graphs look mostly flat to me).  Maybe 10 or 12 years would look better, IMHO.  Also, having 12 national parks on there automatically makes the chart a little bit "busy" for me.  Perhaps just show 4 or 6 parks as the "default" (default to the other parks being off but with the ability to show them).  I'd also like to see some explanatory text on the chart itself -- sort of like a New York Times visualization or something like that.  Put a little text block about where your data were sourced from".  

"Your paragraph explanation of the project was very good.  I don't know if you're turning that part in (?).  I'd really take the key points from that and condense it to 3 lines that you can fit at the top of the chart.  Also choose a title that really grabs me. Your title should be a few words to describe your findings. So you need to weave a story around your data.  I honestly don't know how you would do this with yours, but you know the data well.  Maybe you need to roll in another data set -- average temperature in the month or something like that.   Tell me why Rocky Mountain National Park gets so many more visitors in summer".  

### Response

###### Improved Version after feedback [html file: index_intermediate_V3.html]

1. A little text block was included at bottom left that mentioned the source where data was taken from.
2. Reduced the number of parks from 10 to 5 to avoid cluttering.
3. Explanatory text added to chart itself as an to understand the trend of visitation.
4. Attempt was made to create the visualizaiton which looks like that of a typical New York Times visualization.
5. Appropriate title was chosen for the visualization
6. Explanatory text added to the main chart explains the high summer visitation at Rocky Mountain National Park

###  Feedback 4

##### Sheng Kung (Nanodegree Coach) - Feedback via Udacity Forums

"Hi Saad, looks like your visualization is coming along nicely. The visualization is fairly free-form, so it was good to see the points laid out in the Summary section to help direct attention. One thing that I noticed from playing around with the plot, and which I also saw when reading through your observations in the Summary section, is that there was a lot of emphasis in looking at the monthly trends in the park attendance and comparing them between parks. Since monthly attendance is only visible from the popup charts, it can be a bit tricky to compare multiple parks".

"It may be worth looking at the converse plot to what you created, with month aggregated over years on the horizontal axis, and breakdown or trend by year with the popup charts. This'll make it easier to see the differences between the parks that are year-round and those parks that are seasonal".

### Response

###### Improved Version after feedback [html file: index_intermediate_V5.html]

As suggested, line charts were shift from yearly trend to monthly trend for better comparison of the park visitation as either being year round or seasonal.

Snapshot with both feedback 3 and 4 incorporated is as below:

![After feedback 3 and 4](https://github.com/saadkhan321/Project6_ND/blob/master/images/improvemnt_after_feedback3and4.png)


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
##### http://alignedleft.com/tutorials/d3/axes
##### http://www.nytimes.com/interactive/2009/03/01/business/20090301_WageGap.html?_r=1&
##### http://www.nytimes.com/interactive/2012/05/17/business/dealbook/how-the-facebook-offering-compares.html?_r=0

## Data

Final .tsv file used for data visualization is \index_files\data\parkdata_final.tsv
