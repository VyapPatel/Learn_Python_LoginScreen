# Learn_Python_LoginScreen
# Made a login and create username interface which helped me learn python

from time import sleep

start = input("Login or Create an account\n:")

username = "Vyap Patel"
password = "Vyap2004"



def login(username, password):

    prompt_Login = input("Username:")
    prompt_Password = input("Password:")

    if username == prompt_Login and password == prompt_Password:
        print("Successfully Logged In")
    else:
        print("Failed to Login")



def create():
    global create_Username
    global create_Password
    create_Username = input("Create Username\n=>")
    create_Password = input("Create Password\n=>")

    return create_Username, create_Password


def main():
    global username
    global password
    global create_Username
    global create_Password

    if start == "Login" or start == "login":
        login(username, password)

    elif start == "Create an account" or start == "create an account":
        print("")

        create()
        # create_Username
        # create_Password

        print("Succesfully created an account")

        username = create_Username
        password = create_Password

        sleep(1)
        print()
        login(username, password)

    else:
        print("Try again")


main()
