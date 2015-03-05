# pythonista-scripts
Useful scripts to be run in Pythonista for iOS.  Kudos to [@cclauss](https://github.com/cclauss) for line by line code cleanup and helpful comments on improving these scripts.

- **Search IMDB.py** - A script that I find useful to quickly look up info on a movie title or a TV series.  The results of the query are displayed on the console screen and a Markdown version is copied to the clipboard for pasting to a text editor, etc.

- **PhotosToDropbox.py** - A script that lets you select multiple photos from the iPhone camera roll, resize & geo-tag them, and upload them to Dropbox where they are renamed and organized based on the date and time they were taken.  The cool part is that the script will preserve the metadata of the original photo if desired, using the [Pexif module](https://github.com/bennoleslie/pexif) to read the metadata from the original and write it back to the resized copy.  The Pexif module can be imported into Pythonista by simply copying pexif.py into the Pythonista script directory.

- **WeatherAnywhere.py** - This script was inspired by @cclauss' script '[weather_where_you_are.py](https://github.com/cclauss/weather_where_you_are)' and uses the [weather api](http://openweathermap.org/api) from www.openweathermap.org.  The script displays all it's information on the console screen, ideally suited for an iPhone in portrait orientation. The only graphics shown are weather icons (png files) illustrating the forecast, all available on the openweathermap website. Lots of weather info is provided in text, including forecast, humidity, pressure, temperature, precipitation amounts, wind speed, and wind chill. The info is in imperial units, but could easily be changed to metric via a flag in the url. The script makes use of a csv file, 'cities.csv', to be located in the same folder as the script, and 18 png files that display weather types, also located in the script's folder. The csv file can contain popular local, regional, national and international cities of your choosing, including their country and ID's.  The file is easily editable with the Pythonista editor. The [city ID's](http://openweathermap.org/help/city_list.txt) are important to target a specific city's weather, as the api does not consider the state the city is located in, only the [country](http://www.geonames.org/countries/). I've included a sample csv file in this repository. The conversion functions used in the script were taken from [here](http://jim-easterbrook.github.io/pywws/doc/en/html/_modules/pywws/conversions.html). This script would be a good candidate for a ui.

- **WeatherAnywhere\cities.csv** - A sample csv file for 'WeatherAnywhere.py'.  Put it in the same folder as the script.

- **WeatherAnywhereScene.py** - Inspiration behind this was @cclauss's script,'WeatherAnywhereView.py in this
repository. I wanted to be able to add weather icons and have them scroll with the text, so a scene seemed to be the
best answer.  This script allows scrolling the scene by inertia.  A basic scrolling example was created by Dalorbi on the forums at: http://omz-software.com/pythonista/forums/discussion/213/scrolling-in-scene-module/p1
Ability for scrolling the scene with inertia was added by [hroe](https://gist.github.com/henryroe/6724117).
Known Issues: Line and image placements are hard coded so they don't auto adjust if text size is changed from the current 12 pts.  Increasing text size results in missing text for the last 2 days of extended forecast.
