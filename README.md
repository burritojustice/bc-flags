# Map of Flags of Municipalities of British Columboa

CBC Vancouver's Justin McElroy / @j_mcelroy ranked every single municipal flag in British Columbia in this [epic Twitter thread](https://twitter.com/j_mcelroy/status/1066885174112047104). 

Thread reader version here:
https://threadreaderapp.com/thread/1066885174112047104.html

I [turned it into a zoomable slippy map](https://burritojustice.github.io/bc-flags), and converted the rankings into emoji. Why? Because that's just what how you make maps in 2018.

Points to Emoji table:

|1|2|3|4|5|6|7|7.8|
|---|---|---|---|---|---|---|---|
| 😱| 😳| 😬| 🤔| 🙂| 😃| 😍| 😎 |

![image of map](https://github.com/burritojustice/bc-flags/blob/master/bc_flag_emoji_ranking_map.png)

(Sorry if your OS doesn't have all these emoji, this map _cutting-edge_.)

The map works on mobile, just tap on the emoji, but is more fun on a bigger screen with hover. Sorry if the popups sometimes stick above the top of the screen.

# How did I make this map?

- a great deal of regexing and strategic deleting turned the html of Justin's thread into a CSV
- I geocoded the CSV using the [batch geocoder](https://github.com/pelias/scripts-batch-search) from [Pelias](http://pelias.io). 
- I uploaded the CSV to [HERE XYZ](https://explore.xyz.here.com/) using [XYZ Studio](https://xyz.here.com/studio/).
- I used the table editor in XYZ Studio to fix a bunch of notes and data I regexed a little too hard
- I used XYZ Studio's map edit feature to nudge some of the points to better locations (because centroids of large municipalities are often not quite where the town is). 
- I made the map in [Tangram Play](https://tangram.city/play/?scene=https://raw.githubusercontent.com/burritojustice/bc-flags/master/scene.yaml#10.9898/48.5373/-123.4756), pulling the points in from the HERE XYZ API and using conditional formatting to convert scores to emoji. I displayed the map with [tangram.js](https://github.com/tangrams/tangram) top of a Refill basemap from [Nextzen](https://nextzen.org/).

