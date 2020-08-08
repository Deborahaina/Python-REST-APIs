REST APIs

Data's true power lies in its ability to answer questions definitively. I will be diving into th world of  Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"

![Equator](Images/equatorsign.png)


## Considerations

* The city data is generated based on random coordinates.I drew samples from a uniform distribution. Samples are uniformly distributed over the half-open interval [high, low]

* I refreshed my memory on the geographic coordinate system( A refresher is always good)Link is below
(http://desktop.arcgis.com/en/arcmap/10.3/guide-books/map-projections/about-geographic-coordinate-systems.htm).

* Next, I spent the requisite time necessary to study the OpenWeatherMap API. Based on my initial study, you should be able to answer  basic questions about the API: Where do you request the API key? Which Weather API in particular will you need? What URL endpoints does it expect? What JSON structure does it respond with? Before you write a line of code, you should be aiming to have a crystal clear understanding of your intended outcome.

#Packages, Libraries and Modules Used

*Citipy package, a very uselful python library returns a list of world cities based on longitude and latitude coordinates. This however does not generate uniformly distributed random sample so it is important to use the numpy built in 'uniform' method.This is so we can avoid creating a biased dataset that concentrates on a particular region of the world.

Used this in conjuction with the OpenWetherMap Api which returned information on the unique cities returned from looping through citipy library. I converted the data returned into a json format for easy parsing. I used the city name endpoint and this returned the data that I needed to plot my visualizations.You can sign up for an Api key using the free tier. There are other paid tiers available as well.(https://openweathermap.org/api)

Pandas ====>
TUsed pandas to create an empty list which was used to append the dataset processed from the API requests. This was converted into a pandas dataframe and finally saved as a csv file.

Matplotlib
My objective is to build a series of scatter plots to showcase the following relationships:
Latitude Vs Max Temperature
Latitude Vs Humidity
Latitude Vs Cloudiness
Latitude Vs Windspeed











