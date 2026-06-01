# Initialize variables
height = 0.0
weight = 0
bmi = 0.0

# 1. Get and validate height (Must be between 1.0m and 2.4m)
while height < 1.0 or height > 2.4:
    height = float(input("Patient height (metres): "))
    if height < 1.0 or height > 2.4:
        print("Invalid height. Please enter a value between 1.0 and 2.4.")
   
# 2. Get and validate weight (Must be a realistic positive number, e.g., > 0)
while weight <= 0 or weight > 250:
    weight = int(input("Patient weight (kg): "))
    if weight <= 0 or weight > 250:
        print("Invalid weight. Please enter a realistic weight in kg.")

# 3. Calculate BMI
bmi = weight / (height * height)

# 4. Output result (Rounded to 2 decimal places for accuracy)
print("BMI:", round(bmi, 2))



#Q02e
# import math library to access PI constant
import math

# program variables
radius = 0
height = 0
volume = 0.0

# constant PI taken from math library
PI = math.pi

# get integer values for radius and height
radius = int(input("Enter cylinder radius in cm: "))
height = int(input("Enter cylinder height in cm: "))

# calculate the volume of the cylinder
volume = PI * radius * radius * height

# round volume to whole number before output
volume = round(volume)

# output result
print("The volume of the cylinder is", volume, "cm³")

# Q01c
# Program variables
days = ["Monday", "Tuesday", "Wednesday", "Thursday",
        "Friday", "Saturday", "Sunday"]

minsWeek = 0

# Get level
level = input("Please enter e (elite) or c (club): ").lower()

# Get total minutes exercised for the week
for day in days:
    minsToday = int(input("Please enter total minutes exercise on " + day + " > "))
    minsWeek = minsWeek + minsToday

# Check exercise target
if level == "e" and minsWeek < 300:   # Elite runner has not met target
    print("Weekly exercise:", minsWeek, "minutes")
    print("You have not met your exercise target of 300 minutes.")

elif level == "c" and minsWeek < 200:  # Club runner has not met target
    print("Weekly exercise:", minsWeek, "minutes")
    print("You have not met your exercise target of 200 minutes.")

else:
    print("Weekly exercise:", minsWeek, "minutes")
    print("Well done, you have met your weekly exercise target.")

