# Goodreads Yearly Tracker
_"Is there a better motivation to hit my reading goals?"_

I got back into reading recently and to accompany it I started logging my reads in Goodreads. At the start of the year, Goodreads notified me of their feature to set a 2024 reading goal. I thought the idea was cool, and may motivate me to keep consistent with reading throughout the year, but unfortunately a simple count of the books I had read + a translated percentage based on my static goal turned out to not be very engaging.

So I thought it would be cool to look into other ways to visualizer my progress, and so I spent some free time one weekend writing code to turn my books read into a hike up Mt. Everest.

The idea is simple: books read this year and logged into Goodreads get queried for their page lengths, that page length is converted into an approximate word count (Goodreads doesn't store this data), and that word count is converted into an approximate distance which it would span. Those latter two conversions come from a combination of online opinions and random sampling measurements I took. 

There's a Jupyter notebook which steps through the entire process, with comments explaining my thoughts and the underlying data (Mt. Everest hike details, conversions, etc.). In the end, the journey gets plotted either as an "acclimization hike" or a "single hike". This was based on blogger details of hiking Mt. Everest, where the exact hike involved many stages of hiking to higher camps and then returning to base camp to better acclimate to the elevation gains. 

Here's an example of the outcome for an acclimization hike using my 2024 data as of 6/10/2024. The label is drawn at a different position because that's the actual spot in the hike including backtracking, whereas the trail gets drawn to the highest point reached. 

![image](https://github.com/thestroh/goodreads-goal-tracking/assets/78974700/72e19e93-efc5-4c5e-b08e-7d6b5a91fed6)

This image is "everest_reading_journey_acclim", and there's an accompanying verison for the solo hike ("everest_reading_journey_solo") which is a straight shot from base camp to summit that's easier to cover for more casual readers. 

everest_template_clean is the base image which the trail and label are drawn on, and "test2" is my non-renamed version for the edit of the template, removing some more icons to make it easier to analyze the trail using CV2. 

If you want to create a version for yourself, you can replace the user_id value in the notebook with the ID found on your own Goodreads profile URL. I was going to upload an API file with all of the functions, but querying from Goodreads can be pretty slow especially if you have a lot of books completed, so the notebook just functions better so you don't re-query if making changes. 

In the future I may return to this project to update the visualization, especially since the label is pretty crudely done, but for now it's a good framework that at least gives me the key data and visual for what I wanted. 
