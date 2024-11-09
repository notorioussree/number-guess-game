# number-guess-game
import random

def guess_the_number():
    """A simple number guessing game."""

    number = random.randint(1, 100)
    guess = 0
    attempts = 0

    print("Welcome to the Guess the Number game!")
    print("I've picked a number between 1 and 100. Can you guess it?")

    while guess != number:
        try:
            guess = int(input("Enter your guess: "))
            attempts += 1

            if guess < number:
                print("Too low. Guess higher.")
            elif guess > number:
                print("Too high. Guess lower.")
            else:
                print(f"Congratulations! You guessed the number in {attempts} attempts.")
        except ValueError:
            print("Invalid input. Please enter a number.")

if __name__ == "__main__":
    guess_the_number()
