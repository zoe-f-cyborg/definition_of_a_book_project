```
#the following program generates a "definition of the book" in a wide variety of combinations

#initial set up
import random
userTry = "yes"

#intro for readers
print("""
This program generates definitions of a book based on a combination of user inputs and preset definitions.
Through it, you will be allowed to pariticpate in the process of meaning-making, but not determine it.
Sometimes the program will select your definition, but sometimes it will not. 
Once the program times out, your answers will not be saved. 
You may choose to generate as many definitions as you like. 
Enjoy.""")

#user inputs
uservar1 = input("What do you think a book is? ")
uservar2 = input("Who do you think makes it? ")
uservar3 = input("How do you think it is made? (i.e. 'printing the pages') ")
uservar4 = input("How do you think it is read? ")
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
VAR1 = ("a collection of words or pictures", "something over 80 pages, with a beginning, middle, and end", "a physical pbject", "an amalgamation of knowledge", "a series of words grouped together in a specific order", "a series of words grouped together in a specific order which tell a story", "a portable collection of information", "a heavy object bound in leather containing a sacred text", uservar1)
VAR2 = ("an author", "a single mind in isolation", "a publicist", "a designer", "an editor", "a publisher", "a printer", "a bull", "a monk", "a team of collaborators", uservar2)
VAR3 = ("writing with vellum and paint in a scriptorium", "writing with pen and ink", "pulling a printing press", "sending an email", "printing the pages with an industrial laser printer", "binding the pages", uservar3)
VAR4 = ("out loud to an audience", "silently to one's self", "in a linear fashion", "in a nonlinear fashion", "in a hypertextual fashion", "closely", "distantly", uservar4)
VAR5 = ("to tell a story", "to transmit information", "to preserve sacred texts", "to transport one into the mind of another", "to delight the reader", "to earn money", "to be sold", "to educate", "to train one in middle class life", "to be displayed", "to control", uservar5)

#randomly chooses a variable for each slot and and prints the definition, then asks the user if they would like to try again. Anything besides "yes" should exit the program. 
while userTry == "yes":
    var1 = random.choice(VAR1)
    var2 = random.choice(VAR2)
    var3 = random.choice(VAR3)
    var4 = random.choice(VAR4)
    var5 = random.choice(VAR5)
    print("A book is " + var1 + " made by " + var2 + " " + var3 + ". It is meant to be read " + var4 + ". Its purpose is " + var5 + ".")
    userTry = input("generate another definition? (yes/no) ")
