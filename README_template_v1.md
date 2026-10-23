# 🚀 Space Bot API Investigation Sheet

**Total Marks: 40**  
**TASK 1: Collect Required API Documentation**

This investigation sheet helps you gather key technical information from the three APIs required for the Space Bot project: **Webex Messaging API**, **ISS Current Location API**, **Weather API** and a **Geocoding API** , plus the Python time module. Also furhter investigate the application of Web Architecture and MVC design pattern in development of the Bot

---

##  Webex Messaging API (4 marks)

| Criteria | Details |
|---------|---------|
| API Base URL | `https://webexapis.com/v1/rooms` |
| Authentication Method | `Bearer Token` |
| Endpoint to list rooms | `https://webexapis.com/v1/room/tabs?roomId= ` |
| Endpoint to get messages | `https://webexapis.com/v1/messages/{messageId} \` |
| Endpoint to send message | `https://webexapis.com/v1/messages \` |
| Required headers | `'Authorization: Bearer ZWIzY2QzZTItOTU0YS00M2Q4LWFjNDUtMTllMTc0NTY0ZGU3ODAyNWU4Y2MtMmJk_PE93_c18e13ae-5575-4bc0-ae01-e48905f14f17' 'Accept: application/json'` |
| Sample full GET or POST request | `
"id": "Y2lzY29zcGFyazovL3VybjpURUFNOmV1LWNlbnRyYWwtMV9rL1JPT00vNzEyOWNhYjAtYjczNS0xMWYxLTg3ZGItMTMxNmExYmNlYzEx",
            "title": "Welcome space",
            "type": "group",
            "lastActivity": "2026-09-23T09:59:18.701Z",
            "creatorId": "Y2lzY29zcGFyazovL3VzL1BFT1BMRS80N2FkZjFmZS02NmNkLTRiNTAtYWI4YS1lNjdkOGVhNTJmZmM",
            "created": "2026-09-23T09:59:18.491Z",
            "ownerId": "Y2lzY29zcGFyazovL3VzL09SR0FOSVpBVElPTi9jMThlMTNhZS01NTc1LTRiYzAtYWUwMS1lNDg5MDVmMTRmMTc",
            "isPublic": false,
            "isReadOnly": false,
            "isLocked": false` |

---

##  ISS Current Location API (2 marks)

| Criteria | Details |
|---------|---------|
| API Base URL | `http://open-notify.org/` |
| Endpoint for current ISS location | `http://open-notify.org/Open-Notify-API/ISS-Location-Now/` |
| Sample response format (example JSON) |  
```
{
  "message": "success", 
  "timestamp": UNIX_TIME_STAMP, 
  "iss_position": {
    "latitude": CURRENT_LATITUDE, 
    "longitude": CURRENT_LONGITUDE
  }
}
```


---

##  Geocoding API (4 marks)

| Criteria | Details |
|---------|---------|
| Provider used (Choose one) | **LocationIQ / Mapbox/ OpenWeatherMap other -provide detail** |
| API Base URL | `https://openweathermap.org/` |
| Endpoint for geocoding | `https://openweathermap.org/api/geocoding-api?collection=other` |
| Endpoint for reverse geocoding | `https://openweathermap.org/api/geocoding-api?collection=other#reverse` |
| Authentication method | `appid` |
| Required query parameters | `q,appid,units` |
| Sample request with latitude/longitude | `
    "coord": {
        "lon": 10.13,
        "lat": 51.51
    },

| Sample JSON response (formatted example) |  
```
   "coord": {
        "lon": 10.13,
        "lat": 51.51
    },
    "weather": [
        {
            "id": 803,
            "main": "Clouds",
            "description": "broken clouds",
            "icon": "04d"
        }
    ],
    "base": "stations",
    "main": {
        "temp": 13.72,
        "feels_like": 13.29,
        "temp_min": 12.28,
        "temp_max": 13.99,
        "pressure": 1030,
        "humidity": 82,
        "sea_level": 1030,
        "grnd_level": 1000
    },
    "visibility": 10000,
    "wind": {
        "speed": 3.69,
        "deg": 278,
        "gust": 8.01
    },
    "clouds": {
        "all": 84
    },
    "dt": 1791972733,
    "sys": {
        "type": 2,
        "id": 197911,
        "country": "DE",
        "sunrise": 1791956469,
        "sunset": 1791995375
    },
    "timezone": 7200,
    "id": 6552341,
    "name": "Landolfshausen",
    "cod": 200
}` |
```
|

---


##  Weather API (3 marks)

| Criteria | Details |
|---------|---------|
| API Provider (OpenWeatherMap) | **OpenWeather, OpenWeatherMap (or other – provide details)** |
| API Base URL | `https://openweathermap.org/` |
| Endpoint for current weather | `https://api.openweathermap.org/data/2.5/weather?lat={lat}&lon={lon}&appid={API key}` |
| Authentication method | `Appid` |
| Required query parameters | `key:q;value=London.
key:appid;value=fd54cefecad481234d577ac3200920c8,key:units;value=metric` |
| Sample JSON response ({
    "coord": {
        "lon": -0.1257,
        "lat": 51.5085
    },
    "weather": [
        {
            "id": 803,
            "main": "Clouds",
            "description": "broken clouds",
            "icon": "04d"
        }
    ],
    "base": "stations",
    "main": {
        "temp": 21.02,
        "feels_like": 21.34,
        "temp_min": 19.99,
        "temp_max": 22.25,
        "pressure": 1012,
        "humidity": 83,
        "sea_level": 1012,
        "grnd_level": 1009
    },
    "visibility": 10000,
    "wind": {
        "speed": 6.7,
        "deg": 202,
        "gust": 9.2
    },
    "clouds": {
        "all": 70
    },
    "dt": 1790764567,
    "sys": {
        "type": 2,
        "id": 2075535,
        "country": "GB",
        "sunrise": 1790747944,
        "sunset": 1790790114
    },
    "timezone": 3600,
    "id": 2643743,
    "name": "London",
    "cod": 200
}) |  
```

```
|

---

##  Epoch to Human Time Conversion (Python time module) (2 marks)

| Criteria | Details |
|---------|---------|
| Library used | `_______________________________` |
| Function used to convert epoch | `_______________________________` |
| Sample code to convert timestamp |  
```  
```
|
| Output (human-readable time) | `_______________________________` |

---

##  Extended Feature API ( 3 marks)

| Criteria | Details |
|---------|---------|
| API Provider | 'AstronomyAPI' |
| API Base URL | `https://docs.astronomyapi.com/` |
| Endpoint | `https://api.astronomyapi.com/api/v2/bodies` |
| Authentication method | `HTTP Basic authentication , Application id and Application secret` |
| Required query parameters | `Longitude,Latitude,From Date,To Date,Time,Coordinates` |
| Sample JSON response ({
  "data": {
    "dates": {
      "from": "2026-10-16T12:48:26.000-04:00",
      "to": "2026-10-16T12:48:26.000-04:00"
    },
    "observer": {
      "location": {
        "longitude": -84.39733,
        "latitude": 33.775867,
        "elevation": 1
      }
    },
    "table": {
      "header": [
        "2026-10-16T12:48:26.000-04:00"
      ],
      "rows": [
        {
          "entry": {
            "id": "sun",
            "name": "Sun"
          },
          "cells": [
            {
              "date": "2026-10-16T12:48:26.000-04:00",
              "id": "sun",
              "name": "Sun",
              "distance": {
                "fromEarth": {
                  "au": "0.99684",
                  "km": "149125725.47307"
                }
              },
              "position": {
                "horizontal": {
                  "altitude": {
                    "degrees": "46.39",
                    "string": "46° 23' 24\""
                  },
                  "azimuth": {
                    "degrees": "167.54",
                    "string": "167° 32' 24\""
                  }
                },
                "horizonal": {
                  "altitude": {
                    "degrees": "46.39",
                    "string": "46° 23' 24\""
                  },
                  "azimuth": {
                    "degrees": "167.54",
                    "string": "167° 32' 24\""
                  }
                },
                "equatorial": {
                  "rightAscension": {
                    "hours": "13.42",
                    "string": "13h 25m 12s"
                  },
                  "declination": {
                    "degrees": "-8.93",
                    "string": "-9° 4' 12\""
                  }
                },) |  
```

```
|

--- 

##  Evaluation – Web Architecture, MVC Design & Security 

In this section, evaluate how web technologies, architecture, and design patterns have been applied in your **AstroBot**. Your responses must relate directly to your implementation and include reflection on your design decisions.

---

###  Web Architecture – Client–Server Model (3 marks)

Explain how the client–server model applies to your AstroBot:

- Client:The astrobot python bot I built using the requests library to send hhtp requests.The webex app also is a client used to create test room.
- servers: The servers include webex to send messages , openweathermap,opennotify and astronomy api.
- Describe how data flows between:
  - User inputs what he wants like sending a message to AstroBot , astro requests and checks to find the message on webex. APIs send the data to astrobot and it turns the message into something very readable for a human.

Include a **simple block diagram** to illustrate this interaction.
user--> webex-->astrobot-->apis-->astrobot-->webex
####  Security Considerations: (3 marks )
API keys arent stored in the code but as a placeholder. ,this additionally stops leaks happening on hubs like github .Futhermore you cant access it without the keys from an external source like webex. Webex for example also have a 12 hour time limit on each bearer code so you must go back and change the keys.
example of security cinsideration in my code|:
def get_webex_token():
    choice = input("Use hard-coded Webex token? (y/n): ").lower()
    if choice == "n":
        token = input("Enter your Webex Access Token: ")
        return f"Bearer {token}"
    else:
        return "Bearer YOUR_WEBEX_TOKEN"


###  RESTful API Usage in Your Application (3 marks )

Explain how REST APIs are used in your AstroBot: 

- Describe how HTTP methods (GET, POST) are used
Astrobot I built uses GET to read date and POST to create data.
  
- Explain how your bot interacts with APIs (Webex, Weather, ISS, Geocoding)
webex uses bearer token to list rooms , and post replies. OpenWeather and geocdoing return data for \weather and \iss .AstronomyAPI uses some command chains APIs for example /sky geocoding to astronomyAPI.
- Describe how JSON responses are received and processed  
each function checks response.status_code,converts with response.json(),extracts fields such as weather['main][/temp']
Note: Relate your explanation directly to your code for higher grade. 

#### Security Considerations: (2 marks)
- Check response status codes, Handling invalid or unexpected API responses, Avoiding excessive API calls

---

###  MVC Design Pattern in AstroBot (3 Marks)

Explain how the **Model–View–Controller (MVC)** pattern applies to your solution:
Provide a short example based on your implementation

| Component   | Description and Example (Relate to your Bot) |
|------------|----------------------------------|
| **Model**  | The data layer.Functions fetch and proccess data from apis and return readable data.For example get_weather() returns weather data |
| **View**   | What the user sees. Send_message() posts the formatted text into the Webex space ,for example "/weather london" and the terminal prints recieved and u see the weather in London |
| **Controller** | The main() function loop. It polls for new messages and get_latest_message(),reads the command(/weather,/iss,/sky,/help,/quit) |

---
short example: User asks fot /sky London. The controller detects the comman , the model (get_sky) retrieves the data from the APIs and the view send_message delivers the formatted answer to the user in webex.
### 📝 Reflection and Evaluation ( 8 marks )

Reflect on your AstroBot (400 words):

- How effective is your bot in meeting the Astronomy Club’s needs?
The Astrobot meets the astronomy clubs’ standards. The design was simplified and allows club members to type /Weather(Returns the weather report for a city),/iss(longitude and latitude),/sky (returns planets positions over cities )in to the chatbot or Webex space and get answers for those questions. 
- What design decisions worked well?
  The structure of the starter code worked very well , each feature has its own purpose for Webex , weather ,ISS and Astronomy so I added a new function and a new command branch.I reused function get_city_coordinates for both weather and sky to avoid coupling and code being duplicated.
- What challenges did you face when integrating APIs?
The main challenge I faced when integrating the APIs was the different authentication methods example using bearer tokens for Webex and api id and secret for astronomy .Testing is an issue as openweather key takes time to activate and other issues would be that after 12 hours the Webex token expires and needs to be refreshed.
- What security risks did you identify and how were they handled?
The major security risk I had during the process of building astrobot is leaking the api keys and credentials. The source uses text placeholders and real value are entered into the terminal. Webex personal tokens expire after 12 hours which also helps security even though it might hurt convenience.I also noted that the input() shows typed keys on the screen which can be seen in the demo video.I replaced those with keys afterwards.

- How could your solution be improved in the future?  
I would use exact command matches and checking the length of city to reduce the amount of times api is called .I would also filter the /sky command just to display visible planets/bodies such as moon mars sun etc.
---

 **Tip:** Link your answers directly to your code and examples for higher marks.
### Notes

- Use official documentation for accuracy (e.g. developer.webex.com, locationiq.com or Mapbox, open-notify.org or other ISS API).
- Be prepared to explain your findings to your instructor or demo how you retrieved them using tools like Postman, Curl, or Python scripts.

---

###  Total: /40
