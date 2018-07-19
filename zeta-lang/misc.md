### Miscellaneous programs 

## Guessing game
~~~~
let rand = random(5);
let count = 0;
let check = false;
while(count < 3) {
    let guess = readInt();
    if(guess == rand) {
        print "You won";
        check = true;
    }
    count = count + 1;
}
if(!check) print "You loose";
~~~~

## 2-D point

~~~~
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