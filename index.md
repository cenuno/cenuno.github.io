# Home

Welcome to Urban Data Science:  Using Open-Source Tools to Study Urban Life.

My name is Cristian E. Nuno and I am an aspiring urban data scientist. 

One year ago I never knew about [GitHub](https://github.com/). I thought [R](https://www.r-project.org/about.html) was a sound pirates made; I thought [Python](https://www.python.org/about/gettingstarted/) was a type of snake. 

For those of you who are new to coding in either language, welcome! I share with you a quote by *[This American Life](https://www.thisamericanlife.org/about)*'s [Ira Glass](https://www.goodreads.com/quotes/309485-nobody-tells-this-to-people-who-are-beginners-i-wish):

> Nobody tells this to people who are beginners, I wish someone told me. All of us who do creative work, we get into it because we have good taste. But there is this gap. **For the first couple years you make stuff, it’s just not that good.** It’s trying to be good, it has potential, but it’s not. But your taste, the thing that got you into the game, is still killer. And your taste is why your work disappoints you. A lot of people never get past this phase, they quit. Most people I know who do interesting, creative work went through years of this. We know our work doesn’t have this special thing that we want it to have. We all go through this. And if you are just starting out or you are still in this phase, you gotta know its normal and the most important thing you can do is do a lot of work. Put yourself on a deadline so that every week you will finish one story. **It is only by going through a volume of work that you will close that gap, and your work will be as good as your ambitions**. And I took longer to figure out how to do this than anyone I’ve ever met. It’s gonna take awhile. It’s normal to take awhile. **You’ve just gotta fight your way through**.

This quote inspires me to continuosly improve my analytical skills. I hope it inspires you to do the same, regardless if you're a beginner or an experienced developer.


*****************

## CPS Locator Update (September 2017)

Hi everyone. First off, thank you to my old professor and colleague for their advice on the CPS Locator App. Their feedback has pushed me to slow down on the development, and instead spend more time on the user-experience of the app.

In the meantime, please [check out my progress for CPS Locator Version 3.0](https://github.com/cenuno/shiny/projects/1). I'm taking advantage of [GitHub's Project Board tool](https://help.github.com/articles/about-project-boards/).

There's a lot of work that remains! Enjoy your weekend.

## CPS Locator (September 2017)

### CPS Locator: making it easier to find the right Chicago Public School for you.

[![CPS Locator Home Tab](https://github.com/cenuno/shiny/raw/master/Images/cps_locator_v2.png)](https://cenuno.shinyapps.io/cps_locator/)

[![CPS Locator Downloads Tab](https://github.com/cenuno/shiny/raw/master/Images/cps_locator_Downloads_v2.png)](https://cenuno.shinyapps.io/cps_locator/)

[Chicago Public Schools (CPS) Locator](https://cenuno.shinyapps.io/cps_locator/) is a web-based [Shiny app](https://shiny.rstudio.com/) that empowers users to interact firsthand with [CPS school year 2016-2017 data](https://data.cityofchicago.org/Education/Chicago-Public-Schools-School-Profile-Information-/8i6r-et8s).

### Run App from RStudio/R Console

Copy and paste the following R commands to run the app locally on your machine:

```R
# Install necessary packages
install.packages( c("shiny", "DT", "shinydashboard", "dplyr"
                     , "magrittr", "htmltools", "htmlwidgets"
                     , "rgdal", "splancs", "stringr", "rgeos" 
                     , "devtools"
                     ) )
                     
# install `leaflet` package from source
# for more info, click here: https://rstudio.github.io/leaflet/
devtools::install_github("rstudio/leaflet")

# Load necessary packages
library( shiny )

# Run shiny app from your R/RStudio Console
shiny::runUrl( url = "https://github.com/cenuno/shiny/archive/master.zip"
                , subdir = "cps_locator"
                )
```

### Next Steps

As of September 4, 2017 version 2.0 deployment, here is what needs to be done:

#### Version 1.0
- [x] [Launch Version 1.0 of App](https://cenuno.shinyapps.io/cps_locator/)
- [x] [Post .R script of Version 1.0](https://github.com/cenuno/shiny/blob/master/cps_locator/app.R)

#### Version 2.0
- [x] Solicit feedback
- [x] Launch Version 2.0 of App
- [x] Update .R script of Version 2.0
- [x] ~~Build a regular expression tool that returns a list of CPS schools based on user-defined grade level(s) of interest~~
- [x] Separate grades based on a user-defined drop-down selection by using a list

#### Version 3.0
- [ ] Solicit feedback

##### Filtering Map
- [ ] Use the Checkbox Shiny Widget to allow users to filter which CPS schools appear on the Leaflet map based on the type of school (i.e. neighborhood, charter, military academy, etc.)
- [ ] Add CTA 'L' rail lines, CTA bus stops, and bike paths to indicate which schools are located near public transportation
- [ ] Download button where dataset is filtered based on which CPS schools are located on the map based on the users preferences.
- [ ] Radio button that filters schools by all categories, only primarily elementary schools, only primarily middle schools, or only primarliy high schools
- [ ] Slider widget that filters schools based on their [School Quality Rankings (Level 1+, Level 1, Level 2+, Level 2, and Level 3)](http://cps.edu/Performance/Documents/SQRP_Introduction.pdf)(slide page number 10, entitled *What Does the School's Rating Mean?*)

##### Download Data 
- [ ] Filter data tables by Citywide or by Community Area
- [ ] Enable a "master search" input box, where that value populates each datatables "Search" box
- [ ] Make collapsible buttons white on blue, rather than blue on white

##### Speed Up the App
- [ ] Save .RDS file of pre-processed data cleaning work inside of GitHub folder
- [ ] Build out folder structure of cps_locator app
- [ ] Split app.r file into two files: ui.r and server.r
- [ ] Create custom css file and save it in GitHub. This file will store all the color, font, spacing, and other customizations I used to modify the `shinydashboard` appearance.
- [ ] Clean up code and ensure readability -- doesn't matter if it works if no one else can learn from what I've written

Thank you everyone for your feedback and encouragement on this project!

*Last updated on September 4, 2017*

*****************

## Catalog of Federal Domestic Assistance (CFDA) Search Tool (August 2017)

[![](https://github.com/cenuno/Spatial_Visualizations/raw/master/Images/CFDA.png)](http://rpubs.com/cenuno/cfda_search)

A [search-engine](http://rpubs.com/cenuno/cfda_search) was created to help users browse the CFDA by typing in keywords. Click here for the [source code](https://github.com/cenuno/Spatial_Visualizations/blob/master/USAspending/cfda_extraction_datatable.r).

***********

## Mapping the CTA (August 2017)

[![](https://github.com/cenuno/Spatial_Visualizations/raw/master/Images/CTA_L_RailLines_Stations_2017-08-19.png)](https://rpubs.com/cenuno/Mapping_CTA)

[Tutorial](https://rpubs.com/cenuno/Mapping_CTA) on how to plot the Chicago Transportation Authority (CTA) 'L' Rail Line, Rail Stations, Bus Routes, and Bus Stops for the City of Chicago.

******************

## Point-n-Polygon (August 2017)

[![](https://github.com/cenuno/Spatial_Visualizations/raw/master/Images/PointNPolygon.png)](https://rpubs.com/cenuno/spatial_analysis_pts_poly)

What follows is a [tutorial](https://rpubs.com/cenuno/spatial_analysis_pts_poly) on the key spatial elements needed to understand how to identify points which reside in specific polygons.

*******************

## Querying USAspending API data from RStudio (June 2017)

[![](https://github.com/cenuno/Spatial_Visualizations/raw/master/Images/QueryUSA.png)](https://rpubs.com/cenuno/USAspendingAPI)

[USAspending API](https://api.usaspending.gov/) offers an interactive way for active citizens to query relevant federal spending data on a variety of fields. People can query data by geography, type of federal spending, CFDA program number, and much more. [Click here a tutorial](https://rpubs.com/cenuno/USAspendingAPI) on querying the data for FY17 Austin, Texas.

*****************

## My Journey

I want to be an urban data scientist. I understand that this title is a [neologism](http://www.dictionary.com/browse/neologism); however, I firmly believe the future will require all social scientists, policy makers, and business people to harness the power of technology to showcase their research, policy recommendations, and business decisions.

I studied urban planning and economics at the [University of Illinois at Chicago](https://www.honors.uic.edu/) (UIC). While economics taught me how certain things influence people to take one action over another, it was urban planning that engrained in me the value of looking at things at the individual level.

It is one thing to say the city is doing well; it is an entirely different thing to say the same for one particular block in one particular neighborhood.

The emphasis on the individual was eloquently expressed through the writings of [Mike Royko](http://www.press.uchicago.edu/Misc/Chicago/730719.html) and [Studs Terkel](https://www.youtube.com/watch?v=Oyl1BvHo9LM). I learned of great Chicago leaders such as [Jane Addams](http://www.hullhousemuseum.org/), [Harold Washington](https://www.thisamericanlife.org/radio-archives/episode/84/harold), and [Florence Scala](http://www.encyclopedia.chicagohistory.org/pages/410114.html).

Yet all these people led me to one inescapable conclusion: my hometown needs to do a better job of ensuring its residents a chance to succeed in life.

### Urban Policy Meets Data Science

At Syracuse University's [Maxwell School of Citizenship and Public Affairs](https://www.maxwell.syr.edu/paia/), I took a class in the fall of 2016 with Professor Jesse Lecy entitled [*Data Driven Management*](http://www.lecy.info/data-driven-management). His class exposed me to the power of open-source software. The programming language [R](https://www.r-project.org/about.html) and the code hosting platform [GitHub](https://guides.github.com/activities/hello-world/) enable users from around the world to build, update, and revise tools in real time. 

No longer would policy decisions be hidden in an appendix behind some report; now, anyone with a computer could extract the exact code used to reach those same conclusions. 

With the help of Professor Lecy, I finished my time at Syracuse with both a Masters of Public Administration and Certificate in Advanced Study in Data Science. The two fields will help me quantify, visualize, and simplify urban policy decisions to aid in the slow march of equal opportunity in my hometown. 
