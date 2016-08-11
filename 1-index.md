---
layout: default
title: HTML
---

# HTML

Here's a very light template that you can use as a base for a new HTML page: [blank.html](blank.html). It looks like this:

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8">
        <title>Hello, world!</title>
        <meta name="viewport" content="width=device-width, initial-scale=1">

        <link rel="stylesheet" href="css/main.css">
    </head>
    <body>
        <p>Hello, world!</p>

        <script src="js/main.js"></script>
    </body>
</html>
```

It's a trimmed version of the [HTML5 Boilerplate](https://html5boilerplate.com/), which is widely used and respected by the Front-end development community. Their documentation has lots of great advice.

## The bare bones

* Every [valid HTML document](https://validator.w3.org/) needs a `doctype`. This tells the browser what the document is (HTML), and therefore gives it somes clues about how to render it.
* The document starts and ends with `<html>` tags. The inside of that has two bits:
    * the `head` for metadata (data about the document);
    * the `body` for the content of the document itself.

## All in your head

* `<meta charset="utf-8">` is the character encoding for Unicode. This tells the browser how to read the content of the page.
* `<title>Hello, world!</title>` sets the title of the page in the browser tab and in search engine results. You must have a `title` in your `head`.
* `<meta name="viewport" content="width=device-width, initial-scale=1">` is for improving the display on mobile devices. It sets the width of the page to the width of the device. Try removing it on a site to see the difference it makes.
* `<link rel="stylesheet" href="css/main.css">` points to an external stylesheet. When the browser hits this line, it stops rendering the page until it's downloaded the `main.css` file. It goes at the top so that we have the styles (the presentation) before we show the HTML (the structured content) to the user.
* `<script src="js/main.js"></script>` points to an external JavaScript file.  When the browser hits this line, it stops rendering the page until it's downloaded the `main.js` file. Since the rest of the page (and the CSS) has already loaded, the can interact with the page while the JavaScript is loading.

## Semantics

When writing HTML, think about what elements to use. `div` and `span` are two generic containers. You should only use them if no other semantic element more appropriate. Is the content a list? Use a `ul` or `ol`. If you need to style something, can you add a class to an existing element rather than adding a new `div` or `span` with the class?
