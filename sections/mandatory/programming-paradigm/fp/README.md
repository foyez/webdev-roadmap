[✔]: ../../../../assets/images/checkbox-small-blue.png

# Functional Programming

<br /><br />

## Table of contents

1. [At a Glance](#1-at-a-glance)

<br /><br />

# `1. At a glance`

<details>
<summary>View contents</summary>

## ![✔] 1.1 What is functional programming?

- `a programming paradigm`
- `a code style`
- `a mindset`
- `a sexy, buzz-wordy trend`

## ![✔] 1.2 Why functional JavaScript?

- `object-oriented JS gets tricky(prototypes? this?!?)`
- `safer, easier to debug/maintain`
- `established community`

## ![✔] 1.3 Do everything with functions

input &#8594; output

### Non functional / imperative programming:

```js
var name = “Anjana”;
var greeting = “Hi, I’m ”;
console.log(greeting + name);

> “Hi, I’m Anjana”
```

### functional:

```js
function greet(name) {
  return “Hi, I’m ” + name;
}
greet(“Anjana”);

> “Hi, I’m Anjana”
```

## ![✔] 1.4 Avoid side effects

- use `pure` functions

### Not pure:

```js
var name = 'Foyez'
function greet() {
  console.log("Hi, I'm " + name)
}
```

### Pure:

```js
function greet(name) {
  return "Hi, I'm " + name
}
```

## ![✔] 1.5 Use higher-order functions

- `functions can be inputs/outputs`

```js
function makeAdjectifier(adjective) {
  return function (string) {
    return adjective + “ ” + string;
  };
}

var coolifier = makeAdjectifier(“cool”);
coolifier(“conference”);

> “cool conference”
```

## ![✔] 1.6 Don't iterate

- `use map, reduce, filter`

## ![✔] 1.7 Avoid mutability

- `use immutable data`

### Mutation (bad!):

```js
var rooms = [“H1”, “H2”, “H3”];
rooms[2] = “H4”;

// rooms => ["H1", "H2", "H4"]
```

### No mutation (good!):

```js
var rooms = [“H1”, “H2”, “H3”];
var newRooms = rooms.map(function (rm) {
  if (rm === “H3”) {
    return “H4”;
  }  else {
    return rm;
  }
});

// newRooms => ["H1", "H2", "H4"]
// rooms => ["H1", "H2", "H3"]
```

## ![✔] 1.8 Persistent data structures for efficient immutability

- `libraries`: Mori, Immutable.js

## ![✔] 1.9 FP libraries for JS

- Mori (http://swannodette.github.io/mori)
- Immutable.js (https://facebook.github.io/immutable-js/)
- Underscore (http://underscorejs.org)
- Lodash (https://lodash.com)
- Ramda (http://ramdajs.com)

## ![✔] 1.10 Useful links

- [Curry and Function Composition](https://medium.com/javascript-scene/curry-and-function-composition-2c208d774983)
- [Composing Software: The Book](https://medium.com/javascript-scene/composing-software-the-book-f31c77fc3ddc)
- [An introduction to functional programming](https://codewords.recurse.com/issues/one/an-introduction-to-functional-programming)
- [Functional Programming in Javascript: How and Why](https://blog.bitsrc.io/functional-programming-in-javascript-how-and-why-94e7a97343b)
- [Functional JavaScript: Function Composition For Every Day Use](https://hackernoon.com/javascript-functional-composition-for-every-day-use-22421ef65a10)
- [An introduction to functional programming in JavaScript](https://opensource.com/article/17/6/functional-javascript)

</details>

<br>[⬆ Back to top](#table-of-contents)
