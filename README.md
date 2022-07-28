

![enter image description here](https://kaggle2.blob.core.windows.net/datasets-images/18/18/default-backgrounds/dataset-cover.jpg)
#  K-NN on Amazon Fine Food Reviews
Analyze ~500,000 food reviews from Amazon

>**About this Dataset**
### Context
This dataset consists of reviews of fine foods from amazon. The data span a period of more than 10 years, including all ~500,000 reviews up to October 2012. Reviews include product and user information, ratings, and a plain text review. It also includes reviews from all other Amazon categories
### Contents
-   Reviews.csv: Pulled from the corresponding SQLite table named Reviews in database.sqlite  
    
-   database.sqlite: Contains the table 'Reviews'  
      
    

Data includes:  
- Reviews from Oct 1999 - Oct 2012  
- 568,454 reviews  
- 256,059 users  
- 74,258 products  
- 260 users with > 50 reviews

>### Table of Contents

 1. Loading the dataset
 2. Pre-processing the dataset
 3. Feature engineering
 	* Review Text -->Text Vector
 4. K-NN with different hyperparameter
 5. Accuracy

>### Output Sample

*********k-fold knn (n_neighbors=k , weights='uniform') ***********
  ************* using k-fold to find best K-value ******************* 
    best accuracy is 88.97500048734379 on cv datatset using 10 fold at k-value 7
    genearalisation accuracy on best k-value at k = 7 is accuacy = 0.8746
			 
