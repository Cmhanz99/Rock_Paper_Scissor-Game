# Rock_Paper_Scissor-Game

import random 
data = ["rock", "paper", "scissor"]

human_score = 0
computer_score = 0

print("Welcome to my Game!")

while True :
    user_input = input("Select an option (rock, paper, scissor), or press    to 'Quit' : ")
    user_input = user_input.lower()
    if user_input == "q" :
        break
    
    if user_input not in data :
        print("You must enter a valid input!")
        continue
    
    # Computer guess
    index = random.randint(0,2)
    computer_guess = data[index]
    if user_input == "rock" and computer_guess == "scissor" :
        human_score += 1
        print(f"You win!, computer picks : {computer_guess}")
    elif user_input == "paper" and computer_guess == "rock" :
        human_score += 1
        print(f"You win!, computer picks : {computer_guess}")
    elif user_input == "scissor" and computer_guess == "paper" :
        human_score += 1
        print(f"You win!, computer picks : {computer_guess}")
    elif user_input == computer_guess :
        print("Draw!")
    else :
        computer_score += 1
        print(f"You lose, computer picks : {computer_guess}")

print(f"\nYour total wins : {human_score}")
print(f"Computer total wins : {computer_score}")

if human_score > computer_score :
    print("Human wins")
else :
    print("Computer wins")
        
