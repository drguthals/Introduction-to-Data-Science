# Basketball Summer Internship 2019

## Data Exploration
<1-3 setences of what the goal was>

### Cleaning the Data
First we identified 6 variables from the "messy" dataset that we thought were good predictors of scoring success (shot_clock, shot_type, three, fouled, distance, outcome); next, we isolated those columns of data in a separate dataframe. In order to contextualize the x and y coordinates that at first sight seemed like a jumble of numbers, we applied the .loc function to split the court into 4 general areas: left, right, center, and 3-pt territory; we applied the same .loc function to the shot clock column in order to categorize each shot taken as either a desperate shot, a standard shot, or a rushed shot. With our 8 variables placed in a new dataframe, we were then able to create graphs etc... to analyze the data.

### Exploring the Data
<1-2 sentences of the goal>

#### <Shot-Type Based on Made Shots>
<img width="472" alt="Screen Shot 2019-08-08 at 11 48 21 AM" src="https://user-images.githubusercontent.com/51301795/62717780-852b7800-b9d2-11e9-84cf-58dbb1dc7032.png">
  
This pie chart tells us that out of all the MADE shots during the 2018-19 NBA season, 47% of the makes were layups, 42% of the makes were jumpers, 6% of the makes were floaters(in between a jumper and a layup), 5% of the makes were post shots, and 0% of the makes were heaves. This analysis is expected because layups are attempted closest to the basket and thus have the highest percentage of going in. On the other hand, no heaves were made at all because they are desperation shots attempted extremely far from the basket(usually when the clock is winding down), thus making them nearly impossible to make.
