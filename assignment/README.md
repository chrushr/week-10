# Final Project Proposal

Your assignment this week is to write a detailed proposal for your final
project. In proposing your final, try to address each of the following
areas.

## Problem / Question

<!-- Applications are ultimately just tools. What problem or question does
your application attempt to resolve or grapple with? How does your
application speak to this problem/question? -->

Location is key to successful operations and overall growth of a business. The location can affect many aspects of how a business operates, especially in terms of total sales and service area. In an increasingly competitive business world, it has become crucial for businesses to choose wisely where to operate, and one of the biggest factors to consider is the potential customer population in their primary trade areas. Addressing this issue is essential for a business to thrive.

This project/tool aims to propose suitable sites for supermarkets to locate a new store, considering the store’s features, the various factors affecting the store’s success, and the potential customer population for both the store itself and the competitor stores; by doing so, the tool aims to provide supermarkets with data-driven solutions for siting and market analysis and provide better services to the communities.


## The data
<!--
Geospatial applications are all about working with data. What datasets
would you plan/like to use? If the data you'll be working with isn't
already stored in a way that you can use, how will you be storing your data? -->


Part 1: Siting the new supermarket

Census Tract Demographic Data
Filtered consumer base data basing on age, income, etc. (not sure if this is needed, need to further research on Huff Model)
Supermarket data
Parcel data
Land Use data
Transportation data

Part 2: Market Analysis

Huff Model Parameters
Size(sqft) or sales floor or store parcel size, Location, Name, sales volume, number of products in inventory (ideally)
Tabular/shp.
Otherwise: Building Foot Print Data + Google Map to estimate square footage; search supermarkets on google map and scrape address data?
Street centerline shp.
Distance (network analyst) from census tracts to supermarkets
Geocoded new supermarket based on user’s selection


Storing Data:
For the siting part, data will be stored as point shapefiles geojsons
For the market analysis part, data will also be stored as shapefiles  geojsons




## Technologies used

<!-- Which technologies covered in class (or discovered on your own!) do you
plan to use? How do you anticipate using each of these technologies?

Review the APIs/online examples of leaflet, turf, jQuery, underscore (or
any library not explicitly covered in class) for functions/uses which
you'd like to explore. Briefly describe how you might use them. -->

I plan to use the following technologies:

R: for scraping and cleaning data
GIS: for siting analysis and market analysis
Leaflet: for mapping and displaying geojsons in general
Carto: possibly using carto to visualize market analysis maps
D3 & Chart-3: possibly using them for creating infographics
jQuery: for functions that realize user interactivity and for frontend framework design
Turf: possibly used for vector layer calculations?
Underscore: for filtering and selecting data



## Design spec

#### User experience

<!-- At a high level, how do you expect people to use your application?
- Who are the users? -->
- The users will be supermarket owners/marketing staff (in this case, those of the three supermarket chains)

<!-- - What do they gain from your application' use? -->
-They’ll have a better idea about where to locate their potential new store

<!-- - Are there any website/application examples in the wild to which you can compare your final? -->
-Not exactly. But I hope to do something similar to the functions of GeoTrellis: letting user inputs change the mapping result


#### Layouts and visual design
<!--
So far, we've built all our applications with a side bar for
representing non-map content and navigation. This is not the only
successful design. Extra content could be displayed in a top bar,
through modals, through side bars on both sides, and any combination of
these as well as a number not mentioned. Try to describe your
application's visual layout. Conceptually (no need for extensive CSS
here), what will this design require? -->

I imagine my app to have a permanent side bar on the left with user-input space, map in the middle/right, and pop-up side bars with graphs and analysis results when clicking on maps



## Anticipated difficulties

<!-- Thinking about weaknesses can be useful. What do you anticipate being
most difficult about this project? How will you attempt to cope with
these difficulties? For example, asynchronous behavior (ajax, events)
are hard to use and think about. Global variables are a strategy for
coping with that difficulty by breaking data out of the asynchronous
context. -->

-The biggest difficulty I anticipate now is to make the interactive process from user inputs to site selection/market analysis results happen. Except for generating every possible scenario in GIS beforehand and use the generated results (csv., shp., etc.) directly,  I’m not sure how to calculate synchronously using JavaScript or other libraries…



## Missing pieces
<!--
We've only managed to scratch the surface of the available technologies
by which you could construct an application. What use-cases haven't we covered
that you think would be useful? What technologies not covered seem exciting to
you (you don't necessarily have to fully understand what they're for,
this is a chance for you to get our help interpreting a technology's
purpose/usage). -->

As I mentioned above, one thing I really want to learn is how to process both vector and raster layers “online” (e.g. overlay analysis); instead of generating things in ArcGIS beforehand, can they be done using JavaScript and other libraries?
