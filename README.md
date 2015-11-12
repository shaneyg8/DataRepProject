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
###Home
Here is an idea I created for the home page of the Galway City Car Parking Locations, here is a simple way to navigate and find your way around through a drop down list of all the locations in Galway City with Car Parks.

## Idea For the API's URL

### 1. Galway Cities Car Park Location

From here you can can get the location of the specific Car Park you are looking for, for example given the URL: 
<<< *http://galwaycarparks.ie/location/[carparklocation]* >>> where you have "[carparklocation]" will be your desired location.

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

### 2. Galway Cities Car Park Spaces

From here you will get access to the information of how many spaces the car park holds and what type of facility you would be entering, example: "TYPE": "Multistorey Carpark" 
<<< *http://galwaycarparks.ie/location/[carparklocation]/[type]* >>> where you have "[carparklocation]" will be your desired location and where you have [type] will give you back the information on the type of car park it is and also how many spaces the car park holds. 

This is what will show for this direct link:

|Heading | Description  |
|---------|:-----------|
| Name | This will give back the name you've entered for 'carparklocation' |
| Type | What type of car parking facility it is |
| NO_SPACES | The amount of vehicles the parking facility can hold |
| Lat | Latitude of the Car Park |
| Long | Longitude of the Car Park |
| EastITM | Old Irish Grid Reference EAST |
| NorthITM | Old Irish Grid Reference NORTH |
| EastIG |  Cartesian co-ordinates - Easting |
| NorthIG |  Cartesian co-ordinates - Northing |

For example:

```json
{
        "NAME": "Jurys Hotel",
        "TYPE": "Multistorey Carpark",
        "NO_SPACES": "348",
        "Lat": "53.271",
        "Long": "-9.055",
        "EastITM": "529620.784",
        "NorthITM": "725010.839",
        "EastIG": "129654.828",
        "NorthIG": "224981.613"
}
```
Above shows the multistorey car park facility and the number of spaces

Another example:

```json
{
        "NAME": "Gaol Rd / Cathedral",
        "TYPE": "Pay/Surface Carpark",
        "NO_SPACES": "161",
        "Lat": "53.274",
        "Long": "-9.057",
        "EastITM": "529481.534",
        "NorthITM": "725397.739",
        "EastIG": "129515.546",
        "NorthIG": "225368.595"
}
```

Here it shows the pay/surface carpark

##HTTP Request Methods  
|Method | Description |
|---------|:-----------|
| GET | GET Retrieves Information from the server |
| HEAD | HEAD Retrieves response header  |
| PUT | PUT Sets the data at the URI to request data |
| POST | POST Sends data to the server |
| DELETE | Delete the data at the URI |

##Status Code
| Code | Description |    
|------|:--------|     
**200** | Ok | 
**202** | Accepted  |  
**400** | Bad Request | 
**404** | Not Found  |  
**405** | Method Not Allowed | 
**503** | Service Unavaiable

