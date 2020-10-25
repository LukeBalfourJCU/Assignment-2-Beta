"""

"""

from placecollection import PlaceCollection

MENU = """
L \t---- List places
A \t---- Add new place
M \t---- Mark a place as visited
Q \t---- Quit
>>> 
"""

FILENAME = "visitList.csv"
data = []

#LIST FUNCTION

def listFunction(PlaceCollection):
    for places in PlaceCollection.places:
        print(places)

#ADD FUNCTION
def addFunction(data,FILENAME):

    dataMark = 1
    inputFile = open(FILENAME, "a")

    for data in range(1, dataMark + 1):

        name = str(input("Name: "))
        while name == "":
            print("Input cannot be blank")
            name = str(input("Name: "))

        country = str(input("Country: "))
        while country == "":
            print("Input cannot be blank")
            country = str(input("Country: "))

        try:
            priority = int(input("Priority: "))
            while priority == "":
                print("Invalid input; enter a valid number")
                priority = int(input("Priority: "))
        except:
            print("Invalid input; enter a valid number")

        visited = "*"
        compiler = (name, country, priority, visited)
        data = str(compiler)
        inputFile.write(str(compiler))
        return data



#MARK FUNCTION
def markFunction(data, FILENAME):

#    data = []
    inputFile = open(FILENAME, "w")
    total = ""

    for data, information in enumerate(inputFile):
        total += information
        print("{} {}".format(data, information))
        for dataMark in inputFile:
            dataMark = 0
            if "X" in inputFile:
                dataMark += 1
        print("{}".format(dataMark))

    userInput = str(input("Enter the number of a place to mark as visited"))

def saveFunction(inputFile, FILENAME):
    inputFile = FILENAME
    inputFile.close(FILENAME)

#MAIN FUNCTION
def main():
    choice = input(MENU).upper()
    print(data)
    while choice != "Q":
        if choice == "L":
            listFunction(data, FILENAME)
        elif choice == "A":
            PlaceCollection.add_places(PlaceCollection)
        elif choice == "M":
            markFunction(PlaceCollection)
        else:
            print("Invalid menu choice")
        choice = input(MENU).upper()
    PlaceCollection.save_places(PlaceCollection)

main()





