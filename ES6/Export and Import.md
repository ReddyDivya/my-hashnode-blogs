## An important message

**Hello coders**👋 and **innovative people!** First, I'd like to say a huge thank you to those who have read and reacted to my [Arrow Functions](https://thedivyareddyy.hashnode.dev/arrow-function) blog post. My posts have never gotten that many views before. So, Thank you. I hope to continue sharing valuable blogs here.


![priscilla-du-preez--_ojDIDjt60-unsplash.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1654665028265/1uwNfhACG.jpg align="left")


*Photo by Priscilla Du Preez from Unsplash*

So after publishing that blog, someone reached out to me to ask me when to use **export** and **export default**. So here's the blog.

In order to make JavaScript more modular, clean, and maintainable.  ES6 introduced a way to easily share code among JavaScript files as an **export** & **import**. 

It involves exporting parts of a file for use in one or more other files and importing the parts you need, where you need them.

In order to take advantage of this functionality, we need to create a script in our HTML document with a type of module. 

**Here is an example👇**

```
<script type="module" src="filename.js"></script>
```

A script that uses this module type can now use the import and export features.

**See this example👇**

```
<html>
  <body>
    <script type="module" src="index.js"></script>
  </body>
</html>
```
Well, we've added a script tag with type="module" in HTML. Now, Let's understand **export** and **import**

# Export

We use the **export** keyword to share a Code Block.

Suppose in an **arithmetic_operations.js** file that contains several functions. If we want to use the **multiplication** variable in other files. we need to export the variable. So, that it can be used wherever it's required instead of writing the same code repeatedly.

Let's see the basic syntax of **export**.

### Exporting individual features

```
export let name1, name2, …, nameN;

export function functionName(){...}

export class ClassName {...}
```

Let's see an example of **exporting a single function**

```
export const multiplication = (x, y) => {
  return x * y;
}
```

### Export list

```
export { name1, name2, …, nameN };

```

Let's see an example of **exporting multiple functions**

```
const multiplication = (x, y) => {
  return x * y;
}

const add = (x, y) => {
  return x + y;
}

export { add, multiplication } ;
```

### Rename export(s)

```
export { variable1 as name1, variable2 as name2, …, nameN };
```

Let's look at an example of **Renaming export(s)**

```
const booksClub = "Books Club";

export { booksClub as favoriteTeam };
```

In the code snippet above, we'll tell the computer to export the **booksClub** variable as **favoriteTeam**.
Therefore, when importing the variable, we’ll use the name **favoriteTeam**— not **booksClub**.

Let’s look at an example of this below.

```
import { favoriteTeam } from "./team.js";

const myBooksClub = favoriteTeam + " " + "is my best club.";

console.log(myBooksClub);
```

When we export a variable or function, we can import it into another file and use it without having to rewrite the code. 

# Import

We can reuse JavaScript code using the **import** keyword.

Let's see the basic syntax of **import**

### Importing individual features

```
import fun1 from './filename.js';
```

Let's see an example of **importing a single function**

```
import add from './arithmetic_operations.js';
```

### Import list 

```
import { fun1, fun2 } from './filename.js';
```

Let's see an example of **importing multiple functions**

```
import { add, multiplication  } from './arithmetic_operations.js';
```

Here, the **import** will find **add**, **multiplication** in **arithmetic_operations.js**.

The **./** tells the import to look for the arithmetic_operations.js file in the same folder as the current file. 

The relative file path (./) and file extension (.js) are required when using import.

### Rename Imports

We can rename imports by separating each **as** a statement with a **comma**.

Let's look at the basic syntax

```
import { variable1 as name1, variable2 as name2 } from './filename.js';
```

Let's look at an example of **Rename Imports**

```
import { 
  bestClub as favoriteTeam, 
  fruits as crop, 
} from "./team.js";

const bestClub = `${crop}s at ${favoriteTeam}.`;
```

### Use * to Import Everything from a File

Suppose we have a file and we wish to **import all of its contents into the current file**. 

This can be done with the **import * ** as syntax.

**Here's an example👇**

```
import * as arithmetic from "./arithmetic_functions.js";
```

The above import statement will create an object called **arithmetic**. 

This is just a variable name, we can name it anything. 

The object will contain all of the exports from arithmetic_functions.js in it, so we can access the functions as we would in any other object property. 

**Here's how we can use the add and multiplication functions that were imported👇**:

```
arithmetic.add(2,3);
arithmetic.multiplication(5,3);
```

# Export Fallback ( export default )

There is another export syntax we need to know, known as **export default**.

Usually, we will use this syntax if **only one value is being exported from a file**. 

It is also used to create a **fallback value for a file** or **module**.

Let's see the basic syntax of **export default**

```
export default function (…) { … }

export default function name1(…) { … }
```

Let's see an example of **export default**

```
export default function mul(x, y) {
  return x * y;
}
```

Since export default is used to declare a fallback value for a module or file, we can only have one value be a default export in each module or file. 

We cannot use export default with var, let, or const.

# Import a Default Export

To import a default export, we need to use a different import syntax👇.

```
import name from "./filename.js";
```

Let's look at an example of **Import a Default Export**

```
import mul from "./arithmetic_operations.js";
```

The syntax differs in one key place. **The imported value, mul, is not surrounded by curly braces ({})**. 
**mul** here is simply a variable name.

**Note:** We can use any name here when importing a default.

**And that's it!**

# Conclusion

Hopefully, you got some clarity on Export and Import✌.

I value your time and I gave my best to write this article. Thanks for sparing your time in reading this article till the end.

I hope this blog has been helpful. If it is, please like and share it with people who you think need it. 

Thanks for reading. Cheers!

last but not least.

Please, feel free to share your feedback on this article.

> P.S.: Thank you for all the support on this blog. Some of you have messaged me, wanting to connect
through Twitter. 

If in case any of you would like to follow me on Twitter: https://twitter.com/thedivyareddyy