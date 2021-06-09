# Introduction
This guide serves as the set of standards that outline how code should be written and organized.


## 1. Statement Rules
Every statement must be terminated with a semicolon.

``` js

  //good example
  let person = {
    firstName: "John",
    lastName: "Doe",
    age: 35,
    eyeColor: "blue"
  };
   //good example
  let animals = ["cat", "dog", "fox"];


  // bad example
    let person = {
    firstName: "John",
    lastName: "Doe",
    age: 35,
    eyeColor: "blue"
  }
   // bad example
  let animals = ["cat", "dog", "fox"]
```

## 2. Naming Convention
Avoid single letter names. Be descriptive with your naming.  Use camelCase when naming objects, functions, and instances.


``` js
  //good example
  const thisIsMyObject = {};
  function thisIsMyFunction() {}
  function count () {}

 // bad example
  const o = {};
  const this_is_my_object = {};
  function c() {}
```
## 3. Variables
Always use **const** or **let** to declare variables. Use **const** by default, unless a variable needs to be reassigned. The **var** keyword must not be used.

```js
  //good example
  const x = 2;
  const array = [1, 2, 3];
  let userName = 'Oksana';

  //  bad example
  var x = 2;
  userName = 'Oksana';
  let sportTeam;
```

## 4. Arrow Functions
Arrow functions are preferred because they allow us to write shorter function syntax.
```js
  //good example
  hello = () => {
  return "Hello World!";
  }

  // Traditional Function
  function (a, b){
    return a + b + 100;
  }

  // Arrow Function
  (a, b) => a + b + 100;
```
## 5.  Strings
Use single quotes '' for strings.
If a string contains a single quote character, consider using a template string to avoid having to escape the quote.
```js
  // good example
  let saying = `Say it ain't so`;
  let phrase = 'We are the so-called "Vikings" from the north.';

  //  bad example
  let saying = 'Say it ain't so';
  let phrase = "We are the so-called "Vikings" from the north.";
```

Use template literals (delimited with `) over complex string concatenation. Template literals may span multiple lines.

```js
  //good example
  function sayHi(name) {
    return `How are you, ${name}?`;
  }

  //  bad example
  function sayHi(name) {
    return 'How are you, ' + name + '?';
  }
```


## 6. One variable per declaration
Every local variable declaration declares only one variable:
```js
  //good example
  let a = 1;let b = 2;let c = 3;

  //  bad example
  let a = 1, b = 2, c = 3;
```
## 7. Constructor
Constructor names must begin with a capital letter.

```js
  //good example
  function Animal () {}
  let dog = new Animal()

  //  bad example
  function animal () {}
  let dog = new animal()
```
Constructors of derived classes must call super.

```js
    //good example
  class Dog extends Animal {
    constructor () {
      super()
      this.legs = 4
    }
  }

    //  bad example
  class Dog extends Animal {
    constructor () {
      this.legs = 4
    }
  }
```

## 8. Array
Use array literals instead of array constructors.


```js
    //good example
  let nums = [1, 2, 3];

    //  bad example
  let nums = new Array(1, 2, 3);
```

## 9. Conditionals
When using for/for...of loops, make sure to define the initializer properly, with a let keyword:
```js
    //good example
  let cats = ['Athena', 'Luna'];
  for(let i of cats) {
    console.log(i);
  }

    //  bad example
  let cats = ['Athena', 'Luna'];
  for(i of cats) {
    console.log(i);
  }
```

## 10. Comments
Use line comments, not block comments. The comments should start at the left margin.
Use ‘//’ in start of comment
```js
    //good example

  // Set i to zero.
     i = 0;
```
