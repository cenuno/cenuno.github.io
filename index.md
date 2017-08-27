# Home

Welcome to Urban Data Science:  Using Open-Source Tools to Study Urban Life.

My name is Cristian E. Nuno and I'm an urban data scientist. One year ago I never knew about [GitHub](https://github.com/). I thought [R](https://www.r-project.org/about.html) was a sound pirates made; I thought [Python](https://www.python.org/about/gettingstarted/) was a type of snake. 

For those of you who are new to coding in either language, welcome! I share with you a quote by *[This American Life](https://www.thisamericanlife.org/about)*'s [Ira Glass](https://www.goodreads.com/quotes/309485-nobody-tells-this-to-people-who-are-beginners-i-wish):

> Nobody tells this to people who are beginners, I wish someone told me. All of us who do creative work, we get into it because we have good taste. But there is this gap. For the first couple years you make stuff, it’s just not that good. It’s trying to be good, it has potential, but it’s not. But your taste, the thing that got you into the game, is still killer. And your taste is why your work disappoints you. A lot of people never get past this phase, they quit. Most people I know who do interesting, creative work went through years of this. We know our work doesn’t have this special thing that we want it to have. We all go through this. And if you are just starting out or you are still in this phase, you gotta know its normal and the most important thing you can do is do a lot of work. Put yourself on a deadline so that every week you will finish one story. It is only by going through a volume of work that you will close that gap, and your work will be as good as your ambitions. And I took longer to figure out how to do this than anyone I’ve ever met. It’s gonna take awhile. It’s normal to take awhile. You’ve just gotta fight your way through.

This quote inspires me to continue to improve my work. Only way to do that is to share your work with others and incorporate their advice.


*****************

## CPS Locator (August 2017)

[![](https://github.com/cenuno/shiny/raw/master/Images/Screen%20Shot%202017-08-27%20at%203.50.54%20AM.png)](https://cenuno.shinyapps.io/cps_locator/)

[Chicago Public Schools (CPS) Locator](https://cenuno.shinyapps.io/cps_locator/) is a Shiny app, a web app made using the R programming language.

The goal is simple: to make finding a CPS school of interest easier using open-source tools. 

## Run App from RStudio/R Console

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

## Next Steps

As of August 27, 2017 deployment, here is what needs to continue to be done:

- [x] [Launch Version 1.0 of App](https://cenuno.shinyapps.io/cps_locator/)
- [x] [Post .R script of Version 1.0](https://github.com/cenuno/shiny/blob/master/cps_locator/app.R)
- [ ] Solicit feedback
- [ ] Build a regular expression tool that returns a list of CPS schools based on user-defined grade level(s) of interest
- [ ] Use the Checkbox Shiny Widget to allow users to filter which CPS schools appear on the Leaflet map based on the type of school (i.e. neighborhood, charter, military academy, etc.)
- [ ] Add CTA 'L' rail lines, CTA bus stops, and bike paths to indicate which schools are located near public transportation.
- [ ] Launch Version 2.0 of App
- [ ] Update .R script of Version 2.0

Thank you everyone for your feedback and encouragement on this project!

*Last updated on August 27, 2017*

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
