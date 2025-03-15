Aimmy Personal, [15-03-2025 13:48]
# QR Code Generator

## Description
This is a simple QR code generator implemented in Python. The program allows users to generate a QR code for any text or URL and save it as an image file.

## Features
- Generates a QR code for any text or URL input.
- Allows users to specify the filename for saving the QR code.
- Uses the qrcode library to create high-quality QR codes.
- Supports customization of box size and border thickness.

## How to Use
1. Run the script in a Python environment.
2. Enter the text or URL you want to encode into the QR code.
3. Specify the filename to save the QR code image.
4. The program generates and saves the QR code as an image file.

## Requirements
- Python 3.x
- qrcode library (can be installed using pip install qrcode[pil])

## Installation
1. Download or clone this repository.
2. Ensure Python is installed on your system.
3. Install the required library using:
      pip install qrcode[pil]
   
4. Run the script using the command:
      python qrcode_generator.py
   

## Example Usage
Enter the text or URL: https://example.com
Enter the filename: my_qrcode.png
QR code saved as my_qrcode.png

## Notes
- The generated QR code will be saved in the current directory.
- The QR code can be scanned using any QR code reader.
- The default colors are black for the QR code and white for the background.

## License
This project is open-source and free to use.

## Author
Developed by Shantanu Suvarna.

Aimmy Personal, [15-03-2025 13:52]
import random

def get_starting_balance():
  while True:
    try:
      balance = int(input('Enter your starting balance: $'))
      if balance <= 0:
        print('Balance must be a positive number.')
      else:
        return balance
    except ValueError:
      print('Please enter a valid number.')


def get_bet_amount(balance):
  while True:
    try:
      bet = int(input('Enter your bet amount: $'))
      if bet > balance or bet <= 0:
        print(f'Invalid bet amount. You can bet between $1 and ${balance}.')
      else:
        return bet
    except ValueError:
      print('Please enter a valid number for the bet amount.')  


def spin_reels():
  symbols = ['🍒', '🍋', '🔔', '⭐️', '🍉']
  return [random.choice(symbols) for _ in range(3)]


def display_reels(reels):
  print(f'{reels[0]} | {reels[1]} | {reels[2]}')


def calculate_payout(reels, bet):
  if reels[0] == reels[1] == reels[2]:
    return bet * 10
  if reels[0] == reels[1] or reels[0] == reels[2] or reels[1] == reels[2]:
    return bet * 2
  return 0


def main():
  balance = get_starting_balance()
  
  print('\nWelcome to the Slot Machine Game!')
  print(f'You start with a balance of ${balance}.')

  while balance > 0:
    print(f'\nCurrent balance: ${balance}')

    bet = get_bet_amount(balance)
    reels = spin_reels()
    display_reels(reels)
    payout = calculate_payout(reels, bet)

    if payout > 0:
      print(f'You won ${payout}!')
    else:
      print('You lost!')

    balance += payout - bet
    if balance <= 0:
      print('You are out of money! Game over.')
      break

    play_again = input('Do you want to play again? (y/n): ').lower()
    if play_again != 'y':
      print(f'You walk away with ${balance}.')
      break


if name == 'main':
  main()

Aimmy Personal, [15-03-2025 13:52]
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