**Hello Readers** &#128075;

In JavaScript, we often **don't need to name our functions**, **especially when passing a function as an argument to another function**. 

Instead, we can create **inline functions**. 

We don't need to name these functions because we don't reuse them anywhere else.

Let's see the syntax 👇

## Basic Syntax

```
const Arrowfun = function() {
  const myVar = "value";
  return myVar;
}
```

We can **omit** the **function keyword**. See the below syntax👇

**(or)**

```
const Arrowfun = () => {
  const myVar = "value";
  return myVar;
}
```

There are different syntaxes to use an arrow function for different scenarios. Confused?
Let me clarify. 

### Case 1: One parameter

**Parentheses are optional** for one parameter of an arrow function. 

See the example👇

```
let cube = a => {
	const sqr = a * a * a;
    return sqr;
} 

console.log(cube(3));   // 27
```

### Case 2:  No return statement

When there's no return we can **omit the body braces** of an arrow function.

See the example👇

```
let cube = a => a * a * a;

console.log(cube(3));   // 27
```
 
**Note:** Return keyword is a must if we keep body braces. Otherwise, it gives **undefined**. 

### Case 3:  Multiple parameters

Multiple parameters **need parentheses**. See the example👇

```
let product = (a, b) =>  a * b;

console.log(product(12, 4));   // 48
```

**Note:**  It throws an error when there are no parentheses for multiple parameters

of an arrow function. See the image👇

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654497714435/tskNwH-zD.png align="left")


### Case 4: Multiline statements

Multiline statements **require body braces and return statements** otherwise, it throws an error.

See the example👇

```
let square = a => {
  let result = a * a;
  return result;
};

console.log( square(12) );      //144
```

### Case 5: Multiple params & Multiline statements

Multiple params **require parentheses**. Multiline statements **require body braces and return statements**.

See the example👇

```
let product = (a, b) => {
  let result = a * b;
  return result;
};

console.log( product (11, 12) );     //132
```

**Well done readers**, We are done with the basic syntaxes of an arrow function. 

Now, Let's dive into the **Advanced syntax**.

## Advanced syntax

### Case 1: Object literal

We **require parentheses around the expression** to return an object's literal. See the example👇

```
let myFunc = params => ({name: "divya"}) // returns the object {name: "divya"}
```

The code inside braces ({}) is parsed as a sequence of statements i.e. name is treated like a label, not a key in an object literal. 

Arrow function supports **Rest parameters**, **Default parameters**, **Destructuring**. 

Let's look into the examples👇

### Case 2: Rest parameters

```
var lang = (arg1, arg2, ...moreArgs) => {

	console.log("arg1 : ", arg1);   //logs arg1
	console.log("arg2 : ", arg2);  //logs arg2
	console.log("moreArgs: ", moreArgs); //logs an array of any other arguments you pass in after arg2
};

console.log(lang('C', 'C++', 'Java', 'HTML', 'JS', 'CSS'));

```

Let's see the output👇

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654499809030/82LQ8Ey8J.png align="left")


### Case 3: Default parameters

```
var lang = (arg1, arg2 = "HTML") => {

	console.log("arg1 : ", arg1);   //logs arg1
	console.log("arg2 : ", arg2);  //logs arg2
};

console.log(lang("JavaScript"));
```

Let's see the output👇

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654499976064/FmO4Fdbp8.png align="left")


### Case 4: Destructuring within params

```
([a, b] = [10, 20]) => a + b;  // result is 30
({ a, b } = { a: 10, b: 20 }) => a + b; // result is 30
```

## Line breaks

An arrow function cannot contain a line break between its parameters and its arrow. See below code snippet👇

```
var func = (a, b, c)
  => 1;
```

This throws an error **SyntaxError: Unexpected token '=>'**

However, this can be amended(**making minor changes**) by putting the line break after the arrow. You can also put line breaks between arguments.

```
var func = (a, b, c) =>
  1;

var func = (a, b, c) => {
  return 1
};

var func = (
  a,
  b,
  c
) => 1;

// no SyntaxError thrown
```

Let's see a few more examples👇

```
const myFunc = () => "value";      //This code will still return the string value by default.
```

```
const magic  = () =>  new Date();       //returns a Date
```

```
let sum = a => a + 100;

console.log(sum(12));   //logs 112
```

Hopefully, you got some clarity on **Arrow Function** &#9996;.

I value your time and I gave my best to write this article. Thanks for sparing your time in reading this article till the end.

So what are you waiting for? Any further doubts? Drop it below 👇

Please, feel free to share your feedback on this article.