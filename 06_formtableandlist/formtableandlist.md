<div align="center">
  <h1>HTML Forms</h1>
<sub>Author:
<a href="https://www.linkedin.com/in/bhuvanaganesan-l-2209047a" target="_blank">Bhuvan Ganesan</a><br>
</sub>
</div>

## HTML Form

A form is a part of a website. Various websites process user data using an HTML form. For example, when we create an account or log in to our account, we fill out an input field. Filling a form on a website is a common activity. Therefore, we need to know how to create a form.
To create a form, we use the _form_ element and the _form_ element encloses other input fields. The input field can be a text, a number, a date, a checkbox, a radio button, a file or any other type.

```html
<form>
  <label>First name:</label>
  <input type="text" />
  <input type="submit" value="Submit" />
</form>
```

The HTML form code below can handle different kind of data. It handles almost any kind of data including file.

```html
<h1 class="section-title">Application Form</h1>
<article class="form-article">
  <form class="contact-form">
    <div class="form-group">
      <label for="firstname">First Name</label>
      <input type="text" id="firstname" placeholder="Your name" />
    </div>
    <div class="form-group">
      <label for="lastname">Last Name</label>
      <input id="lastname" type="text" placeholder="Your last name" />
    </div>
    <div class="form-group">
      <label for="email">Email</label>
      <input type="email" id="email" placeholder="Your email" />
    </div>
    <div class="form-group">
      <label for="company">company</label>
      <input id="company" type="text" placeholder="Your company name" />
    </div>
    <div class="form-group">
      <label for="age">You age: </label>
      <input type = "number" id="age" name="age' placeholder="Age" />
    </div>
    <div class="form-group">
      <label for="date">Date of Birth</label>
      <input id="date" type="datetime-local" />
    </div>
    <div class="form-group">
      <p>What are your skills</p>
      <input type="checkbox" id="html" />
      <label for="html">HTML</label>
      <br />
      <input type="checkbox" id="css" />
      <label for="css">CSS</label>
      <br />
      <input type="checkbox" id="js" />
      <label for="js">JavaScript</label>
      <br />
      <input type="checkbox" id="angular" />
      <label for="js">Angular</label>
      <br />
      <input type="checkbox" id="vue" />
      <label for="redux">vue</label>
    </div>
    <div class="form-group">
      <label for="color">Your favorite</label>
      <input id="color" type="color" />
    </div>

    <div class="form-group">
      <p>Gender</p>
      <input type="radio" id="female" name="gender" />
      <label for="female">Female</label>
      <br />
      <input type="radio" id="male" name="gender" />
      <label for="male">Male</label>
      <br />
      <input type="radio" id="other" name="gender" />
      <label for="other">Other</label>
    </div>

    <div class="form-group">
      <p>Select your country</p>
      <select name="country" id="country">
        <option value="">-Country-</option>
        <option value="Finland">Finland</option>
        <option value="India">India</option>
        <option value="Sweden">Sweden</option>
        <option value="Norway">Norway</option>
        <option value="Chiba">China</option>
      </select>
    </div>
    <div class="form-group">
      <p>Select your country</p>
      <select name="course" id="course">
        <option value="">-Select Course-</option>
        <option value="html-css">Basis of HTML and CSS</option>
        <option value="js">Modern JavaScript</option>
        <option value="angular">Angular</option>
        <option value="react">React</option>
        <option value="data-analysis">Data Analysis</option>
      </select>
    </div>

    <div class="form-group">
      <label for="message">Leave your message here</label> <br />
      <textarea
        cols="120"
        rows="10"
        id="message"
        placeholder="Write your message here..."
      ></textarea>
    </div>
    <div class="form-group">
      <input type="file" id="file-input" />
      <label for="file-input"><i class="fas fa-upload"></i>Upload File</label>
    </div>
    <div>
      <input type="checkbox" id="agree" />
      <label for="agree"
        >Be sure that all the information is yours and true.</label
      >
    </div>
    <div>
      <input type="submit" value="Submit" />
    </div>
  </form>
</article>
```

## HTML Table

In this section we will see how to create an HTML table. A table has an outer frame, header rows and header cells, body rows and their cells, and may also have a footer. To create an HTML table, we need a _table_ element that encloses all the rows and the rows enclose all the data cells.

```html
<table>
  <tr>
    <td>Name</td>
    <td>Gender</td>
    <td>Country</td>
  </tr>
  <tr>
    <td>Bhuvan</td>
    <td>Male</td>
    <td>India</td>
  </tr>
</table>
```

Let us see the output of the above code

<table>
  <tr>
    <td>Name</td>
    <td>Gender</td>
    <td>Country</td>
  </tr>
  <tr>
  <td>Bhuvan</td>
  <td>Male</td>
  <td>India</td>
  </tr>
</table>

However, HTML table has _thead_, **tbody** and **tfooter**. Let us add thead and tbody to the above code. In addition, we can use th in the table head instead to td to make the table heading bold.

```html
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Gender</th>
      <th>Country</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Bhuvan</td>
      <td>Male</td>
      <td>India</td>
    </tr>
  </tbody>
</table>
```

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Gender</th>
      <th>Country</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Bhuvan</td>
      <td>Male</td>
      <td>India</td>
    </tr>
  </tbody>
</table>


```html
<html>
  <head>
    <title>HTML: Table</title>
    <style>
      /* Table CSS */
      table,
      td,
      th {
        border: 2px solid gray;
        border-collapse: collapse;
        border: 1px solid #a785df;
      }
      table {
        margin-top: 15px;
        width: 75%;
      }
      td {
        padding-left: 10px;
      }
      th {
        background-color: #7433df;
        color: white;
      }
    </style>
  </head>
  <body>
    <table>
      <thead>
        <tr>
          <th>Challenge</th>
          <th>Days</th>
          <th>Time</th>
          <th>URL</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>HTML & CSS</td>
          <td>30</td>
          <td>November 2022</td>
          <td>
            <a href="https://github.com/bhuvan-ganesan/quick-htmlcss-guide">Link</a>
          </td>
        </tr>
        <tr>
          <td>JavaScript</td>
          <td>30</td>
          <td>January 2022</td>
          <td>
            <a href="https://github.com/bhuvan-ganesan/quick-htmlcss-guide">Link</a>
          </td>
        </tr>
        <tr>
          <td>React</td>
          <td>30</td>
          <td>October 2022</td>
          <td>
            <a href="https://github.com/bhuvan-ganesan/quick-htmlcss-guide">Link</a>
          </td>
        </tr>
        <tr>
          <td>Angular</td>
          <td>30</td>
          <td>February 2022</td>
          <td>
            <a href="https://github.com/bhuvan-ganesan/quick-angular-guide">Link</a>
          </td>
        </tr>
      </tbody>
    </table>
  </body>
</html>
```

## Lists

Lists are important to list down items. In HTML, we have different list types such as ordered list, unordered list and description list.

### Ordered List


```html
<ol>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
  <li>React</li>
  <li>Redux</li>
  <li>Node</li>
  <li>MongoDB</li>
  <li>GatsBy</li>
</ol>
```

### Unordered List


```html
<ul>
  <li>Finland</li>
  <li>Sweden</li>
  <li>Norway</li>
  <li>Denmark</li>
  <li>Iceland</li>
</ul>
```

### Description List

A description list indent the list to the right.

```html
<dl>
  <dt>HTML</dt>
  <dd>HTML(HyperText Markup Language) is the build block the web.</dd>
  <dt>CSS</dt>
  <dd>CSS(Cascading Style Sheet) that make HTML page look beautiful.</dd>
  <dd></dd>
  <dt>JavaScript</dt>
  <dd>
    JavaScript is a programming language that can add interactivity to websites
  </dd>
  <dt>React</dt>
  <dd>
    React is a modern JavaScript library that was initial released on May 29,
    2013.
  </dd>
</dl>
```

Output of the above code

<dl>
  <dt>HTML</dt>
  <dd>HTML(HyperText Markup Language) is the building block the web.</dd>
  <dt>CSS</dt>
  <dd>CSS(Cascading Style Sheet) that make HTML page look beautiful. <dd>
  <dt>JavaScript</dt>
  <dd>JavaScript is a programming language that can add interactivity to websites</dd>
  <dt>React</dt>
  <dd>React is a modern JavaScript library that was initial released on May 29, 2013.</dd>
</dl>



### Useful links

1. https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form
2. https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics
3. https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form
   