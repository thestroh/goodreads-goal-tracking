# Goodreads Yearly Tracker
_"Is there a better motivation to hit my reading goals?"_

I got back into reading recently and to accompany it I started logging my reads in Goodreads. At the start of the year, Goodreads notified me of their feature to set a 2024 reading goal. I thought the idea was cool, and may motivate me to keep consistent with reading throughout the year, but unfortunately a simple count of the books I had read + a translated percentage based on my static goal turned out to not be very engaging.

So I thought it would be cool to look into other ways to visualizer my progress, and so I spent some free time one weekend writing code to turn my books read into a hike up Mt. Everest.

The idea is simple: books read this year and logged into Goodreads get queried for their page lengths, that page length is converted into an approximate word count (Goodreads doesn't store this data), and that word count is converted into an approximate distance which it would span. Those latter two conversions come from a combination of online opinions and random sampling measurements I took. 

There's a Jupyter notebook which steps through the entire process, with comments explaining my thoughts and the underlying data (Mt. Everest hike details, conversions, etc.). In the end, the journey gets plotted either as an "acclimization hike" or a "single hike". This was based on blogger details of hiking Mt. Everest, where the exact hike involved many stages of hiking to higher camps and then returning to base camp to better acclimate to the elevation gains. 

Here's an example of the outcome for an acclimization hike using my 2024 data as of 6/10/2024. 

![image](https://github.com/thestroh/goodreads-goal-tracking/assets/78974700/72e19e93-efc5-4c5e-b08e-7d6b5a91fed6)

