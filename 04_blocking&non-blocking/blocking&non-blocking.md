<div align="center">
  <h1>Blocking and Non-blocking Elements</h1>
<sub>Author:
<a href="https://www.linkedin.com/in/bhuvanaganesan-l-2209047a" target="_blank">Bhuvan Ganesan</a><br>
</sub>
</div>

## Blocking and Non-blocking Elements

HTML elements are like a box. Some elements take up the entire width of the viewport, while others take up so much space that they fit only for content. In other words, some elements do not allow other elements to be to their left and right, while others allow other elements to be next to them.

- Blocking elements take the whole width of the viewport.
- Non-blocking element only take a space that is enough for the content.

List of blocking elements:

```html
<address></address> - allows to write an address related information
<article></article> - allows to write articles in a section
<aside></aside> - allows to create a section that is indirectly related to the document
<blockquote></blockquote> - to create text a quotation mark
<canvas></canvas> - to create canvas (for js based image )
<dd></dd> - to describe a term or name in a description list
<div></div> - to create section or box
<dl></dl> - to create a description list
<dt></dt> - describes a term a description list
<fieldset></fieldset> - to create related elements in a from
<figcaption></figcaption> - define figure caption
<figure></figure> - to wrap figure, diagram, etc
<footer></footer> - to create footer of a document
<form> - to create a form
<h1></h1> to <h6></h6> - to create different size headings
<header></header> - to create header of a document
<hr /> - to create a horizontal line
<li></li> - create order or an unordered list
<main></main> - to wrap the main content of the document
<nav><nav> - to create navigation
<noscript></noscript> - describe an alternative content to be displayed to users when JS has disabled on their browsers.
<ol></ol> - to create an ordered list
<p></p> - to create paragraph
<pre></pre> - to create a space preserved content, eg poem
<section><section> - to create section
<table></table> - to create table
<tfoot><tfoot> - to create a table footer
<ul><ul> - to wrap order or un-order list
<video></video> - to create a video content
```

Now, let's use some of the blocking elements in following snippet of code.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>blocking elements </title>
  </head>
  <body>
    <main>
      <section>
        <h1 id="title-id">The Building Blocks of the web</h1>
        <article>
          <p>
            There is not website without HTML. Learn HTML and build websites and
            web applications
          </p>
        </article>
      </section>

      <section>
        <h2>Front end</h2>
        <ul>
          <li>HTML</li>
          <li>CSS</li>
          <li>JavaScript</li>
        </ul>
      </section>
      <section>
        <video src="./assets/video/js-project.mp4"></video>
      </section>
    </main>
    <footer>
      <small>Copyright @ Bhuvan Ganesan</small>
    </footer>
  </body>
</html>
```

List of non-blocking elements

```html
<a> - to create a link
<abbr> - to create abbreviation
<acronym> - to create an acronym
<audio> - to create or embed an audio
<b> - to make bold
<bdo> - to reverse a text
<big> - to make text big
<br> - to make a line break
<button> - to create a button
<cite> - to add citation
<code> - to write code on HTML
<dfn> - to write definition using HTML
<em> - to make an emphasis
<i> - to make italic
<img> - to create an image
<input> - to create an input field
<kbd> - to define keyboard inputs
<label> - to create a label for input fields
<map> - to define an image map
<object> - to represent an external resource that used to multimedia such as audios, videos, images, pdf, etc
<output> - to represent a result of a calculation
<q> - short quotation
<samp> - to represent sample output
<script> - to write JS code
<select> - to select items
<small> - to write small size texts
<span> - to mark or separate a text
<strong> - to make text with strong importance
<sub> - to create subscript
<sup> - to make superscript
<textarea> - to create a text area
<time>- represents a specific period of time
<tt> - to represent inline teletype
<var> - is used to define a variable
```

Let's make use of the above tags in the previous snippet of code.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>non-blocking elements</title>
  </head>
  <body>
    <header>
      <span style="color: #e34c26">H</span>
      <span style="color: #264de4">T</span>
      <span style="color: #f0db4f">M</span>
      <span style="color: #61dbfb">L</span>
    </header>
    <main>
      <section>
        <h1 id="title-id">The Building Blocks of the web</h1>
       <article>
          <p>
          There is not website without HTML. Learn HTML and build websites and
          web applications
        </p>
         </article>
      </section>
      <section>
        <h2>Front end Technologies</h2>
        <!-- Unorder list -->
        <ul>
          <li>HTML</li>
          <li>CSS</li>
          <li>JavaScript</li>
          </ul>
          <!-- Ordered list -->
          <p>Ten most populated countries</p>
          <ol>
            <li>China<li>
            <li>India<li>
            <li>USA<li>
            <li>Indonesia<li>
            <li>Brasil<li>
            <li>Pakistan<li>
            <li>Nigeria<li>
            <li>Bangladesh<li>
            <li>Russia</li>
            <li>Japan</li>

          </ol>
            <!-- To link an image: img tag and src attribute, we put the path in the src -->
          <img src ='./assets/images/html.png' alt='HTML Logo'>
            <img src ='./assets/images/css_logo.png' alt='CSS Logo'>
           <img src ='./assets/images/js_logo.png' alt='JS Logo'>
            <img src ='./assets/images/css_logo.png' alt='CSS Logo'>
        </section>
        <!-- button allows to do some action -->
        <button onclick = "alert('Welcome to 30 DaysOfHTML')"> Click Me</button>

        <section>
          <h1>Audios</h1>
          <audio controls>
            <source src="./assets/audios/audio_1.mp3" />
            </audio>
             <audio controls>
            <source src="./assets/audios/audio_2.mp3" />
            </audio>
             <audio controls>

        </section>

    </main>
    <footer>
      <small>Copyright @ Bhuvan Ganesan</small>
      <!-- Social Link: -->
      <ul>
        <li>
          <!-- a tag takes href attribute to target a link resource -->
          <a href="https://www.linkedin.com/">LinkedIn</a>
          </li>
            <li>
          <a href="https://twitter.com/">Twitter</a>
          </li>
            <li>
          <a href="https://github.com/">GitHub</a>
          </li>
        </ul>
    </footer>
  </body>
</html>
```

To create a new line between non-blocking elements we can use the break(br) element.



### Useful links

1. https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements
2. https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements