# GuessNumber

import random
def guess(x):
  rn=random.randint(1,x)
  guess=0
  while guess!=rn:
    guess=int(input(f'guess a number between 1 and {x}: '))
    if guess>rn:
      print('sorry, guess again, too high')
    elif guess<rn:
      print('sorry, guess again, too low: ')

  print(f'yeye, you guessed right number {rn} correctly: ')

def computer_guess(x):
  low=1
  high=x
  feedback=' '
  while feedback!='c':
    if low!=high:
      guess=random.randint(low,high)
    else:
      guess=low
    feedback=input(f'Is{guess} too high(H), too low(L), or correct(C) ?? ').lower()
    if feedback=='h':
      high=guess-1
    elif feedback=='l':
      low=guess+1
  print(f'yeye, the computer guessed your number, {guess}, correctly: ')

computer_guess(10)
