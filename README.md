# ThinkPythonSolutions


*Exercise 3.3. Python provides a built-in function called len that returns the length of a string, so
the value of len('allen') is 5.
Write a function named right_justify that takes a string named s as a parameter and prints the
string with enough leading spaces so that the last letter of the string is in column 70 of the display.*

```
def right_justify(s):
    print((70-len(s))*' '+s)
    
right_justify('open')    
```

*Exercise 3.4. A function object is a value you can assign to a variable or pass as an argument. For example, do_twice is a function that takes a function object as an argument and calls it twice:*
```
def do_twice(f):
    f()
f()
```
*Here’s an example that uses do_twice to call a function named print_spam twice.*
```
def print_spam():
    print 'spam'
do_twice(print_spam)
```

*Modify do_twice so that it takes two arguments, a function object and a value, and calls the function twice, passing the value as an argument.*

```
def do_twice(f,num):
    f(num)
    f(num)
```

*Write a more general version of print_spam, called print_twice, that takes a string as a parameter and prints it twice.*

```
def print_twice(mystring):
    print (mystring)
    print (mystring)
```

*Use the modified version of do_twice to call print_twice twice, passing 'spam' as an argument.*

```
do_twice(print_twice, 'spam')
```

*Define a new function called do_four that takes a function object and a value and calls the function four times, passing the value as a parameter. There should be only two statements in the body of this function, not four.*

```
def do_four(f,num):
    do_twice(f, num)
    do_twice(f, num)

do_four(print_twice, 'spam')
    
```
*Exercise 3.5. This exercise can be done using only the statements and other features we have learned so far.
1. Write a function that draws a grid like the following:*
```
+ - - - - + - - - - +
|         |         |
|         |         |
|         |         |
|         |         |
+ - - - - + - - - - +
|         |         |
|         |         |
|         |         |
|         |         |
+ - - - - + - - - - +

```
```
def do_twice(f):
    f()
    f()
    
 def do_four(f):
    do_twice(f)
    do_twice(f)
    
def print_beam():
    print ('+ - - - -', end= ' '),
    
do_twice(print_beam)

def print_post():
    print ('|        ', end=' '),
    
def print_beams():
    do_twice(print_beam)
    print ('+')

def print_posts():
    do_twice(print_post)
    print ('|') 
    
def print_rows():
    print_beams()
    do_four(print_posts)

def print_grid():
    do_twice(print_rows)
    print_beams()

print_grid()

```
*Write a function called square that takes a parameter named t, which is a turtle. It should use the turtle to draw a square.
Write a function call that passes bob as an argument to square, and then run the program again.
    
```
import turtle
bob=turtle.Turtle()
print(bob)

def square(t):
    for i in range(4):
        t.fd(100)
        t.lt(90)

        square(bob)
        
```

*Add another parameter, named length, to square. Modify the body so length of the sides is length, and then modify the function call to provide a second argument. Run the program again. Test your program with a range of values for length.

```
def square(t, length):
    for i in range(4):
        t.fd(100, length)
        t.lt(90)

        square(bob, 100)
        
```

*
3. The functions lt and rt make 90-degree turns by default, but you can provide a second argument that specifies the number of degrees. For example, lt(bob, 45) turns bob 45 degrees to the left.
Make a copy of square and change the name to polygon. Add another parameter named n and modify the body so it draws an n-sided regular polygon. Hint: The exterior angles of an n-sided regular polygon are 360/n degrees.

```


    

