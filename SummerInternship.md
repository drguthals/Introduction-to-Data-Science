# Summer Basketball Internship 2019

## Data Exploration
<1-3 setences of what the goal was>

### Cleaning the Data
First we identified 6 variables from the "messy" dataset that we thought were good predictors of scoring success (shot_clock, shot_type, three, fouled, distance, outcome); next, we isolated those columns of data in a separate dataframe. In order to contextualize the x and y coordinates that at first sight seemed like a jumble of numbers, we applied the .loc function to split the court into 4 general areas: left, right, center, and 3-pt territory; we applied the same .loc function to the shot clock column in order to categorize each shot taken as either a desperate shot, a standard shot, or a rushed shot. With our 8 variables placed in a new dataframe, we were then able to create graphs etc... to analyze the data.

### Exploring the Data
<1-2 sentences of the goal>

#### Shot-Type Based on Made Shots
<img width="472" alt="Screen Shot 2019-08-08 at 11 48 21 AM" src="https://user-images.githubusercontent.com/51301795/62717780-852b7800-b9d2-11e9-84cf-58dbb1dc7032.png">
  
This pie chart tells us that out of all the MADE field goals during the 2018-19 NBA season, 47% of the makes were layups, 42% of the makes were jumpers, 6% of the makes were floaters(in between a jumper and a layup), 5% of the makes were post shots, and 0% of the makes were heaves. This analysis is expected because layups are attempted closest to the basket and thus have the highest percentage of going in. On the other hand, no heaves were made at all because they are desperation shots attempted extremely far from the basket(usually when the clock is winding down), thus making them nearly impossible to make. 



#### Shot-Type Based on Missed Shots
<img width="540" alt="Screen Shot 2019-08-13 at 1 34 14 PM" src="https://user-images.githubusercontent.com/51301795/63013385-fdfe5a00-be40-11e9-8d46-d5ab73c1a6d6.png">

This pie chart tells us that out of all the MISSED field goals during the 2018-19 NBA season, 54% of the misses were jumpers while 33% of the misses were layups. This makes sense because jumpers (which include threes) are taken farther from the basket than layups but are attempted extremely often, thus making it the most commonly missed shot. At first it was very surprising to see that 33% of missed shots were layups since layups are presumably easy, close range shots (as opposed to heaves, for example, which you would think are a harder, more commonly missed shots). I predict that this is because layups are attempted in traffic most of the time, meaning that these shots are heavily contested by bigger defenders under the basket and thus have a great chance of being blocked or tipped (which equals a miss). Additionally, I assume that players draw the most fouls off of layups since since driving to the basket requires an immense amount of physicality; in other words, players miss layups more than you would think because they are under duress. I also speculate that players don't always attempt shots to score but rather to draw a foul, thus sending them to the free throw line for two (or three) shots - after all, you have a better chance of making two uncontested, unhurried foul shots compared to a contested and likely off-balance jumper. This is yet another reason why jumpers and layups are so commonly missed.
##### Future Graphs
It would be really interesting to know:
Based on one type of jump, what is the likelihood of close made vs miss and far made vs miss


#### Outcome Based on Three-Point Attempts
<img width="482" alt="Screen Shot 2019-08-14 at 3 10 46 AM" src="https://user-images.githubusercontent.com/51301795/63014629-d5c42a80-be43-11e9-802a-1662f68c8a6e.png">

This pie chart tells us that out of all the ATTEMPTED three-point field goals during the 2018-19 NBA season, 65% of the attempts were misses while 35% of the attempts were makes. This aligns with most people's predictions because a three-pointer is obviously farther from the basket than any other type of shot, thus making it harder to make. We can gather from the graph that the NBA league wide three-point shooting percentage is about 35% (.355 to be exact). A common misconception is that since only 35% of three-point field goal attempts were made, NBA players should strictly stick to attempting two-point field goals which are naturally closer to the basket. However, Over the last 20 years, NBA players have averaged 1.05 points per above-the-break three and 1.16 points per corner three. In contrast, players have averaged just 0.79 points per two-point attempt outside of the key. In other words, 100 mid-range jumpers will provide 79 points on average, while 100 above-the-break 3s would provide 105 points on average. This the reasoning behind many teams' recent shift towards shooting more threes and layups and avoiding mid-range jumpers which yield less points yet are almost equally hard to make. 



#### Shot-Clock Situation Based on Made Shots
<img width="522" alt="Screen Shot 2019-08-14 at 3 31 14 AM" src="https://user-images.githubusercontent.com/51301795/63014788-32274a00-be44-11e9-9d05-a26d8062dd97.png">

This pie chart tells us that out of all the MADE field goals during the 2018-19 NBA season, 50% of the makes were standard shots (taken between 8-16 seconds of having the ball), 28% of the makes were rushed shots (taken between 16-24 seconds of having the ball), and 19% of the makes were desperate shots (taken between 0-8 seconds of having the ball). As one would imagine, players find more shooting success when their team takes the time to settle into their offensive sets (which might create more space for the shooter etc...) without waiting until the last second which would put too much pressure on the shooter to actually make the shot. On the other hand, only 19% of the makes were desperation shots; this is understandable because opposing teams know to apply more defensive pressure as the clock winds down, causing the shooter to huck up a heavily contested, forced shot. Additionally, players are simply be more fatigued at the end of the play, causing them to miss last second shots. The rushed shot, however, presents an interesting case. One might think to him/herself: How was a whopping 28% of all made shots attempted within the first eight seconds of inbounding the ball all the way at the other end of the court? In fact, most of the shots we considered to be "rushed" were actually stolen in the back court right as the opposing team inbounded the ball, meaning that the player who stole the ball would simply have to dribble a few feet and lay the ball in the basket - a task that can easily be completed within eight seconds. 



#### Finding the Optimal Shooting Time
<img width="674" alt="Screen Shot 2019-08-14 at 4 03 09 AM" src="https://user-images.githubusercontent.com/51301795/63016586-e7f49780-be48-11e9-80cb-72c1fe6cedfd.png">

<img width="309" alt="Screen Shot 2019-08-14 at 4 04 38 AM" src="https://user-images.githubusercontent.com/51301795/63016528-c98e9c00-be48-11e9-9197-ceb5f2fd0942.png">
