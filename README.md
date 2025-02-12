# python-banking-programm

def show_balance():

    print("*********************************************")
    print(f"Your balance is : Rs {balance:.2f}")
def deposite():
    amount=int(input("enter amount to deposit: "))
    if amount<0:
        print("amount is less the zero")
        return 0
    else:
        return amount
def withdraw():
    amount=int(input("enter amount to withdraw: "))
    if amount>balance:
        print("insufficient balance")
        return 0
    else:
        return amount


balance=0
is_running=True

while is_running:
    print("****************************************")
    print("               python banking programm      ")
    print("****************************************")
    print("1.TO CHECK BALANCE")
    print("2.TO DEPOSITE")
    print("3.TO WITHDRAW")
    print("4.TO EXIT")
    choice=input("enter your choice (1,2,3,4) : ")
    choice=int(choice)
    if choice == 1:
          show_balance()
    elif choice == 2:
        balance+=deposite()
    elif choice ==3:
       balance-= withdraw()
    elif choice ==4:
        break
    else:
        print("invalid choice")
print("THANK YOU")
