<div align="center">
  <h1>CSS Positioning</h1>
<sub>Author:
<a href="https://www.linkedin.com/in/bhuvanaganesan-l-2209047a" target="_blank">Bhuvan Ganesan</a><br>
</sub>
</div>


# CSS Positioning

Even without applying CSS, an HTML document is already styled. Its content follows a natural flow that depends directly on the HTML structure.

But web pages often want elements to be positioned in a particular way to meet specific design requirements, which requires breaking the flow.

## The Flow

An HTML document is a living document

Even without any CSS applied, an HTML document already has its own rules:

- **fluidity**: how the content adapts to browser dimensions
- **ordering**: in which order elements appear
- **stacking**: how elements appear on top of each other

This natural behavior is logical.

### Fluidity

In HTML, the content is King.

All block elements are fluid. They will naturally adapt their layout to accommodate their inner content:

- **width: 100%** - a block will take up the whole width available
- **word wrap** - if a block’s inline content doesn’t fit on a single line, it will continue on a new line
- **height: auto** - a block’s height varies automatically to match its content’s siz
- A block is by default in full width
- Its height is the height of its content


### Ordering

HTML elements are displayed in the order in which they appear in the code. This means that the elements that are written first in the code will be displayed first in the browser. It is important to keep this in mind when coding HTML, as the order of elements can make a huge difference in how the page looks and functions.

```html
<p>First</p>
<p>Second</p>
<p>Third</p>
<p>Fourth</p>
<p>Fifth</p>
```

#### Stacking

The browser's three dimensions are height, width, and stack order. Height and width determine the size of the element, while stack order determines the order of the elements within the page. Stack order is determined by the nesting of elements within each other. Child elements appear on top of their respective parents, and the deeper an element is nested in the hierarchy, the higher it appears in the stack.

```html
<div>
  This parent is behind
  <p>
    This nested child appears <strong>on top</strong> of its parent
  </p>
</div>
```

#### Breaking the flow

CSS properties allow to disrupt the Flow

- **height** and **width** can alter an element’s fluidity
- **float** disrupts an element’s behavior as well as its surroundings
- **position** **absolute** and **fixed** remove an element from the Flow
- **z-index** can alter the order in which elements are stacked


## CSS position

CSS position property can be used to position elements in a variety of ways. It has four possible values: static, relative, absolute, and fixed. Static is the default value, and it positions the element according to the normal flow of the document. Relative positions the element relative to its normal position. Absolute positions the element relative to its parent. Finally, fixed positions the element relative to the browser window.

- static (default value)
- relative
- absolute
- fixed

It’s often used alongside the 4 coordinates properties:

- left
- right
- top
- bottom

#### static

This is the default position value: static elements just follow the natural flow. They aren’t affected by any left, right, top or bottom value.

#### relative

When the position is set to relative, an element can move according to its current position.

```html
<p>Well, Ja should know his own business, I thought, and so I grasped the spear and clambered up toward the red man as rapidly as I could - being so far removed from my simian ancestors as I am</p>
<p>I imagine the slow-witted sithic, as Ja called him, suddenly realized our intentions and that he was quite likely to lose all his meal instead of having it doubled as he had hoped</p>
<p>When he saw me clambering up that spear he let out a hiss that fairly shook the ground, and came charging after me at a terrific rate</p>
```
```css
p{ border: 1px solid blue;}
```
Let’s move the second paragraph:
```html
<p>Well, Ja should know his own business, I thought, and so I grasped the spear and clambered up toward the red man as rapidly as I could - being so far removed from my simian ancestors as I am</p>
<p class="second">I imagine the slow-witted sithic, as Ja called him, suddenly realized our intentions and that he was quite likely to lose all his meal instead of having it doubled as he had hoped</p>
<p>When he saw me clambering up that spear he let out a hiss that fairly shook the ground, and came charging after me at a terrific rate</p>
```
```css
.second{ position: relative; border-color: red; left: 20px; top: 10px;}
```

Notice how the blue paragraphs haven’t moved at all. By using relative positioning, the red paragraph can freely move without disrupting the layout. The only thing out of place is itself. All the other elements don’t know that element has moved.


#### absolute

When the position is set to absolute, an element can move according to the first positioned ancestor.A positioned element is one whose position value is either relative, absolute or fixed. So unless the position is not set or static, an element is positioned.

```html
<section>
  I'm in position relative.
  <p>
    I'm in position absolute!
  </p>
</section>
```
```css
section {
  background: gold;
  height: 200px;
  padding: 10px;
  position: relative; /* This turns the <section> into a point of reference for the <p> */
}

p {
  background: limegreen;
  color: white;
  padding: 10px;
  position: absolute; /* This makes the <p> freely movable */
  bottom: 10px; /* 10px from the bottom */
  left: 20px; /* 20px from the left */
}
```

#### fixed

When the position is set to fixed, it acts like absolute: you can set left/right and top/bottom coordinates.

The only difference is that the point of reference is the viewport. It means that a fixed element won’t scroll with the page ; it is fixed on the screen.

## CSS float

float is probably the most difficult CSS concept to grasp. Its behavior can be intriguing, unexpected, and magical. Probably because, of all positioning properties there are, it is the one that most influences its surroundings.

float can only have one of these 3 values:

- left and right turns an element into a floating one
- none removes the floating aspect

#### When to use float

The purpose of floating an element is to push it to one side and make the text wrap around it.

```html
<p>
  <img src="https://via.placeholder.com/150">
  The bells of the neighboring church made a jangling tumult, a cart carelessly driven smashed, amid shrieks and curses, against the water trough up the street.  Sickly yellow lights went to and fro in the houses, and some of the passing cabs flaunted unextinguished lamps. And overhead the dawn was growing brighter, clear and steady and calm.
</p>
```
After adding a float 
```css
img{ float: left;}
```

