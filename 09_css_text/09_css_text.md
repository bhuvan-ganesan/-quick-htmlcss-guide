<div align="center">
  <h1>CSS Text</h1>
<sub>Author:
<a href="https://www.linkedin.com/in/bhuvanaganesan-l-2209047a" target="_blank">Bhuvan Ganesan</a><br>
</sub>
</div>


# CSS TEXT 
The Web is 90% text, so let's we need to style text.

## CSS font-family

CSS provides several font properties that directly affect text rendering. The font-family property specifies which font to use.

### Generic font families

Fonts are grouped in 5 generic families:

- **serif** fonts have small lines attached to the end of each character
- **sans-serif**
- **monospace**

```css
/* since font family is inherited for HTML  */
body{ font-family: sans-serif;}
```

### Web-safe fonts

The problem with using generic font names is that the design of your website depends on the font that the user has set in their preferences.Since you probably want your website to look the same on all computers, you should specify a particular font to use. To do this, simply use the name of the font.

```css
body{ font-family: Arial;}
```
However, Arial is a safe choice because it is installed on all Windows and Mac computers, as well as on most Linux systems. Therefore, Arial is considered a web-safe font: you can safely use it in your CSS and be almost certain that the user's computer has it installed.

There are 9 web-safe fonts:

- Arial
- Arial Black
- Comic Sans MS
- Courier New
- Georgia
- Impact
- Times New Roman
- Trebuchet MS
- Verdana

```css
/* Applying a list of fonts for safety fallback */
body{ font-family: Arial, Verdana, sans-serif;}
```

### CSS font properties

#### font-size

Bear in mind that setting a font size of 16px won’t make each letter 16px high. The actual size of each letter depends on the font-family used.
```css
p{ font-size: 16px;}
```

#### font-style

Default value: font-style: **normal**;
```css
h2{ font-style: italic;}
```

#### font-weight

This property can make your text bold:
```css
h2{ font-weight: bold;}

/* Default value: font-weight: normal;
Depending on the font-family used, there is a range of font weights available, from 100 to 900: */

font-weight: 100; /* Thin */
font-weight: 200; /* Extra Light */
font-weight: 300; /* Light */
font-weight: 400; /* Which is like font-weight: normal; */
font-weight: 500; /* Medium */
font-weight: 600; /* Semi Bold */
font-weight: 700; /* Which is like font-weight: bold; */
font-weight: 800; /* Extra Bold */
font-weight: 900; /* Ultra Bold */
```

#### font-variant

This property turn your text into small caps:
Default value: font-variant: **normal**;.

```css
h2{ font-variant: small-caps;}
```

### CSS line-height

The line-height property, when applied to block-level elements, defines, as the name implies, the height of each line. It should not be confused with line-spacing (also known as leading), which is found in most graphics programmes (such as Photoshop) and defines the spacing between lines in a paragraph. Although both serve the same purpose (spacing between lines of text), they do so in different ways.

```css
/* The purpose of the line-height is to define a readable line spacing for your text. */
/* unitless numbers is used */
/* !!! for body text, a line height of 1.5 times the size of the text is recommended.
!!!  for headings, a line height of 1.2 is recommended */
body{ font-size: 16px; line-height: 1.5;}
```
The computed line height will thus be 16 * 1.5 = 24px.

#### Line-height inheritance

Since the line height property is inherited by the child elements, it remains consistent no matter what font size is subsequently applied.

```css
body{ font-size: 16px; line-height: 1.5;}
blockquote{ font-size: 18px;}
```
The blockquote element will have a line height of 27px.


### CSS font shorthand

The font property regroups (in this particular order):

- font-style
- font-variant
- font-weight
- font-size
- line-height
- font-family
  
You can thus define 6 properties through a single one:

```css
/* slash / between the font-size and the line-height. */
body{ font: italic small-caps bold 16px/1.5 Arial, sans-serif;}


body{ font: bold 16px/1.5 Arial, sans-serif;}

/* Because font-style and font-variant have not been defined, they’ll use their default value normal. */


/* Beware! If you’ve previously define one of the font properties and use the font shorthand afterwards, it will override the previously defined values. */
body{ font-size: 16px; line-height: 1.5;}
ul{ font: 14px Georgia, serif;}

/* In the font shorthand, the line-height has not been defined, and will lose its ancestor’s value of 1.5 and will revert to its default value medium (which is usually 1.2). */
```


### CSS text properties

#### text-align

The text-align property must be applied on a block-level element and defines how its text and children inline elements are horizontally aligned.
there most used values are left , right , center and justify
```css
body{ text-align: left;}
```

#### text-decoration

The text-decoration property is used to add a line on your text.Default value: none
there most used values are overline , underline and line-through.

```css
.deleted{ text-decoration: line-through;}

a{ text-decoration: none;}
```

#### text-indent

The text-indent property allows to add space before the first letter of the first line of a block-level element.Default value: 0 (zero)

```css
blockquote{ text-indent: 30px;}
```

#### text-shadow

If you’ve ever used Photoshop, you’ve probably used the drop shadow tool. In CSS, you can add shadow to a text, to make it either fancier or more readable.

You define:

- x the horizontal offset
- y the vertical offset
- the blur
- the color

Only the x and y values are required. The blur defaults to 0 (zero), while the color defaults to the color of the text.

```css
h1{ text-shadow: 0 2px 5px rgba(0,0,0,0.5);}
```


### Useful links