# 🎮 Python Mini Games

Welcome to the Python Mini Games project!

This repository includes two fun and beginner-friendly games built using Python:

1. Number Guessing Game

2. Rock–Paper–Scissors Game (also known as Oẳn tù tì in Vietnamese)

These games are designed to help you practice basic Python concepts such as:

- User input and output

- Conditional statements (if, elif, else)

- Loops (while, for)

- Random number generation

- Simple game logic and flow control

🧠 Why This Project?

Whether you’re just getting started with Python or want to reinforce your understanding through interactive mini-projects, this is a great place to build practical skills in a fun way.

🧠 **Problem-Solving Mindset (Step-by-Step Guide)**

Each exercise follows a logical approach that you can use when solving any Python problem:

1. Read & Understand the Problem
→ Identify the goal, keywords, and the expected input/output

2. Clarify Input and Output
→ Know the required data type and format clearly

3. Sketch a Quick Plan
→ Outline your solution idea briefly

4. Link Back to What You've Learned
→ Map your plan to Python knowledge: loops, conditions, etc.

5. Break Down the Problem
→ Think in smaller steps:

    - Looping through data

    - Checking conditions

    - Updating variables or collections

6. Write a Function Skeleton
→ Example: def function_name(params): ...

7. Implement Step-by-Step Logic
→ Code exactly what you planned using loop → condition → update flow

8. Test with Sample Inputs
→ Compare actual output with the expected one

9. Refactor if Needed
→ Improve readability, fix bugs, or optimize performance

# 🎯 [**Games Included**](https://drive.google.com/file/d/1oYgGdQTXVZyUQFBVuIdhhejLL4B4T90m/view?usp=sharing)

## 1. 🔢 Guess the Number

Description:

The computer randomly selects a number within a given range, and the user has to guess it. After each guess, the program gives hints like "Too high" or "Too low" until the user finds the correct number.

Features:

- Uses random module to generate the number

- Simple while loop for multiple attempts

- Keeps track of how many guesses were made

* Code

```ruby
import random

number = random.randint(1,10)
guess_count = 1
guess_limit = 5
player_name = input("Hi! What's your name? ")
print("Nice to meet you, " + player_name + ". Let's play our guessing game")

while guess_count <= guess_limit:
    guess = int(input("The number you guess is: "))
    
    if guess < number:
        print('Your guessing number is too low')
        guess_count = guess_count + 1
    elif guess > number:
        print('Your guessing number is too high')
        guess_count = guess_count + 1
    else:
        print('You got correct number after ' + str(guess_count) + ' tries')
        break # stop while loop if we guess the correct number
if guess_count > guess_limit:
    print('Game over. The correct number is ' + str(number))
```

* Results

<img width="617" height="163" alt="image" src="https://github.com/user-attachments/assets/e2ec9729-2f1d-4dee-b16a-de489d397757" />

## 2. ✊✋✌️ Rock–Paper–Scissors

Description:

A classic game where the player competes against the computer. Each side chooses one of three options: Rock, Paper, or Scissors. The rules are:

- Rock beats Scissors

- Scissors beats Paper

- Paper beats Rock

Features:

- User-friendly input (e.g., rock, paper, scissors)

- Computer randomly selects a move

- Game determines the winner and displays the result

* Code

```ruby
import random

arr = ["rock", "paper", "scissors"]

# computer = arr[random.randint(0,2)]

play = True
while play == True:
    computer = arr[random.randint(0,2)].lower()
    player = input("rock, paper or scissors? ").lower()
    print("You chose " + player + ", Machine chose " + computer)
    
    if player == computer:
        print("Draw")
    
    elif player == "rock":
        if computer == "paper":
            print("You lose!")
        else:
            print("You win!")
            
    elif player == "scissors":
        if computer == "rock":
            print("You lose!")
        else:
            print("You win!")
            
    elif player == "paper":
        if computer == "scissors":
            print("You lose!")
        else:
            print("You win!")
    else:
        print("Enter the correct spelling. rock, paper or scissors?")
        
    computer = arr[random.randint(0,2)].lower()
    
    play_more = input("Do you want to continue playing?: ")
    if play_more.lower() in ('no', 'n'):
        print('Thanks for joining!')
        break
```

* Results

<img width="698" height="318" alt="image" src="https://github.com/user-attachments/assets/982cdf59-92be-4bc7-a8d1-0de025135fd5" />

# 🛠 **What You'll Learn**

These games are simple but cover several key programming concepts:

- input() and print()

- Importing and using the random module

- Loops and conditions

- Handling user interaction

- Basic game logic and structure


# 🙌 **Contributing**

Want to add your own game or improve the existing ones? Contributions are welcome!

You can:

- Submit a pull request

- Suggest new ideas in the Issues tab

- Translate the game logic to other languages
