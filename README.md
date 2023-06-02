# Lucky-Draw-in-Python-v1
# just a random beginner program.

from random import randint
from string import ascii_uppercase
div=int(input('enter no. of divisions'))
val=int(input('enter no. of values'))
tickets=[k+str(i) for i in [j for j in range(1,val+1)] for k in list(ascii_uppercase)[0:div+1]]
print(tickets)
guess=[input(f'enter any divison upto {list(ascii_uppercase)[div]}:'), int(input(f'enter any value upto {val}:'))]
print(guess[0].upper()+str(guess[1]))
print('won') if guess[0].upper()+str(guess[1])==list(ascii_uppercase)[randint(0,div)]+str(randint(1,val)) else print('lost')

