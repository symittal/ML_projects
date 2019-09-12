import random

games = ''

while games == '':
    try:
        games = int(input("Enter the number of games"))
    except:
        print("Please select using number")

for game in range(0, games):
    pick = random.randint(1,25)
    attempts = 1
    userGuess = 0

    try:
        userGuess = int(input("Enter guess"))

    except:
       print("Select proprt number")

    if(pick != userGuess):
         attempts += 1
         if userGuess > pick:
             print("Select low number")
         else:
              print("Slect high number")

    else:
        print("Guess in attempts:%s", attempts)