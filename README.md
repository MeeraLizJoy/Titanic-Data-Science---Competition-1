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
