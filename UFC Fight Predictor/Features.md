We will use the data frame above to calculate the features for all the fights. We will calculate historical features about each fighter. Such as:

* **Probability of landing a significant strike**. This will be the number of significant strikes a fighter has landed over the number they have thrown.
* **Significant strike rate.** The rate at which a fighter attempts to land significant strikes. Preferably per second but could be given per round if necessary.
* **Probability of landing a strike**
* **Strike Rate**
* **Probability of landing a takedown.** A takedown is where one fighter wrestles the other fighter to the ground.
* **Takedown attempt rate.**
* **Takedown,Significant Strike and Strike defence probability**. The probability of defending the attack method based on historical fights.  
* **Knock down rate**. A knock down is when one fighter knocks anther one down with a strike. 
* **Win probability**
* **total number of fights**
* **Age**
* **How many title bouts the fighter has been in**
* **Network Centrality.** A network will be constructed using networkx and the an eigenvector centrality score score will be calculated for every fighter, we will start with katz centrality but may use some others later like PageRank. We will begin with creating a network for all the fighters and one for each weight class. For a fight we will consider each fighters score for the network of all fighters and their score in the weight class of the fights. 
* **Finnish rate**. In MMA finishing an opponent is when one fighter knocks out or taps out an opponent. Clearly a fighter has knocked out every opponent they have faced in the first round they are good fighter. This feature will be number of finishes over total fight time.
* **Current loss streak**
* **Current win streak** 


For training and testing it makes sense to split the fights chronologically rather than randomly. Training the algorithms on the oldest fights and testing them on more recent ones. 

Some other features we may include later are:
* **Reach difference**  A fighters reach is the distance between their fingertips when they hold the arms apart and parallel to the ground. Reach can approximate the distance a fighter can punch at.  
* **Height difference** Will give and indication who is punching with and who is punching against gravity. 

Lets work throw away any data we do not need to calculate the above features. 