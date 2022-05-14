# Games
def display(lst):
    print("{0} | {1} | {2}".format(lst[0],lst[1],lst[2]))
    print("----------")
    print("{0} | {1} | {2}".format(lst[3],lst[4],lst[5]))
    print("----------")
    print("{0} | {1} | {2}".format(lst[6],lst[7],lst[8]))


def user_choice():
    choice="wrong"
    while choice.isdigit()==False :
        choice=input("Please enter a number(0-9) :")
        if choice.isdigit()==False :
            print("Sorry thats not a digit")
    return int(choice)

def place_marker(lst, symbol_player1, position_index):
    lst[position_index] = symbol_player1

lst=[" "," "," ",
     " "," "," ",
     " "," "," "]
display(lst)
symbol_player1=input("Please choose the symbol for the game(x/o) :")
turn=input("Player1 would you like to start the game first(Y/N) :").upper()
if symbol_player1=="x":
    symbol_player2="o"
else:
    symbol_player2="x"
print(symbol_player1)
print(symbol_player2)
position_index=user_choice()
lst[position_index]==symbol_player1
place_marker(lst, symbol_player1, position_index)
display(lst)
