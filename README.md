# Survival-rate-of-titanic-
Predicting Survival rate on the Titanic data set
### Scope
Using machine learning to create a model to predict to the passengers who survived
the Titanic shipwreck. There are two data sets i.e. training set and the test set.
In the training set we have both input and output data. The goal is to predict the
passenger survival rate in the unseen data. The data include features like survival, Age, Sex, sibsp, parch, cabin, embarked(
Boarding port). We can predict on features like what age group people with socio-economic status and gender survived.

### Data set link
https://www.kaggle.com/c/titanic/data

### Data set description
The data include features like survival, Age, Sex, sibsp, parch, cabin, embarked(
Boarding port). Pclass is the socio-economic representation where it is divided into
3 categories as Upper, Middle and Lower class. Age is fractional if it is less than 1.
Estimation of the age is done in the form of xx.5. Sibsp denotes relations with the
family like sibling dening brother and sister, Spouse for wife. parch is for parents
and children. Many kids were travelling only with a nanny, so parch will be 0 for
them. 

### Pipeline

- Step 1:  We will initially load the data into the database for analysis.
- step 2:  This data set contains few outliers, errors and redundancies. The null values are filled with zero.
- step 3:  There are certain variables which must be replaced with other variables.The features  which  are  useful  in  the  prediction  are selected.  Since  multiple  features  are  used  in  predicting  the output,  we  use  vector  assembler  function  to  featurize and transform these features into single column vector.
- step 4:  Random forest algorithm is chosen. This  analytical  form  of  prediction  is  based  on  the  concept of  several  decision-trees.  Boot-strapping (randomly) the data set is used for constructing the multiple trees. As random forest works on rulebased  approach,  it  is  recommended  to  use  for  classification.
- step 5: The performance of the model is checked using a Binary classification evaluator. The AUC-ROC curve is used to evaluate the performance of the model.  If every class is predicted correctly we will get 1.
