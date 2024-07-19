import random
score=0
while(1):
    ch=input("enter y/Y to play the game or else Enter n/N : ")
    if (ch=="y" or ch=="Y"):
        user_choice=eval(input("enter your choice : enter 0 for rock,1 for paper, 2 for scissors :"))
        if user_choice>=3 or user_choice<0:
            print("you entered invalid number ,you lose." )
        else:
            computer_choice=random.randint(0,2)
            print("computer chose : ",computer_choice)
            if user_choice==computer_choice:
                print("It's  a draw")
            elif computer_choice==0 and user_choice==2:
                print("you loose")
            elif computer_choice==2 and user_choice==0:
                print("you win")
                score+=1
            elif computer_choice>user_choice:
                print("you loose")
            elif user_choice> computer_choice:
                print("you win")
                score+=1
        print("your score is : ",score)
     
    else:
        break
