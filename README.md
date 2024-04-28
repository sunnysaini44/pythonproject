# pythonproject

BASIC CALCULATOR
import math
def sum():
    val_1=int(input("enter the number : "))
    val_2=int(input("enter the number : "))
    sum =val_1+val_2
    return sum
def sub():
    val_1=int(input("enter the number : "))
    val_2=int(input("enter the number : "))
    sub =val_1-val_2
    return sub
def mul():
    val_1=int(input("enter the number : "))
    val_2=int(input("enter the number : "))
    mul =val_1*val_2
    return mul
def div():
    val_1=int(input("enter the number : "))
    val_2=int(input("enter the number : "))
    div =val_1/val_2
    return div
def sqrt():
    val_1=int(input("enter the number : "))
    sqrt =math.sqrt(val_1)
    return sqrt
def pow():
    val_1=int(input("enter the number : "))
    val_2=int(input("enter the number : "))
    pow =val_1**val_2
    return pow
def log():
    val_1=int(input("enter the number : "))
    log =math.log(val_1) 
    return log
def sin():
    val_1=int(input("enter the number : "))
    sin =math.sin(val_1)
    return sin
def cos():
    val_1=int(input("enter the number : "))
    cos =math.cos(val_1) 
    return cos
def tan():
    val_1=int(input("enter the number : "))
    tan =math.tan(val_1)
    return tan
def exp():
    val_1=int(input("enter the number : "))
    
    exp =math.exp(val_1)
    return exp
def fact():
    val_1=int(input("enter the number : "))
    
    fact =math.factorial(val_1)
    return fact
def mod():
    val_1=int(input("enter the number : "))
    val_2=int(input("enter the number : "))
    mod =val_1%val_2
    return mod
def sqr():
    val_1=int(input("enter the number : "))
    sqr =val_1**2
    return sqr
def cube():
    val_1=int(input("enter the number : "))
    cube =val_1**3
    return cube
while True:
    choice=int(input("enter your choice 1->sum 2->sub 3->div 4->mul 5->sqrt 6->pow 7->pow 8->log 9->sin 10->cos 11->tan 12->exp 13->fact 14->mod 15->sqr 16->cube 17->exit:"))
    if choice==1:
       print(sum())
    elif choice==2:
       print(sub())
    elif choice==3:
        print(div())
    elif choice==4:
        print(mul())
    elif choice==5: 
        print(sqrt())
    elif choice==6:
        print(pow())
    elif choice==7:
        print(log())
    elif choice==8:
        print(sin())
    elif choice==9: 
        print(cos())
    elif choice==10:
        print(tan())
    elif choice==11:
        print(exp())
    elif choice==12:
        print(fact())
    elif choice==13:
        print(mod())
    elif choice==14:
        print(sqr())
    elif choice==15: 
        print(cube())
    elif choice==16:
        break
    else:
        print("Invalid choice")

 

GRADING SYSTEM

#grading system 
name=input("enter the name of student ")
maths=int(input("enter maths marks "))
english=int(input("enter english marks "))
python=int(input("enter python marks "))
c=int(input("enter c marks "))
java=int(input("enter java marks "))
t=maths+english+python+c+java
percent=t/5
print("your percentage is: ",percent) 
if(maths>100 or english>100 or python>100 or c>100 or java>100 or maths<0 or english<0 or python<0 or c<0 or java<0):
    print("enter the wrong marks criteria")
elif(percent==100):
    print("grade==O")
elif(percent>=90):
    print("grade==A+")
elif(percent>=80):
    print("grade==B+")
elif(percent>=70): 
    print("grade==B")
elif(percent>=60): 
    print("grade==C")
elif(percent>=50):
    print("grade==D")
else:
    print("fail")
 
NUMBER GUESSING GAME

#guessing number game
import random as p

a=int(input("enter the number "))
b=p.randrange(1,a)
c=int(input("enter the number "))
while(True):
    if(c==0):
        print("game over,player quite the game.")
        break
    elif(c==b):
        print("congratulation you are right. the random number was:",c)
        break
    elif(c<b):
        c=int(input("you are near to correct it play some more time"))
    elif(c>b):
        c=int(input("your guessing is around to corect please play more time"))
    else:
        c=int(input("try again")) 

        
        ROLL THE DICE

#roll the  dice
import random as r
a=1
s=p=0
while(a<7):
    b=r.randint(1,6)
    c=int(input("enter the number between 1to 6: "))
    choice=input("if you quite type'quite' otherwise type 'no' : ")
    s+=b
    p+=c
    if(choice=='quite'):
        break
    elif(choice=='no'):
        continue
    else:
        print("wrong choice")
        break
        
print("\n")
print("your score is:",p)
print("the computer score is:",s)
print("\n")
if(s>p):
    print("computer won with score of:",s)
else:
    print("you won with the score of:",p) 
 
INVENTORY

inventory={}
while True:
    a= input("enter what want you to do? add, remove, display,quit: ")
    if a=='add':
        i=input("enter item name: ")
        q=int(input("enter your quantity: "))
        if i in inventory:
            inventory[i]+=q
        else:
            inventory[i]=q
    elif a=='remove':
        i=input("enter the name of item you want to remove: ")
        q=int(input("enter the quantity you want to remove: "))
        if i in inventory and inventory[i]>=q:
            inventory[i]-=q
        elif i in inventory and inventory[i]<q:
            print("There are only {inventory[item]} left in {item} left in inventory.")
        else:
            print(f"ther is no item left in inventory.")
    
    elif a=='display':
        print("Inventory")
        for key,value in inventory.items():
            print(f"{key}:{value}")
    
    elif a =='quit':
        break
    else:
        print("invalid entry please try again. ") 
reverse forward row,column printing
#reverse forward row,column printing
st=int(input("enter the starting point "))
en=int(input("enter the end point "))
up=int(input("enter the updation "))

choice=input("enter your choice for forward printing or reverse printing:")
choice2=input("enter the choice for row printing or column printing:")

if choice=="forward":
    if choice2=="row":
        for i in range(st,en,up):
            print(i,end=',')
    elif choice2=="column":
        for i in range(st,en,up):
            print(i) 
    else:
        print("enter valid choice.")
elif choice=="reverse":
    if choice2=="row":
        for i in range(en,st,-up):
            print(i,end=',')
    elif choice2=="column":
        for i in range(en,st,-up): 
            print(i)
    else:
        print("enter valid choice")
else:
    print("your both choices are wrong" )
    
rock paper scissoR

#rock paper scissor
import random as r
c=r.choice(['rock','scissor','paper'])
a=input("choice only one 'rock,paper,scissor':")
if(a=='rock'):
    if(c=='rock'):
        print("match draw")
    elif(c=='paper'):
        print("computer wins")
    elif(c=='scisor'):
        print("you win")
if(a=='scissor'):
    if(c=='scisor'):
        print("match draw")
    elif(c=='rock'):
        print("computer wins")
    elif(c=='paper'):
        print("you wins")
if(a=='paper'):
    if(c=='paper'):
        print("match draw")
    elif(c=='rock'):
        print("we loose")
    elif(c=='scissor'):
        print("we win")
    else:
        print("nobody wins") 
    VOTING SYSTEM
print("options are BJP,SP,CNG,BSP,AAP")
def vote_given(votes, candidate):
    if candidate in votes:
        votes[candidate] += 1
    else:
        print(f'Error: {candidate} is not a valid candidate')
def tally_votes(votes):
    total_votes = 0
    for candidate, count in votes.items():
        total_votes += count
        print(f'{candidate}: {count} votes')
    print(f'Total votes: {total_votes}')
candidates = input('Enter the candidates (separated by commas): ').split(',')
votes = {}
for candidate in candidates:
    votes[candidate.strip()] = 0
vote_given(votes, 'BJP')
vote_given(votes, 'CNG')
vote_given(votes, 'SP')
vote_given(votes, 'AAP')
vote_given(votes, 'BSP')
tally_votes(votes) 












