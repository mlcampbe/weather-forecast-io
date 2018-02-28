# Weather Forecast-IO
A Ubersicht widget to display the current weather for a location along with a 3-day forecast. By default the widget fetches the currently
conditions and forecast for the next 3 days and displays them as in the 1st screenshot below. However, when the NWS issues any type
weather alert then the widget changes to show an alert icon with the severe alert details/description as seen in the 2nd screenshot below.

# Install
Edit the index.coffee and review/modify the following items:
1) The "iconSet" variable on the first line. This is the main weather icon that is displayed. Take a look at the folders in the "images" folder and decide
which you like best.
2) Edit the "command" on line 7 to set your forecast.io API key. Visit https://darksky.net/dev to register and generate a free API key. Note that the free
key allows up to 1000 calls per day. Be sure to set the refreshFrequency appropriately.
3) In the "command" call on line 7 set the latitude and longitude of the location for which the weather should be displayed.

After edits the command should look like:
command: 'curl -s https://api.forecast.io/forecast/your-api-key/latitude,longitude?exclude=minutely,hourly,flags'

# Customization
There are several iconSets delivered to choose between. The default is "stardock" but the widget also includes the
below as well. Review these to see what you wish to use.
Aqua, Climacons-Color, Grzanka, TWCNew, Yahoo, tick, Climacons, Crystal, Reall, Vclouds

If you want to build your own icon set from other icons make sure to name them with the same names as the delivered icons.

# Screenshots

![Alt text](/screenshot.png?raw=true)

![Alt text](/alert.png?raw=true)
