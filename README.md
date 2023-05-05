# recommender-systems-project-1

This  project  is a content-based  recommender system  build on hotel data. The goal was to achieve the best HR@10 in the final  evaluation and to beat Amazon's  recommender. In order to do so data had to be preprocessed, user and item  features  prepared and the  recommender  had to be tuned and validated  using  multiple  methodes.  

  

### Data preprocessing  

Data preparation  contains  of adding, filtering out, aggregating  and bucking  data to get the most important  features and reduce the offer  space  size.  

  

### Preparing  user and item  features  

For user  features the one-hot encoding was used. Every  feature was taken  into  account but only  n values with the largest  number of occurrences  were  encoded  where n was based on the number of values  of  feature.  

  

For item  features one-hot encoding was used for every  feature. Duplicates of  item_id  were  dropped.  

  

 

### Preparing  recommender  

In fit  function  of the recommender  class  negative  interactions  were  generated, user_id and item_id was randomly  created  from defined  range in order for this  user and item to exist, then  it was checked  if the pair  is  in existing interactions, if not then  it was added to the list of negative  ones.   

  

In recommend  method  cartesian  product of users and items was created and scores  were  calculated. Best recommendtaions for every  user  were  added to the list.  

  

 

### Tuning  

Recommender  wast  tuned  using  three  algorithms. SVR method was not executed  beacuse  it was not efficient.  

  

  

The results of every  method  are as follows:  

  


#### LinearRegressionCBUIRecommender 

  ![image](https://user-images.githubusercontent.com/73062201/236559673-75c53818-5474-48ea-b271-cb7d31385830.png)


#### RandomForestCBUIRecommender 

  ![image](https://user-images.githubusercontent.com/73062201/236559786-eaede0dc-e0a3-431d-a74c-030a40ce556f.png)


#### XGBoostCBUIRecommender 

  ![image](https://user-images.githubusercontent.com/73062201/236559838-6c462578-c78c-4886-b10a-9e16c9a2623a.png)


  

## Final  result  

In final  evaluation amazon recommender was beaten.

![image](https://user-images.githubusercontent.com/73062201/236560103-6f751dfe-b6d8-4f0e-8c3c-6820efe7e141.png)

  

### Requirements to run the project: 

- install Anaconda, 

- install all used python libraries: 

        - numpy, 

        - pandas, 

        - hyperopt, 

        - matplotlib, 

        - seaborn. 
