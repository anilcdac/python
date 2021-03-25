# python
python100dayschallenge


Resources
draw.io - to draw diagram , flow chart


https://developers.google.com/edu/python/lists#for-and-in


Day1
Print(“Hello World”)

#Fix the code below 👇

print("Day 1 - String Manipulation")
print('String Concatenation is done with the "+" sign.')
print('e.g. print("Hello " + "world")')
print("New lines can be created with a backslash and n.")


1.2 input()
print(“hello ” + input(“What is your name”))

Prints input first on screen
What is your name
User enter name : Anil
Final output printed:  Hello Anil

1.3 input() exercise
Write a program that prints the number of characters in a user's name. You might need to Google for a function that calculates the length of a string. 

Solution
print(len(input("Enter your name: \n")))
1.4 Variables
Instructions
Write a program that switches the values stored in the variables a and b.
Warning. Do not change the code on lines 1-4 and 12-18. Your program should work for different inputs. e.g. any value of a and b.

# 🚨 Don't change the code below 👇
a = input("a: ")
b = input("b: ")
# 🚨 Don't change the code above 👆

####################################
#Write your code below this line 👇

c = a
a = b
b = c



#Write your code above this line 👆
####################################

# 🚨 Don't change the code below 👇
print("a: " + a)
print("b: " + b)

==

Day 1 Project
#1. Create a greeting for your program.
print("Welcome to Band Name Generator\n")
#2. Ask the user for the city that they grew up in.
city = input("Which city you were born in?:\n")
#3. Ask the user for the name of a pet.
pet = input("What's your pet name?\n")
#4. Combine the name of their city and pet and show them their band name.
print("Suggested band names :\n" + "1:" + city + pet + "Band\n"
 + "2:"  + pet + city+"Band\n")
#5. Make sure the input cursor shows on a new line, see the example at:
#   https://band-name-generator-end.appbrewery.repl.run/
=====


Day2
2.1

## Data Types

# Instructions

Write a program that adds the digits in a 2 digit number. e.g. if the input was 35, then the output should be 3 + 5 = 8


# 🚨 Don't change the code below 👇
two_digit_number = input("Type a two digit number: ")
# 🚨 Don't change the code above 👆

####################################
#Write your code below this line 👇
first_digit = two_digit_number[0]
second_digit=two_digit_number[1]
result=int(first_digit)+int(second_digit)
print(result)


2.2 BMI Calculator
# 🚨 Don't change the code below 👇
height = input("enter your height in m: ")
# height is in meter so 174 cm is 1.74
weight = input("enter your weight in kg: ")
# 
# 🚨 Don't change the code above 👆

#Write your code below this line 👇

BMI = float(weight)/(float(height)**2)
bmi_as_int = int(BMI)
print(bmi_as_int)

==

Day 2.3 Life in weeks
# 🚨 Don't change the code below 👇
age = input("What is your current age?")
# 🚨 Don't change the code above 👆

#Write your code below this line 👇

age_as_int = int(age)

years_remaining = 90 - age_as_int
months_remaining = years_remaining*12
weeks_remaining = years_remaining*52

result =f"You have {years_remaining} Years {months_remaining} months {weeks_remaining} weeks"

print(result)

===
Day 2.4

Tip calculator
  total_bill = float(input("How much is total bill: "))
tip_percent = int(input("How much tip you wish to give "))
bill_with_tip = total_bill+ (total_bill)*((tip_percent)/100)
no_of_people = int(input("How many people you want to divide the bill: "))
bill_contri_formated = "{:.2f}".format(bill_contri)
print(f"each person need to pay: {bill_contri_formated}")

#If the bill was $150.00, split between 5 people, with 12% tip. 
#Each person should pay (150.00 / 5) * 1.12 = 33.6
#Format the result to 2 decimal places = 33.60
#Tip: There are 2 ways to round a number. You might have to do some Googling to solve this.💪
#HINT 1: https://www.google.com/search?q=how+to+round+number+to+2+decimal+places+python&oq=how+to+round+number+to+2+decimal
#HINT 2: https://www.kite.com/python/answers/how-to-limit-a-float-to-two-decimal-places-in-python



Day 3
3.1 Logical Operators
# 🚨 Don't change the code below 👇
number = int(input("Which number do you want to check? "))
# 🚨 Don't change the code above 👆

#Write your code below this line 👇

result = number%2

if result==0:
  print("Number is even")
else:  
  print("Number is odd")

====
check the cod running




=
3.2 BMI Advanced
# 🚨 Don't change the code below 👇
height = float(input("enter your height in m: "))
weight = float(input("enter your weight in kg: "))
# 🚨 Don't change the code above 👆

#Write your code below this line 👇

bmi = round(weight / height ** 2)
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


===
1.	If the year is evenly divisible by 4, go to step 2. Otherwise, go to step 5.
2.	If the year is evenly divisible by 100, go to step 3. Otherwise, go to step 4.
3.	If the year is evenly divisible by 400, go to step 4. Otherwise, go to step 5.
4.	The year is a leap year (it has 366 days).
5.	The year is not a leap year (it has 365 days).
=IF(OR(MOD(A1,400)=0,AND(MOD(A1,4)=0,MOD(A1,100)<>0)),"Leap Year", "NOT a Leap Year")  

# 🚨 Don't change the code below 👇
year = int(input("Which year do you want to check? "))
# 🚨 Don't change the code above 👆

#Write your code below this line 👇
Y = year
if Y%4 !=0:
  print(f"{Y} is not leap year1") 
elif Y%100 != 0 and Y%4 ==0:
    print(f"{Y} is leap year2")     
elif Y%4 ==0 and Y%100 == 0 and Y%400==0:
    print(f"{Y} is leap year3") 


Refer the diagram-flowchart screenshot-day3-leapyear
==
# 🚨 Don't change the code below 👇
year = int(input("Which year do you want to check? "))
# 🚨 Don't change the code above 👆

#Write your code below this line 👇
Y = year
if Y%4 ==0:
  if Y%100 == 0:
    if Y%400 ==0:
      print(f"{Y} is leap year")  
    else:
      print(f"{Y} is not leap year") 
  else:
    print(f"{Y} is leap year")  
else:
  print(f"{Y} is not leap year")  

===
Love calculator- Day 3- 36
# 🚨 Don't change the code below 👇
print("Welcome to the Love Calculator!")
name1 = input("What is your name? \n")
name2 = input("What is their name? \n")
# 🚨 Don't change the code above 👆

#Write your code below this line 👇

concat_strings= name1+name2
name_lower = concat_strings.lower() 

t=name_lower.count("t")
r=name_lower.count("r")
u=name_lower.count("u")
e=name_lower.count("e")
l=name_lower.count("l")
o=name_lower.count("o")
v=name_lower.count("v")
e=name_lower.count("e")

count1 = t+r+u+e+l+o+v+e
print(f"your love score is {l}")

print(f"your love score is {count1}")



==
37 Treasure Island


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
choice1 = input('You\'re at a cross road. Where do you want to go? Type "left" or "right" \n').lower()
if choice1 == "left":
  choice2 = input('You\'ve come to a lake. There is an island in the middle of the lake. Type "wait" to wait for a boat. Type "swim" to swim across. \n').lower()
  if choice2 == "wait":
    choice3 = input("You arrive at the island unharmed. There is a house with 3 doors. One red, one yellow and one blue. Which colour do you choose? \n").lower()
    if choice3 == "red":
      print("It's a room full of fire. Game Over.")
    elif choice3 == "yellow":
      print("You found the treasure! You Win!")
    elif choice3 == "blue":
      print("You enter a room of beasts. Game Over.")
    else:
      print("You chose a door that doesn't exist. Game Over.")
  else:
    print("You get attacked by an angry trout. Game Over.")
else:
  print("You fell into a hole. Game Over.")

===
another way

print("Welcome to Treasure Island.")
print("Your mission is to find the treasure.") 

#https://www.draw.io/?lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=Treasure%20Island%20Conditional.drawio#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1oDe4ehjWZipYRsVfeAx2HyB7LCQ8_Fvi%26export%3Ddownload
direction = (input("Do you want to go left ot right? left / right :")).lower()


if direction != str("left"):
  print("You fall into a hole. GAME OVER!")
else: 
  direction=(input("Do you want to swim or wait? swim /wait :")).lower()
  if direction != str("wait"):
    print("You are attacked by trout. GAME OVER!") 
  else:
    direction = (input("which door you want to go in? Red / Blue/ Yellow :")).lower()
    if direction == str("red"):
      print("You got burned by fire, GAME OVER!")
    elif  direction == str("blue"):
      print("You got burned by fire, GAME OVER!")
    elif  direction == str("yellow"):
      print("You Win!")
    else:
        print("GAME OVER!")
==
Day 4
4 List Randomizasions


4.1 Random person pay the bill from List
import random
# Split string method
names_string = input("Give me everybody's names, separated by a comma. ")
names = names_string.split(", ")
# 🚨 Don't change the code above 👆

#Write your code below this line 👇

names_length  = int(len(names))
random_number = random.randint(0,names_length-1)
selected= names[random_number]

print(f"{selected} is going to buy milk today")



==

Treasure Map difficulty - High
# 🚨 Don't change the code below 👇
row1 = ["⬜️","⬜️","⬜️"]
row2 = ["⬜️","⬜️","⬜️"]
row3 = ["⬜️","⬜️","⬜️"]
map = [row1, row2, row3]
print(f"{row1}\n{row2}\n{row3}")
position = input("Where do you want to put the treasure? ")
# 🚨 Don't change the code above 👆
12
#Write your code below this row 👇
horizontal = int(position[0])
vertical=int(position[1])


selected_row = map[vertical-1]
selected_row[horizontal-1] = "X"


#Write your code above this row 👆

# 🚨 Don't change the code below 👇
print(f"{row1}\n{row2}\n{row3}")
===
# 🚨 Don't change the code below 👇
row1 = ["⬜️","⬜️","⬜️"]
row2 = ["⬜️","⬜️","⬜️"]
row3 = ["⬜️","⬜️","⬜️"]
map = [row1, row2, row3]
print(f"{row1}\n{row2}\n{row3}")
position = input("Where do you want to put the treasure? ")
# 12 - 1st column and 2nd row
# 🚨 Don't change the code above 👆

#Write your code below this row 👇
horizontal = int(position[0]) #column1
vertical=int(position[1])   #row2

print(horizontal) #1st column
print(vertical) #2nd row 

selected_row = map[vertical-1]   #2-1=1
# 1 means second row gets selected-vertically

selected_row[horizontal-1] = "X" #1-1=0
# 1 means first column gets selected-horizontally

#Write your code above this row 👆

# 🚨 Don't change the code below 👇
print(f"{row1}\n{row2}\n{row3}")
===

Game 
import random

rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''
game_images = [rock, paper, scissors]

user_choice = int(input("What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors.\n"))
print(game_images[user_choice])

computer_choice = random.randint(0, 2)
print("Computer chose:")
print(game_images[computer_choice])

if user_choice >= 3 or user_choice < 0: 
  print("You typed an invalid number, you lose!") 
elif user_choice == 0 and computer_choice == 2:
  print("You win!")
elif computer_choice == 0 and user_choice == 2:
  print("You lose")
elif computer_choice > user_choice:
  print("You lose")
elif user_choice > computer_choice:
  print("You win!")
elif computer_choice == user_choice:
  print("It's a draw")

####### Debugging challenge: #########
#Try running this code and type 5.
#It will give you an IndexError and point to line 32 as the issue.
#But on line 38 we are trying to prevent a crash by detecting
#any numbers great than or equal to 3 or less than 0.
#So what's going on?
#Can you debug the code and fix it?
#Solution: https://repl.it/@appbrewery/rock-paper-scissors-debugged-end


==
Day5
5 Loops


fruits = {"Apple", "Mango", "Banana"}
for fruit in fruits:
    print(fruit)
    print(fruit + " Pie")
print(f"After for loop{fruits}") 
===
>>> %Run loops.py
Apple
Apple Pie
Mango
Mango Pie
Banana
Banana Pie
After for loop{'Apple', 'Mango', 'Banana'}
===

5.1 Average Height
# 🚨 Don't change the code below 👇
student_heights = input("Input a list of student heights ").split()
for n in range(0, len(student_heights)):
  student_heights[n] = int(student_heights[n])
# 🚨 Don't change the code above 👆

#Write your code below this row 👇

print(student_heights)

total_height=0
for height in student_heights:
  total_height=height+total_height
print(f"Total height: {total_height}")

total_students=0
for student in student_heights:
  total_students = total_students+1
print(f"Total number of students: {total_students}")

Average = round(total_height/total_students)

print(f"Avergae Height is :{Average}")



====
5.2 High Score

# 🚨 Don't change the code below 👇
student_scores = input("Input a list of student scores ").split()
for n in range(0, len(student_scores)):
  student_scores[n] = int(student_scores[n])
print(student_scores)
# 🚨 Don't change the code above 👆

#Write your code below this row 👇


length = 0
for score_length in student_scores:
  length = length+1

highest_score = 0
for score in student_scores:
  if score > highest_score:
    highest_score = score
print(f"highest score is: {highest_score}")

===
#Write your code below this row 👇
# Add even number 1 to 100
#1st way
total1=0
for number1 in range(2,101,2):
  print(number1) # 2 4 6 8
  total1+=number1
print(total1)

#2nd way
total2=0
for number2 in range(1,101):
  print(number2) # 1 2 3 4
  if number2 % 2==0:
    total2+=number2
print(total2)



== 5.4 Fizz Buzz exercise
# Divisible by 3 - Fizz,  divisible by 5 - buzz
# divisible by both - FizzBuzz
# Note: div by 3 and 5 need to be added at start, as it should not overlap *interview
#Write your code below this row 👇

for number in range(1,101):
  if(number %3 ==0 and number % 5 == 0):
    print("FizzBuzz") 
  elif(number % 5 == 0):
    print("Buzz")
  elif(number %3 ==0):
    print("Fizz") 
  else:
    print(number) 



===

#Password Generator Project
import random
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']

print("Welcome to the PyPassword Generator!")
nr_letters= int(input("How many letters would you like in your password?\n")) 
nr_symbols = int(input(f"How many symbols would you like?\n"))
nr_numbers = int(input(f"How many numbers would you like?\n"))

#Eazy Level - Order not randomised:
#e.g. 4 letter, 2 symbol, 2 number = JduE&!91

# password = ""
# for char in range(1,nr_letters+1):
#   password += random.choice(letters)

# for char in range(1,nr_symbols+1):
#   password += random.choice(symbols)

# for char in range(1,nr_numbers+1):
#   password += random.choice(numbers)

# print(password)

#Hard Level - Order of characters randomised:
#e.g. 4 letter, 2 symbol, 2 number = g^2jk8&P
password_list = []
for char in range(1,nr_letters+1):
  password_list.append(random.choice(letters))

for char in range(1,nr_symbols+1):
  password_list.append(random.choice(symbols))

for char in range(1,nr_numbers+1):
  password_list.append(random.choice(numbers))

print(password_list)
random.shuffle(password_list)
print(password_list)

password=''
for char in password_list:
  password+=char
print(f"Your Password is: {password}")

==
Day 6
6 Functions

https://reeborg.ca/reeborg.html?lang=en&mode=python&menu=worlds%2Fmenus%2Freeborg_intro_en.json&name=Alone&url=worlds%2Ftutorial_en%2Falone.json


Hurdle1
def turn_right():
    turn_left()
    turn_left()
    turn_left()

move()
turn_left()
move()
turn_right()
move()
turn_right()
move()
turn_left()
===
L2

def turn_right():
    turn_left()
    turn_left()
    turn_left()

def jump():
    move()
    turn_left()
    move()
    turn_right()
    move()
    turn_right()
    move()
    turn_left()


===
L3

def turn_right():
    turn_left()
    turn_left()
    turn_left()

def jump():
    move()
    turn_left()
    move()
    turn_right()
    move()
    turn_right()
    move()
    turn_left()

for step in range(6):
	jump()

or
number_of_hurdles = 6
while number_of_hurdles > 0:
	jump()
	number_of_hurdles -= 1
	print(number_of_hurdles)

===
while not at_goal:
	jump()


==
Day 7
Hangman Game

#Step 1 
import random

word_list = ["aardvark", "baboon", "camel"]

#TODO-1 - Randomly choose a word from the word_list and assign it to a variable called chosen_word.
word_list_len = len(word_list)
chosen_word = random.choice(word_list)
print(f"Selected word: {chosen_word}")


#TODO-2 - Ask the user to guess a letter and assign their answer to a variable called guess. Make guess lowercase.
guess = input("guess a letter: ").lower()


#TODO-3 - Check if the letter the user guessed (guess) is one of the letters in the chosen_word.
for char in chosen_word:
  if(guess == char ):
    print("Correct")
  else:
    print("Wrong")  


====
#Step 2

import random
word_list = ["aardvark", "baboon", "camel"]
chosen_word = random.choice(word_list)
word_length = len(chosen_word)
#Testing code
print(f'Pssst, the solution is {chosen_word}.')

#TODO-1: - Create an empty List called display.
#For each letter in the chosen_word, add a "_" to 'display'.
#So if the chosen_word was "apple", display should be ["_", "_", "_", "_", "_"] with 5 "_" representing each letter to guess.
display=[]
chosen_word_len = word_length
# for _ in range(chosen_word)
for char in chosen_word: 
  display += "_"
print(display)
guess = input("Guess a letter: ").lower()

#TODO-2: - Loop through each position in the chosen_word;
#If the letter at that position matches 'guess' then reveal that letter in the display at that position.
#e.g. If the user guessed "p" and the chosen word was "apple", then display should be ["_", "p", "p", "_", "_"].
for position in range(word_length):
  letter = chosen_word[position]
  if letter == guess:
    display[position]=letter
print(display)    
#TODO-3: - Print 'display' and you should see the guessed letter in the correct position and every other letter replace with "_".
#Hint - Don't worry about getting the user to guess the next letter. We'll tackle that in step 3.




====
Day 8
# Simple Function
def greet():
  print("Hi Anil")
  print("Good Morning")
  print("How are you")

greet()  

# Function that allows for input
def greet_with_name(name):
  print("Hi "+ name)
  print(f"Good Morning {name}")
  print(f"How are you {name}")

greet_with_name("Angela")  
===

#Simple Function
def greet():
  print("Hello Angela")
  print("How do you do Jack Bauer?")
  print("Isn't the weather nice today?")
greet()

#Function that allows for input
#'name' is the parameter.
#'Jack Bauer' is the argument.
def greet_with_name(name):
  print(f"Hello {name}")
  print(f"How do you do {name}?")
greet_with_name("Jack Bauer")

#Functions with more than 1 input
def greet_with(name, location):
  print(f"Hello {name}")
  print(f"What is it like in {location}?")

#Calling greet_with() with Positional Arguments
greet_with("Jack Bauer", "Nowhere")
#vs.
greet_with("Nowhere", "Jack Bauer")


#Calling greet_with() with Keyword Arguments
greet_with(location="London", name="Angela")


==
#Write your code below this line 👇
import math

def paint_calc(height, width, cover):
  area = height * width
  number_of_cans = math.ceil(area / cover)
  print(f"You will need {number_of_cans} cans")

#Write your code above this line 👆
# Define a function called paint_calc() so that the code below works.   

# 🚨 Don't change the code below 👇
test_h = int(input("Height of wall: "))
test_w = int(input("Width of wall: "))
coverage = 5
paint_calc(height=test_h, width=test_w, cover=coverage)




==
Prime Number
# Prime Number -2,3,7,13, 17,19
#Write your code below this line 👇

def prime_checker(number):
  is_prime = True
  for i in range(2,number):
    if number % i == 0:
      # not prime
      is_prime = False
  
  if is_prime:
    print(f"Given number {number} is prime number")
  else:
    print(f"Given number {number} is not prime number")

#Write your code above this line 👆
    
#Do NOT change any of the code below👇
n = int(input("Check this number: "))
prime_checker(number=n)




====


Ciphar Encrypt Decrypt
alphabet = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']

def caesar(start_text, shift_amount, cipher_direction):
  end_text = ""
  if cipher_direction == "decode":
    shift_amount *= -1
  for char in start_text:
    #TODO-3: What happens if the user enters a number/symbol/space?
    #Can you fix the code to keep the number/symbol/space when the text is encoded/decoded?
    #e.g. start_text = "meet me at 3"
    #end_text = "•••• •• •• 3"
    if char in alphabet:
      position = alphabet.index(char)
      new_position = position + shift_amount
      end_text += alphabet[new_position]
    else:
      end_text += char
  print(f"Here's the {cipher_direction}d result: {end_text}")

#TODO-1: Import and print the logo from art.py when the program starts.
from art import logo
print(logo)

#TODO-4: Can you figure out a way to ask the user if they want to restart the cipher program?
#e.g. Type 'yes' if you want to go again. Otherwise type 'no'.
#If they type 'yes' then ask them for the direction/text/shift again and call the caesar() function again?
#Hint: Try creating a while loop that continues to execute the program if the user types 'yes'.
should_end = False
while not should_end:

  direction = input("Type 'encode' to encrypt, type 'decode' to decrypt:\n")
  text = input("Type your message:\n").lower()
  shift = int(input("Type the shift number:\n"))
  #TODO-2: What if the user enters a shift that is greater than the number of letters in the alphabet?
  #Try running the program and entering a shift number of 45.
  #Add some code so that the program continues to work even if the user enters a shift number greater than 26. 
  #Hint: Think about how you can use the modulus (%).
  shift = shift % 26

  caesar(start_text=text, shift_amount=shift, cipher_direction=direction)

  restart = input("Type 'yes' if you want to go again. Otherwise type 'no'.\n")
  if restart == "no":
    should_end = True
    print("Goodbye")
    































