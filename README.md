# Module: BOMAU-weather
The `BOMAU-weather` module is a modification to the WB-weather module which was  designed  to complement the `WallberryTheme` module and displays the current weather and forecast. 

This started out as just an attempt to utilize the Australian Bureau of Meterology data in place of DarkSky data but due to the number of changes required I have spun it out into a modudle on its own. The Wallberry Theme is available from https://github.com/delightedCrow/WallberryTheme 

## Using the module

To use this module, add it to the modules array in the `config/config.js` file:
````javascript
modules: [
	{
		module: "BOMAU-weather",
		position: "bottom_bar",  // Highly suggested location
		config: {
			// See "Configuration options" for more information.
			forecastSource: "link to source data",
			stationID: "BOM StationID",
			
		}
	}
]
````

## Configuration options

The following properties can be configured:


| Option                      | Type    | Description
| ----------------------------|---------| -----------
| `roundTemp`                 | Boolean | Round temperature value to nearest integer. <br><br> **Possible values:** `true` (round to integer) or `false` (display exact value with decimal point) <br> **Default value:** `true`
| `language`                  | String  | What language to use. [Full language list available at DarkSky API docs (language parameter)](https://darksky.net/dev/docs#forecast-request). <br><br> **Possible values:** `en`, `nl`, `ru`, etc...<br> **Default value:** uses value of _config.language_
| `daysToForecast`            | Number  | How many days to forecast in weekly forecast. <br><br> **Possible values:** `0` - `8` <br> **Default value:** `4`
| `updateInterval`            | Number  | How often to fetch new weather data. (Milliseconds) <br><br> **Default value:** `600000` (10 minutes)
