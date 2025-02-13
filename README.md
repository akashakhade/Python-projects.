# Python-projects.
This is my first project which is calculator. 


 _____________________
|  _________________  |
| | Pythonista   0. | |  .----------------.  .----------------.  .----------------.  .----------------. 
| |_________________| | | .--------------. || .--------------. || .--------------. || .--------------. |
|  ___ ___ ___   ___  | | |     ______   | || |      __      | || |   _____      | || |     ______   | |
| | 7 | 8 | 9 | | + | | | |   .' ___  |  | || |     /  \     | || |  |_   _|     | || |   .' ___  |  | |
| |___|___|___| |___| | | |  / .'   \_|  | || |    / /\ \    | || |    | |       | || |  / .'   \_|  | |
| | 4 | 5 | 6 | | - | | | |  | |         | || |   / ____ \   | || |    | |   _   | || |  | |         | |
| |___|___|___| |___| | | |  \ `.___.'\  | || | _/ /    \ \_ | || |   _| |__/ |  | || |  \ `.___.'\  | |
| | 1 | 2 | 3 | | x | | | |   `._____.'  | || ||____|  |____|| || |  |________|  | || |   `._____.'  | |
| |___|___|___| |___| | | |              | || |              | || |              | || |              | |
| | . | 0 | = | | / | | | '--------------' || '--------------' || '--------------' || '--------------' |
| |___|___|___| |___| |  '----------------'  '----------------'  '----------------'  '----------------' 
|_____________________|

import art
""" write code for input of +, -,*,/.
"""

def add(n1, n2):
    return n1 + n2

def subtract(n1, n2):
    return n1 - n2

def multiply(n1, n2):
    return n1 * n2

def divide(n1, n2):
    return  n1 / n2

""" Add these 4 functions into a dictionary as the values. Keys = "+", "-", "*", "/"
 """

operation = {
    "+" : add,
    
    "-" : subtract,
    
    "*" : multiply,
    
    "/" : divide

}

"""  Use the dictionary operations to perform the calculations. Multiply 4 * 8 using the dictionary."""

def calculation():
   
   print(art.logo)

   should_i= True
   
   a = float(input("Enter the 1 num = "))
   
   while should_i:
     
     for symbol in operation:
         
         print(symbol)
     
     operator = input("Enter operator = ")
     
     b = float(input("Enter the 2 num = "))

     if operator in operation:
      result = operation[operator](a, b)
      print(f" {a} {operator} {b}= {result}")
     else:
      print("invalid operation")

     choice = input("Do you want continue ? (yes / no) = ").strip().lower()

     if choice == "yes":
        a = result
     else:
         print(f"Existing answer is = {result}")
         should_i = False
         print("\n" * 20)
         calculation()

calculation()
