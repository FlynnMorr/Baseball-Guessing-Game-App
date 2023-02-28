# Baseball-Guessing-Game-App
Baseball Player Guessing Game App
def check_guess(guess, answer):
    global score
    still_guessing = True
    attempt = 0
    while still_guessing and attempt < 3:
        if guess.lower() == answer.lower():
            print("Correct Answer")
            score = score + 1
            still_guessing = False
        else:
            if attempt < 2:
                guess = input("Sorry Wrong Answer, try again")
            attempt = attempt + 1
    if attempt == 3:
        print("The Correct answer is ", answer)


score = 0
print("Guess the Player")
guess1 = input("Which player led the league in Home Runs in 2022 ")
check_guess(guess1, "Aaron Judge")
guess2 = input("Who won the NL Cy Young Award ")
check_guess(guess2, "Sandy Alcantara")
guess3 = input("Which player won the World Series MVP ")
check_guess(guess3, "Jeremy Pena")
print("Your Score is " + str(score))
