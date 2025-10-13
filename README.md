# EGBI122-Project
This project is a part of the course EGBI122, conducted as part of the academic curriculum.  
The project team consists of:  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Titinan Phoarsai<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;6813361  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Pranchalee Chaemcharoen<span>&nbsp;&nbsp;&nbsp;&nbsp;6813379  

### Function explain  
<span>&nbsp;&nbsp;&nbsp;&nbsp;**calculate_bmi function**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; There’re 3 main conditions to check. First, check if the user puts weight and height correctly or not if not return the message, “Please enter valid weight and height”. Second, if the units are imperial unit convert to metric unit. calculate BMI in formular weight(kg) / height(m) power 2 and keep it in bmi variable. Third, classify BMI by if bmi is lower than 18.5 it’s Underweight. bmi is more than or equal to 18.5 and less than 25 it’s Normal weight. bmi more than or equal to 25 and less than 30 it’s Overweight. Others are Obesity. Return bmi with 2 decimals and Category.    
<br>&nbsp;&nbsp;&nbsp;&nbsp;**calculate_metabolic_rate function**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; There’re 2 main conditions to check. First, check if the user puts age, weight and height correctly or not if not return the message, “Please enter valid age, weight, and height". Second, check the gender if it’s male calculate in male formula. Others calculate it in another formula. Save the calculated value in bmr variable. Calculate the calories per day by multiplying bmr and activity_level (the value of each activity_level is in Metabolic Rate Calculator Tab part). Return bmr with 2 decimals and estimated daily calorie needs with 2 decimals.  
<br>&nbsp;&nbsp;&nbsp;&nbsp;**add_food_entry function**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; First, this function will check if the user puts food items and calories count correctly or not if not return the message, “Please enter a valid food item and calorie count". Add food items and calories in food_log dict (This dict is set [ ] at the first of all code). Make dict log_output (to make data easier to display) which uses a for loop to get every dictionary inside food_log and collects each one’s "item" and "calories" values. And use another for loop to sum all calories in food_log keep the sum in total_calories variable. Return the message “Food added!” ,log_output and total_calories.  
<br>&nbsp;&nbsp;&nbsp;&nbsp;**clear_food_log function**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Use global food_log to tell python that we are using food_log from outside (Other function) and set food_log dict empty. Return the message “Log cleared!”, empty list and total calories after clearing (0).  

### Tab explain
