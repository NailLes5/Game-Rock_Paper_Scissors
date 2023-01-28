# Game-Rock_Paper_Scissors
The simple game of rock - paper - scissors by Borislav Staykov

import random
rock = "Rock"
paper = "Paper"
scissors = "Scissors"

player_move = input("Choose [r]ock, [p]aper, [s]cissors: ")

if player_move == "r":
    player_move = rock
elif player_move == "p":
    player_move = paper
elif player_move == "s":
    player_move = scissors
else:
    raise SyntaxError("Invalid Input. Try again...")

computer_random_number = random.randint(1, 3)
computer_move = ""

if computer_random_number == 1:
    computer_move = "Rock"
elif computer_random_number == 2:
    computer_move = "Paper"
else:
    computer_move = "Scissors"

print(f"The computer chose {computer_move}.")

if (player_move == rock and computer_move == scissors) or \
        (player_move == paper and computer_move == rock) or \
        (player_move == scissors and computer_move == paper):
    print("You win!")

elif player_move == computer_move:
    print("Draw!")

else:
    print("You Lose!")
