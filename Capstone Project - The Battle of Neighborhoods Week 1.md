# Capstone Project - The Battle of Neighborhoods (Week 1)

*Kyle Bao | 29 May 2020 | IBM Applied Data Science Capstone Project*

## Introduction

Singapore is a multicultural city-state with a vibrant food scene. There are numerous restaurants serving cuisines from around the world, contributing to the city's high-quality diversified food scene. Due to the diversity of the food scene in Singapore, visitors may be spoilt for choices when deciding which eateries to visit. A map showing the distribution of high-quality restaurants and eateries in Singapore will be helpful in planning a culinary adventure through the city.

## Business Problem

How can we provide a map showing the distribution of high-quality restaurants and eateries in Singapore?

## Data

Instead of using data on the boundaries of neighborhoods in Singapore, we will use location data of the stations of the Mass Rapid Transit (MRT) and Light Rail Transit (LRT) train network. Not only does this serve as a proxy for neighborhoods, the resultant data product will also be more useful to a tourist visiting the city. Due to the cheap and efficient MRT train network, it is effortless for one to utilise the train network to plan one's itinerary and visit different parts of the city. Using the location data of the train stations, we will search for restaurants within walking distance of the station. The resultant map will be a map of high quality restaurants within walking distance of the train stations.

Location data for the train stations are obtained from the following Wikipedia pages:

- [List of Singapore MRT stations](https://en.wikipedia.org/wiki/List_of_Singapore_MRT_stations)
- [List of Singapore LRT stations](https://en.wikipedia.org/wiki/List_of_Singapore_LRT_stations)

We will only use data for stations that are currently in operation.

The longitude and latitude coordinates for the stations will be obtained via the `Nominatim` geocoder for OpenStreetMap data from the `geopy` Python package.

The Foursquare API will be used to extract the list of restaurants around each station, as well as the restaurants' ratings and cuisine categories.

Finally, the map data used is provided by the `folium` package.