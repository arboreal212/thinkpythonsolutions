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


    

    

