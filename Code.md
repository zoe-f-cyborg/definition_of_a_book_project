'#the following program generate a "definition of the book" in a wide variety of combinations

#initial set up
import random
userTry = "yes"

#intro for readers
print(""""
This program generates definitions of a book based on a combination of user inputs and preset definitions.
Through it, you will be allowed to pariticpate in the process of meaning-making, but not determine it.
Sometimes the program will select your definition, but sometimes it will not. 
Sometimes it will make sense, sometimes it will not. It may cause anger, joy, fear, excitement, or any other number of emotions.
You may choose to generate as many definitions as you like. Enjoy.""")

#user inputs
uservar1 = input("What do you think a book is? ")
uservar2 = input("Who do you think makes it? ")
uservar3 = input("Where do you think it is made? ")
uservar4 = input("which tools do you think they use? ")
uservar5 = input("What do you think its purpose is? ")

#this part of the code is bracketed off with apostrophes becuase it is under cosntruction. It is inessential however, so I may not use it. 
'''VAR1 = ("an object", "a series of written words numbering over 50,000, meant to be read together", "an idea", "anything which was intended to be a book", "a book")
if uservar1 == VAR1
    uservar1 = ()
    print("that is already a definition")
    userchoice1 = input("would you like to enter a new word? (yes/no) ")
    if userchoice1 = "yes"
        uservar1 = input("What is your new coice? ")'''

#creating a list of potential words/phrases for each variable
VAR1 = ("an object", "a series of written words numbering over 50,000, meant to be read together", "an idea", "anything which was intended to be a book", "a book", uservar1)
VAR2 = ("an author", "a publisher", "a bull", "an editor," "a monk", "dictating", uservar2)
VAR3 = ("a scriptorium", "a printing house", "a word processing program", uservar3)
VAR4 = ("pen and paper", "vellum and ink", "industrial digital printers", "hands", "minds", uservar4)
VAR5 = ("to teach", "to delight", "to sell", "to burn", "to preserve knoweldge", "to preserve records", "to aggregate knowledge", "to control you", uservar5)

#randomly chooses a variable for each slot and and prints the definition, then asks the user if they would like to try again. Anything besides "yes" should exit the program. 
while userTry == "yes":
    var1 = random.choice(VAR1)
    var2 = random.choice(VAR2)
    var3 = random.choice(VAR3)
    var4 = random.choice(VAR4)
    var5 = random.choice(VAR5)
    print("A book is " + var1 + " made by " + var2 + " in " + var3 + " with " + var4 + ". Its purpose is " + var5 + ".")
    userTry = input("generate another definition? (yes/no)")'
