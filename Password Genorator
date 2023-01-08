#main.py
#!/usr/bin/env python

#imported libraries
import random
import string

#prompt user for desired inputs and sets the amount to variables
print("Hello! Let's get you a new password!\n\n")

while True:
  try:
    lengthAmount = int(input("Enter the desired length of the password: \n"))
  except ValueError:
    print('Please enter a valid integer')
    continue
  break
amountLeft = lengthAmount

while True:
  try:
    lowerAmount = int(input("Enter the desired number of LOWERCASE characters in the password: \n"))
  except ValueError:
    print('Please enter a valid integer')
    continue
  break

while lowerAmount > amountLeft:
  print("Please make sure the amount of lowercase characters is equal too or less than the total length of the password.\n")
  print("How many characteres left to choose for in your new password: ",amountLeft)
  lowerAmount = int(input("Enter the desired number of LOWERCASE characters in the password: \n"))
amountLeft -= lowerAmount
print("How many characteres left to choose for in your new password: ",amountLeft)

while True:
  try:
    upperAmount = int(input("\nEnter the desired number of UPPERCASE characters in the password: \n"))
  except ValueError:
    print('Please enter a valid integer')
    continue
  break

tempAmountLeft = amountLeft
while upperAmount > tempAmountLeft:
  print("Please make sure the amount of uppercase characters is equal too or less than the amount of characters left to choose for.")
  print("How many characteres left to choose for in your new password: ",tempAmountLeft)
  upperAmount = int(input("\nEnter the desired number of UPPERCASE characters in the password: \n"))
amountLeft -= upperAmount
print("How many characteres left to choose for in your new password: ",amountLeft)

while True:
  try:
    specialAmount = int(input("\nEnter the desired number of SPECIAL characters in the password: \n"))
  except ValueError:
    print('Please enter a valid integer')
    continue
  break

tempAmountLeft = amountLeft
while specialAmount > tempAmountLeft:
  print("Please make sure the amount of special characters is equal too or less than the amount of characters left to choose for.")
  print("How many characteres left to choose for in your new password: ",tempAmountLeft)
  specialAmount = int(input("\nEnter the desired number of SPECIAL characters in the password: \n"))
amountLeft -= specialAmount
print("How many characteres left to choose for in your new password: ",amountLeft)

while True:
  try:
    numericalAmount = int(input("\nEnter the desired number of NUMERICAL characters in the password: \n"))
  except ValueError:
    print('Please enter a valid integer')
    continue
  break

tempAmountLeft = amountLeft
while numericalAmount > tempAmountLeft:
  print("Please make sure the amount of numerical characters is equal too or less than the amount of characters left to choose for.")
  print("How many characteres left to choose for in your new password: ",tempAmountLeft)
  numericalAmount = int(input("\nEnter the desired number of NUMERICAL characters in the password: \n"))
amountLeft -= numericalAmount

#creates lists to include all lowercase, uppercase, numerical, and special characters
lower = list(string.ascii_lowercase)
upper = list(string.ascii_uppercase)
special = list(string.punctuation)
num = list(string.digits)

#combines all lists
alphaList = lower + upper + special + num

print('')
print('Here is a list of all characters that can be in your password:')
print(alphaList)

#generates password list
tempPassword = []
i = 0
count = 0

#adds the correct number of lowercase characters to tempPassword list
for i in range(0, lowerAmount):
  randomLower = random.choice(lower)
  tempPassword.insert((random.randint(0,lengthAmount)),randomLower)
  count += 1
  
#adds the correct nubmer of uppercase characters to tempPassword list
for i in range(upperAmount):
  randomUpper = random.choice(upper)
  tempPassword.insert((random.randint(0,lengthAmount)),randomUpper)
  count += 1

#adds the correct number of special characters to tempPassword list
for i in range(specialAmount):
  randomSpecial = random.choice(special)
  tempPassword.insert((random.randint(0,specialAmount)),randomSpecial)
  count += 1

#adds the correct number of numerical characters to tempPassword list
for i in range(numericalAmount):
  randomNumerical = random.choice(num)
  tempPassword.insert((random.randint(0,numericalAmount)),randomNumerical)
  count += 1

#if count == length, done, otherwise add random characters until length is obtained
if count == lengthAmount:
  print("Password is generated!")
else:
  while len(tempPassword) < lengthAmount:
    tempPassword += ''.join(random.choice(alphaList))
    count += 1

#prints password
print('')
print("Here's your password as a list: \n",tempPassword)

newPass = []
newPass = (''.join(tempPassword))
print('')
print("Here's your final randomly generated password:\n",newPass)


