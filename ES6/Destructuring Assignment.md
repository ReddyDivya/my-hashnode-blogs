**Hello coders**👋 and **innovative people!**

Another wonderful concept of ES6 i.e., **Destructuring Assignment**. So here's the blog. 

# Destructuring Assignment

Destructuring in JavaScript is a simplified method of **extracting multiple values from data that are stored in an array or objects**.

- allows us to **break down a complex structure into simpler parts**.

- allows us to **destructure properties of an object or elements of an array into individual variables.**

Let's start with an **array destructuring**

## Array Destructuring

### Basic Assignment

```
let languages = ["Hindi", "English"];

let [lang1, lang2] = languages;

console.log(lang1);
console.log(lang2);

```

**Output**

Hindi

English

In the above example, **lang1** is assigned with **Hindi** and **lang2 **is assigned with **English**.

**It uses an index of an array i.e position in an assignment.**

### Ignore values

If we want to **unpack elements from an array** then we're supposed to **leave space**.

for example👇

```
let colors = ["red", "black", "green", "blue"];

//unpicking 'green' color
let [color1, color2, , color4] = colors;

console.log(color1);
console.log(color2);
console.log(color4);
```

**Output**

red

black

blue

### Rest parameters

We can **unpack and assign the remaining part of it to a variable** using the **rest parameter**.

```
[a, b, ...rest] = [110, 210, 50, 430];

console.log(rest);
```

**Output**

[50, 430]

**Warning**

```
const [a, ...b,] = [1, 2, 3];
```

**SyntaxError: rest element may not have a trailing comma**.

Note: **Always consider using the rest operator as the last element.**

Let's have a look at an example of **unpacking values from the sourced variable**

```
const x = [13, 22, 73, 44, 5];
const [y, z] = x;

console.log(y);
console.log(z);
```

**Output**

13

22

### Separate Assignment from the declaration

A variable can be assigned its value via destructuring, separate from the variable's declaration.

```
let a, b; //declaration

[a, b] = [11, 2];
console.log(a);
console.log(b);
```

**Output**

11

2

### Default Values

A **variable can be assigned a default**, in the case that the **value unpacked from the array is undefined**.

```
let [x=50, y=70] = [150] ;

console.log(x);
console.log(y);
```

**Output**

150

70

The **default value of x = 50, y = 70** but the **x value is replaced by 150 but the y value remains the same.**

### Swap

**Two variables values can be swapped in one destructuring expression**. We don't need a temporary variable to swap values anymore. 

```
let x = 40, y = 80;

[x, y] = [y, x];

console.log(x);
console.log(y);
```

**Output**

80

40

### Parsing an array returned from a function

It's always been possible to return an array from a function. Destructuring makes working with an array return value more concise.

```
function student() {
  return ["Divya", "24"];
}

let a, b;
[name, age] = student();
console.log(name); 
console.log(age);
```

**Output**

Divya

24

In this example, student() returns the values ["Divya", "24"] as its output, which can be parsed in a single line with destructuring.

### Ignoring some returned values

We can ignore return values that we don't need it.

```
function student() {
  return ["Divya", "Reddy", "24"];
}

let a, b;
[firstname, lastname, ] = student();
console.log(firstname); 
console.log(lastname);
```

**Output**

Divya

Reddy

I hope you got some clarity on **Array Destructuring**. So, let's get to know about **Object Destructuring**

## Object Destructuring

### Basic assignment
```
const student = {
    std_id: 42,
    std_name: "Jack"
};

const {std_id, std_name} = student;

console.log(std_id);
console.log(std_name);
```

**Output**

42

Jack

### Separate assignment from declaration

```
let name, age;

({name, age} = {name: "James", age: 24});
```

**Output**

{name: 'James', age: 24}

**Note**

- The parentheses ( ... ) around the assignment statement are required when using **object literal destructuring assignment without a declaration**.

- {a, b} = {a: 1, b: 2} is not valid syntax, as the {a, b} on the left-hand side is considered a block and not an object literal.

- However, **({a, b} = {a: 1, b: 2})** is valid, as is **const {a, b} = {a: 1, b: 2}**.

### Assigning new variable names

A property can be unpacked from an object and assigned to a variable with a different name than the object property.

```
const student = {age: 52, name: "Jenny"};
const {age: s_age, name: s_name} = student ;

console.log(s_age);
console.log(s_name); 
```

**Output**

52

Jenny

**const {age: s_age, name: s_name} = student;** takes from the object **student** the property named **age** and **name** are assigned to a local variable named **s_age** and **s_name** respectively.

### Default values

A variable can be assigned a default, in the case that the value unpacked from the object is undefined.

```
const {name = "James", id = 345} = {name: "James Cameroon"};

console.log(name);
console.log(id);
```

**Output**

James Cameroon

345

### Unpacking properties from objects passed as a function parameter

Objects passed into function parameters can also be unpacked into variables, which may then be accessed within the function body. 

### Rest in Object Destructuring

```
let {a, b, ...rest} = {a: 10, b: 20, c: 30, d: 40}
console.log(a); 
console.log(b); 
console.log(rest);
```

**Output**

10

20

{c: 30, d: 40}

**And that's it!**

# Conclusion

Hopefully, you got some clarity on **Destructuring Assignment**✌.

I value your time and I gave my best to write this article. Thanks for sparing your time in reading this article till the end.

I hope this blog has been helpful. If it is, please like and share it with people who you think need it.

Thanks for reading. **Cheers**!🎊

last but not least.

Please, feel free to share your feedback on this article.