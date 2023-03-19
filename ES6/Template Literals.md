**Hello coders**👋 and **innovative people!**.

I would like to share with everyone that I've decided to write **ES6 series**  blog posts in **hash node** and you can easily find it as the **[ES6](https://thedivyareddyy.hashnode.dev/series/es6)** widget in my profile.

So, Let's get into another wonderful concept of ES6 i.e., **Template Literals**. So here's the blog.

# Template Literals

**Template literal** makes **creating complex strings easier** & **allows to create multi-line strings**.

Template literals are sometimes informally called **template strings** because they are used most commonly for **string interpolation**.

Hmm..wait

I guess you are stuck with the term **String Interpolation**

So, let's get to know
## String interpolation

When we want to combine output from expressions with strings, we'd concatenate them using the "**+**" (plus sign) (addition operator).

Let's look at an example👇

```
let a = 5;
let b = 10;
console.log('Fifteen is ' + (a + b) + ' and\nnot ' + (2 * a + b) + '.');
```

**Output**

Fifteen is 15 and
not 20.

**That can be hard to read**. Especially when we have **multiple expressions**.

So, How can we overcome this problem?

With **template literals**, we can avoid the **concatenation operator** and **improve the readability of our code** by using placeholders of the form "**${expression}**" to perform substitutions for embedded expressions.

Let's look at an example for more clarity👇

```
let a = 5;
let b = 10;
console.log(`Fifteen is ${a + b} and
not ${2 * a + b}.`);
```

**Output**

Fifteen is 15 and
not 20.

The example uses **backticks (`)** to wrap the string. Notice that **the string is multi-line, both in the code and the output**. This saves **inserting \n within strings**. 

The **${variable}** syntax used above is a **placeholder**.

We won't have to use **concatenation with the + operator** anymore.

To **add variables to strings**, we **drop the variable in a template string** and wrap it with **${ and }**

Similarly, we can **include other expressions in our string literal**, for example, **${a + b}**.

This new way of creating strings gives us more flexibility to create robust strings.

**That's easy to read and write**. **Am I Right?**

So, Let's look at the **different syntaxes**👇

```
//Single-line string
`string text`

//Multi-line strings
`string text line 1
 string text line 2`

//Variable and expression substitutions
`string text ${expression} string text`
```

Let's look at an example one by one👇

## Single-line strings

```
const name = "Irish Proverb";

console.log(`The light heart lives long. ${name }.`);

```

**Output**

The light heart lives long. Irish Proverb.

## Multi-line strings

```
const person = {
  name: "Krishna Dev",
  age: 26
};

const greeting = `Hello, my name is ${person.name}!
I am ${person.age} years old.`;

console.log(greeting);
```

**Output**

Hello, my name is Krishna Dev!
I am 26 years old.


This is an **another example**👇

```
const result = {
    names: ["James", "Jessie", "Genealia"],
    lang: ["C", "CPP", "Java"]
};

function makeList(arr) {
  const names = arr.map(item => `<li class="text-warning">${item}</li>`);
  
  return names;
}

const namesList= makeList(result.names);

console.log(namesList);
```

**Output**

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654857517338/Dnb5XbJKV.png align="left")

**And that's it!**

