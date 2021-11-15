# Flight_Price_Prediction

#### ➡️ This machine learning model predict the price of the Flight ticket using some parameters

## 👉 Parameters
#### 1⃣ Airline name 
#### 1⃣ Source city
#### 1⃣ destination city
#### 1⃣ departure Time & Date
#### 1⃣ Arival Time & Date

<br>

## 👉 About Data :-

#### ➡️ The Data was collected from the <a href="https://www.kaggle.com/nikhilmittal/flight-fare-prediction-mh/">Kaggle</a>.
#### ➡️ There are 2 xlsx files for train data & test data.
#### ➡️ The train dataset contain 11 columns and 10.7k rows and the test dataset contains 10 columns and 2k rows.

<br>

## 👉 Data Cleaning :-
#### 🔶 As a 1st stap of data cleaning I've performed the shorting on columns like "Airline", "Source". "Destination" of  both datastes in <a href="https://docs.google.com/spreadsheets/d/1o-7FhCs56fJf07h9PSBM2y5abIVCALyo1uTFCNdhfK4/edit#gid=64045463"> google sheet </a>.

![shorting](https://user-images.githubusercontent.com/75326769/141683825-c151a7ca-aaa4-4ccb-990e-7182936782fe.png)

#### 🔶 After that, there is an airline named "Jet airways" & "Jet airways Business" which is no longer in india so we don't need that data, for that I followed the below steps...

<br>
 
#### 🔹 step 1 :  Select the column and Create the filter, in a filter select the Jet Airway and Jet Airway Business and clock OK.

![filter1](https://user-images.githubusercontent.com/75326769/141692819-21166277-8e30-432e-92eb-82e83dee4c1c.png)

#### 🔹 step 2 :  After click OK select the rows which displayed after flter. and delet the selected row.

![filter 2](https://user-images.githubusercontent.com/75326769/141693604-9a156e3b-b62a-4536-bd55-9b53edf2e2f9.png)

#### 🔹 step 3 :  After deleting the rows click on filter icon and removeit.  

![filter3](https://user-images.githubusercontent.com/75326769/141693738-bb92f74f-4223-4d47-bf1d-be624b259540.png)

## 👉 EDA part :-

#### 🔸 step 1 : In EDA part, first of all we find some odd columns which neet to be fixed, colimns like "Date_of_journey", "dep_time", "Arrival_time".

![EDA 1](https://user-images.githubusercontent.com/75326769/141733110-ba83c430-f546-4c64-bb4b-1930856e40b8.png)

#### 🔸 step 2 :  For the "Date_of_jorney" I've create one function named "date" and and using (pd.to_datetime) Picked the journey bay and journey month from it and drop the Date_of_jorney column.

![EDA 2](https://user-images.githubusercontent.com/75326769/141734085-bd441b94-7863-4e83-a95f-6ef2a117489a.png)

#### 🔸 step 3 : There are two columns with the same formats name "Dep_Time", "Arrival_Time". to solve this I've Picked the Dep_hours and Dep_min and, Arrival_hours and Arrival_min using same (pd.to_datetime) adn droped bothe the columns.

#### For Dep_Time :
![EDA 3](https://user-images.githubusercontent.com/75326769/141736683-572ce0a0-257a-41b2-8052-cc51181b206a.png)

#### Fro Arrival_Time :
![EDA 4](https://user-images.githubusercontent.com/75326769/141736780-0e06af9f-3297-4aef-a04f-6b9027f5a950.png)


#### 🔸 step 4 : Picking the hours and minutes from the "Duration" coloumn
![EDA 5](https://user-images.githubusercontent.com/75326769/141746227-1b144ebe-5814-4478-b22c-28e57dc0ee5e.png)


## 👉 Select the Algorithm :-
![Screenshot 2021-11-15 135539](https://user-images.githubusercontent.com/75326769/141747405-ccafe4e7-071f-4192-a68a-ff4a1d04cdfc.png)

#### -> As we see in this comparision table the "DecisionTreeRegressor" performing very well on the dataset
![algo](https://user-images.githubusercontent.com/75326769/141749087-9cd07037-b899-4d49-9f61-418aef964bad.png)

 


