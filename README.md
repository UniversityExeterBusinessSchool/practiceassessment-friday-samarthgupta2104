[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/pfNOK2_w)
# PracticeAssessment-Friday-

#######################################################################################################################################################
# 
# Name:
# SID:740092276
# Exam Date:
# Module:
# Github link for this assignment:  
#
# ######################################################################################################################################################
# Instruction 1. Read the questions and instructions carefully and complete scripts.

# Instruction 2. Only ethical and minimal use of AI is allowed. You might use AI to give advice on how to use a tool or programming language.  
#                You must not use AI to create the code. You might make use of AI to aid debugging of the code.  
#                You must indicate clearly how and where you have used AI.

# Instruction 3. Copy the output of the code and insert it as a comment below your code e.g # OUTPUT (23,45)

# Instruction 4. Ensure you provide comments for the code and the output to show contextual understanding.

# Instruction 5. Upon completing this test, commit to Git, copy and paste your code into the word file and upload the saved file to ELE.
#                There is a leeway on when you need to upload to ELE, however, you must commit to Git at 
#                the end of your session.

# ######################################################################################################################################################
# Question 1 - Data Processing and Loops
# You are given a string representing customer reviews. Use a for loop to process the text and count occurrences of specific keywords.
# Your allocated keywords are determined by the first and last digit of your SID.
# Count and store occurrences of each keyword in a dictionary called keyword_counts.
 
customer_reviews = """The product is well-designed and user-friendly. However, I experienced some issues with durability. The customer service was helpful, 
but I expected a faster response. The quality of the materials used is excellent. Overall, the purchase was satisfactory."""

# Keywords dictionary
keywords = {
    0: 'user-friendly',
    1: 'helpful',
    2: 'durability',
    3: 'response',
    4: 'satisfactory',
    5: 'quality',
    6: 'service',
    7: 'issues',
    8: 'purchase',
    9: 'materials'
}

# Write your code to process the text and count keyword occurrences

# Taking my keywords from my SID
Selected_keywords = ['issues', 'service']

# To store keyword counts an empty dictionary is created
keyword_counts = {}

# Each keyword is then looped around 
# we will count the times the word appears through .count()
# then we will finally store it in dictionary
for word in Selected_keywords:
    count = customer_reviews.lower().count(word)
    keyword_counts[word] = count

# Printing the final output
print(keyword_counts)

# Output {'issues': 1, 'service': 1}


##########################################################################################################################################################

# Question 2 - Business Metrics
# Scenario - You work in an online retail company as a business analyst. Your manager wants weekly reports on financial performance, including:
# Gross Profit Margin, Inventory Turnover, Customer Retention Rate (CRR), and Break-even Analysis. Implement Python functions 
# that take relevant values as inputs and return the computed metric. Use the first two and last two digits of your ID number as input values.

My ID number:740092276
# Insert first two digits of ID number here:
# Insert last two digits of ID number here:

# Write your function for Gross Profit Margin

# Write your function for Inventory Turnover

# Write your function for Customer Retention Rate (CRR)

# Write your function for Break-even Analysis

# Call your functions here

# The inputs from my ID
first_number = 74
last_number = 76

# we use def to store in funtions and then in future we can call it anytime to use it
# Function for Gross Profit Margin
def gross_profit_margin(gross_profit, revenue):
    return (gross_profit / revenue) * 100

# Inventory Turnover Function
def inventory_turnover(cost_of_goods_sold, average_inventory):
    return cost_of_goods_sold / average_inventory

#  Customer Retention Rate Function
def customer_retention_rate(retained_customers, total_customers):
    return (retained_customers / total_customers) * 100

# Break-even Analysis Function
def break_even_analysis(fixed_costs, price_per_unit, variable_cost_per_unit):
    return fixed_costs / (price_per_unit - variable_cost_per_unit)

# Calling all the functions
print("Gross Profit Margin:", gross_profit_margin(74, 276))
print("Inventory Turnover:", inventory_turnover(740, 92))
print("Customer Retention Rate:", customer_retention_rate(74, 276))
print("Break-even Point:", break_even_analysis(740, 92, 76))

# output for the functions
# Gross Profit Margin: 26.81159420289855
# Inventory Turnover: 8.043478260869565
# Customer Retention Rate: 26.81159420289855
# Break-even Point: 46.25

##########################################################################################################################################################

# Question 3 - Forecasting and Regression
# A logistics company has gathered data on delivery costs and shipment volumes. The table below provides different costs and their corresponding shipment volumes.
# Develop a linear regression model and determine:
# 1. The optimal delivery cost that maximizes profit
# 2. The expected shipment volume when the cost is set at £68


"""
Delivery Cost (£)    Shipment Volume (Units)
-------------------------------------------
25                  500
30                  480
35                  450
40                  420
45                  400
50                  370
55                  340
60                  310
65                  290
70                  250
"""

# Write your regression model code here

import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# Data is inputted first
delivery_cost = np.array([25, 30, 35, 40, 45, 50, 55, 60, 65, 70]).reshape(-1, 1)
shipment_volume = np.array([500, 480, 450, 420, 400, 370, 340, 310, 290, 250])

# We will train and create a regression model
model = LinearRegression()
model.fit(delivery_cost, shipment_volume)

# now we predict the shipment volume
predicted_volume = model.predict(np.array([[68]]))
print("Expected shipment volume at £68:", predicted_volume[0])

# Now we Plot the regression line

plt.scatter(delivery_cost, shipment_volume, color='blue')  # Actual data
plt.plot(delivery_cost, model.predict(delivery_cost), color='red')  # Regression line
plt.xlabel("(£) Delivery Cost ")
plt.ylabel("(Units) Shipment Volume ")
plt.title("Cost vs Volume")
plt.grid(True)
plt.show()

# outcome will be - Expected shipment volume at £68: 270.0

##########################################################################################################################################################


# Question 4 - Debugging and Data Visualization

import rand as random
import matplotlib.pyplt as plt

# Generate 100 random numbers between 1 and student ID number
your_ID=input("Enter your Student ID: ")
max_value = int(your_ID)
random_numbers = [random.randint(your_ID, max_valu) in range(100)]

# Plotting the numbers in a histogram
plt.histogram(random_number, bin=10, edgecolour='blue', alpha=0.7, colour='red')
plt.title="Histogram of 100 Random Numbers"
plt.xlabel="Value Range"
plt.ylabel="Frequency"
plt.grid("True")
plt.show("plot")


# right code is here
import random
import matplotlib.pyplot as plt

# we convert the student ID into integer 
your_ID = input("Enter your Student ID: ")
max_value = int(your_ID)

# now we use random.randint to product 100 random number between 1 to my id number
random_numbers = [random.randint(1, max_value) for _ in range(100)]

# then we plot the histogram
plt.hist(random_numbers, bins=10, color='red', edgecolor='blue', alpha=0.7)
plt.title("Histogram of 100 Random Numbers")
plt.xlabel("Value Range")
plt.ylabel("Frequency")
plt.grid(True)
plt.show()

# the output will be a histogram of 100 random numbers
