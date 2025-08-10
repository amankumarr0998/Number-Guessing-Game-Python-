# Number-Guessing-Game-Python-
import random

print("Welcome to Number Guessing Game!")
print("I have selected a number between 1 and 100.")

# Random number generate
secret_number = random.randint(1, 100)
attempts = 0

while True:
    guess = input("Enter your guess: ")

    # Input validation
    if not guess.isdigit():
        print("Please enter a valid number.")
        continue

    guess = int(guess)
    attempts += 1

    if guess < secret_number:
        print("Too low! Try again.")
    elif guess > secret_number:
        print("Too high! Try again.")
    else:
        print(f"Congratulations! You guessed it in {attempts} attempts.")
        break

