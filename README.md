# Map of Flags of Municipalities of British Columboa

CBC Vancouver's Justin McElroy / @j_mcelroy ranked every single municipal flag in British Columbia in this [epic Twitter thread](https://twitter.com/j_mcelroy/status/1066885174112047104). 

Thread reader version here:
https://threadreaderapp.com/thread/1066885174112047104.html

I [turned it into a zoomable slippy map](https://burritojustice.github.io/bc-flags), and converted the rankings into emoji. Because that's what you do.

|1|2|3|4|5|6|7|7.8|
|---|---|---|---|---|---|---|---|
| 😱| 😳| 😬| 🤔| 🙂| 😃| 😍| 😎 |

![image of map](https://github.com/burritojustice/bc-flags/blob/master/bc_flag_emoji_ranking_map.png)

(sorry if your OS doesn't have all these)

# How did I make this map?

- a great deal of regexing turned the HTML of Justin's thread into a CSV
- I geocoded the CSV using [Pelias](http://pelias.io)
- I uploaded the CSV to [HERE XYZ](https://explore.xyz.here.com/)
- I used the table editor in [XYZ Studio](https://xyz.here.com/studio/) to fix a bunch of data I broke because I am bad at rege (I also used Studio to nudge some of the points to better locations because centroids of large municipalities are often not quite where the town is). 
- I made the map in [Tangram Play](https://tangram.city/play/?scene=https://raw.githubusercontent.com/burritojustice/bc-flags/master/scene.yaml#10.9898/48.5373/-123.4756), pulling the points in from the HERE XYZ API and using conditional formatting to convert scores to emoji. I displayed the map with [tangram.js](https://github.com/tangrams/tangram) top of a Refill basemap from [Nextzen](https://nextzen.org/).

