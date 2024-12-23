# task-4
NUMBER GUESSING GAME  Create a number guessing game where the computer selects a random number, and the user has to guess it
import random

# Generate a random number between 1 and 100
number_to_guess = random.randint(1, 100)
attempts = 0
guessed = False

print("Welcome to the Number Guessing Game!")
print("I'm thinking of a number between 1 and 100.")

# Game loop
while not guessed:
    try:
        # Get user's guess
        user_guess = int(input("Enter your guess: "))
        attempts += 1

        if user_guess < number_to_guess:
            print("Too low! Try again.")
        elif user_guess > number_to_guess:
            print("Too high! Try again.")
        else:
            print(f"Congratulations! You guessed the number in {attempts} attempts.")
            guessed = True
    except ValueError:
        print("Please enter a valid number.")

print("Thank you for playing!")
