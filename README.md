#PASSWORD GENERATOR
import random

print("\tPASSWORD GENERATOR")

#storing available characters and digits in variables
up_case="ABCDEFGHTIJKLMNOPQRSTUVWXYZ"
low_case=up_case.lower()
digits="0123456789"
symbol=";<>/:()[]{}=+-#@_$%^*!&?"

#empty string to store password
total = ""

print("How do you want password?")
print("1.No uppercase\n2.No lowercase\n3.No digits\n4.No symbols")
ch=int(input("Enter your choice: "))

upper=True
lower=True
num=True
sym=True

if ch==1:
    upper=False
if ch==2:
    lower=False
if ch==3:
    num=False
if ch==4:
    sym=False

#to append characters in password acc to user's choice
if upper:
    total+=up_case
if lower:
    total+=low_case
if num:
    total+=digits
if sym:
    total+=symbol

l=int(input("Enter length for pasword: "))
n=int(input("Enter number of passwords to be generated: "))

for i in range(n):
    pas="".join(random.sample(total,l))
    print("Password ",i+1," -> ",pas)


