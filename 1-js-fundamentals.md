# Javascript Fundamentals

## Functions
- Anatomy of a function
- Functions as 'callbacks'
- Interpreting our code
- Scope and Closure

```javascript
  function puppyMaker(name, age, colour) {
    return {
      name,
      age,
      colour,
      bark: drDoolittling => drDoolittling ? `Hello, my name is ${name}, I am ${age} year(s) old! And I have ${colour} fur!!` : 'Woof!'
    }
  }

  const bark1 = puppyMaker('Steph', 12, 'brown').bark(false);
  const bark2 = puppyMaker('Steph', 12, 'brown').bark(true);
```

```javascript
  /* --Functions should not update variables that exist outside of their definitions-- */
  const adder = (a, b) => a + b;

  /* --------Functions should always have returns when possible---------- */
  const sayHello = name => {
    console.log(`Hello ${name}`);
    return 1;
  }

  /* ----------Remember functions can return functions--------- */
  let sum = (numToDouble) => {
    let doubler = numToDouble * 2;
    return num => {
      console.log(doubler + num);
      return 1;
    }
  }
```

```javaScript
  function illGiveYouTen(callBackFunc){
    return callBackFunc(10);
  }

  const shouldEqualTwenty = illGiveYouTen(num => num * 2);
  const shouldEqualFive = illGiveYouTen(num => num / 2);
  const shouldEqualFifteen = illGiveYouTen(num => num + 5);

  console.log(shouldEqualTwenty);
  console.log(shouldEqualFive);
  console.log(shouldEqualFifteen);
```

## Data types

## ES6
- var vs const vs let
- spread operator

## resources
- [You Don't Know JS: Function VS Block Scope](https://github.com/getify/You-Dont-Know-JS/blob/master/scope%20%26%20closures/ch3.md)
- [Closures - MDN documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)
- [Learn ES6 by doing it. Fix failing tests.](http://es6katas.org/)
- [ECMAScript 6 equivalents in ES5](https://github.com/addyosmani/es6-equivalents-in-es5)
- [egghead course on es6](https://egghead.io/courses/learn-es6-ecmascript-2015)
