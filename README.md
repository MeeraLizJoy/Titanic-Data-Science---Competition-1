# Titanic-Data-Science---Competition-1

# Project Name: Titanic Machine Learning from Disaster


----
# Project Objective: 
The sinking of the Titanic is one of the most infamous shipwrecks in history.

On April 15, 1912, during her maiden voyage, the widely considered “unsinkable” RMS Titanic sank after colliding with an iceberg. Unfortunately, there weren’t enough lifeboats for everyone onboard, resulting in the death of 1502 out of 2224 passengers and crew.

While there was some element of luck involved in surviving, it seems some groups of people were more likely to survive than others.

In this challenge, we ask you to build a predictive model that answers the question: “what sorts of people were more likely to survive?” using passenger data (ie name, age, gender, socio-economic class, etc).



----
# Data Sourcing: 
Kaggle Titanic - Machine Learning from Disaster Dataset - https://www.kaggle.com/competitions/titanic/overview

----
# Attributes
1. PassengerId: Unique identifier for each passenger

2. Survived: Survival status (0 = No, 1 = Yes)

3. Pclass: Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)

4. Name: Passenger's name

5. Sex: Gender of the passenger

6. Age: Age of the passenger

7. SibSp: Number of siblings/spouses aboard the Titanic

8. Parch: Number of parents/children aboard the Titanic

9. Ticket: Ticket number

10. Fare: Passenger fare

11. Cabin: Cabin number

12. Embarked: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)


----
# Data Transformation:
1. Creating new feature from existing one (Title)
2. Converting Titles to ordinal values
3. Drop the Name feature
4. Converting categorical feature Sex to ordinal values
5. Completing numerical continous features
6. Created Age Band field and found correlation with survival
7. converting the age bands to ordinal values
8. drop AgeBand feature
9. Creating new feature from existing one (FamilySize, IsAlone)
10. Drop FamilySize, Parch, SibSp
11. Created Fare Band field and found correlation with survival
12. Converting the fare band to numeric values
13. Droping Fare Band field



----
# Findings and Recommendations:
how representative is the training dataset of the actual problem domain? - 

total samples are 891 - 40% of actual no.of passengers on board the Titanic(2224)

Survived - catagorical feature with values 0 and 1


distribution of categorical features:-

1. Names - all unique
2. Sex  - 2 variables -  more than 65% male (top = male, freq = 577, count = 891)
3. Cabin - has duplicates across sample. several passengers shared cabins 
4. Embarked - 3 possible values - most people with S


Assumptions - 

1. find correlation between all features with Survival.
2. Complete the Age feature since it will definitly correlate with Survival
3. Complete Embarked
4. Drop Ticket since there is a lot of duplication
5. Drop Cabin due to duplication and null values
6. Drop PassengerId sine it does not correlate to survival
7. Drop Name since it does not necessarily correlate to survival


1. Create column Family from Parch and SibSp to find the no.of families on board
2. Extract titles of the people from the Name column


1. Woman were more likely to be survived (Sex = female)
2. Children were more likely to be survived (Age < ?)
3. Upper class passengers were more likely to be survived (Pclass = 1)


Analysing the assumptions - 

1. Pclass - signifacant correlation ( > 0.5) among Pclass = 1 and Survived. therefore include Pclass in the model.
2. Sex - sex = female has high survival rate (>0.74).
3. Parch and SibSp has 0 correlation for some values. So derive some other features from these features.



From visualization- 

Age - 

      a. Infants Age <= 4 had high survival rates
      b. Oldest passenger ( Age = 80) survived
      c. Large number of people in 15-35 years did not survive
      d. most of the passengers were 15 - 35 years of age
      

So we have to include Age in the model.
Complete the Age will null vales
create Age bands


Pclass - 
       a. Pclass = 3 had most of the passengers , most did not survive.
       b. infant class in Pclass = 2 and Pclass = 3 mostly survived.
       c. Most people in Pclass = 3 survived

Include Pclass for model making
  
Embarked, Sex- 

       a. Females had much higher rate of survival
       b. Exception in Embarked = C where men had more rate of survival

Add Sex feature for model training
Complete and add Embarked feature for model training


correlating categorical and numerical features

      a. Port of embarkation correlates to survival
      b. Higher fare paying passenger had better survival

Drop features - Ticket, Cabin in train_df, and Ticket in test_df

Making new feature from Name - 

Extract Title from Name feature - make Title feature ordinal and drop the Name feature

Make Sex feature categorical

Completing numerical continous features - 

using other correlated features.

Correlation among Age, Gender, and Pclass

Guess Age values using median values of Age across sets of Gender and Pclass.

making Age bands

converting age bands into ordinal values

Drop AgeBand feature

Making new feature from Parch and SibSp - 
FamilySize, IsAlone

Drop Parch, SibSp, FamilySize

Making Fare Band field and converting it to ordinal values
