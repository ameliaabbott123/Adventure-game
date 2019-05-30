# Adventure-game
#textadventuregame
lives=3
lives_numbergame=3
score=0 
while lives_numbergame>0 and lives>0:
    gamechoice=input("Hello and welcome to the Dragon Cave. You have three lives. Get a score of 3 to win. 1 for Guess the Number, 2 for Rock paper scissors lizard Spock, 3 for hangman")
    gamechoice=int(gamechoice)

    def numbergame(choice,score,lives):
        import random
        value= random.randint(1,6)
        ans= 0
        lives_numbergame=3

        if lives_numbergame==0:
            str(numbergame)
            lives=lives-1
            print("Lives"+ str(lives)) 
        while (ans==0 and lives_numbergame!=0):
            
            
            guess= input("Guess the number between 1 and 6, you have three lives")
            guess= int(guess)

            def closeness(guesss):
                distance= int(value)-int(guess) 
                if distance==1 or distance==-1:
                    print("You are very warm")
                if distance==2 or distance==-2:
                    print("You are quite warm")
                if distance>=3 or distance<=-3:
                    print("You are cold")
            closeness= closeness(guess)
            
            if guess <(value):
                print("Your guess is too low")
                lives_numbergame=lives_numbergame-1
                print(str(closeness))

            if guess == (value):
                print("Well done! You are correct!")
                ans=1
                score=score+1
                print("Points " + str(score))
                print("Lives " + str(lives))
                print("Choose another game")

            if guess > (value):
                print("Your guess is too high")
                lives_numbergame=lives_numbergame-1
                print(str(closeness))
        
            if lives_numbergame==0:
                print("Points " + str(score))
                lives= lives-1 
                print("Lives " + str(lives))
                print("Choose another game")

    if gamechoice==1:
        
        gamechoice= numbergame(gamechoice,score,lives)
if lives==0:
    playagain= input("You have lost! :( Press 9 to play again or 8 to quit")
    playagain=int(playagain)
    if playagain==9:
        lives=3
    else : print("The End. We'll see you next time")

if score==3:
    playagain= input("You have won! :D Press 9 to play again or 8 to quit")
    playagain=int(playagain)
    if playagain==9:
        lives=3
    else : print("The End. We'll see you next time")
    
