<div align="center">
  <h1>TITLE</h1>
<sub>Author:
<a href="https://www.linkedin.com/in/bhuvanaganesan-l-2209047a" target="_blank">Bhuvan Ganesan</a><br>
</sub>
</div>


## Links

The a anchor tag, along with the href attribute, create a hyperlink. Links are the backbone of the internet. 

```html
<a href="https://machinelearningworkshop.com">Machine Learning Workshop</a>
```

###  The href attribute

The href attribute, while not required, occurs in almost all \<a\> tags. By specifying the address of the hyperlink, the \<a\> becomes a link. The href attribute is used to hyperlink to locations on the current page, to other pages within a site, or to other sites altogether. It can also be encoded to download files or send an email to a specific address, even with a subject and suggested content for the email.

```html
<a href="https://machinelearningworkshop.com">Machine Learning Workshop</a>
<a href="#teachers">Our teachers</a>
<a href="https://machinelearningworkshop.com#teachers">MLW teachers</a>
<a href="mailto:hal9000@machinelearningworkshop.com">Email Hal</a>
<a href="tel:8005551212">Call Hal</a>
```



The second link is just a link fragment identifier, and will link to the element with id="teachers", if there is one, on the current page. Browsers also support two "top of page" links: clicking on \<a href="#top"\>Top\</a\> (case-insensitive) or simply \<a href="#"\>Top\</a\> will scroll the user to the top of the page, unless there is an element with the id of top set in the same letter casing.

MLW is a fairly long document. To save scrolling, you can add a link back to the top from the bottom of the #teachers section:

The first link contains an absolute URL that can be used on any website in the world to navigate to the MLW home page. Absolute URLs contain a protocol, in this case https://, and a domain name. If the protocol is written simply as //, it is an implicit protocol and means "use the same protocol that is currently in use"

Relative URLs do not contain a protocol or a domain name. They are "relative" to the current file. MLW is a one-page website, but this HTML series has multiple sections. To link from this page to the lesson on attributes, a relative URL is used \<a href="../attributes/"\>Attributes\</a\>.

The second link is just a link fragment identifier, and will link to the element with id="teachers", if there is one, on the current page. Browsers also support two "top of page" links: clicking on \<a href="#top">Top\</a\> (case-insensitive) or simply <a href="#">Top</a> will scroll the user to the top of the page, unless there is an element with the id of top set in the same letter casing.

```html
<a href="#top">Go to top.</a>
```

### Browsing context

The target attribute enables the defining of the browsing context for link navigation (and form submission. The four case-insensitive, underscore-prefixed keywords were discussed with the \<base\> element. They include the default _self, which is the current window, _blank, which opens the link in a new tab, _parent, which is the parent if the current link is nested in an object or iframe, and _top, which is the top-most ancestor, especially useful if the current link is deeply nested. _top and _parent are the same as _self if the link is not nested. The target attribute is not limited to these four key terms: any term can be used.

Every browsing context—basically, every browser tab—has a browsing context name. Links can open links in the current tab, a new unnamed tab, or a new or existing named tab. By default, the name is the empty string. To open a link in a new tab, the user can right-click and select "Open in a new tab". Developers can force this by including target="_blank".

A link with target="_blank" will be opened in a new tab with a null name, opening a new, unnamed tab with every link click. This can create many new tabs. Too many tabs. For example, if the user clicks on \<a href="registration.html" target="_blank"\>Register Now\</a\> 15 times, the registration form will be opened in 15 separate tabs. This problem can be fixed by providing a tab context name. By including the targetattribute with a case-sensitive value—such as \<a href="registration.html" target="reg"\>Register Now\</a\>—the first click on this link will open the registration form in a new reg tab. Clicking on this link 15 more times will reload the registration in the reg browsing context, without opening any additional tabs.

```html
_blank  Opens the linked document in a new window or tab
_self   Opens the linked document in the same frame as it was clicked (this is default)
_parent     Opens the linked document in the parent frame
_top    Opens the linked document in the full body of the window
framename   Opens the linked document in a named frame
```


## Image Tag

The image tag is used to place an image on the web page.

```html
<img src="image1.jpg">
```

**Size Attributes**

The size attributes define the width and height of the image. They look like this:

```html
<img src="image.jpg" width="200" height="150">
```
**Alt & Title Tags**
```html
<img src="image.jpg" alt="Photo of Mr and Mrs Owen" title="Mr and Mrs Owen">
```


## Audio Tag

The audio element defines a browser-internal audio player. The audio player can provide a single piece of audio content. To specify the source file of the audio content, use one or more source elements within the audio element. All source files should contain the same audio content, but in different file formats. The browser will choose the first file format it can play. (So arrange them as you wish.) If you do not provide multiple source file formats, you can specify the source file in the src attribute, rather than in a separate source element.


```html
<audio src="/uploads/flamingos.mp3" controls> 
```


#### Audio File Formats

The most supported audio format is .mp3, which is recognized by all popular browsers that recognize the audio element. The second most common format is .wav, which is supported by most browsers that are still in development (i.e., not Internet Explorer). Other formats, such as .ogg and .acc, are supported only sporadically. If you want to use one of these formats, you should provide a better-supported alternative.


## Video

The Video element, which adds native support for video playback to the HTML specification in HTML5, can be used to embed a video in an HTML document. Add the video URL to the element by either using the src attribute of the video element or nesting one or more source elements between the opening and closing video tags.


```html
<video width="640" height="480" src="https://archive.org/download/Popeye_forPresident/Popeye_forPresident_512kb.mp4" controls> Sorry, your browser doesn't support HTML5 <code>video</code>, but you can download this video from the <a href="https://archive.org/details/Popeye_forPresident" target="_blank">Internet Archive</a>. </video>

```

**iframe vs video**

Many video hosting sites such as YouTube and Vimeo offer a code to embed videos that uses an iframe instead of the video tag. Which tag should you use when embedding a video from a video streaming service like YouTube or Vimeo? In almost all cases, it makes the most sense to use the embed code provided by the video streaming service. This way, you'll benefit from all the optimization techniques built into the streaming service's video player. The optimizations help improve playback speed and include fallback options for users of older browsers.




### Useful links

1. https://html.com/tags/audio/
2. https://html.com/tags/image/
3. https://html.com/tags/video/
4. https://html.com/media/