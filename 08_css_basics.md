<div align="center">
  <h1>CSS Basics</h1>
<sub>Author:
<a href="https://www.linkedin.com/in/bhuvanaganesan-l-2209047a" target="_blank">Bhuvan Ganesan</a><br>
</sub>
</div>


# CSS Basics

CSS is about the styling of a web page. That means defining colors, fonts, dimensions, margins and positions of the elements of a web page. CSS brings a web page to life by applying a coat of paint to the static content and elevates its purpose through color, space, emphasis, and movement

## What CSS is

CSS stands for Cascading Style Sheets. Its purpose is to style markup languages (like HTML or XML). Therefore, CSS is worthless on its own unless it is associated with an HTML document.

CSS brings an HTML document to life by selecting fonts, using colors, defining margins, positioning elements, animating interactions, and more.

## How CSS works

The way CSS works is to select an HTML element (such as a paragraph), select a property to change (such as the color), and apply a specific value (such as blue):

```css
p{ color: blue;}
```

## Where do I write CSS?

**CSS as an attribute**
```css
<p style="color: blue;">Lorem Ipsum is simply dummy text of the printing</p>
```
**CSS in the \<head\>**

```html
<html>
  <head>
    <title>Hello World</title>
    <style type="text/css">
      p{ color: blue;}
    </style>
  </head>
  <body>
    <p>Lorem Ipsum is simply dummy text of the printing</p>
  </body>
</html>
```
**CSS in a separate file**
You can write your CSS in a separate file with the extension .css and then link it to your HTML using the HTML tag.
```css
p{ color: blue;}
```
```html
<html>
  <head>
    <title>Hello World</title>
    <link rel="stylesheet" type="text/css" href="style.css">
  </head>
  <body>
    <p>This paragraph will be red.</p>
  </body>
</html>
```
This 3rd method of using a separate CSS file is preferred.

## CSS Syntax

The purpose of CSS is to define the layout and design of your HTML elements. The syntax is very simple:
```css
/* A CSS rule */
selector{ property: value;}
```
You can read that as:
```css
who{ what: how;}
```
CSS is a 3-part process:

- the **selector** defines which HTML element(s) are targeted
- the **property** defines which feature is to be changed 
- the **value** defines how this feature is to be changed
  
This entire block (selector/property/value) is a CSS rule.

Example

```html
<div>Something something</div>
```
```css
div{ background: lightgreen;}

//the text color doesn’t really match the background color. Let’s improve tha
div{
  background: lightgreen;
  color: darkgreen;
}
```
we have 2 selectors and 2 properties. We consequently have a set of selectors and a set of properties (with their respective values).
```css
q,
div{
  background: lightgreen;
  color: darkgreen;
}
```

## Comments 
As in HTML, it can be handy to write CSS comments:
```css
/* This is a CSS comment */
q,
blockquote{
  background: lightgreen;
  color: darkgreen;
}
/*
Comments are only meant to be read by humans
and won't be parsed by the computer
*/
```

## CSS Selectors

CSS selectors define which elements we want our styling to be applied to.

### Generic tag selectors

Targeting generic HTML tags is easy: just use the tag name.

```css
a{ /* Links */ }
p{ /* Paragraphs */ }
ul{ /* Unordered lists */ }
li{ /* List items */ }
```
There’s a direct connection between the name of the HTML tag and the CSS selector used.

### Classes

Just put a dot . in front of the class name you want to use:
```css
.date {
  color: red;
}
```

```html
<p class="date">
  Saturday Feb 21
</p>
<p>
  The event will be on <em class="date">Saturday</em>.
</p>
```

### IDs

You can also use the id attribute in your HTML, and target it with a hash # in your CSS: 
**ID are similar to Classes, as they rely upon an HTML attribute.**

```css
#tagline{ color: orange;}
```
```html
<h1 id="tagline">This heading will be orange.</h1>
```

Some details about selectors

```html
<div class="global"></div>
<!--Possible CSS selectors--> <!--What it means-->
div -- Every <div>
.global -- Every elements with class=”global”
div.global -- Every <div> with class=”global”


<ol class="dico">
  <li>Un cobaye</li>
  <li>Des cobaux</li>
</ol>
<!--Possible CSS selectors--> <!--What it means-->
li -- Every <li>
ol li -- Every <li> with an <ol> as ancestor
.dico li -- Every <li> with a class="dico" element as ancestor
```

### Combining selectors

```css
.date {
  color: red;
}
```
```html
<p class="date">
  Saturday Feb 21
</p>
<p>
  The event will be on <em class="date">Saturday</em>.
</p>
```
What if we want our dates that are in em elements to blue instead? We can add the following CSS rule
```css
em.date {
  color: blue;
}
```
The **em.date** combines:

- a tag selector **em**
- a class selector **.date**

It will only apply to \<em class="date"\>\</em\> HTML elements. It won’t affect other **.date** or **em**.

### Hierarchy selectors

A **space** in a selector defines a ancestor/descendant relationship. Let’s say we want the links in our header to be in red:

This can be read from right to left as: “Select all **a** elements that are within a **header** element”. This will prevent all other links (that aren’t in the header) from being affected.

```css
header a {
  color: red;
}
```

### Pseudo-class selectors

HTML elements can have different **states**. The most common is when you move the mouse pointer over a link. In CSS, it's possible to apply a different style when such an event occurs.

Pseudo-class selectors are appended to normal selectors and start with a colon **:** :
```css
a {
  color: blue;
}

a:hover {
  color: red;
}
```

## CSS Inheritance

Let’s say we want to change the text color of a webpage. It would be tedious to specify a color for every HTML element

```css
p,
ul,
ol,
li,
h1,
h2,
h3,
h4,
h5,
h6{ color: grey;}
```

### Value propagation

The **color** value can be inherited from an **ancestor**. Considering that we want to change the whole web page, we choose the ancestor of all HTML elements, the **body** tag

```css
body{ color: grey;}
```

All child and descendant elements will inherit the value **grey** from their common ancestor **body**, which naturally encompasses all elements.

### Inherited properties

Only a few CSS properties can be inherited from predecessors. These are mainly text properties:

- text color
- font (family, size, style, weight)
- line-height

## CSS Priority

### When several rules collide

Several CSS rules can be applied to one HTML element. For example, take a simple paragraph

```html
<p class="message" id="introduction">
  Lorem Ipsum has been the industry's standard.
</p>
```
```css
/* We can change this paragraph by simply using its tag name: */
p{ color: blue;}

/* Or we can use its class name: */
.message{ color: green;}

/* Or we can use its id: */
#introduction{ color: red;}
```
Since the browser can only select one color for this paragraph, it must decide which CSS rule takes precedence over other rules. This is what CSS precedence (or CSS specificity) is all about.

In our example, the paragraph will be red because a #id selector is more specific and thus more important than other selectors.

### How to avoid conflicts

When writing CSS, it's easy to have conflicting rules where the same property is applied multiple times.

- ​use classes only: use **.introduction** instead of **#introduction**, even if this element appears only once on your website
- avoid applying **multiple classes** to a single HTML element: don't write \<p class="big red important"\>but what is \<p class="title"\> semantically more descriptive
- don’t use inline styles like \<div style="background: blue;"\>

## CSS Color units

Colors are widely used in CSS, be it for text color, background color, gradients, shadows, borders... There are several ways to define colors in CSS, each with its own advantages and disadvantages.

The color property defines the color of the text. It is quite simple. But more important are the different types of color units that are available.

### Color names

CSS offers [145 color names](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value), from the simplest (black, white, orange, yellow, blue...) to the more specific (lawngreen, orchid, crimson...).

```css
body{ color: black;}
a{ color: orange;}
```

### Hexadecimal

Colors in CSS can also be defined with hexadecimal values, like #db4e44.

hexadecimal 16 possible values 
- 0	1	2	3	4	5	6	7	8	9	A	B	C	D	E	F
In hexadecimal, we have 16 symbols to form numbers. Because 0-9 are not enough symbols, we also use A-F. And it starts at zero. So:

### rgb

Computer monitors, televisions, and cell phones all use the RGB color model to represent colors. Basically, each color is defined by a combination of red, green, and blue. There are 256 possible values for red, green or blue. Since computers start counting at 0 (zero), the maximum value is 255.

Considering that a color is the result of a combination of red, green, and blue, and each of these three colors has 256 possible values, there are 256 * 256 * 256 = 16,777,216 possible colors.

Since the RGB model is directly related to how colors are physically rendered, it has become a CSS color unit.

```css
/* For example, the red color of this website consists of 219 parts red, 78 parts green, and 68 parts blue:  */
a{ color: rgb(219, 78, 68);}
/* The black color is no amount of either Red, Green or Blue: */
body{ color: rgb(0, 0, 0);}
/* On the other side of the spectrum, white is the full amount of each Red, Green and Blue: */
body{ color: rgb(255, 255, 255);}
```

### rgba

The color unit rgba is rgb, to which we add an alpha value (in the range 0 to 1, in decimal values) that defines how transparent the color is:

```css
body{ color: rgba(0, 0, 0, 0.8);}
```
The purpose of a transparent color is to blend with the background and therefore look slightly different depending on the context. This is especially useful for background colors.




### Useful links
1. https://www.csszengarden.com/
2. https://developer.mozilla.org/en-US/docs/Web/CSS/color_value
