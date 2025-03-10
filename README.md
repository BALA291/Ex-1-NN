<H3>BALAMURUGAN B</H3>
<H3>REGISTER NUMBER:212222230016</H3>
<H3>EX. NO.1</H3>
<H3>DATE: 24-02-24</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
```
#IMPORT THE REQUIRED LIBRARIES
import pandas as pd
from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import train_test_split

#READ THE DATASET
df=pd.read_csv("/content/Churn_Modelling.csv", index_col="RowNumber")
df

#REMOVE THE UNWANTED COLUMNS USING DROP OPERATION
df.drop(['CustomerId'],axis=1,inplace=True)
df.drop(['Surname'],axis=1,inplace=True)
df.drop('Age',axis=1,inplace=True)
df.drop('Geography',axis=1,inplace=True)
df.drop('Gender',axis=1,inplace=True)
df

#CHECK FOR THE NULL VALUES
df.isnull().sum()

#CHECK FOR DUPLICATED VALUES
df.duplicated()

#DESCRIBE THE DATASET
df.describe()

#PREPROCESSING THE DATASET
scaler=StandardScaler()
df1=pd.DataFrame(scaler.fit_transform(df))
df1

#Allocating X and Y attributes
x=df1.iloc[:,:-1].values
x
y=df1.iloc[:,-1].values
y

#SPLIT THE DATASET INTO TRAINING AND TESTING DATA
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2)
print(x_train)
print(len(x_train))
print(x_test)
print(len(x_test))
```


## OUTPUT:

### DATASET
![DATASET](https://github.com/BALA291/Ex-1-NN/assets/120717501/081b4f21-9b40-40aa-a61d-78a36363ebcb)

### AFTER DROP OPERATION
![drop](https://github.com/BALA291/Ex-1-NN/assets/120717501/cbd01046-2f82-4cf2-9470-c4f9897aa817)

### CHECK NULL VALUES
![null values](https://github.com/BALA291/Ex-1-NN/assets/120717501/784d9de7-b071-4645-a9ed-b50226ff3f1f)

### DESCRIBE DATA
![described](https://github.com/BALA291/Ex-1-NN/assets/120717501/50361816-fa50-46bd-b81b-d27bb97445d4)

### PREPROCESSING
![preprocessed data](https://github.com/BALA291/Ex-1-NN/assets/120717501/cce4e7a2-28f5-45ce-a3db-e364b251f992)

### ALLOCATE X AND Y VALUES
![x and y values](https://github.com/BALA291/Ex-1-NN/assets/120717501/3a6e466d-dc72-4b04-9ccc-d1b12518c509)

### SPLIT INTO TRAINING AND TESTING DATA
![splitvalue](https://github.com/BALA291/Ex-1-NN/assets/120717501/3fc60cd9-cd6a-402a-9120-5c916e910299)





## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


