# Slot Machine Game

## Description
This is a simple command-line slot machine game implemented in Python. Players start with a balance, place bets, spin the reels, and win or lose money based on the outcome.

## Features
- Users can enter a starting balance.
- Players place bets before each spin.
- Reels display randomly chosen symbols.
- Payouts are calculated based on matching symbols.
- The game continues until the player runs out of money or chooses to quit.

## How to Play
1. Run the script in a Python environment.
2. Enter your starting balance.
3. Place a bet (must be within your current balance).
4. The reels spin and display the results.
5. If you match symbols, you win money according to the payout rules.
6. If you lose all your money, the game ends.
7. You can choose to continue playing or walk away with your remaining balance.

## Payout Rules
- Three matching symbols: 10x the bet amount
- Two matching symbols: 2x the bet amount
- No matching symbols: Lose the bet amount

## Requirements
- Python 3.x
- random module (included in Python by default)

## Installation & Execution
1. Download or clone this repository.
2. Ensure Python is installed on your system.
3. Run the script using:
      python slot_machine.py
   

## Example Gameplay
Enter your starting balance: $100

Welcome to the Slot Machine Game!
You start with a balance of $100.

Current balance: $100
Enter your bet amount: $10
🍒 | 🍋 | 🔔
You lost!

Current balance: $90
Enter your bet amount: $20
⭐️ | ⭐️ | ⭐️
You won $200!

Do you want to play again? (y/n): n
You walk away with $270.

## Notes
- Players should bet responsibly.
- The game ends automatically when the balance reaches $0.
- This is a text-based game for entertainment purposes.

## License
This project is open-source and free to use.

## Author
Developed by Shantnu Suvarna
