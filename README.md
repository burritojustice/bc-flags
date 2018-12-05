# Map of Flags of Municipalities of British Columboa

CBC Vancouver's Justin McElroy / @j_mcelroy ranked every BC municipality's flag in this [epic Twitter thread](https://twitter.com/j_mcelroy/status/1066885174112047104). 

Thread reader version here:
https://threadreaderapp.com/thread/1066885174112047104.html

I [turned it into a zoomable slippy map](https://burritojustice.github.io/bc-flags), and converted the rankings into emoji. Because that's what you do.

|1|2|3|4|5|6|7|7.7|
|---|---|---|---|---|---|---|---|
| 😱| 😳| 😬| 🤔| 🙂| 😃| 😍| 😎 |

![iamge of map](https://github.com/burritojustice/bc-flags/blob/master/bc_flag_emoji_ranking_map.png)

(sorry if your OS doesn't have all these)

# How did I make this map?

- a great deal of regexing turned Justin's thread into a CSV
- I geocoded the CSV using [Pelias](http://pelias.io)
- I uploaded the CSV to the [HERE XYZ](https://explore.xyz.here.com/)
- I used the table editor in [XYZ Studio](https://xyz.here.com/studio/) to fix a bunch of the notes and scores I broke because I am bad at regex. (I also used Studio to nudge some of the points to better locations because label centroids of large municipalities are often not quite where the town is)
- I made the map in [Tangram](https://github.com/tangrams/tangram), pulling the geojson from the XYZ API and converted the scores to emoji, and displayed them on top of a Refill basemap from [Nextzen](https://nextzen.org/).

