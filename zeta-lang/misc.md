### Miscellaneous programs 

## Guessing game
~~~~ zeta
let rand = random(5);
let count = 0;
let check = false;
print "Enter a number:";
while(count < 3) {
    let guess = readInt();
    if(guess == rand) {
        print "You won";
        check = true;
        break;
    }
    count = count + 1;
}
if(!check) print "You loose";
~~~~

## 2-D point

~~~~ zeta
class Point {
    Point(x,y) {
        this.x = x;
        this.y = y;
    }
}

let point = Point(3,5);
print point.x;
print point.y;

~~~~
