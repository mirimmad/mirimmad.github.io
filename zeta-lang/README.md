### Zeta Programming langauge

## Comments, Variables, Value Types and Assignment
~~~~ zeta
// This is a comment
~~~~

~~~ zeta
let a;      // declare and assign nil to a
let b = 50; // declare and assign 50 to b

~~~

~~~~ zeta
let a = nil;    // value nil
let a = true;   // boolean true
let a = false;  // boolean false
let a = 123;    // number
let a = 123.32; // number
let a = "hello"; // string
~~~~

~~~~ zeta
a = 32;   // assign to 32
a = true; // assign a to true
~~~~
> * Variables are always mutable.
* Global variables can be re-declared but local variables can't be.


## Operators

~~~~ zeta
print 1 + 2;
print 1 - 2;
print 5 * 30;
print 30/6;
print 22.0/7.0;
print "hello" + "hi";
print 1 + "one";
print "hello" * 5;      // prints hello five times
print 5 * "hello";      // Runtime Error
~~~~

## The print Statement

~~~~ zeta
print "hello"; // prints hello
print 1+2+3;   //prints 6
~~~~

## Block Statement 

~~~~ zeta
let x = 0;
{
    x = x + 1;
    print x;     // prints 1
    let y = "hey";
    print y;     // prints hey
}
print x;         //prints 1
print y;         // Undefined variable;
~~~~

## Conditonal statements

~~~~ zeta
// if

if(a == 42) {
    print "solved";
}

// if-else

if(a == 42) {
    print "solved";
} else {
    print "failed";
}

~~~~

## Loops
 
~~~~ zeta
// While Loop

while(a < 42) {
    a = a + 1;
}

while(true) print "infinite loop";

// for loop

for( let i = 0 ; i < 50 ; i = i + 1 ) {
    print i;
}

for(;;) print "infinite loop";
~~~~ 
## Break Keyword
~~~~ zeta
let x = 0;
while(true) {
    print x;
    x = x + 1;
    if (x == 10) {
        break; 
    }
} // should print 1 .. 10
~~~~
## Functions

~~~~ zeta
fn hello() {
    print "hello";
}

// parameters

fn greet(name) {
    print "Hello " + name;
}
~~~~

## Closures

~~~~ zeta
// A function that returns updated `count` on every call
fn makeCounter() {
    let count = 0;
    fn increment() {
        count = count + 1;
        print count;
    }
    return increment;
}
~~~~

## Function calls

~~~~ zeta
hello();      // without argument(s)
greet("Mir")  // with argument(s)
~~~~
## Inbuilt Functions

~~~~ zeta
let rand   = random(10);      // Takes a number, n, and returns a random number between 0 and n
let name   = readString();    // reads a string from user
let number = readInt();       // reads a number from user otherwise `nil`

~~~~


## Classes

~~~~ zeta
class Greeting {
    Greeting(name) { // The Constructor
        this.name = name; // Instance field
    }

    sayHello() { // Instance method
        return "Hello " + name;
    }

    sayNight() {
        return "Good Night " + name;
    }
}
~~~~
## Class Instance

~~~~ zeta
let greeting = Greeting("Immad");
print greeeting.sayHello();     // prints Hello Immad
print greeting.sayNight();      // prints Good Night Immad
~~~~

> * A value cannot be retured from the constrcutor.

## Inheritance

~~~~ zeta
class A {
    methodA1() {
        print "methodA1";
    }
}

class B <  A {
    methodB1() {
        super.methodA1();
        print "methodB1";
    }
}

let inst = B();
inst.methodB1();  // prints methodA1
                  //        methodB1
~~~~

[Miscellaneous Programs](/misc)
