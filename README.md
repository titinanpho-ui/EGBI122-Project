# EGBI122-Project
This project is a part of the course EGBI122, conducted as part of the academic curriculum.  
The project team consists of:  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Titinan Phoarsai<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;6813361  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Pranchalee Chaemcharoen<span>&nbsp;&nbsp;&nbsp;&nbsp;6813379  

### Function explain  
<span>&nbsp;&nbsp;&nbsp;&nbsp;**calculate_bmi function**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; There’re 3 main conditions to check. First, check if the user puts weight and height correctly or not if not return the message, “Please enter valid weight and height”. Second, if the units are imperial unit convert to metric unit. calculate BMI in formular weight(kg) / height(m) power 2 and keep it in bmi variable. Third, classify BMI by if bmi is lower than 18.5 it’s Underweight. bmi is more than or equal to 18.5 and less than 25 it’s Normal weight. bmi more than or equal to 25 and less than 30 it’s Overweight. Others are Obesity. Generate BMI graph when overtime by plot_bmi_history function. Return bmi with 2 decimals, Category and BMI graph.   
<br>&nbsp;&nbsp;&nbsp;&nbsp;**calculate_metabolic_rate function**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; There’re 2 main conditions to check. First, check if the user puts age, weight and height correctly or not if not return the message, “Please enter valid age, weight, and height". Second, check the gender if it’s male calculate in male formula. Others calculate it in another formula. Save the calculated value in bmr variable. Calculate the calories per day by multiplying bmr and activity_level (the value of each activity_level is in Metabolic Rate Calculator Tab part). And calculate the calories per day for gaining or losing weight. Return bmr, estimated daily calorie needs, Calorie Goals (approx.) with 2 decimals.  
<br>&nbsp;&nbsp;&nbsp;&nbsp;**add_food_entry function**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; First, this function will check if the user puts food items and calories count correctly or not if not return the message, “Please enter a valid food item and calorie count". Add food items and calories in food_log dict (This dict is set [ ] at the first of all code). Make dict log_output (to make data easier to display) which uses a for loop to get every dictionary inside food_log and collects each one’s "item", "calories" and “timestamp” values. And use another for loop to sum all calories in food_log keep the sum in total_calories variable.Compare total_calories and TEDEE check is it over the limit or not. Plotting graph by plot_weekly_calories function. Return the message “Food added!” ,log_output, total_calories, tdee_comparison and the plot.  
<br>&nbsp;&nbsp;&nbsp;&nbsp;**clear_food_log function**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Use global food_log to tell python that we are using food_log from outside (Other function) set food_log dict empty and plotting graph. Return the message “Log cleared!”, empty list, total calories after clearing (0) and the plot.  
<br>&nbsp;&nbsp;&nbsp;&nbsp;**plot_bmi_history function**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Designed to generate a line plot showing the trend of Body Mass Index (BMI) over time. Filter the history_data to select only entries where the BMI value is greater than 0. If no usable BMI data is available, display an empty plot with the message: "No BMI data available to plot."  And if data is available, plot Date on the x-axis and BMI on the y-axis as a line graph with point markers. Set the graph title to "BMI Trend Over Time".  
<br>&nbsp;&nbsp;&nbsp;&nbsp;**plot_weekly_calories function**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; We use datetime and timedelta library to determine the date range, 7 days, Next, we use for loop to create daily calories dictionary which have date and calories inside and another for loop to aggregate the calories. We use Matplotlib to plot the graph. X-axis is days of week, and Y-axis is calories. The tittle of this graph is “Daily Calorie Intake (Last 7 Days)”.

### UI & format part  
- we custom theme to make colors similar to the image by this code.  
custom_theme = gr.themes.Soft(  
    <span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;primary_hue="cyan",   
).set(  

<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;So mostly it will be in cyan color. But we want to change color of buttons, blocks, tap. Then we have to set the color we like in #.  
For example,<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; button_primary_background_fill="#77c2c7",   
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;button_primary_background_fill_hover="#18acba",   
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;button_secondary_background_fill="white",  

- UI on the website, we have to separate the sections by tabs like header, image, main container for design our website.  

We use this code to change size and position of texts, etc.  
  <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.header-section h1 {  
        <span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;font-size: 2em;  
        <span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;margin-bottom: 5px;  
        <span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;display: flex;  
        <span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;align-items: center;  
        <span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;justify-content: center;  
        <span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;gap: 10px;  
    <span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}  

<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Moreover, in this you can change color to fill the block in header or whatever you want by using this  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;background-color: #a8e1e6  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Don't forget #  

### Tab explain
<span>&nbsp;&nbsp;&nbsp;&nbsp;**BMI Calculator Tab**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This tab, labeled “📊 BMI Calculator”, allows users to calculate their Body Mass Index (BMI), view their weight category, and visualize changes in BMI over time through a plotted graph.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Inside tab:  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**1.Headers (Markdown):**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Display text titles and descriptions for clarity.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**2.Inputs:**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	bmi_unit_system : a dropdown menu to choose between metric (cm, kg) and imperial (lb, in) units.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	bmi_height_input and bmi_weight_input : number input fields for height and weight.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**3.Button:**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	bmi_calculate_btn : triggers calculate BMI value, classify BMI category and updated BMI trend plot when clicked.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**4.Outputs:**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	bmi_result_output : shows the numeric BMI value with 2 decimals.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	bmi_category_output : shows which weight category the user belongs to, based on the BMI result.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- bmi_plot_output : uses a function plot_bmi_history() to visualize BMI history as a line chart over time.  

<br>&nbsp;&nbsp;&nbsp;&nbsp;**Metabolic Rate Calculator Tab**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This tab, “🔥 Metabolic Rate”, estimate their Basal Metabolic Rate (BMR) and Total Daily Energy Expenditure (TDEE) based on individual information such as age, gender, weight, height, and physical activity level.
The results help users understand how many calories they burn per day and how to adjust their intake according to fitness or weight goals.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Inside tab:  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**1.Headers (Markdown):**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Display text titles and descriptions for clarity  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**2.Inputs:**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	mr_age_input : user’s age.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	mr_gender_input : gender (male/female).  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	mr_weight_input : weight (kg).  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	mr_height_input : height (cm).  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	mr_activity_input : physical activity level, with five options (Sedentary to Extra Active).  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**3.Calculation Function (get_calories):**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The function retrieves the correct activity multiplier based on user selection (Sedentary = 1.2, Lightly Active = 1.375, Moderately Active = 1.55, Very Active = 1.725, Extra Active = 1.9 ) and then calls calculate_metabolic_rate.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**4.Calculation Button:**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	mr_calculate_btn : runs the get_calories() function with the user’s inputs when clicked.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**5.Output:**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	mr_result_output : a formatted Markdown explanation of their BMR, TDEE, and goal recommendations.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	tdee_value_output : a numeric output (hidden) storing the raw TDEE value for internal use.  

<br>&nbsp;&nbsp;&nbsp;&nbsp;**Food Tracker tab**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This tab, “🍎 Food Tracker”, allows users to record their meals by entering food items and calories, view the log in a table, calculate total  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;calories, and clear the log when needed.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Inside tab:  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**1.Headers (Markdown):**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Display text titles and descriptions for clarity  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**2.Inputs:**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- tdee_input_tracker : This lets users enter their daily calorie goal (TDEE = Total Daily Energy Expenditure).  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- food_date_input : records date and time of each meal automatically (default = current time).  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- food_item_input : users type the food name.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- food_calories_input : users enter how many calories it contains.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**4.Add Food Button:**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- it calls the function add_food_entry() with the food name and calories as inputs.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	The function updates the data table (food_log_list) with the new meal.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	Refreshes the total calories for the day.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	Shows a comparison between total intake and TDEE.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	Updates the calorie plot showing recent daily calorie trends.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**5.Clear Log Button:**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- When clicked, it calls clear_food_log(), which resets the list and calorie count to zero.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-	The table becomes empty, and the total calories label shows “0 kcal” and the plot is refreshed.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**6.Output:**  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- food_log_list : shows all recorded foods in a table format.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- total_calories_label : displays the sum of all calories in the log.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- tdee_comparison_output : Displays a message comparing total calories with the user’s TDEE goal.  
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- calorie_plot_output : Graphs daily calorie intake over the past week using the function plot_weekly_calories().
