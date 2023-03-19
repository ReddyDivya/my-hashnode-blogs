
**Hey Readers** 👋

This is my first ever blog. So, In this article, we’ll learn about the
**JavaScript Array methods to simplify our code**.

Before heading to array methods. First, let us know about

## What is an array?
In JavaScript, An array is a single variable that is used to store different elements.
It is often used when we want to store a list of elements and access them by a single variable.

## Declaration of an Array
There are basically two ways to declare an array. 

> var House = [ ]; // method 1 

> var House = new Array(); // method 2 

Generally, method 1 is preferred over method 2.

Now, we know about an array & declaration.  Let's straightly dive into our topic i.e., **Array methods**.

### 1. push() 
This method **appends new elements to the end of an array** and returns the new length of the array.

**Syntax**
> array.push(element1, elements2.....)

![push.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1633612927502/lbzvBipt1.png)

### 2. pop()
This method **removes the last element from an array** and returns it. If the array is empty, **undefined ** is returned and the array is not modified.

**Syntax**
> array.pop()

![pop.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1633612971941/WqjMcqvYw.png)

### 3. shift()
This method **removes the first element and shift all other elements ** to a lower index and return the value that was shifted out.

**Syntax**
> array.shift()

![shift.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1633612987509/Nt6vJ2ioSS.png)

### 4. unshift()
This method **inserts new elements at the start of an array**, and returns the new length of the array.

**Syntax**
> array.unshift(item)

![unshift.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1633613013155/KcpCWHp-1.png)

### 5. splice()
This method **removes elements from an array ** and, if necessary, insert new elements in their place, returning the deleted elements.

**Syntax**
> array.splice(startIndex, deleteCount)

![splice.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1633613225043/p56bcOua6.png)

### 6. slice()
This method **returns a copy of a section of an array**. For both start and end, a negative index can be used to indicate an offset from the end of the array. For example, -2 refers to the second to last element of the array.

If **startIndex is undefined, then the slice begins at index 0**. Have a look at the below image for clarity.

**Syntax**
> array.slice(startIndex, endIndex)

![slice.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1633613065487/_wKzZbdt8.png)

### 7. join()
**Adds all the elements of an array into a string**, separated by the specified separator string.

**Syntax**
> array.join(stringSeparator)

![join.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1633613078751/PLOPhuWNg.png)

### 8. concat()
This method **combines two or more arrays**. This method returns a new array without modifying any existing arrays.

**Syntax**
> array1.concat(array2)

![concat.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1633613097231/WKbihzGN6.png)

### 9. reverse()
This method reverses the elements in an array in place. This method mutates the array and returns a reference to the same array.

**Syntax**
> array.reverse()

![reverse.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1633613112135/gwNbVy6yu.png)

### 10. includes()
This method determines **whether an array includes a certain element**, returning true or false as appropriate. 
 
It checks if argument 1 is available in the array, argument 2 is from which element it has to start searching.

**Syntax**
> array.includes(searchElement, fromIndex)

![includes.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1633613261607/RbhP9D60V.png)

Let's not make this article even bigger. There are many array methods. So, Let's continue the other methods in the next blog.

I value your time and I gave my best to write this article. **Thanks for sparing your time in reading this article till the end**. 

So what are you waiting for? Any further doubts? Drop it below 👇

Please, feel free to share your feedback on this article.