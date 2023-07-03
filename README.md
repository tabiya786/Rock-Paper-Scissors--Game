# Rock-Paper-Scissors--Game


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


import random 

games_images =[rock, paper, scissors]

user_choice = int(input("what do you wanna choose? Type 0 for Rock , 1 For Paper or 2 For Scissors.\n"))
if user_choice >=3 or user_choice < 0:
 
 print("You type an invalid number, therefore you lose!")
else:
 print(games_images[user_choice])

computer_choice = random.randint(0,2)
print(f"Computer choose: {computer_choice}")
print(games_images[computer_choice])


if user_choice == 0 or computer_choice == 2:
 print("You win")
elif computer_choice == 2 or user_choice == 0:
  print("You lose")
elif computer_choice > user_choice:
 print("You lose")
elif user_choice > computer_choice:
  print("You win")
elif computer_choice == user_choice:
  print("It's a Draw!")
