# IBM-Recommendation-Engine
As part of the Udacity Data Science Nanodegree, built a recommendation engine that performs rank-based filtering and Matrix Factorization to recommend articles to users.

For this project I will analyze the interactions that users have with articles on the IBM Watson Studio platform, and make recommendations to them about new articles I think they will like. Below you can see an example of what the dashboard could look like displaying articles on the IBM Watson Platform.

![image](https://github.com/user-attachments/assets/77f7bf8f-ef68-4411-b6e9-c31b5758d45c)


# Methodology
**I. Exploratory Data Analysis**

Before making recommendations of any kind, you will need to explore the data you are working with for the project. Dive in to see what you can find. There are some basic, required questions to be answered about the data you are working with throughout the rest of the notebook. Use this space to explore, before you dive into the details of your recommendation system in the later sections.

**II. Rank Based Recommendations**

To get started in building recommendations, you will first find the most popular articles simply based on the most interactions. Since there are no ratings for any of the articles, it is easy to assume the articles with the most interactions are the most popular. These are then the articles we might recommend to new users (or anyone depending on what we know about them).

**III. User-User Based Collaborative Filtering**

In order to build better recommendations for the users of IBM's platform, we could look at users that are similar in terms of the items they have interacted with. These items could then be recommended to the similar users. This would be a step in the right direction towards more personal recommendations for the users. You will implement this next.

**V. Matrix Factorization**

Finally, you will complete a machine learning approach to building recommendations. Using the user-item interactions, you will build out a matrix decomposition. Using your decomposition, you will get an idea of how well you can predict new articles an individual might interact with (spoiler alert - it isn't great). You will finally discuss which methods you might use moving forward, and how you might test how well your recommendations are working for engaging users.

# Observations
1. Cold Start Problem - Since the new user will have no interaction history with us, we cannot assign a similarity score to that user against other already-existing users. To solve this problem, we can either recommend to the user the most-interacted articles in the data OR perform a Content-Based Recommendation
   
![image](https://github.com/user-attachments/assets/f12a7f11-7b33-4288-ab5a-04436e0a3e0b)
 
2. Based on the graph above, it is evident that with the rise in latent features the accuracy of the training data increases upto a certain point (approx. 250), but the same is not true for test data where as soon as we start increasing latent features there is rise in drop in accuracy, however marginal.

As the quantity of data is very less, it automatically reduces the quality of data to be able to derive insights that can help us be certain with a greater confidence. To measure our performance in reality, we can track users click-through rate on our recommendations that will verify whether they like what we recommend or not.

# Acknowledgments
Thanks to Udacity for hosting this project and to the wonderful people at IBM for providing this dataset.

