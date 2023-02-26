<div align="center">
  <h1>Advanced CSS</h1>
<sub>Author:
<a href="https://www.linkedin.com/in/bhuvanaganesan-l-2209047a" target="_blank">Bhuvan Ganesan</a><br>
</sub>
</div>

--------

# Advanced CSS

## CSS pseudo-classes

We’ve seen how there are mainly 3 types of CSS selectors:

generic where p in CSS targets <p> HTML elements
classes where .intro in CSS targets HTML elements with a class="intro" attribute
ids where #logo in CSS targets HTML elements with a id="logo" attribute
All of these selectors can have pseudo-classes attached to them. A pseudo-class:

defines a particular state of the element
is a keyword that starts with a colon :

**Syntax**
```css
/* There is no space between the selector and the pseudo-class, to signify that they are linked together. */
.selector:pseudo-class{ }
```
### :hover

We apply a CSS style when the targeted element is hovered.
```css
a{ color: blue;}
a:hover{ color: red;}
```

### :visited

This pseudo-class targets links that have been visited. By default, links are blue and turn purple when you’ve visited them

```css
a{ color: dodgerblue;}
a:visited{ color: rebeccapurple;}
```
```html
<a href="https://www.google.com">Google</a>
<a href="https://twitter.com">Twitter</a>
<a href="https://www.facebook.com">Facebook</a>
<a href="https://www.mozilla.org">Mozilla</a>
<a href="https://marksheet.io/visited.html">MarkSheet</a>
```

### :focus

This pseudo-class happens when an HTML element is in focus. This is particularly useful for HTML inputs.

```css
.form-input{ border: 2px solid grey; padding: 5px;}
.form-input:focus{ background: lightyellow; border-color: blue; outline: none;}
/* The outline: none; rule removes the glow from the input. */
```

### :first-child and :last-child

These pseudo-classes are related to the HTML hierarchy. They target HTML elements depending on the order in which they appear in the code.

```html
<ul>
  <li>One</li>
  <li>Two</li>
  <li>Three</li>
  <li>Four</li>
</ul>
```
```css
li:first-child{ background: greenyellow;}
li:last-child{ background: lightsalmon;}
```

### :nth-child

This pseudo-class is a more global version of :first-child and :last-child. With :nth-child, you can calculate which child element you want to target.

```css
li:nth-child(2){ background: violet;}

li:nth-child(odd){ background: gold;}
li:nth-child(even){ background: silver;}

li:nth-child(3n){ background: hotpink;}

li:nth-child(3n+1){ background: limegreen;}
```

check the link for other pseudo-class [click me](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)



## CSS gradients

2 types of gradients in CSS:
- **linear**: colors go from point to another, in a straight line
- **radials**: colors go from the center of a circle to its edges, in all directions
  
A gradient is considered a background image and must be used with the according property.

### linear-gradient

the basic idea is to define:

- which **colors** you want
- where these colors must appear **along the axis** (at the start, middle, end, etc.)
- in which **direction** the gradient must go

```css
div{ background-image: linear-gradient(red, blue);}
```
```html
<div>A simple vertical background gradient</div>
```
**to bottom right**
```css
div{ background-image: linear-gradient(to bottom right, yellow, purple); width: 200px;}
```
```html
<div>A diagonal gradient from the top left corner to the bottom right one</div>
```
**with degrees**
```css
div{ background-image: linear-gradient(20deg, green, blue); width: 150px;}
```
```html
<div>A diagonal gradient with an angle of 20 degrees</div>
```
**more color**
```css
div{ background-image: linear-gradient(orange, grey, yellow); width: 150px;}
```
```html
<div>A rather ugly gradient, but you get the idea</div>
```
**Setting specific color stops**
```css
div{ background-image: linear-gradient(orange, grey 10%, yellow 50%); width: 150px;}
```
```html
<div>An even uglier gradient, but you get the idea</div>
```

### radial-gradient

```css
div{ background-image: radial-gradient(red, yellow); padding: 1rem; width: 300px;}
```
```html
<div>This looks like the sun, doesn't it?</div>
```
you can try out many option similar to linear-gradient


Some sample idea on button 
```css
.button-grey  { background-image: linear-gradient(#f2f2f2, #f2f2f2);}
.button-yellow{ background-image: linear-gradient(#fce374, #fcdf5b);}
.button-orange{ background-image: linear-gradient(#f58a38, #f57c20);}
.button-red   { background-image: linear-gradient(#ed6d64, #ed574c);}
.button-purple{ background-image: linear-gradient(#847bba, #7568ba);}
.button-blue  { background-image: linear-gradient(#42b0e3, #2ba9e3);}
.button-green { background-image: linear-gradient(#97cc76, #8bcc62);}
```
check the link for online generator [click me](https://cssgradient.io/)

-----

## CSS transitions

CSS transitions allow to smoothly go from one element’s state to another. How it works is that individual properties are animated from an initial to a final state.

You can define:

- **transition-property**: which properties to animate
- **transition-duration**: how long the animation lasts
- **transition-timing-function**: how the intermediate states are calculated
- **transition-delay**: to start the animation after a certain amount of time

### Example 
```css
a{ background: lightgrey; color: grey;}
a:hover{ background: yellow; color: red;}
a.with-transition{ transition: 1s;}
```
```html
<a>Without transition</a>
<a class="with-transition">With transition</a>
```

### transition-duration

```css
a{ background: lightgrey; color: grey;}
a:hover{ background: yellow; color: green;}
a.with-fast-transition{ transition-duration: 0.5s;} /* or 500ms */
a.with-slow-transition{ transition: 3s;}
```
```html
<a>Without transition</a>
<a class="with-fast-transition">A 0.5s transition</a>
<a class="with-slow-transition">A 3s transition</a>
```

### transition-property

```css
a{ background: lightgrey; color: grey;}
a:hover{ background: yellow; border: 5px solid blue; color: green;}
a.with-background-transition{ transition-duration: 2s; transition-property: background;}
a.with-all-transition{ transition-duration: 2s;}
```
```html
<a>Without transition</a>
<a class="with-background-transition">With only background transition</a>
<a class="with-all-transition">With all transitions</a>
```

### transition-timing-function

```css
div{ left: 0; position: relative; transition: 1s;}
main:hover div{ left: 200px;}
.ease{ transition-timing-function: ease;} /* Default behavior */
.linear{ transition-timing-function: linear;} /* Constant speed */
.ease-in{ transition-timing-function: ease-in;}
.ease-out{ transition-timing-function: ease-out;}
.ease-in-out{ transition-timing-function: ease-out;}
```
```html
<main>
  <p><strong>Ease</strong>: slow start, fast middle, slow end</p>
  <div class="ease"></div>
  <p><strong>Linear</strong>: constant speed</p>
  <div class="linear"></div>
  <p><strong>Ease In</strong>: slow start, fast end</p>
  <div class="ease-in"></div>
  <p><strong>Ease Out</strong>: fast start, slow end</p>
  <div class="ease-out"></div>
  <p><strong>Ease In Out</strong>: like ease, but with more pronounced acceleration/deceleration curves</p>
  <div class="ease-in-out"></div>
</main>
```

### transition-delay

```css
a{ background: blue; color: white; transition: all 1s;}
div:hover a{ background: red;}
a.with-delay{ transition-delay: 1s;}
```
```html
<div>
  <p>Hover the grey area</p>
  <a>Without any delay</a>
  <a class="with-delay">With a second delay</a>
</div>
```

check the link for list for Animatable CSS properties [click me](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties)

-----

## CSS animations

CSS animations are like mini movies where you are the director giving out instructions (CSS rules) to your actors (HTML elements) for different scenes (keyframes).

### Animation properties

animation is a shorthand property too: 

- **name**: the animation’s name
- **duration**: how long the transition lasts
- **timing-function**: how the intermediate states are calculated
- **delay**: to start the animation after a certain amount of time
- **iteration-count**: how many times the animation should be performed
- **direction**: if the animation should be reversed or not
- **fill-mode**: what styles are applied before the animation starts and after it ends

### Example 
```css
@keyframes bouncing{
  0%  { bottom: 0; box-shadow: 0 0 5px rgba(0,0,0,0.5);}
  100%{ bottom: 50px; box-shadow: 0 50px 50px rgba(0,0,0,0.1);}
}

.loading-button{ animation: bouncing 0.5s cubic-bezier(0.1,0.25,0.1,1) 0s infinite alternate both;}
.result{ padding: 1rem;};
```
```html
<div class="result" >
  <a>Loading</a>
</div>
```

### @keyframes

Before you can apply animations to HTML elements, you must write animations using keyframes. Basically, keyframes are every intermediate step in an animation. They are defined with percentage

- 0% is the first step of the animation
- 50% is the step halfway through the animation
- 100% is the last step

You can also use the keywords **from** and **to** instead of 0% and 100% respectively.

```css
@keyframes around {
  0%  { left: 0; top: 0;}
  25% { left: 240px; top: 0;}
  50% { left: 240px; top: 140px;}
  75% { left: 0; top: 140px;}
  100%{ left: 0; top: 0;}
}
p{ animation: around 4s linear infinite;}

#result-2 {
    height: 300px;
    padding: 0;
    width: 300px;
}
```
```html
<div class="result" id="result-2">
  <p>Hello</p>
</div>
```

### animation-name

whatever is animation-name  which can be used in css selector's 

Like CSS class names, animation names can only include:

- letters (a-z)
- numbers (0-9)
- underscores (_)
- dashes (-)

It can not start with a number or two dashes.

```css
@keyframes whatever{
  /* ... */
}

.selector{ animation-name: whatever;}
```

### animation-duration

Just like transition durations, animation durations can be set in seconds 1s or milliseconds 200ms.

```css
.selector{ animation-duration: 0.5s;}
```

### animation-timing-function

Just like transition timing functions, animation timing functions can use keywords like linear, ease-out, or be defined using custom cubic bezier functions.
It defaults to ease.

```css
.selector{ animation-timing-function: ease-in-out;}
```

### animation-delay

Just like transition delays, animation delays can be set in seconds 1s or milliseconds 200ms.
It defaults to 0s, which means no delay at all.
It’s useful when triggering multiple animations in sequence.

```css
.a,.b,.c{ animation: bouncing 1s;}
.b{ animation-delay: 0.25s;}
.c{ animation-delay: 0.5s;}
```

### animation-iteration-count

By default, animations are only played once (value of 1). You can set 3 types of values:

- **integers** like 2 or 3
- **non-integers** like 0.5 which will play only half the animation
- the *keyword* **infinite** which will repeat the animation indefinitely

```css
.selector{ animation-iteration-count: infinite;}
```

### animation-direction


The animation’s direction defines in which order the keyframes are read.

- **normal**: starts at 0%, ends at 100%, starts at 0% again
- **reverse**: starts at 100%, ends at 0%, starts at 100% again
- **alternate**: starts at 0%, goes to 100%, goes to 0%
- **alternate-reverse**: starts at 100%, goes to 0%, goes to 100%

It’s easier to visualize if the animation’s iteration count is set to **infinite**.

```css
#result-3 {
    padding-bottom: 1rem;
}
#result-3 div {
    background: hsl(217,4%,96%);
    height: 20px;
    width: 220px;
}
#result-3 .normal div {
    animation-direction: normal;
}
#result-3 .reverse div {
    animation-direction: reverse;
}
#result-3 .alternate div {
    animation-direction: alternate;
}
#result-3 .alternate-reverse div {
    animation-direction: alternate-reverse;
}
/* f0r each P tag add color */
```
```html
<div class="result" id="result-3">
  <p><strong>Normal</strong>: 0% --&gt; 100%</p>
  <div class="normal"><div></div></div>
  <p><strong>Reverse</strong>: 100% --&gt; 0%</p>
  <div class="reverse"><div></div></div>
  <p><strong>Alternate</strong>: 0% &lt;--&gt; 100%</p>
  <div class="alternate"><div></div></div>
  <p><strong>Alternate reverse</strong>: 100% &lt;--&gt; 0%</p>
  <div class="alternate-reverse"><div></div></div>
</div>
```
-----

### CSS responsiveness

The Web is meant to provide a platform to share information easily across the Internet, no matter which device the information is viewed on. While the only disparaties between computers accessing the Web consisted mostly upon different screen resolutions, the rapid growth of mobile devices has changed the requirements: a website needs to be accessible on mobile in order to be relevant.

What options are available to handle mobile devices?

1. Not doing anything and let mobile users zoom in to read your website
2. Create a second website, like m.facebook.com, and redirect mobile devices to that website
3. Use responsive web design

### Device, browser, viewport

Before going further, we need to define some terms:

**device**
the hardware used: smartphone, tablet, pc or laptop
**browser**
the software running: Firefox, Google Chrome, Safari, Internet Explorer
**viewport**
the region within the browser that actually displays the webpage

### Responsive web design

The idea behind responsive web design is to make your website adapt to fit to any device. It does so by targetting devices with your CSS and applying certain styles on these devices only.

Responsiveness relies upon the properties of either the device or the viewport. For example:

- how wide is the viewport?
- how high is the viewport?
- how is the viewport oriented?
- what is the device’s resolution?
  
Depending on the answer to these questions, a responsive CSS will apply different or additional CSS rules.

Up until now, every part of our CSS was used by every device that accessed our webpage. Responsive web design allows us to apply certain styles in certain cases.

### media queries

We need to write blocks in our CSS that will only be used by devices that match that block’s criteria. These blocks are called media queries.

The media query syntax is reminiscent of the animation keyframes syntax, as it defines a block within the CSS, in which you write additional CSS rules that are only applied in certain cases.

```css
/* This part is read by every device/viewport */
body{ font-size: 14px;}

@media (min-width: 1200px) {
  /* This part is only read by viewports wider than 1200 pixels */
  body{ font-size: 16px;}
}
```
Here, the default text size is 14px. But to accomodate for larger viewports, the text size is set to 16px if the viewport is wider than 1200 pixels.

Keep in mind that we’re talking about the viewport, not the device’s.

On mobile, considering browsers are running in fullscreen, the two widths are interchangeable. If you’re on desktop, resize your browser window to see media queries being activated/desactivated.

**Several parameters**

You can require 2 conditions for a media query to be activated.
```css
body{ font-size: 18px;}

@media (min-width: 1000px) and (orientation: landscape) {
  body{ font-size: 20px;}
}
```

**Several CSS rules**

You can include as many CSS rules as you want in the media query.

```css
body{ font-size: 14px;}
.button{ display: block;}
.title{ text-align: center;}

@media (min-width: 1200px) {
  body{ font-size: 16px;}
  .container{ margin: 0 auto; width: 960px;}
  .button{ display: inline-block;}
  .title{ text-align: left;}
}
```



### Useful links
1. https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes
2. https://cssgradient.io/
3. https://angrytools.com/gradient/
4. https://mycolor.space/gradient
5. https://mycolor.space/gradient3
6. https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties
7. https://animista.net/
8. https://webcode.tools/generators/css/keyframe-animation
9. https://marksheet.io/css-animations.html
10. https://marksheet.io/css-animations.html#keyframes
11. https://marksheet.io/css-responsiveness.html