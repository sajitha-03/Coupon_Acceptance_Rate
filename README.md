# Will the Customer Accept the Coupon?

Jupyter Notebook : https://github.com/sajitha-03/Coupon_Acceptance_Rate/

## Problem Statement
The goal of this project is to use what we know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those who did not.

## Data
The data is from the UCI Machine Learning Repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios, including the destination, current time, weather, and passenger, and then asks people whether they will accept the coupon if they are the driver. There are three possible answers people can choose from:

- “Right away” -> labeled as "Y=1"
- “Later, before the coupon expires” -> labeled as "Y=1"
- “No, I do not want the coupon” -> labeled as "Y=0"

There are five different types of coupons used for the analysis -- less expensive restaurants (under 20), coffee houses, carry out & take away, bar, and more expensive restaurants (20 - $50).

## Key Findings
Overall coupon acceptance rate regardless of the type of coupon is 57% which confirms data is not skewed.

<img width="620" height="495" alt="Screenshot 2025-07-24 at 2 23 15 AM" src="https://github.com/user-attachments/assets/9ea5f13f-fdad-478c-b38d-4e4da6cee1e4" />

Further analysis was targeted on bar coupons. The accepatnce rate was studied against different aspects such as drivers frequency of bar visits, age, occupation, marital status. Acceptance rate seems to have some correlation with certain conditions:

- Frequency of bar visits :

  Acceptance rate is 76% for drivers who go to bars more than three times a month compared to those who do not frequently go to a bar
 
- Frequency of bar visits & age : 

  Acceptance rate is 69% for drivers who go to bars more than once a month and over the age 25 compared to those who visit less than once and over 25.
  Acceptance rate is 72% for drivers who go to bars more than once a month and under 30.
  
- Frequency of bar visits & Passenger not a kid & Occupation other than Farming,Fishing & Forestry :

  Acceptance rate is 71% when the driver who tends to go to bar more than once a month, travels wihtout a kid and not working in Farming,Fishing & Forestry sector.

- Frequency of bar visits & Passenger not a kid & not widowed :

  Acceptance rate is 71% when driver who tends to go to bar more than once a month, not widowed and travels wihtout a kid.

- CheapRestaurant & Income : 

  Acceptance rate is 45% for a driver who go to cheap restaurants and income less than 50K.

Based on the above analysis, the acceptance rate of bar coupon is more correlated to "Bar" data representing driver's frequency of bar visits is more than once( 1~3) and when'age' is in 20-30 range.
Probability of drivers accepting coupons are the ones who falls under groups listed below:

- go to bars more than once a month (higher probabilty with 1~3 group)
- age between 20-30
- single who travel alone
- unemployed who travel alone
- singles who are unemployed
- students who travel alone ignoring the frequency of bar visits data

Those who visit cheap restaurants more than four times in a month and whose income < 50K have less chance of accepting bar coupons.
  
  
## Recommendations

The analysis of bar coupon acceptance rate can be extended to include more comparison such as single vs married, student vs employed, time of the day and geographical location of the user. 

## Findings from Carry out & Take away coupon

Overall acceptance rate for takeout coupons is 74%.

<img width="645" height="498" alt="Screenshot 2025-07-24 at 2 29 20 AM" src="https://github.com/user-attachments/assets/4cecef92-f89d-4c84-b5bb-8ee3ebeadcbc" />

- Acceptance rate is higher on Sunny day which is 76%.
- Higher acceptance rate for drivers who takeout more than 3 times a month which is 74%
- Higher acceptance rate for dinner coupon based on accepted coupons vs destination and time of the day data which is 79%.
