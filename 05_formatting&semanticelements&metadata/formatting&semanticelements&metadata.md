<div align="center">
  <h1>Formatting Elements, Semantic Elements and Metadata</h1>
<sub>Author:
<a href="https://www.linkedin.com/in/bhuvanaganesan-l-2209047a" target="_blank">Bhuvan Ganesan</a><br>
</sub>
</div>

## HTML5 Formatting Elements

We format text in different ways every day. Every Microsoft Office user knows how to format text in a Microsoft Office document. Similarly, we can format text on the Internet using various HTML elements.

HTML Formatting Elements

```html
- <b> - Create bold text
- <strong> - Make an important text
- <i> -  Make italic text
- <em> -  Make emphases to text
- <mark> - Marks text
- <small> - Make smaller text
- <del> - Deleted text
- <ins> - Inserted text
- <sub> - Subscript text
- <sup> - Superscript text
- <pre> - Preserve text space
- <u> -To underline
```

I want to be <b>bold Text </b>  
I am very <strong>important text </strong>  
I want to be <i>an italic text </i>  
I am <em>emphasized text </em>  
I am <mark> marked text </mark>  
I am <small>a smaller text </small>  
I am <del> deleted text </del>  
My favorite language is not <del>Python</del>. It is <ins>JavaScript</ins>  
2H<sub>2</sub> + O<sub>2</sub> = 2H<sub>2</sub> O<sub></sub>
2<sup>10</sup> = 1024

<pre>I like to make break her
I like to start a new line
This is the third line. The pre tag is 
good to use when a space is need to be
preserved for instance for poem.</pre>

<u>I am underlined</u>

## HTML5 Semantic Elements

Semantic elements have special meaning and describe their significance to the browser. For example, _<div>_ and _<span>_ are not semantic elements because they have no meaning to a browser. however, _<header>_ or _<foot>_ is a semantic element because it uniquely describes and defines its content.

List of some semantic elements:

```html
 <article>
 <aside>
 <details>
 <figcaption>
 <figure>
 <footer>
 <header>

 <main>
 <mark>
 <nav>

 <section>
 <summary>
 <time>
```

To know more about each semantic element, you can read this [article](https://www.freecodecamp.org/news/semantic-html5-elements/).


## HTML Document metadata

The HTML document begins with a declaration followed by the  _<html>_ tag. Inside the _<html>_ tag, there is _<head>_ and _<body>_. The _<head>_ contains the _metadata of the HTML document. The metadata contains information about the page, including styles, scripts, and data that helps the software use and render the page. In this section, we will learn how to use the various metadata. See the table to understand the different metadata.

Source, [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

- base: The base tag refers to the base URL for all relative URLs in a document

```html
<!DOCTYPE html>
<html>
  <head>
    <!-- character encoding for the HTML document -->
    <meta charset="UTF-8" />

    <!-- the following meta tags for Search engine optimization(SEO)-->
    <meta name="description" content="HTML Session by Bhuvan" />
    <meta name="keywords" content="HTML, CSS, Web Development" />
    <meta name="author" content="Bhuvan ganesan" />
    <!-- base url https://www.bhuvan.com -->
    <base href=" https://www.bhuava.com" target="_blank" />
    <!-- Goes to the task bar on the browser-->
    <title>HTML Session on MetadataL</title>
    <!-- to lik external css -->

    <link rel="stylesheet" href="" />
    <!-- inline styling is very tideous, we can also use internal style
     we can use tag name, id or class to select an element. Id is unique and class is for a single or group of elements

     When we select by id we use # followed by the id name and if we select by class name we use . followed by a class name.
     
     -->
    <style>
      .letter {
        font-size: 68px;
      }
      #letter-h {
        color: #e34c26;
      }
      #letter-t {
        color: #264de4;
      }
      #letter-m {
        color: #f0db4f;
      }
      #letter-l {
        color: #61dbfb;
      }
    </style>
    <!-- The script tag allows to write JS code -->
    <script>
      console.log('Welcome to html session')
    </script>
  </head>
  <body>
    <main>
      <section>
        <h1 id="title">The Building Blocks of the web</h1>
        <p>Learn HTML and build websites and
          web applications
        </p>
        <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element">MDN</a>
      </section>
    </main>
    <footer>
      <small>Copyright @ Bhuvan Ganesan</small>
    </footer>
  </body>
</html>
```




### Useful links

1. https://www.freecodecamp.org/news/semantic-html5-elements/
2. https://developer.mozilla.org/en-US/docs/Web/HTML/Element