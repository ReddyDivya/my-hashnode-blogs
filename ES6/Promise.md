**Hello coders👋 and innovative people!**

Thank you so much for supporting my blogs. I hope to continue sharing valuable blogs here.


![manuel-cosentino-M3fhZSBFoFQ-unsplash.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1654687823703/bEEHMxthA.jpg align="left")

*Photo by **Manuel Cosentino** from Unsplash*

Today's topic is **Promise in ES6**. Let's get into the blog.

## Promise

A **promise** in JavaScript is exactly what it sounds like - **we use it to make a promise to do something, usually asynchronously**.

A Promise can either be **rejected** or **resolved** based on the operation outcome.

When the task completes, we either **fulfill** our promise or **fail** to do so.

The promise is a **constructor** function, so we need to use the **new** keyword to create one. 

 It takes a **function, as its argument**, with two parameters - **resolve** and **reject**.

These methods determine the outcome of the promise. 

**Let's see the syntax**

```
const myPromise = new Promise((resolve, reject) => {

});
```

Let's understand the purpose of **resolve** and **reject** parameters

A promise has **three states**: **pending**, **fulfilled**, and **rejected**.

The promise we created earlier is forever stuck in the **pending state** because we did not add a way to complete the promise. 

The **resolve** and **reject** parameters given to the promise argument are used to do this.

## Resolve and Reject Methods

**resolve** is used **when we want our promise to succeed** and  **reject** is used **when we want it to fail**.

These are methods that take an argument, see below code snippet for more clarity

```
const myPromise = new Promise((resolve, reject) => {
  if(condition here) {
    resolve("Promise was fulfilled");
  } else {
    reject("Promise was rejected");
  }
});
```

The example above uses strings for the argument of these functions, but it can really be anything.

**Let's see the example for more clarity**

```
const myPromise = new Promise((resolve, reject) => {
  let a = 10;
    
  if(a == 10) {
      resolve("Success");
  } else {  
    reject("Failed");
  }
});
```

## Handle a Fulfilled Promise with then()

Promises are most useful when we have a process that takes an **unknown amount of time in your code 
**(i.e. something asynchronous), like a **server request**. 

When we make a server request it takes some amount of time, and after it completes we usually want to 
do something with the response from the server. This can be achieved by using the **then()**.

The **then()** is **executed immediately after your promise is fulfilled with resolve**.

**Let's see the syntax**

```
myPromise.then(result => {
  
});
```

**result** comes from the **argument given to the resolve method**.

**Let's add then() to our previous example to make it work**

```
const myPromise = new Promise((resolve, reject) => {
  let a = 10;
    
  if(a == 10) {
      resolve("Success");
  } else {  
    reject("Failed");
  }
});

myPromise .then(result => {
     console.log("The result of the promise is >> "+ result);
})
```

**Output**:

**The result of the promise is >> Success**

## Handle a Rejected Promise with a catch()

The **catch()** is used when our promise has been rejected. It is **executed immediately after a promise's reject method is called**.

**Here’s the syntax**

```
myPromise.catch(error => {
  
});
```

**error** is the **argument passed into the reject method**.

Let's add **catch()** to our previous example to make it work

```
const myPromise = new Promise((resolve, reject) => {
  let a = 1;
    
  if(a == 10) {
      resolve("Success");
  } else {  
    reject("Failed");
  }
});

myPromise .then(result => {
     console.log("The result of the promise is >> "+ result);
})

myPromise.catch(error => {
     console.log("The result of the promise is >> "+ error);
})
```

**Output**:

**The result of the promise is >> Failed**

**And that's it!**

Hopefully, you got some clarity on **Promise in ES6**✌.

I value your time and I gave my best to write this article. Thanks for sparing your time in reading this article till the end.

I hope this blog has been helpful. If it is, please like and share it with people who you think need it.

Thanks for reading. Cheers!

last but not least.

Please, feel free to share your feedback on this article.