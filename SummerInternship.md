# Summer Basketball Internship 2019

## Data Exploration
<1-3 setences of what the goal was>

### Cleaning the Data
First we identified 6 variables from the "messy" dataset that we thought were good predictors of scoring success (shot_clock, shot_type, three, fouled, distance, outcome); next, we isolated those columns of data in a separate dataframe. In order to contextualize the x and y coordinates that at first sight seemed like a jumble of numbers, we applied the .loc function to split the court into 4 general areas: left, right, center, and 3-pt territory; we applied the same .loc function to the shot clock column in order to categorize each shot taken as either a desperate shot, a standard shot, or a rushed shot. With our 8 variables placed in a new dataframe, we were then able to create graphs etc... to analyze the data.

### Exploring the Data
<1-2 sentences of the goal>

#### Shot-Type Based on Made Shots
<img width="472" alt="Screen Shot 2019-08-08 at 11 48 21 AM" src="https://user-images.githubusercontent.com/51301795/62717780-852b7800-b9d2-11e9-84cf-58dbb1dc7032.png">
  
This pie chart tells us that out of all the MADE shots during the 2018-19 NBA season, 47% of the makes were layups, 42% of the makes were jumpers, 6% of the makes were floaters(in between a jumper and a layup), 5% of the makes were post shots, and 0% of the makes were heaves. This analysis is expected because layups are attempted closest to the basket and thus have the highest percentage of going in. On the other hand, no heaves were made at all because they are desperation shots attempted extremely far from the basket(usually when the clock is winding down), thus making them nearly impossible to make. 


#### Shot-Type Based on Missed Shots
<img width="540" alt="Screen Shot 2019-08-13 at 1 34 14 PM" src="https://user-images.githubusercontent.com/51301795/63013337-db6c4100-be40-11e9-9e85-3d11a2e14f74.png">

This pie chart tells us that out of all the MISSED shots during the 2018-19 NBA season, 54% of the misses were jumpers while 33% of the misses were layups. This makes sense because jumpers (which include threes) are taken farther from the basket than layups but are attempted extremely often, thus making it the most commonly missed shot. At first it was very surprising to see that 33% of missed shots were layups since layups are presumably easy, close range shots (as opposed to heaves, for example, which you would think are a harder, more commonly missed shots). I predict that this is because layups are attempted in traffic most of the time, meaning that these shots are heavily contested by bigger defenders under the basket and thus have a great chance of being blocked or tipped (which equals a miss). Additionally, I assume that players draw the most fouls off of layups since since driving to the basket requires an immense amount of physicality; in other words, players miss layups more than you would think because they are under duress. I also speculate that players don't always attempt shots to score but rather to draw a foul, thus sending them to the free throw line for 2 (or 3) shots - after all, you have a better chance of making 2 uncontested, unhurried foul shots compared to a contested and likely off-balance jumper. This is yet another reason why jumpers and layups are so commonly missed.
