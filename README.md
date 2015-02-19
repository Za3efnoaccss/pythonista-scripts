# pythonista-scripts
Useful scripts to be run in Pythonista for iOS.  Kudos to [cclause](https://github.com/cclauss) for line by line code cleanup and helpful comments on improving these scripts.

- **Search IMDB.py** - A script that I find useful to quickly look up info on a movie title or a TV series.  The results of the query are displayed on the console screen and a Markdown version is copied to the clipboard for pasting to a text editor, etc.

- **PhotosToDropbox.py** - A script that lets you select multiple photos from the iPhone camera roll, resize & geo-tag them, and upload them to Dropbox where they are renamed and organized based on the date and time they were taken.  The cool part is that the script will preserve the metadata of the original photo if desired, using the Pexif module to read the metadata from the original and write it back to the resized copy.  The Pexif module can be imported into Pythonista by simply copying pexif.py into the Pythonista script directory. The Pexif module can be found [here](https://github.com/bennoleslie/pexif).

- **WeatherAnywhere.py** - This script was inspired by @cclaus's script located [here](https://github.com/cclaus/weather_where_you_are.py) and uses the weather api from www.openweathermap.org.  The script displays all it's information on the console screen, ideally suited for an iPhone in portrait orientation. The only graphics shown are weather icons (png files) illustrating the forecast, all available on the openweathermap website. Lots of weather info is provided in text, including forecast, humidity, pressure, temperature, precipitation amounts, wind speed, and wind chill. The info is in imperial units, but could easily be changed to metric via a flag in the url. The script makes use of a csv file, 'cities.csv', to be located in the same folder as the script, and 12 png files that display weather types, also located in the script's folder. The csv file can contain popular local, regional, national and international cities of your choosing, including their country and ID's.  The file is easily editable with the Pythonista editor. The city ID's are important to target a specific city's weather, as the api does not consider the state the city is located in, only the country. The list of city ID's is located [here](http://openweathermap.org/help/city_list.txt). I've included a sample csv file in this repository. The conversion functions used in the script were taken from [here](http://jim-easterbrook.github.io/pywws/doc/en/html/_modules/pywws/conversions.html). This script would be a good candidate for a ui.

- **WeatherAnywhere\cities.csv** - A sample csv file for 'WeatherAnywhere.py'.  Put it in the same folder as the script.
