import operator
import sys

ops = {"+": operator.add, "-": operator.sub, '*': operator.mul, '/': operator.truediv, }

def calculation():

    while True:
        calculation_input = input('Enter an operation: ')

        if calculation_input == '+' or calculation_input == '-' or calculation_input == '*' or calculation_input == '/':
            return cal(calculation_input)
            break

def isint(value):
    try:
        int(value)
        return True
    except:
        return False



def cal(calculation):

    while True:

        number_2 = input('Enter another number: ')
        if isint(number_2):
            number_2 = int(number_2)
            result = ops[calculation](number_1, number_2)
            print('Result:', result)
            print(' ')
            calculation1()
        else:
            print ("This is not a number.")
            cal(calculation)
            break

def calculation1():
    while True:
        number_1 = input('Enter number (or a letter to exit): ')
        if isint(number_1):
            number_1 = int(number_1)
            calculation()
        else:
            sys.exit(0)

while True:
    number_1 = input('Enter number (or a letter to exit): ')
    if isint(number_1):
        number_1 = int(number_1)
        calculation()
    else:
        break
