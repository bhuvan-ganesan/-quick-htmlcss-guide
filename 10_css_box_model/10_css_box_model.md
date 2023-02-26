<div align="center">
  <h1>CSS Box Model</h1>
<sub>Author:
<a href="https://www.linkedin.com/in/bhuvanaganesan-l-2209047a" target="_blank">Bhuvan Ganesan</a><br>
</sub>
</div>


# CSS Box Model

HTML element is displayed in the browser as a rectangle. The dimensions of this rectangle are dynamic: they vary depending on the content of the element. You can think of these rectangles as fluid, adapting their shape to the content.

## CSS background

The background of an HTML element is what appears behind the text. Although CSS allows you to apply a background to any type of HTML element, it's most often used on block-level elements.
Backgrounds are applied only to the element in question. However, since most HTML elements have a transparent background, applying a background to the body looks like applying it to all elements.

#### background-color

Default value: transparent Inherited by children elements: no.

```css
body{ background: #f2eee9;}
```

#### background-image

Since plain colors are usually not enough, CSS allows the use of images as backgrounds for elements.

To use a background image, you just need to specify its URL:

```css
body{ background-image: url(images/diagonal-pattern.png);}
```

#### background-position

By default, a background image will repeat itself indefinitely. You can specify its original position, by choosing a horizontal x value, and a vertical y one.

For each coordinate, you either use:

- pixel values px
- percentages, relative to the HTML element’s dimensions
- keywords like center, left, bottom

```css
body{ background-position: right bottom;}

body{ background-position: center 20px;}
```

#### background-repeat

By default, a background image will repeat itself indefinitely. You can choose to make it repeat only horizontally, only vertically, or not at all.

```css
body{ background-repeat: repeat-x;} /* Only horizontally */
body{ background-repeat: repeat-y;} /* Only vertically */
body{ background-repeat: no-repeat;} /* The background image will only appear once */
```

### CSS display

The display property allows to change the type of HTML element. By default, a paragraph <p> (a block-level element) will have a default display value of block, but can be rendered as an inline one

```css
p{ display: inline;}
```
In short, **display** allows to alter the type of an element without changing its meaning.

Each **display** options have specific rendering behaviors:

- **block** will take up the whole width available
- **inline** will act as plain text
- **inline-block** is, as its name suggests, a compound of block and inline behavior, a “best of both worlds” option
- **list-item** is similar to **block** as it takes up the whole width available, but shows an additional bullet point
- **table**, **table-row** and **table-cell** all have very specific, albeit unexpected, behavior that allow more interesting layouts


#### display: block

This will turn any element into a block element.This technique is often used on links in order to increase their clickable zone, which can be easily evaluated by setting a background color.

```css
.menu a{ background: red; color: white;}

<ul class="menu">
  <li>
    <a>Home</a>
  </li>
  <li>
    <a>Features</a>
  </li>
  <li>
    <a>Pricing</a>
  </li>
  <li>
    <a>About</a>
  </li>
</ul>
```

```css
/* if we turn these links into blocks, we increase their target area: */
.menu a{ background: red; color: white; display: block;}
```

#### display: inline

This turns any element into inline elements, as if they were just simple text.It’s often used to create horizontal navigation's, where list items are semantically but not visually useful.

```css
<ul class="menu">
  <li>
    <a>Home</a>
  </li>
  <li>
    <a>Features</a>
  </li>
  <li>
    <a>Pricing</a>
  </li>
  <li>
    <a>About</a>
  </li>
</ul>


/* adding  inline */
.menu li{ display: inline;}
```

#### display: list-item

The only HTML elements that are displayed as list elements are (unsurprisingly) the list elements, but also the definition descriptions.

A list element is represented with a bullet (if it is an unordered list) or with a sequential number (if it is an ordered list).

Since the display of these bullet points and numbers is different in different browsers and is also difficult to design in CSS, the display: list-item rule is never used. As a rule, bullets are displayed as display: block or display: inline, because they are more flexible to design.


#### display: none

Applying display: none; to an HTML element removes it from your webpage, as if it never existed in your code.

```css
.gone-baby-gone{ display: none;}
```
```html
<p>Did I hear someone speaking??</p>
<p class="gone-baby-gone">Hahahahahah</p>
<p>I must be dreaming...</p>
```

#### visibility: hidden

The CSS visibility property is slightly similar to the display property. Applying visibility: hidden; hides an element on your page, but only makes it invisible: it continues to occupy the space it should.

```css
.hollow-man{ visibility: hidden;}
```
```html
<p>So far away from me </p>
<p class="hollow-man">So far i just can't see</p>
<p class="hollow-man">So far away from me</p>
<p class="hollow-man">You're so far away from me</p>
<p>You're so far away...</p>
```

### CSS height and width

The dimensions (or height and width) of an element are **dynamic**, as they fluctuate in order to fit the content. It is somehow possible to set **specific** dimensions.

```css
blockquote{ width: 600px;}
```

The blockquote does not take up the entire available width, but remains 600px wide in any situation:

if the browser window is less than 600px wide, a horizontal scrollbar is displayed. If the browser window is wider than 600px, the blockquote remains 600px wide and does not take up all the space
Since we have set only the width, the blockquote remains fluid in height: the height becomes the variable dimension to adjust the blockquote content.

#### Setting both height and width

When you set the dimensions of an element, it remains fixed regardless of the length of its contents.

What happens if the content is longer than the element can hold?

Because we prevent the element from dynamically changing its dimensions, there is a possibility that the content is longer than the element can hold, and it subsequently overflows.

The default behavior can be surprising: The content is displayed anyway!

```css
blockquote{ background: yellow; height: 50px; width: 100px;}
```
```html
<blockquote>The content er... finds a way</blockquote>
```

#### CSS overflow

The CSS property overflow allows us to manage the case when the content is longer than its container.

The default value is visible: the content is displayed anyway, because "why would you want to prevent the content from being read by the user if it's in the code?". You can consider HTML to be advantageous to CSS.

By applying overflow: hidden;, you simply prevent overflowing content from being seen.

If you want your content to overflow but still be accessible, you can show scroll bars by applying overflow: scroll.

A better option is to use overflow: auto, since the scroll bars appear only when the content overflows, but remain hidden until then.

#### Beware of fixed dimensions

Applying specific dimensions are often required for a design to look visually appealing but can have unintended consequences. In that regard:

- make sure your content doesn’t overflow
- if it does, use overflow: hidden or overflow: auto to prevent your design from breaking


### CSS border

Since an HTML element is rendered as a rectangle, it can have up to 4 borders: top, bottom, left, and right. You can set a border on all sides at once or on each side individually.

#### Border types and location

A CSS border has 3 properties:

- border-color defined by using a color unit
- border-style can be solid, dashed, dotted…
- border-width defined by using a size unit

It also has 4 possible sides:

- border-top
- border-bottom
- border-left
- border-right


```css
blockquote{ border-color: yellow; border-style: solid; border-width: 1px;}
/* The shorthand property border allows to define all 3 properties at once: */
blockquote{ border: 1px solid yellow;}
```

### Single border

If you want to set a border on only one of the four sides, you need to include the border’s position in the CSS property. For example, for a bottom border, you can write:

```css
blockquote{ border-bottom-color: yellow; border-bottom-style: solid; border-bottom-width: 1px;}
/* As for the border property, each side has its shorthand version: */
blockquote{ border-bottom: 1px solid yellow;}
```

### Shorthand combinations

| border | border-color | border-style | border-width |
| ----- | :---------------: |  :---------------: |  :---------------: |
| **border-top** |border-top-color| border-top-style | border-top-width |
| **border-bottom** |border-bottom-color| border-bottom-style | border-bottom-width |
| **border-left** |border-left-color| border-left-style | border-left-width |
| **border-right** |border-right-color| border-right-style | border-right-width |



### CSS padding

Padding is the space between the edge of an element and its content.
The size of the space can be defined with one of the size units.

```css
blockquote{ padding: 20px;}
/* the padding can be set individually for any of the 4 sides. */
blockquote{ padding-bottom: 20px;}

blockquote{ background: yellow; border: 1px solid blue;}
/* Adding a padding will provide space between the textual content and the borders: */
blockquote{ background: yellow; border: 1px solid blue; padding: 20px;}

```

### CSS margin

If padding adds space inside an element (between its border and its content), margins adds space outside between an element and other elements.

```html
<p>space inside an element</p>
<p>This question arises when neither a </p>
<p>element and other elements</p>
<p>none is present</p>
<p>Hey, can blend into each other</p>
<p>present and the borders?</p>
```
```css
p{ margin: 40px;}
```

#### Merging vertical margins

```css
.title{ margin-bottom: 30px;}
.subtitle{ margin-top: 15px;}
```
```html
<h1 class="title">MarkSheet</h1>
<h2 class="subtitle">A simple HTML/CSS tutorial</h2>
```

#### Choosing between margin and padding

Tricky question. This question arises when neither a frame nor a background is used. Indeed, if a frame or a background is specified for either element, the visual representation will be different. However, if none is present and the borders and spacing are transparent, the result will look the same.

Ask yourself why you're keeping the spacing. Is it to give the inner content more breathing room? Or is it to give the whole element more space? In the first case it's padding, in the second case it's margins.

Also consider how edges can blend into each other.


### CSS size shorthand wheel

Setting 4 values

```css
blockquote{ padding: 20px;}
/* Is equivalent to */
blockquote{ padding-top: 20px; padding-bottom: 20px; padding-left: 20px; padding-right: 20px;}

/* Short Hand */

blockquote{ padding: 20px 0 10px 50px;}

```

Setting 2 or 3 values

```css
blockquote{ padding: 20px 0;}
/*
       top
       20px
left         right
 0             0
      bottom
       20px
*/

```

### How to remember the shorthand order


Instead of focusing on the values you’ve entered, think about the values you haven't.

- if you enter 2 values (top/right), you omit setting bottom and left. Because bottom is the vertical counterpart of top, it will use top’s value. And because left is the horizontal counterpart of right, it will use right’s value.
- if you enter 3 values (top/right/bottom), you omit setting left. As right’s counterpart, it will use its value.
