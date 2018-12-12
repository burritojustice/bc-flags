# Map of Flags of Municipalities of British Columbia

CBC Vancouver's Justin McElroy / @j_mcelroy ranked every single municipal flag in British Columbia in this [epic Twitter thread](https://twitter.com/j_mcelroy/status/1066885174112047104). 

Thread reader version here:
https://threadreaderapp.com/thread/1066885174112047104.html

I [turned it into a zoomable slippy map](https://burritojustice.github.io/bc-flags), and converted the rankings into emoji. Why? Because that's just what how you make maps in 2018.

![image of map](bc_flag_grey_gold.png)

mapmoji table:

|1|2|3|4|5|6|7|7.8|
|---|---|---|---|---|---|---|---|
| 😱| 😳| 😬| 🤔| 🙂| 😃| 😍| 😎 |

#Apologies:

- The map works on mobile, just tap on the emoji, but is more fun on a bigger screen with hover. 
- the popups are a little wonky if the icon is at the very top of the screen - sorry, the popup doesn't know how big the image will be and I am am bad at CSS. SOLUTION: scroll down and then over or click.
- Sorry if your OS doesn't have all these emoji, this map _cutting-edge_.

# How did I make this map?

- a great deal of regexing and strategic deleting turned the html of Justin's thread into a CSV
- I geocoded the CSV using the [batch geocoder](https://github.com/pelias/scripts-batch-search) from [Pelias](http://pelias.io). 
- I uploaded the CSV to [HERE XYZ](https://explore.xyz.here.com/) using [XYZ Studio](https://xyz.here.com/studio/).
- I used the table editor in XYZ Studio to fix a bunch of notes and data I regexed a little too hard
- I used XYZ Studio's map edit feature to nudge some of the points to better locations (because centroids of large municipalities are often not quite where the town is). 
- I made the map in [Tangram Play](https://tangram.city/play/?scene=https://raw.githubusercontent.com/burritojustice/bc-flags/master/scene.yaml#10.9898/48.5373/-123.4756), pulling the points in from the HERE XYZ API and using conditional formatting to convert scores to emoji. I displayed the map with [tangram.js](https://github.com/tangrams/tangram) top of a Refill basemap from [Nextzen](https://nextzen.org/).

# Notes:
- Oak Bay [was robbed](https://twitter.com/burritojustice/status/1068339114070597634). 

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr"><a href="https://twitter.com/j_mcelroy?ref_src=twsrc%5Etfw">@j_mcelroy</a> I mean come on top 30 at least look at the jaunty blue stripe <a href="https://t.co/N1FOuaLgco">https://t.co/N1FOuaLgco</a> <a href="https://t.co/px5HNGd4Yo">pic.twitter.com/px5HNGd4Yo</a></p> </blockquote>

![oak bay flag](https://pbs.twimg.com/media/DtOAwl_U0AAvwRB.jpg)
 
