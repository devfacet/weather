## Weather

[weather](http://github.com/cmfatih/weather) is a Node.js module for 
obtaining weather information.  

[![Build Status][travis-image]][travis-url] | [![NPM][npm-image]][npm-url]
---------- | ----------

### Installation

For latest release
```
npm install weather-js
```

For HEAD
```
git clone https://github.com/cmfatih/weather.git
```

### Usage

#### Test
```
npm test
```

#### Examples

```javascript
var weather = require('weather');

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
      "zipcode": "94109",
      "lat": "37.7835152",
      "long": "-122.4169334",
      "timezone": "-7",
      "alert": ""
    },
    "degreetype": "F",
    "current": {
      "temperature": "68",
      "skycode": "32",
      "skytext": "Clear",
      "date": "2014-06-04",
      "observationtime": "16:53:00",
      "observationpoint": "Oakland, Metro Oakland International Airport",
      "feelslike": "68",
      "humidity": "55",
      "winddisplay": "14 mph WNW",
      "day": "Wednesday",
      "shortday": "Wed",
      "windspeed": "14"
    },
    "forecast": [
      {
        "low": "53",
        "high": "69",
        "skycodeday": "30",
        "skytextday": "Partly Cloudy",
        "date": "2014-06-04",
        "day": "Wednesday",
        "shortday": "Wed",
        "precip": "0"
      },
      {
        "low": "54",
        "high": "67",
        "skycodeday": "28",
        "skytextday": "Mostly Cloudy",
        "date": "2014-06-05",
        "day": "Thursday",
        "shortday": "Thu",
        "precip": "0"
      },
      {
        "low": "53",
        "high": "67",
        "skycodeday": "30",
        "skytextday": "Partly Cloudy",
        "date": "2014-06-06",
        "day": "Friday",
        "shortday": "Fri",
        "precip": "0"
      },
      {
        "low": "54",
        "high": "74",
        "skycodeday": "32",
        "skytextday": "Sunny (Clear)",
        "date": "2014-06-07",
        "day": "Saturday",
        "shortday": "Sat",
        "precip": "0"
      },
      {
        "low": "54",
        "high": "76",
        "skycodeday": "32",
        "skytextday": "Sunny (Clear)",
        "date": "2014-06-08",
        "day": "Sunday",
        "shortday": "Sun",
        "precip": "0"
      }
    ]
  }
]
*/
```

### Notes

* It uses `weather.service.msn.com`

### Changelog

For all notable changes see [CHANGELOG.md](https://github.com/cmfatih/weather/blob/master/CHANGELOG.md)

### License

Copyright (c) 2014 Fatih Cetinkaya (http://github.com/cmfatih/weather)  
Licensed under The MIT License (MIT)  
For the full copyright and license information, please view the LICENSE.txt file.

[npm-url]: http://npmjs.org/package/weather-js
[npm-image]: https://badge.fury.io/js/weather-js.png

[travis-url]: https://travis-ci.org/cmfatih/weather
[travis-image]: https://travis-ci.org/cmfatih/weather.svg?branch=master