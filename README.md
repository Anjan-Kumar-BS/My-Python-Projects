# My-Python-Projects
I have been saving and documenting all my learnings, from base to pro (till I become one).
Note: All my codes are documented for my profiling purposes.
Day 1 Baby Name Generator:
#1. Create a greeting for your program.
print("Welcome to Children Name Generator")
#2. Ask the user for the city that they grew up in.
Husband_Name = input("What is the starting 3 letters of Husband's name?\n")
#3. Ask the user for the name of a pet.
Wife_Name = input("What is the Ending 3 letters of Wife's name?\n")
#4. Combine the name of their city and pet and show them their band name.
print("Your Baby's name can be \n"+(Husband_Name + Wife_Name))

#Day 2.1 BMI Calculator:
height = input("enter your height in m: ")
weight = input("enter your weight in kg: ")
result = int(weight) / float(height)**2
result_as_int = int(result)
print(result_as_int)

#Day 2.2 Remainder life expectancy in days, weeks and months:
#This is my Code 
age = input("What is your current age? ")
Current_Age_Days = int(age) * int(365) 
Current_Age_Weeks = int(age) * int(52)
Current_Age_Months = int(age) * int(12)
max_age = 90
max_age_Days = int(max_age) * int(365) 
max_age_Weeks = int(max_age) * int(52)
max_age_Months = int(max_age) * int(12)
print(f"You have {max_age_Days - Current_Age_Days} days, {max_age_Weeks - Current_Age_Weeks} Weeks and {max_age_Months -Current_Age_Months} months ")

#This is what she thought me
age = input("What is your current age? ")
age_as_int = int(age)
Years_remaining = 90 - age_as_int
Days_Remaining = Years_remaining * 365
Weeks_Remaining = Years_remaining * 52
Months_Remaining = Years_remaining * 12
print(f"You have {Days_Remaining} days, {Weeks_Remaining} weeks, and {Months_Remaining} weeks")

#Day 2.3 Tip and Split Calculator:
print("Welcome to the Tip and Bill Split Calculator")
Total_Bill = float(input("What was the total bill? "))
Tip_Percentage = int(input ("What Percentage tip would you like to give? 10 , 12 or 15? "))
split  = int(input("How many people to split the bill? "))

Tip_Amount = Tip_Percentage / 100
Total_Cost = Total_Bill + Tip_Amount
Totol_Cost_Percent = Total_Bill * (1 + Tip_Percentage)
Each_Person = Total_Cost / split
print(round(Each_Person, 2))

#Day 3.1 Number is odd or even:
number = int(input("Which number do you want to check? "))
number_Sol = number % 2
if number_Sol == 0:
    print("This is a even Number")
else:
    print("This is a Odd Number")

#Day 3.2 BMI Calculator comparision:
height = float(input("enter your height in m: "))
weight = float(input("enter your weight in kg: "))
bmi = round(weight/height**2)
if bmi < 18.5:
    print(f"Your BMI is {bmi}, you are underweight.")
elif bmi < 25:
    print(f"Your BMI is {bmi}, you have a normal weight.")
elif bmi < 30:
    print(f"Your BMI is {bmi}, you are slightly overweight.")
elif bmi < 35:
    print(f"Your BMI is {bmi}, you are obese.")
else:
    print(f"Your BMI is {bmi}, you are clinically obese.")

#Day 3.3 Given Year is leap Year or not.
#MY CODE:

year = int(input("Which year do you want to check? "))
if year % 4 == 0:
    print("Leap Year")
elif year % 100 > 0:
    print("Not Leap year")
elif year % 400 == 0:
    print("Leap Year")
else:
    print("Not leap year")

#different method:
year = int(input("Which year do you want to check? "))
if year % 4 == 0:
   if year % 100 == 0:
       if year % 400 == 0:
            print("Leap Year")
       Else:
             print(“Nota Leap Year”)
    Else:
         print(“leap year”)
Else:
     print(“Not a leap year”)	

#Day 3.4 Pizza Order pricing:

print("Welcome to Python Pizza Deliveries!")
size = input("What size pizza do you want? S, M, or L ")
add_pepperoni = input("Do you want pepperoni? Y or N ")
extra_cheese = input("Do you want extra cheese? Y or N ")
bill = 0

#1st method
# if size == "S":
#   bill += 15
#   if add_pepperoni == "Y":
#     bill += 2
#   if add_pepperoni == "N":
#     bill += 0
#     if extra_cheese == "Y":
#       bill += 1
#     if extra_cheese == "N":
#       bill += 0
# if size == "M":
#   bill = 20
#   if add_pepperoni == "Y":
#     bill += 3
#   if add_pepperoni == "N":
#     bill += 0
#     if extra_cheese == "Y":
#       bill += 1
#     if extra_cheese == "N":
#       bill += 0
# if size == "L":
#   bill = 25
#   if add_pepperoni == "Y":
#     bill += 3
#   if add_pepperoni == "N":
#     bill += 0
#     if extra_cheese == "Y":
#       bill += 1
#     if extra_cheese == "N":
#       bill += 0
# print(f"Your final bill is: ${bill}")

#2nd Method:
if size == "S":
  bill += 15
elif size =="M":
  bill += 20
else:
  bill += 25

if add_pepperoni == "Y":
  if size == "S":
    bill += 2
  else:
    bill += 3

if extra_cheese == "Y":
  bill += 1

print(f"Your final bill is ${bill}")

#3.5 Love Calculator:
name1 = input("What is your name? \n")
name2 = input("What is their name? \n")
combined_names = name1 + name2
combined_names_lower = combined_names.lower()
t = combined_names_lower.count("t")
r = combined_names_lower.count("r")
u = combined_names_lower.count("u")
e = combined_names_lower.count("e")
first_digit = t + r + u + e

l = combined_names_lower.count("l")
o = combined_names_lower.count("o")
v = combined_names_lower.count("v")
e = combined_names_lower.count("e")
second_digit = l + o + v + e

combined_digits = int(str(first_digit)+str(second_digit))
if (combined_digits < 10) or (combined_digits > 90):
    print(f"your score is {combined_digits}, you go together like coke and mentos")
elif (combined_digits >= 40) and (combined_digits <= 50):
    print(f"your score is {combined_digits}, you are alright together")
else:
    print(f"your score is {combined_digits}.")

#3.6 TREASURE GAME (very important):
print('''
*******************************************************************************
          |                   |                  |                     |
 _________|________________.=""_;=.______________|_____________________|_______
|                   |  ,-"_,=""     `"=.|                  |
|___________________|__"=._o`"-._        `"=.______________|___________________
          |                `"=._o`"=._      _`"=._                     |
 _________|_____________________:=._o "=._."_.-="'"=.__________________|_______
|                   |    __.--" , ; `"=._o." ,-"""-._ ".   |
|___________________|_._"  ,. .` ` `` ,  `"-._"-._   ". '__|___________________
          |           |o`"=._` , "` `; .". ,  "-._"-._; ;              |
 _________|___________| ;`-.o`"=._; ." ` '`."\` . "-._ /_______________|_______
|                   | |o;    `"-.o`"=._``  '` " ,__.--o;   |
|___________________|_| ;     (#) `-.o `"=.`_.--"_o.-; ;___|___________________
____/______/______/___|o;._    "      `".o|o_.--"    ;o;____/______/______/____
/______/______/______/_"=._o--._        ; | ;        ; ;/______/______/______/_
____/______/______/______/__"=._o--._   ;o|o;     _._;o;____/______/______/____
/______/______/______/______/____"=._o._; | ;_.--"o.--"_/______/______/______/_
____/______/______/______/______/_____"=.o|o_.--""___/______/______/______/____
/______/______/______/______/______/______/______/______/______/______/_____ /
*******************************************************************************
''')
print("Welcome to Treasure Island.")
print("Your mission is to find the treasure.") 

#https://www.draw.io/?lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=Treasure%20Island%20Conditional.drawio#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1oDe4ehjWZipYRsVfeAx2HyB7LCQ8_Fvi%26export%3Ddownload

Question_1 = input("1. You're at a crossroad. Where do you want to go? Type 'left' or 'right' \n")
if Question_1 == "left":
  question_2 = input("Right Now you in the bridge, do you want to 'wait' or 'swim'?\n")
  if question_2 == "wait":
    Question_3 = input("Which Color door do you select? 'Red', 'Blue' or 'Green'\n")
    if Question_3 == "green":
      print("you win.")
    elif Question_3 == "red":
      print("you got eaten by Beasts, yum yummmm Game Over.")
    else:
      print("You are burned by fire. Grab some water, its Game Over.")
  else: 
    print("you got attacked by Sea Monster.Game Over, see you in next life.")
else:
  print("You fell into a Hole - Dig yourself up, Game Over")
  


