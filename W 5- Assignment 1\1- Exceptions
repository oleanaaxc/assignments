Part 1 — Errors in Data vs. Errors in Code
Sitiuations 1-3:
The program expects an integer but the user enters hello.		
The programmer writes prin() instead of print().		
The program divides by a value entered by the user, and the user enters 0.

Situation 1:
Bad inpit/data because "heelo" is not the input the program cannot respond in the intended way and will probably stop the program.
Situation 2:
Bug in the code because prin isn't a function name therefor leading to an error/bug.
Situation 3:
Bad input/data because even in math it's not possible so it would lead to an error. You can't divide any number by zero.




Part 2 — Reading an Exception
1: "int(" causes the exception.
2: The exception occurs because without a value there is nothing to convert to an integer.
3: The exception name provides the programmer with the reasoning for error: a value. 
This prompt the user to revisit the code with an entered value.
4: The same exception would not occur, but a different one. 0 can be a value but then, print(1 / value) is not possible because a number cannot be divided by zero. 
It would be a zero division error.




Part 3 — Complete a Basic try-except
try:
    value = int(input("Enter an integer: "))
    print("You entered:", value)
except ValueError:
print("Invalid value")

If entered 4: Program runs smooth
If entered abc: Program output: Invalid value




Part 4 — Trace try-except Control Flow
execution path for 2: 
A
B
C
D
Except branches are skipped with no exception.

execution path for 0:
A
B
Cannot divide by zero
D
C and ValueErro are skipped but there is an exception: ZeroDivisionError

execution path for hello:
A
Invalid Value
D
B, C, and ZeroDivisionError are skippe3d but there is an exception: ValueError.

print("C") doesn't excecute because ZeroDivisionError is connected to a value input in this part of the code: result = 10 / value.
Because there was no valid value input to begin with it skips over and heads straight to the except ValueError.




Part 5 — Handle More Than One Exception
My code:
try:
    value = int(input("Enter an integer: "))
    reciprocal = 1 / value
    print("Reciprocal:", reciprocal)

except ValueError:
    print("This value cannot be used as an integer.")

except ZeroDivisionError:
    print("No value is able to be divided by zero, please enter new value.")

 Explain why only one matching except branch executes for a raised exception: Only one matching except branch executes for a raised exception
because Python matches the error to the specific except rather than using them all.




Part 6 — Common Python Exceptions
# A
number = int("hello") : The exception is ValueError, caused by entering hello rather than an integer.

# B
result = 10 % 0 : The exception is ZeroDivisionError, caused by 10 not being able to be divided by 0.

# C
values = [10, 20, 30]
print(values[1.5]) : The exception is TypeError, caused by 1.5 being a float which MUST be an integer.

# D
values = [1, 2]
values.depend(3) : The exception is AttributeError, caused by depend being used for a list which is not possible/a programming method when used for a list.




Part 7 — The Default except Branch
1: The purpose is to have "Some other exception occurred" be the output if the input code has an exception that doesn't match ValueError or ZeroDivisionError.

2: It excecutes when there's an invalid input that doesn't match ValueError or ZeroDivisionError. Ex: values = [10, 20, 30]
print(values[1.5]) because this is a TypeError which is not a listed except but still an except although not listed.

3: It must appear last so that Python doesn't skip over the other mentioned exceptions since the default except would catch ANY except first and outright output: 
"Some other exception occurred" without checking the prior exceptions.

4: Because then the user can see exactly what the issue is and retry rather than just getting "Some other exception occurred".




Part 8 — Syntax Errors Are Different
ex:
if value > 0
    print("Positive")
Question 1: SyntaxError
Question 2: No colon after "if" statement.
Question 3: Because the error is in the code rather than a user input, and it needs proper syntax to run.




Part 9 — Test Every Execution Path:
testing every conditional execution path in ex:

number = float(input("Enter a number: "))

if number > 0:
    print("Positive")
elif number < 0:
    print("Negative")
else:
    print("Zero")

Test Input: 1
Expected Path: if number > 0: 
    print("Positive")
Expected Result: positive
Actual Result: positive
Pass/Fail: pass

Test Input: -1
Expected Path: if number > 0:
    print("Positive")
elif number < 0:
    print("Negative")
Expected Result: negative
Actual Result: negative
Pass/Fail: pass

Test Input: 0
Expected Path: 
if number > 0:
    print("Positive")
elif number < 0:
    print("Negative")
else:
    print("Zero")

Expected Result: zero
Actual Result: zero
Pass/Fail: pass

Explain why one successful test does not demonstrate that every path works correctly: if we had just put 1 and not checked different inputs we would not be able to verify it worked correctly. It could possibly contain Syntax errors.




Part 10 — Find the Hidden Bug
Question 1: Yes it works.
Question 2: elif value < 0:
    prin("Negative")
Question 3:-1
Question 4: It demonstrates that you must check with different input possibilities rather than just relying on what you see because humans make mistakes and it's possible to slip over the mispell of "prin". AKA triple check with Python's mind.

Correct code:
value = float(input("Enter a number: "))

if value > 0:
    print("Positive")
elif value < 0:
    print("Negative")
else:
    print("Zero")




Part 11 — Print Debugging
Question 1: 50.00
Question 2: 16.5
Question 3: 
def calculate_total(price, quantity):
    print("Entered calculate_total")
    total = price + quantity
    print("Total before return:", total)
    return total

price = float(input("Price: "))
quantity = int(input("Quantity: "))

print("Price:", price)
print("Quantity:", quantity)

result = calculate_total(price, quantity)
print("Total:", result)

Question 4:
 print("Entered calculate_total")- shows that calculate_total is used. 
print("Price:", price)- shows price entered was not the error.
print("Quantity:", quantity)- shows that quantity entered was not the error.
print("Total before return:", total)- shows the calculation before returning meaning that the problem is in the calculation.

Question 5:
   total = price + quantity must become price * quantity

Question 6: Yes. 

Question 7: 
def calculate_total(price, quantity):
    total = price * quantity
    return total

price = float(input("Price: "))
quantity = int(input("Quantity: "))

result = calculate_total(price, quantity)
print("Total:", result)




Part 12 — Integrated Exception-Handling Program
My code:

try:
    number1 = int(input("Enter the first integer: "))
    number2 = int(input("Enter the second integer: "))

    quotient = number1 / number2
    print("Quotient:", quotient)

except ValueError:
    print("Invalid value.")

except ZeroDivisionError:
    print("Cannot divide by zero.")

print("Process completed.")

Tests:
Input 1: 6
Input 2: 3
Expected Path: Completes without issue.
Expected Result: 2
Actual Result: 2
Pass 

Input 1: 1
Input 2: 0
Expected Path: except ZeroDivisionError:
    print("Cannot divide by zero.")
Expected Result: Cannot divide by zero.
Actual Result: Cannot divide by zero.
Pass (pass meaning it did what it needed to.)

Input 1: hello
Input 2:
Expected Path: except ValueError:
    print("Invalid value.")
Expected Result: Invalid value.
Actual Result: Invalid value.
Pass 

Input 1: 1
Input 2: hello
Expected Path: input to except ValueError:
    print("Invalid value.")
Expected Result: Invalid value.
Actual Result: Invalid value.
Pass

Analysis and Reflection:
Question 1:
It means an error occurred with the program while running.
Question 2:
Python matches the issue with the correct except branc, skipping the ones that do not apply.
Question 3:
It provides a reasoning that the user can use as reference.
Question 4:
Because Syntax or other issues may occur that must be tried.
Question 5:
Because it finds the root problem.
Question 6:
Because print shows the inputs and functions being used which helpes show where the program has an issue.
