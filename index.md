---
layout: default
title: Index
---

# HTML

Used [h5bp](https://html5boilerplate.com/) (the HTML5 Boilerplate) as a base. Our base: [blank.html](blank.html).

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8">
        <title>Hello, world!</title>
        <meta name="viewport" content="width=device-width, initial-scale=1">

        <!-- <link rel="stylesheet" href="css/main.css"> -->
    </head>
    <body>
        <p>Hello, world!</p>

        <!-- <script src="js/main.js"></script> -->
    </body>
</html>
```

## HTML

Web sites as blocks.

* `meta` (charset, viewport), title, link (position in doc), script (position in doc)
* `div`, `span` (use only if no other semantic element is better. Do you really need to add another element?)

## HTML forms

HTML is static: something has to catch the `form`.

* `form` (method, action)
* `input` text, `name` attribute, `id` attribute
* `input` submit
* password
* `label`, `for` attribute (UX, accessibility)
* hidden
* `textarea`
* radio, select, option (pick one)
* checkbox (pick many)
* file
* `fieldset`, `legend` (semantics, UX, accessibility)

## New HTML elements

* `section`, `article`, `aside`, `main`, `header`, `footer`, `nav` (accessibility, semantics)
* `picture` and `srcset` (responsive) (look at [HTML of FEFG](http://fefg.projectcodex.co/html.html))

## New HTML form features

### Input types

Ordered by improvmments -> new stuff.

* email
* url
* number
* tel
* search
* date
* range
* color

### Helper attributes

* `placeholder` (UX)
* `pattern` (validation)
* `required` (validation)
* `autofocus` (potentially evil)
