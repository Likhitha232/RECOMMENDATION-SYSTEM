# RECOMMENDATION-SYSTEM

*COMPANY*: CODTECH IT SOLUTIONS

*NAME*: H LIKITHA

*INTERN ID*: CTO6DF2216

*DOMAIN*: MACHINE LEARNING

*DURATION*: 6 WEEKS

*MENTOR*: NEELA SANTOSH

The machine learning domain encompasses the recommendation system used in this task, which is based on collaborative filtering utilizing matrix factorization.  The Python programming language, which is popular for machine learning applications because of its readability, robust ecosystem, and simplicity of integration with data science libraries, was utilized for the complete implementation in the Jupyter Notebook platform.  Pandas, NumPy, Scikit-learn, and SciPy are the main libraries utilized in this project; they are all essential resources for data preparation, numerical computing, evaluation metrics, and matrix manipulation, respectively.  This code solely concentrates on traditional matrix factorization techniques, which have been at the heart of recommendation systems since the early 2000s, and does not rely on any other machine learning frameworks like TensorFlow or PyTorch. 

The MovieLens 100k dataset, one of the most widely used and standardized datasets for evaluating recommendation system models, was used in this implementation.  This dataset, which includes 100,000 user reviews of 1,682 different films, is freely accessible via GroupLens.  Four fields make up each record in the dataset: user ID, item ID (which represents a movie), assigned rating (ranging from 1 to 5), and timestamp.  However, the timestamp is removed during preprocessing because it is not required for the model's construction and evaluation of recommendations.  The fundamental principle of collaborative filtering is to forecast future preferences by leveraging the commonalities between users and objects based on their previous interactions (in this case, ratings).In other words, it makes the assumption that two individuals who have previously given comparable ratings to a number of films will probably also have similar tastes in the future.

 The procedure begins by loading the dataset into a Pandas DataFrame and converting it into a user-item matrix, in which a user is represented by each row, a movie by each column, and the related rating by each cell.  Many of the values in this matrix are missing (or zero) since not every user has reviewed every movie.  Singular Value Decomposition (SVD), a linear algebraic method that breaks down the original matrix into three lower-rank matrices, is used to perform matrix factorization in order to deal with this.  Latent associations between people and products are captured by this method by projecting them into a common feature space.  Prior to applying SVD, rating bias is normalized by subtracting each user's mean rating (some users may tend to rate higher or lower in general).  We get the expected ratings for every user-item pair after breaking down and rebuilding the matrix with less latent characteristics (in this case, 50).

 Train_test_split from Scikit-learn is used to divide the dataset into a training set and a testing set in order to assess the recommendation system's effectiveness.  Only the training data is subjected to matrix factorization.  In the evaluation, the predicted rating from the rebuilt matrix is used to make predictions for the user-item pairs in the test set. As assessment metrics, the Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE) are computed to ascertain how well the actual ratings match the expected ratings.  Better performance is shown by lower RMSE and MAE values; when employing basic SVD on the MovieLens 100k dataset, typical values are approximately 0.9 for RMSE and 0.7 for MAE.

 Lastly, a function to create Top-N movie recommendations for any user—aside from those the user has already rated—is also included in the code.  This feature simulates a recommendation list similar to those seen on real-world platforms like Netflix or Amazon by ranking the anticipated ratings for unrated goods and returning the top ones. A list of movie IDs and the corresponding expected scores is the output.  In conclusion, this system uses common Python tools to illustrate a collaborative filtering recommendation engine that is fully functioning.  It demonstrates the application of a simple yet effective machine learning method, such as matrix factorization, to tailored recommendations.  The method works rather well on benchmark datasets like MovieLens, is simple to apply, and is interpretable.

 *OUTPUT:*

 ![Image](https://github.com/user-attachments/assets/081e0edd-2354-48bb-8e42-ec3475c8d75c)
 
