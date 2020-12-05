# 160 Line Hello World

##### 2020.12.05

## Pardon?

After coming across Javascript features I didn't know so many times, I decided to finally learn a good portion of them. I decided the best way to do this, was by creating a hello world program that attempts to use as many language features as possible, and be generally overly-complicated and stupid. If you want to look at it yourself [here it is running](https://rsninja.dev/how-are-you-world/index.html), and [here is the code](https://github.com/rsninja722/how-are-you-world)

## Planning

"hello world" is just so cliché, and besides, now one ever bothers to ask how the Earth is feeling, it's just alway hello from this language, hello from that language. With this, I decided I wanted to output the text "how are you world?". I wanted to add every letter separately, so I didn't end up with one big blob of code. I also wanted to display the text in a complex way, so I created a canvas and drew the text on it one letter at a time.

## Creation

I would only do a few letters at a time, since each one would take about an hour of learning, and/or an hour of messing around in the console to figure out the most unnecessary way possible to add the letter. This is the project I have learned the most about javascript with, since I tried to find and use all the obscure parts of js I could. I still don't feel like I have complete knowledge of js, but doing this got me much closer.

## Findings

Here are some of my favorite things I found

#### Nullish coalescing operator

It returns the left side, if it is a falsy value that is not null, or undefined

```js
var bar = 0 ?? 2; // bar = 0
```

#### Void

It returns undefined no matter what it evaluates

```js
function f() {
    return true;
}
var bar = void f(); // bar = undefined
```

#### Static

Methods and properties in js classes can have the static prefix

```js
class w {
    static x = 2;
    static y() { return 1; }
    z() { return 1; }
}
var foo = w.x; // foo = 2;
var bar = new w().x; // bar = undefined
var baz = w.y(); // baz = 1
var qux = w.z(); // Uncaught TypeError: x.z is not a function
```

#### calling methods on numbers

All of these are valid

```js
(42).toString();
(42.0).toString();
(42).toString();
(42).toString();
// but not 42.toString();
```

#### (almost) EVERYTHING is an object

even booleans

```js
new Boolean(1);
// > Boolean {false}
//    > __proto__: Boolean
//      [[PrimitiveValue]]: false

true.__proto__; // Boolean {false, constructor: ƒ, toString: ƒ, valueOf: ƒ}
```

#### yield can be chained

```js
function* q() {
    yield yield;
}
var r = q();
r.next(); // {value: undefined, done: false}
r.next(1); // {value: 1, done: false}
```

#### BigInt

BigInt

```js
BigInt(1);
```

#### Symbols

using symbols lets you define some crazy stuff, like a custom iterator. Also, since functions are objects, they too can have properties

```js
var x = {};
x[Symbol.iterator] = () => {
    return { // all that's needed for a valid iterator, is a method that returns an object with a next method 
        next() {
            this.y = this.y === undefined ? 0 : this.y + 1; // iterate y, or create it if the "next" method doesn't have it yet
            return { value: this.y, done: this.y == 5 };
        }
    };
};
for(var i of x) {
    console.log(i);
}
// > 0  1  2  3  4

var foo = [...x]; // [0, 1, 2, 3, 4]
```
also /\ spread operator /\ is cool. Any iterable object can be spread out into an array

#### With
the with block is similar to c++ "using namespace", whatever is in the brackets, you don't have to put in front of its methods and properties.
```js
with (Math) {
    console.log(sin(PI)); // 1.2246467991473532e-16
}
```

#### Labels

labels can only be used with break and continue, but let you jump around in loops.

```js
loop1:
for(var i=0;i<10;i++) {
    for(var j=0;j<10;j++) {
        console.log(j);
        if(j == 3) { 
            break loop1;
        }
    }
    console.log(i);
}
// > 0  1  2  3
```

## Conclusion

Javascript is just weird. It has a lot of freedom and leniency, most of the time, too much of it. I had fun doing this project, but after peeling off the Javascripts' mask and starring it in the ugly, convoluted eyes (which are Objects by the way), I want to do c++ or something.