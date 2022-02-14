# begining-javascript
Highlights from Wes Bos course - Beginner Javascript



## **The Tricky Bits** *(Module 3)*

**Closures**: is the ability to access to a parent level scope from a child scope, even after the parent function has been closure.

```javascript
function sayHi(greeting = ''){
  const gretting = 'Hi'
  
  return function sayName(name){
    return `${greeting} ${name}!`
  }
}

const myGreeting = sayHi('Hey');
console.log(myGreeting('folks!')) // This logs Hey folks!

```




**Hoisting**: Two things are hoisted in JS, which means that are accesible even before where they are declare:
- var variables.
- regular functions (not anonymous function, as arrow functions)

Example:


```javascript
sayHi(); // it logs hello

function sayHI() {
   console.log('hello')
}
```

The DOM (Document Object Model) is the start base for every framework.

- window: is a global scope in the browser. Where all our global variables are stored and everything about the current open browser.


**Element Selectors**:
- querySelector().
- querySelectorAll().

```javascript
const header = document.querySelectorAll('h2')

// document selects all the h2 tag elements in out html file
```

```javascript
const items = document.querySelectorAll('.item')
const paragraphs = header.querySelector('p')

//selects every <p> tag the inside item class.
```
**Getters**:
