# Book-Recommender-System


![147267701-b3d5fa41-6c69-4089-860f-16e0b10fef2f](https://user-images.githubusercontent.com/118175602/202086367-20980521-e166-4b20-ade2-b8e2bd03d6d1.png)

## Objective

The main objective is to create a book recommendation system for users. Recommender systems are really critical in some industries as they can generate a huge amount of income when they are efficient or also be a way to stand out significantly from competitors.

## Methods Used

- Descriptive Statistics

- Data Visualization

- Machine Learning

## Technologies

- Python

- Pandas

- Numpy

- Matplotlib

- Seaborn

- Scikit-learn

- Surprise

## Data

The Book-Crossing dataset comprises 3 files.

- Users : Contains the users. Note that user IDs (User-ID) have been anonymized and map to integers. Demographic data is provided (Location, Age) if available. Otherwise, these fields contain NULL values.

- Books : Books are identified by their respective ISBN. Invalid ISBNs have already been removed from the dataset. Moreover, some content-based information is given (Book-Title, Book-Author, Year-Of-Publication, Publisher), obtained from Amazon Web Services. Note that in the case of several authors, only the first is provided. URLs linking to cover images are also given, appearing in three different flavors (Image-URL-S, Image-URL-M, Image-URL-L), i.e., small, medium, large. These URLs point to the Amazon website.

- Ratings : Contains the book rating information. Ratings (Book-Rating) are either explicit, expressed on a scale from 1-10 (higher values denoting higher appreciation), or implicit, expressed by 0.

## Project Description

- EDA - Performed exploratory data analysis on numerical and categorical data.

- Data Cleaning - Missing value imputation,Outlier Treaatment

- Feature Selection - Used User-ID,ISBN and Books-Rating for model development.

- Model development - Tried Popularity based model and Collaborative filtering (Both Memory based and Model based).

## Needs of this project

- data exploration

- data processing/cleaning

- recommendation system developer

## Methods Used

### Popularity Based Approach
It is a type of recommendation system which works on the principle of popularity and or anything which is in trend. These systems check about the books which are in trend or are most popular among the users and directly recommend them.

For example, if a product is often purchased by most people then the system will get to know that that product is most popular so for every new user who just signed it, the system will recommend that product to that user also and chances become high that the new user will also purchase that.

Why Is this model relevant? The answer to this is the Cold-Start Problem. Cold start is a potential problem in computer-based information systems which involves a degree of automated data modelling. Specifically, it concerns the issue that the system cannot draw any inferences for users or items about which it has not yet gathered sufficient information. The cold start problem is a well known and well researched problem for recommender systems.

### Collaborative Filtering
It is considered to be one of the very smart recommender systems that work on the similarity between different users and also items that are widely used as an e-commerce website and also online movie websites. It checks about the taste of similar users and makes recommendations.

The similarity is not restricted to the taste of the user, moreover there can be consideration of similarity between different items also. The system will give more efficient recommendations if we have a large volume of information about users and items. There are various types of collaborative filtering techniques.

![147267186-e1033461-bdd2-445e-8426-2eb8f38f3778](https://user-images.githubusercontent.com/118175602/202088556-086af5c2-4c2a-456b-9f54-2b7634579fbd.png)

## Model Based Approach:

Model-based recommendation systems involve building a model based on the dataset of ratings. In other words, we extract some information from the dataset, and use that as a "model" to make recommendations without having to use the complete dataset every time. This approach potentially offers the benefits of both speed and scalability.

Model based collaborative approaches only rely on user-item interactions information and assume a latent model supposed to explain these interactions. For example, matrix factorisation algorithms consists in decomposing the huge and sparse user-item interaction matrix into a product of two smaller and dense matrices: a user-factor matrix (containing users representations) that multiplies a factor-item matrix (containing items representations). Matrix Factorization can be of two types :

### Non-Negative Matrix Factorization (NMF)

### Singular Value Decomposition (SVD)
## Memory Based Approach:

The main characteristics of user-user and item-item approaches is that they use only information from the user-item interaction matrix and they assume no model to produce new recommendations.

### User-User:
In order to make a new recommendation to a user, the user-user method roughly tries to identify users with the most similar “interactions profile” (nearest neighbours) in order to suggest items that are the most popular among these neighbours (and that are “new” to our user). This method is said to be “user-centred” as it represents users based on their interactions with items and evaluates distances between users.

### Item-Item:
To make a new recommendation to a user, the idea of the item-item method is to find items similar to the ones the user already “positively” interacted with. Two items are considered to be similar if most of the users that have interacted with both of them did it in a similar way. This method is said to be “item-centred” as it represents items based on interactions users had with them and evaluates distances between those items.

## Conclusions

● In EDA, the Top-10 most rated books were essentially novels. Books like The Lovely Bone and The Secret Life of Bees were very well perceived.

● Majority of the readers were of the age bracket 20-35 and most of them came from North American and European countries namely USA, Canada, UK, Germany and Spain.

● If we look at the ratings distribution, most of the books have high ratings with maximum books being rated 8. Ratings below 5 are few in number.

● Author with the most books was Agatha Christie, William Shakespeare and Stephen King.

● For modelling, it was observed that for model based collaborative filtering SVD technique worked way better than NMF with lower Mean Absolute Error (MAE) .

● Amongst the memory based approach, item-item CF performed better than user-user CF because of lower computation requirements .
