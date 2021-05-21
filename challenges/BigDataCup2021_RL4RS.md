## BigDataCup2021
http://bigdataieee.org/BigData2021/BigDataCupChallenges.html


## Kaggle Challenge
https://www.kaggle.com/c/bigdata2021-rl-recsys

## Description
In 2020, retail e-commerce sales worldwide amounted to 5.23 trillion US dollars and e-retail revenues are projected to grow to 6.54 trillion US dollars in 2022. Such rapid growth promises a great future for the worldwide e-commerce industry signifying a strong market and increased customer demand. Besides the huge increment of the traffic volume, there has been a rapid growth of various recommendation scenarios, including bundle recommendation (a set of items), sequential item recommendation, and many others. It is worth exploring the various challenges that the modern e-commerce industry faces today. Most current e-commerce and retail companies build their recommender systems by implementing supervised learning based algorithms on their websites. The recommender systems are designed to maximize immediate user satisfaction in a greedy manner. However, the item-wise greedy recommendation strategy is imperfect fitting to the real recommendation system. With more and more new upcoming recommendation scenarios, more and more challenges have to be solved. For instance, in sequential recommendation scenarios, traditional methods often consider different ranking steps in a session to be independent and fail to maximize the expected accumulative utilities in a recommendation session. Moreover, in the news feed recommendation or bundle recommendation, the conversion rate of an item does not solely depend on itself. If an item is surrounded by similar but expensive items, the likelihood of buying it increases, known as the decoy effects. However, the possible combinations of all the items can be billions, which is an NP-hard problem and less explored in traditional supervised learning. To deal with these challenges, recent researches resort to adopting reinforcement learning for recommendations, in which the recommendation process is formulated as a sequential interaction between the user (environment) and the recommendation agent (RL agent). Reinforcement learning is a promising technology since the RL paradigm is inherently suitable for optimizing long-term user satisfaction directly, exploring the combinatorial space, and solving multi-step decision-making problems.

Thus, understanding how to build the RL-based recommendation system is practical and has a deep influence on the development of e-commerce platforms. To help tackle these challenges and further nourish the development in this field, we propose the following competing tasks, recall for reinforcement learning based recommender system challenge.

Specifically, we are motivated by one of the most popular games released by NetEase Games for providing an online item recommendation service. This item recommendation task is characterized by its mid-dimensional action spaces (roughly 400 item candidates after reducing) and special interaction rules. As is shown in Figure 1, for each user request, the recommendation engine will respond with 3 item lists (3 items per list), and the next item list is locked until the items of the current list are sold out. The users' response depends on not only the current item but also the items of the next list. This item recommendation problem can be naturally formalized as a multi-step decision-making problem in which the agent recommends an item or an item list in each step.

So, our goal is to recommend nine items for each user request to maximize the aggregated rewards. Because other user satisfaction indicators are difficult to quantify, here we define the reward as the sum of the users' purchase amount of the nine items. An obvious baseline is to recommend the users' most likely items in each item list, but this strategy does not take into account the relationship between different item lists and cannot achieve the optimal solutions.

![Figure 1](https://cdn.mathpix.com/snip/images/S9UF6fch8HhiTH0pJnFvbp74oRYdnpc1MJA9zl4xxeA.original.fullsize.png)


Remarks:
+ There are no overlap users between the test set and the train set. So the winning solutions need to avoid the over-fitting problem (reinforcement learning algorithms are prone to over-fitting).
+ The training data is collected across three months and includes several sales campaigns (release new items). The test data is provided as a real-time reinforcement learning environment API. Simply speaking, the environment is a user purchase simulator trained by the data ten times the size of the training data. The test environment is only used to evaluate the submission and not accessible to participants. 
+ compare to the billions of possible combinations, the training data only covers limited state-action space. It means the RL algorithms may respond to unseen state-action confidently but falsely.
+ We provide content features of the items as well as anonymized user features, to help the participants explore solutions that are capable of handling the under-explored items well.


## Track I Leaderboard
Please refer to Kaggle Page: https://www.kaggle.com/c/bigdata2021-rl-recsys/leaderboard

## Track II Leaderboard
We will update the Track II Leaderboard every day. The submission result may be delayed by at most one day.

| Email Name | Score | Entries |
| :--- | :--- | :--- |
| null | 0 | 0 |