**Hey Readers** 👋

In this article, we’ll learn about **CSS Box Model to layout our content**.

So, Let's dive into the article.

Everything we see on a website is a **rectangular box**. 

CSS determines the **size**, **position**, and **properties **(**color**, **background**, **border size**, etc.) of these boxes.

Every box is composed of four parts (or areas), defined by their respective edges: the **content edge**, **padding edge**, **border edge**, and **margin edge**.

![Box Model.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1641966003515/RerDx9HF6.png)


## Content area

The content area is bounded by the content edge and contains **real** content of the elements like **text**, an **image**, or a **video**.

It's dimensions are the **content width** and **content height**


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1641971951162/PYuChw99Q.png)


## Padding area

The padding area is bounded by the padding edge, used to create space around an element's content, inside of any defined borders. 

Its dimensions are the **padding-box width** and the **padding-box height**.

The thickness of the padding is determined by the **padding-top**, **padding-right**, **padding-left**, **padding-bottom**. 

Let's look into the individual padding properties 👇

### Individual Padding Properties 

CSS has properties for specifying the padding for each side of an element:

**padding-top** : 10px;

**padding-right** : 30px;

**padding-left** : 200px;

**padding-bottom** : 67%;

Let's see an example for more clarity 👇


```
div {
    border: 5px solid green;
    background-color: rgb(255, 128, 0);
    padding-top: 50px;
    padding-right: 30px;
    padding-bottom: 40px;
    padding-left: 180px;
}

``` 

See the **output** 👇

![1.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1641968093932/dOdVShq96.png)

There's also a **shorthand property to set all four sides at once**. 

Let's have a look into it 👇.


### Padding Shorthand Property

*a)* ** Apply to all four sides **

**padding** : 10px;  

*b)* ** vertical | horizontal**

**padding ** : 5px 10px;  

*c)* ** top | horizontal  |  bottom**

**padding ** : 5px 10px 30px;  

*d)* ** top | right  |  bottom  |  left**

**padding ** : 5px 1px 3px 4px;  


See the below 👇 code snippet with shorthand property which works exactly the same as the above one.


```
div {
  border: 5px solid green;
  background-color: rgb(255, 128, 0);
  padding: 50px 30px 40px 180px;  /* top | right | bottom | left */
}
``` 


## Border area

The border area is bounded by the border edge, extending the padding area to include the element's borders. 

Its dimensions are the **border-box width ** and the **border-box height**.

Let's look into the **border properties**

### Border Width

The **border-width** property **specifies the width of the four borders**.

Let's see an example  👇


```
p.one {
  border-style: solid;
  border-width: 5px;
}

p.two {
  border-style: solid;
  border-width: medium;
}

p.three {
  border-style: dotted;
  border-width: 2px;
}

``` 

See the output 👇

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1641970859447/SihtyYR19.png)


### Border Color 

The **border-color** property is used to **set the color of the four borders**.

The color can be set by **name**, **HEX**, **RGB**, **HSL**.

Let's see an example 👇

```
p.one {
  border-style: solid;
  border-color: red;
}

p.two {
  border-style: solid;
  border-color: green;
} 

p.three {
  border-style: dotted;
  border-color: blue;
} 

``` 

See the **output**👇

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1641970597029/OJOeLfLFv.png)


### Border Style

The border-style specifies the **line style of the border like **dashed**, **solid**,  **dotted** etc., 

Let's see an example for more clarity 👇


```
   p.dotted {border-style: dotted;}
   p.dashed {border-style: dashed;}
   p.solid {border-style: solid;}
``` 

See the **output ** 👇

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1641970268151/lcSCFtqjc.png)

There's also a **shorthand property** to specify all the individual border properties in one property.

Let's have a look 👇


### Border Shorthand Property

The **border ** property is a shorthand property for the following individual border properties:

**border-width**
**border-style**
**border-color**

**Example**

```
p {
  border: 5px solid red;
}
``` 

See the **output** 👇

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1641971238507/2kZQYuuIp.png)



## Margin area

The margin area is bounded by the margin edge, used to create space around elements, outside of any defined borders. 

Its dimensions are the **margin-box width** and the **margin-box height**.

The size of the margin area is determined by **margin-top**, **margin-right**, **margin-left**, **margin-bottom**.

Let's look into the individual margin properties 👇

### Individual Margin Properties 

CSS has properties for specifying the margin for each side of an element:

**margin-top** : 10px;

**margin-right** : 3px;

**margin-left** : 20px;

**margin-bottom** : 5%;


Let's see an example for more clarity 👇


```
body{
	border: 3px solid red;
}
div {
    border: 3px solid orange;
    margin-top: 10px;
    margin-bottom: 20px;
    margin-right: 50px;
    margin-left: 80px;
    background-color: darkblue;
    color: white;
}

``` 

See the output 👇


![2.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1641968694441/ZjQuY0WOr.png)

There's also a **shorthand property to set all four sides at once**. 

Let's have a look into it 👇

### Margin Shorthand Property

*a)* ** Apply to all four sides **

**margin** : 10px;  

*b)* ** vertical | horizontal**

**margin** : 5px 10px;  

*c)* ** top | horizontal  |  bottom**

**margin** : 5px 1px 3px;  

*d)* ** top | right  |  bottom  |  left**

**margin** : 5px 1px 3px 4px;  


See the below code snippet 👇 with shorthand property which works exactly the same as the above one.

```
body{
	border: 3px solid red;
}
div {
  border: 3px solid orange;
  margin: 10px 50px 20px 80px;   /* top | right | bottom | left */
  background-color: darkblue;
  color: white;
}

``` 

Hopefully, you got some clarity on CSS Box Model.

I value your time and I gave my best to write this article. Thanks for sparing your time in reading this article till the end.

So what are you waiting for? Any further doubts? Drop it below 👇

Please, feel free to share your feedback on this article.
