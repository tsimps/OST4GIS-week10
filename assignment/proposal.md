# Final Project Proposal

Your assignment this week is to write a detailed proposal for your final
project. In proposing your final, try to address each of the following
areas.

## Problem / Question

Applications are ultimately just tools. What problem or question does
your application attempt to resolve or grapple with? How does your
application speak to this problem/question?

SEPTA runs around 130 bus routes in Philadelphia and surrounding counties. Most
of these routes are essentially the same (down to the numbers) as the original
trolley routes planned at the turn of the 20th century (i.e. a person who took
the 17 trolley in 1920 would find the 17 bus making the same trip today). However,
the world has changed a lot since then. Commutes are different, and the routes
do not make sense in many places. Moreover, continual minor alterations, many
of which were often favors for support or to solve a minor problem, have created
service that is duplicative about 20% of the time. Today, transit planners in
Philadelphia are following a national trend to reexamine and replan the bus service
in major cities. However, the large number of routes create a large amount of
data that planners must understand when working with routes. This tool will be
a small application that will allow planners to view a variety of cuts of data
that will allow better, faster understanding of existing service and how riders
use that service.

## The data

Geospatial applications are all about working with data. What datasets
would you plan/like to use? If the data you'll be working with isn't
already stored in a way that you can use, how will you be storing your data?
(If it is too large for a javascript application, using a backend might
be necessary)

I have been working with a large set of passenger count data that is aggregated
and cut in R. The files are then imported to QGIS and exported to GeoJSON. So far,
the size has not been too unwieldy, but there may be a need for a database on the
backend.


## Technologies used

Which technologies covered in class (or discovered on your own!) do you
plan to use? How do you anticipate using each of these technologies?

Review the APIs/online examples of leaflet, turf, jQuery, underscore (or
any library not explicitly covered in class) for functions/uses which
you'd like to explore. Briefly describe how you might use them.

* Leaflet - I will rely on Leaflet mapping API for the basic map styles and functions
* Underscore - Will be used for general data manipulation and code refactoring
* jQuery - Used for making asynchronous calls
* Mapbox - Will use the Map Matching API to aggregate bus stop data to
street segments.
* Turf JS - may use the aggregation features to compile transit usage in census
tracts or neighborhoods.
* Chart.js - will be used to display dynamic analytics

## Design spec

#### User experience

At a high level, how do you expect people to use your application?
- Who are the users?
  - User are expected to be planners that need access to transit analytics, but
    are not necessarily experts on transit operations.
- What do they gain from your application' use?
  - Fast, reliable access to key analytics that maximize the ideation stage
    of transit/complete streets projects.
- Are there any website/application examples in the wild to which you can compare your final?
  - There is a non-public project from University of Pittsburgh researchers that
    has inspired this. The ease of use of Remix is also inspiring.

#### Layouts and visual design

So far, we've built all our applications with a side bar for
representing non-map content and navigation. This is not the only
successful design. Extra content could be displayed in a top bar,
through modals, through side bars on both sides, and any combination of
these as well as a number not mentioned. Try to describe your
application's visual layout. Conceptually (no need for extensive CSS
here), what will this design require?

The map will be the most prominent UI feature. A header bar with a horizontal
control bar will allow users to change which feature set they're using. A
sidebar will be used to display analytics (numbers, charts, graphs), based on
what is done on the map.

## Anticipated difficulties

Thinking about weaknesses can be useful. What do you anticipate being
most difficult about this project? How will you attempt to cope with
these difficulties? For example, asynchronous behavior (ajax, events)
are hard to use and think about. Global variables are a strategy for
coping with that difficulty by breaking data out of the asynchronous
context.

Asynchronous issues do exist but are relatively minor (just calling JSON from
a GIT folder). Dealing with larger, server hosted data could be incorporated
to give the user more control over how much manipulation is possible. The
minimum viable product will not need this, as data can be pre-cut and served
in lightweight JSON files.

## Missing pieces

We've only managed to scratch the surface of the available technologies
by which you could construct an application. What use-cases haven't we covered
that you think would be useful? What technologies not covered seem exciting to
you (you don't necessarily have to fully understand what they're for,
this is a chance for you to get our help interpreting a technology's
purpose/usage).

Using data visualization libraries like chart.js to show dynamic data visuals
would be great.
