import random

def get_computer_choice():
    return random.choice(["rock", "paper", "scissors"])

def get_user_choice():
    while True:
        user_input = input("\nEnter your choice (rock, paper, or scissors): ").lower()
        if user_input in ["rock", "paper", "scissors"]:
            return user_input
        else:
            print("Invalid input. Please choose 'rock', 'paper', or 'scissors'.")

def determine_winner(user, computer):
    if user == computer:
        return "tie"
    elif (user == "rock" and computer == "scissors") or \
         (user == "scissors" and computer == "paper") or \
         (user == "paper" and computer == "rock"):
        return "user"
    else:
        return "computer"

def play_game():
    user_score = 0
    computer_score = 0

    print("Welcome to Rock-Paper-Scissors Game!")
    print("Type rock, paper, or scissors to play. Let's go!")

    while True:
        user_choice = get_user_choice()
        computer_choice = get_computer_choice()

        print(f"\nYou chose:      {user_choice}")
        print(f"Computer chose: {computer_choice}")

        winner = determine_winner(user_choice, computer_choice)

        if winner == "tie":
            print("Result: It's a Tie!")
        elif winner == "user":
            print("Result: You Win!")
            user_score += 1
        else:
            print("Result: You Lose.")
            computer_score += 1

        print(f"\n Scoreboard - You: {user_score} | Computer: {computer_score}")

        play_again = input("\nDo you want to play again? (yes/no): ").lower()
        if play_again != "yes":
            print("\nThanks for playing! Final Score:")
            print(f"You: {user_score} | Computer: {computer_score}")
            break

# Start the game
play_game()
