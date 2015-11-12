# DataRepProject

### Galway City Car Parking Locations

### Shane Gleeson - G00311793

## Introduction
This project is based on the dataset Galway City Car Parking Locations and can be found here at the link  
<<< https://data.gov.ie/dataset/galway-city-car-parking-locations >>>

## About the Dataset
The CSV file has 18 rows and 12 columns
This dataset gives us information about the parking locations in the City of Galway. We are given the location based on their longitude and latitude, the other information we are given is the number of spaces their is to park in.

Here is the breakdown of the dataset
 
 
|Heading | Description  |
|---------|:-----------|
| X | Longitude |
| Y | Latitude |
| ObjectID | Here the id is given to each parking location |
| Name |  Name of the Parking Location|
| Type | What type of car parking facility it is |
| NO_SPACES | The amount of vehicles the parking facility can hold |
| Lat | Latitude of the Car Park |
| Long | Longitude of the Car Park |
| EastITM | Old Irish Grid Reference EAST |
| NorthITM | Old Irish Grid Reference NORTH |
| EastIG |  Cartesian co-ordinates - Easting |
| NorthIG |  Cartesian co-ordinates - Northing |

## Design 
## Idea For the API's URL

### Galway Cities Car Park Location

From here you can can get the location of the specific Car Park you are looking for, for example given the URL: 
<<< *http://galwaycarparks.ie/location/carparklocation* >>> where you have "carparklocation" will be your desired location

Here a list of car parks will be listed in front of you that are near the location in Galway City you've entered.

This is what will show for this direct link:

|Heading | Description  |
|---------|:-----------|
| Name | This will give back the name you've entered for 'carparklocation' |
| Lat | Latitude of the Car Park |
| Long | Longitude of the Car Park |
| EastITM | Old Irish Grid Reference EAST |
| NorthITM | Old Irish Grid Reference NORTH |
| EastIG |  Cartesian co-ordinates - Easting |
| NorthIG |  Cartesian co-ordinates - Northing |

For Example if you are looking for a carpark near the docks the URL would look something like this 
<<< *http://galwaycarparks.ie/location/Docks* >>> :

```json
{
        "NAME": "Docks",
        "Lat": "53.271",
        "Long": "-9.049",
        "EastITM": "530015.932",
        "NorthITM": "725055.66",
        "EastIG": "130050.06",
        "NorthIG": "225026.446"
}
```
