# Weather

[![NPM][npm-image]][npm-url] [![Build Status][travis-image]][travis-url]

Weather is a module for obtaining weather information.

## Installation

```bash
npm install weather-js
```

## Usage

```javascript
var weather = require('weather-js');

// Options:
// search:     location name or zipcode
// degreeType: F or C

weather.find({search: 'San Francisco, CA', degreeType: 'F'}, function(err, result) {
  if(err) console.log(err);

  console.log(JSON.stringify(result, null, 2));
});
/*
[
  {
    "location": {
      "name": "San Francisco, CA",
      "lat": "37.777",
      "long": "-122.42",
      "timezone": "-8",
      "alert": "",
      "degreetype": "F",
      "imagerelativeurl": "http://blob.weather.microsoft.com/static/weather4/en-us/"
    },
    "current": {
      "temperature": "50",
      "skycode": "30",
      "skytext": "Partly Sunny",
      "date": "2017-03-05",
      "observationtime": "16:35:00",
      "observationpoint": "San Francisco, CA",
      "feelslike": "45",
      "humidity": "58",
      "winddisplay": "13 mph West",
      "day": "Sunday",
      "shortday": "Sun",
      "windspeed": "13 mph",
      "imageUrl": "http://blob.weather.microsoft.com/static/weather4/en-us/law/30.gif"
    },
    "forecast": [
      {
        "low": "47",
        "high": "59",
        "skycodeday": "11",
        "skytextday": "Rain",
        "date": "2017-03-04",
        "day": "Saturday",
        "shortday": "Sat",
        "precip": ""
      },
      {
        "low": "46",
        "high": "52",
        "skycodeday": "34",
        "skytextday": "Mostly Sunny",
        "date": "2017-03-05",
        "day": "Sunday",
        "shortday": "Sun",
        "precip": "40"
      },
      {
        "low": "47",
        "high": "56",
        "skycodeday": "28",
        "skytextday": "Mostly Cloudy",
        "date": "2017-03-06",
        "day": "Monday",
        "shortday": "Mon",
        "precip": "60"
      },
      {
        "low": "49",
        "high": "58",
        "skycodeday": "28",
        "skytextday": "Mostly Cloudy",
        "date": "2017-03-07",
        "day": "Tuesday",
        "shortday": "Tue",
        "precip": "10"
      },
      {
        "low": "52",
        "high": "62",
        "skycodeday": "32",
        "skytextday": "Sunny",
        "date": "2017-03-08",
        "day": "Wednesday",
        "shortday": "Wed",
        "precip": "10"
      }
    ]
  }
]
*/
```

## Notes

- It uses `weather.service.msn.com`

## License

Licensed under The MIT License (MIT)  
For the full copyright and license information, please view the LICENSE.txt file.

[npm-url]: http://npmjs.org/package/weather-js
[npm-image]: https://badge.fury.io/js/weather-js.svg

[travis-url]: https://travis-ci.org/devfacet/weather
[travis-image]: https://travis-ci.org/devfacet/weather.svg?branch=master
