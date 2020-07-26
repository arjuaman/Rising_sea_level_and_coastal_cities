# Predicting how long will it take the sea levels to rise enough to submerge the countries

Global Mean Sea Level has been rising over the past century, and the rate has increased in recent decades. 
In 2014, global sea level was 2.6 inches above the 1993 average—the highest annual average in the satellite record (1993-present). 
Sea level continues to rise at a rate of about one-eighth of an inch per year, or concretely 3mm per year.

This graph from EDA of our data summarizes our point:</br>
![alt_text](https://github.com/arjuaman/Rising_sea_level_and_coastal_cities/blob/master/SeaLevel.png)

The two major causes of global sea level rise are thermal expansion caused by warming of the ocean (since water expands as it warms) and increased melting of land-based ice, such as glaciers and ice sheets. The oceans are absorbing more than 90 percent of the increased atmospheric heat associated with emissions from human activity. 

## Data and Scraping

Data was taken from, and scraped from various sources like: 

https://en.wikipedia.org/wiki/List_of_countries_by_average_elevation </br>
https://climate.nasa.gov/vital-signs/sea-level/ </br>
https://datacatalog.worldbank.org/dataset/world-sea-level-rise-dataset/resource/b2e00824-a018-4b23-ab37-149202d34515#{} </br>
https://www.eea.europa.eu/data-and-maps/indicators/sea-level-rise-3/assessment </br>

BeautifulSoup worked good enough to scrape the required data.

## Data preparation and EDA

After cleaning a data for considerate amount of time(*!), I plotted the following curves:

![alt_text](https://github.com/arjuaman/Rising_sea_level_and_coastal_cities/blob/master/GMSL.png)

![alt_text](https://github.com/arjuaman/Rising_sea_level_and_coastal_cities/blob/master/std_dev_GMSL.png)

![alt_text](https://github.com/arjuaman/Rising_sea_level_and_coastal_cities/blob/master/smoothened_GMSL.png)

![alt_text](https://github.com/arjuaman/Rising_sea_level_and_coastal_cities/blob/master/variance_GMSL.png)

![alt_text](https://github.com/arjuaman/Rising_sea_level_and_coastal_cities/blob/master/smoothened_variance_GMSL.png)

![alt_text](https://github.com/arjuaman/Rising_sea_level_and_coastal_cities/blob/master/smoothened_variance_GMSL_wrt_mean.png)

which clearly gave us the idea that a Linear Regression Model would perfectly fit the data:

![alt_text](https://github.com/arjuaman/Rising_sea_level_and_coastal_cities/blob/master/variance.png)

## Modeling

A linear fit using </br>
Coefficients:  [[9264469.09283385]] </br>
Intercept:  [1.09036098e+09]  </br>

gave the following fit:

![alt_text](https://github.com/arjuaman/Rising_sea_level_and_coastal_cities/blob/master/fit_1.png)

## Prediction & Result Analysis

Now reversing the axes, because we need to predict "time" when the countries will be submerged: </br>
![alt_text](https://github.com/arjuaman/Rising_sea_level_and_coastal_cities/blob/master/fit_2.png)

On predicting against the elevation of countries above Global Mean Sea Level (in mm) ,which I obtained from scraping the wikipedia, 
the prediction I got matched the global trend!

<strong>Maldives</strong> was the worst affected, followed by <strong>Singapore</strong>, <strong>Qatar</strong>, <strong>Netherlands</strong> and <strong>Denmark</strong>.

According to our model, Maldives would be completely under the waters by year <em>2533</em>, i.e. approx <em>500 years from now</em>!

## Concerns and Solutions

We need to take remedial measures asap to counter this issue, or future would be fatal!

Remedial measures:

1. Reduce your footprint.
Greenhouse gasses are a major contributor to sea
level rise. Calculate your “Carbon Footprint” at
www.carbonfootprint.com to learn how to
reduce the amount of greenhouse gases you
produce each day.
2. Protect wetlands. Wetlands act as natural
buffers for coastal areas during rainstorms and
hurricanes. They absorb precipitation and storm
surge waters. Learn about wetland restoration
activities in your area and get involved.
3. Let it soak in. Hard surfaces prevent water
from permeating into the ground and lead to an
increase in runoff and erosion. Use stepping
stones for walkways and paver blocks for patios.
If you are repaving use permeable pavement
which allows water to soak into the ground.
Direct rain runoff to rain gardens and barrels.
4. Plant more plants and save trees. Plants
clean the air and soak up rain. Reduce paper use
to prevent trees from being cut down. Set all
computers and printers to double-sided printing
and reuse one-sided copies as scrap paper.
5. Reduce your energy use. Reducing your
energy usage is good for your wallet and the
environment. Turn off your lights and appliances
when not in use and replace them with more
energy efficient varieties. Unplug your chargers
and appliances when possible because many use
energy even when turned off. Adjust your
thermostat to reduce AC and heat use. 
6. Obey “no-wake” zones. Waves produced by
motor crafts increase erosion along shore lines.
Operate in deeper water and keep an eye out for
“fragile area” and “slow no wake” signs.
7. Leave the car at home. Vehicles are a leading
source of carbon dioxide production. Reduce the
number of cars on the road by carpooling,
walking, biking, or using mass transit. When
driving, turn your car off if idling for more than
30 seconds. This will conserve fuel, save money,
and reduce greenhouse gas emissions.
8. Watch what you’re dune. Dunes and grasses
protect inland areas from wind and wave action,
thus preserving the shore. Dunes and sod banks
are fragile areas, so stay on designated paths to
avoid them. Support restoration!
9. Know your flood zone. Knowing your risk for
flooding before a storm strikes will help you be
much better prepared for high storm surge.
Contact your local government or go to
www.msc.fema.gov to view your local
flood map.
10. Push for a Climate Action Plan. Many cities
and states do not have plans to address climate
change, which is the primary cause of current
sea level rise. Contact your local elected
officials and encourage them to take action now. 

Thank You!
