# Querying a Document Database

## Objectives

* Execute queries on a Mongodb document collection.

## Instructions


* Start MongoDB if it isn't already running by launching the executable mongo.exe. It should be located in the /bin directory of your local MongoDB installation.
* Add Azure Cosmos DB extention to VS Code
* Attach the running version of MongoDB from the Azure Cosmos pane.  Instructions for how to do this can be found in the extention tab or at https://code.visualstudio.com/docs/azure/mongodb
* Import volcanoes.json into your mongo database.  This can be done by right-clicking on the connected database in the Azure Cosmos pane.  You can also do this from a command prompt, but it is more difficult.  Change directories so that you are in the mongodb bin folder.  There should be an executable named mongoimport.exe.  From this bin directory, execute the following command:

                   `mongoimport --db geo --collection volcanoes < {pathway to volcanoes.json} --jsonArray`

`volcanoes.json` contains a data set of 804 historical volcanic eruptions.  Below is a sample of the data for each eruption.

```JSON
  {
    "Year": 1362,
    "TSU": "",
    "EQ": "",
    "Name": "Oraefajokull",
    "Location": "Iceland-SE",
    "Country": "Iceland",
    "Latitude": 64,
    "Longitude": -16.65,
    "Elevation": 2119,
    "Type": "Stratovolcano",
    "VEI": 5,
    "Agent": "T,F",
    "DEATHS": 220
  }
```

Use the Azure Cosmos DB extention in VS Code to query the volcanoes database and retrieve the following records:

--We will do these together

 1. Find the volcanoes that erupted in the 1970s.
 2. Find the names of the volcanoes that had an eruption with a Volcanic Explosivity Index (VEI) of 7 or higher.
 3. Find the eruption with the highest number of recorded deaths.
 4. Find the percentage of eruptions that caused mudflows (Agent_Code "M" for Mudflow).
 5. Find the most common type of volcano in the set.

--On Your Own
 
 6. Find the eruptions that occured in your home country.
 7. Find the average elevation of all eruptions.
 8. Find a list of the types of volcanoes.
 9. Find the percentage of eruptions that occurred in the Northern Hemisphere.
10. Find the names of eruptions that occurred after 1900, that did NOT cause a mudflow, happened in the Southern Hemisphere, and had a VEI of 5.
11. Return the names of eruptions that occurred at or above an elevation passed in as an argument.
12. Return the agents of death for the ten most deadly eruptions.


### References

Volcano data retrieved from: National Geophysical Data Center / World Data Service (NGDC/WDS): Significant Volcanic Eruptions Database. National Geophysical Data Center, NOAA. [doi:10.7289/V5JW8BSH](https://data.nodc.noaa.gov/cgi-bin/iso?id=gov.noaa.ngdc.mgg.hazards:G10147)
