<div align="center">
  <h1>HTML Basic</h1>
<sub>Author:
<a href="https://www.linkedin.com/in/bhuvanaganesan-l-2209047a" target="_blank">Bhuvan Ganesan</a><br>
</sub>
</div>

# What is HTML?

The word HTML is an acronym. It stands for Hypertext Markup Language. It is the standard markup language for developing websites. HTML is the basic building block of the web that allows you to create layouts of pages with HTML elements. HTML is not a programming language, but a markup language.

HTML code is rendered by a browser and gives human readable output. Take a look at the figure below to better understand how HTML code is converted into a website using a browser.

### HTML Element

HTML elements consist of an open tag(<>), Attribute(s), content and closing tag(<>). See the following code to understand the syntax of an HTML element

```html
<tag-name> content </tag-name>
```
```html
<h1>HTML</h1>
```

The tag name is *h1* and the content is 'HTML'. The h1 will tell the browser to make the text a big font size that why we call HTML a markup language.

```sh
<p>
  Learn HTML and build a website.
</p>
```

The *p* tag marks the text to be paragraph that why we call HTML a markup language.

### Attribute

HTML attributes provide additional information about the element. An attribute can be added only in the opening tag. It will be difficult to list all HTML attributes, but we can list the most common ones.

- alt - to add information about added image, use with img element.
- autocomplete - to enable auto complete feature of a form, use with form and input.
- autofocus - enable auto focus of input fields
- autoplay - allows playing an audio/video on the page loads
- charset - enable character encoding of meta tag
- checked - to make a checkbox checked of an input element
- class - to give a common identifier for HTML elements
- cols - to determine the width of a textarea element
- contenteditable - make any element editable
- download - allows a link to download a resource(image, pdf, PPT, etc)
- draggable - to make an element draggable, apply to all elements
- for - to connect/bound a label element with a specific input field, use with a label tag
- href - to specify a URL or a path of a resource, use with a link tag
- id - a unique id for an HTML element, apply to all elements
- lang - specifies the language of the page
- type - specifies the type of the element and it uses with only a certain elements
- src - to specify URL of a media file(img, audio, video, source, embed, script)
- style - to add an inline CSS style to an element

There are also event listener attributes that listen on mouse or keyboard. For example, onclick, onsubmit, onkeydown, onkeyup, onscroll, etc. Remember, do not try to remember it tediously. 

Detailed information about HTML attributes can be found at the following [link](https://www.w3schools.com/tags/ref_attributes.asp)

An attribute is optional in an HTML element. See the following h1 tag with an id attribute value of title-id.
```html
<tag-name attribute-name="attribute-value"> content </tag-name>
```
```html
<h1 id="title-id">HTML</h1>
```
An HTML element can have multiple attributes
```html
<h1 id="title-id" class="title">HTML</h1>
```

The above *p* tag has a style attribute. The style attribute has a color property and a value gray. The style changes the text color to gray. You can try it by adding other property and value in the style. Each value has to be separated by a semicolon.

```html
<p style="color:gray;">
Learn HTML and build a website.
</p>
```

Some HTML elements do not have a closing tag, instead they have a self-closing tag.

The slash is optional, but I strongly recommend using the slash with self-closing tags. For example, React.js does not allow you to work without the slash.

```html
<area />
<base />
<br />
<col />
<embed />
<hr />
<img />
<input />
<link />
<meta />
<para />
<source />
<track />
<wbr />
```

### HTML Comment

Comment in any programming language help a code to be more readable. Therefore, it is common to leave some text on a code to make it more readable and maintainable. Let us the syntax of an HTML comment below

```sh
<!-- The is an HTML comment -->
```

### Useful links
1. what is html - https://www.freecodecamp.org/news/what-is-html-what-does-html-stand-for-solved/
2. Attributes - https://www.w3schools.com/tags/ref_attributes.asp
   
