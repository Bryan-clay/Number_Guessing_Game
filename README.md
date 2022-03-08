# Number_Guessing_Game
A simple number guessing game

import random

def guessing_game():
    number = random.randint(1,10)
    guesses = 0
    print('I am guessing a number between 1 and 10!')

    while guesses < 5:
        guess = int(input('What is your guess? '))
        guesses += 1
        if guess > number:
            print('Too high, guess again!')
        if guess < number:
            print('Too low, guess again!')
        if guess == number:
            break
    if guess == number:
        print(f'Correct! The correct number is {number}! You correctly guessed it'
              f' in {guesses} guesses.')
    else:
        print(f'You did not correctly guess the number. The number was {number}'
              f' try again.')
