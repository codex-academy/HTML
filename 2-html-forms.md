---
layout: default
title: HTML forms
---

# HTML forms

HTML forms are a way to gather data and send it to a server to be processed. Popular servers are Nginx and Apache. The server will have an application written in Node.JS, Ruby, Python, PHP, or some other language that does the processing.

A `form` element needs an `action` attribute (what URL should the data be sent to?) and a `method` (which HTTP protocol should it use: GET or POST?). A GET is a request for a resource like a web page or a CSS file. A POST is a request to look at the data and respond accordingly.

```html
<form action="/" method="post">
  <!-- Form controls go here -->
</form>
```

## Form controls

Form controls like `input`s are used to enter data, and `button`s are used to submit the form. Here's [an example of a short form](form-1.html).

```html
<form action="/" method="post">
  <input type="text" name="first-name">
  <button type="submit">Send the data</button>
</form>
```

The `name` attribute is the how the piece of data will be identified by the server.

For improved accessibility (identifying what the control is for) and UX (click anywhere on the label to bring focus to the control) you can use `label`s. You can:

* put the `input` inside the `label` or
* put the `label` near the `input` and use a `for` attrbiute on the label that matches the `id` of the `input`.

Here's [a slightly larger example](form-2.html) showing the two ways to use labels, and introducing a new control, `textarea` for larger text.

```html
<form action="/" method="post">
  <label>First Name<br >
    <input type="text" name="first-name" id="first-name">
  </label>
  <br />

  <label for="last-name">Last Name</label><br />
  <textarea name="last-name" id="last-name">
  </textarea>
  <br />

  <button type="submit">Send the data</button>
</form>
```

Other `input`s to look at include `password` and `hidden` types.

### Pick one

When you want your user to pick from some options, rather than type something in, you have a few controls to choose from. If the user should pick more than one thing, use a `checkbox`. If they should pick only one thing, use a `radio` or a `select`

To improve the logical grouping of your form, and improve UX and accessiblity, you can use the `fieldset` element to group controls and the `legend` element to add a description for each group.

Here's [an example](form-3.html) showing these new controls. Note the difference between `name` and `id` on the `checkbox` and `radio` `input`s.

It's a good idea to add `:focus` styles so that you can easily see which form control is active.
