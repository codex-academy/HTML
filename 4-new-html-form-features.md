---
layout: default
title: New HTML form features
---

# New HTML form features

## Input types

A new set of `input` types were added to HTML to offer improved semantics, accessibility, and User Experience (UX). They do this mostly by replacing custom, usually heavy, JavaScript solutions with things closer to the browser.

### Make things a little better

`email` and `url` `input` types are for email addresses and web addresses, respectively. They offer validation, helping users enter correct information.

`number` and `tel` are for numbers and telephone numbers. `number` can have `min`, `max`, and `step` attributes. These also offer validation, helping users enter correct information. These are particularly noticable on mobile devices, where the displayed keyboard changes: `number` or `tel` can trigger the numerical keyboard rather than the standard alphanumeric one.

Here's an example with the new input types: [form-easier.html](form-easier.html)

```html
<form action="4-new-html-form-features.html" method="post">
  <fieldset>
      <legend>Your info</legend>

      <label>Your email<br />
        <input type="email" name="your-email">
      </label>
      <label>Your URL<br />
        <input type="url" name="your-url" value="https://">
      </label>
  </fieldset>

  <fieldset>
      <legend>Number and numbers</legend>

      <label>Pick an even number between 0 and 10<br />
          <input type="number" name="your-number" min="0" max="10" step="2">
      </label>

      <label>Your phone number<br />
        <input type="tel" name="your-phone-number">
      </label>
  </fieldset>

  <button type="submit">Send the data</button>
</form>
```

* What happens if you don't enter a correctly formatted email address or URL?
* Can you enter "3" into the "Pick an even number" field and submit the form?
* Why did we add `value="https://"`? What happens if we remove it?

### Going native

Some of the new HTML form elements "pave the cowpaths" and give the browser native ways of providing some of the features that used to only be possible with lots of JS.

JS date pickers can be replaced by `<input type="date" />`. JS sliders can be replaced by `<input type="range" />`. Both of these accept `min` and `max` attributes, and range accepts `step`. Elaborate JS colour pickers can be replaced by `<input type="color" />`.

JS is still needed to for some client-side updates (such as live-updating the selected value of a `range`), but the form control itself comes from the browsers. This is better because these types of inputs can now render more consistently across sites in terms and look & feel and operation. It also reduces the amount of code you need to write since the browser is handing the form control for you.

Here's an example these new controls: [form-going-native.html](form-going-native.html).

```html
<form action="4-new-html-form-features.html" method="post">

  <label>Pick a date in January 2017<br />
    <input type="date" min="2017-01-01" max="2017-01-31">
  </label>

  <label>Pick a thingy<br />
      <input type="range" min="0" max="10" step="2" >
  </label>

  <label>Pick a colour<br />
      <input type="color" value="#8bc53f">
  </label>

  <button type="submit">Send the data</button>
</form>
```

* What do the `min` and `max` attributes on the `date` do? Can you pick a date in 2016?
* What's going on with the `range`? Why can't we see what the selected value is?
* What does the `value` on `color` do? What happens if we change it to `#789abc`?

## Helper attributes

On top of the new `input` `type`s, some new attributes where added to further help with UX.

The `required` attribute is probably the most widely used. It replaces JS checks for whether or not a field has been filled out.

The `placeholder` attribute adds "ghost text" as an extra hint to the user. This should only be used as additional information, and usually takes the form of an example. The `input`s label should make the desired input clear to the user.

The `pattern` attribute allows for validation on the input based on the supplied a Regular Expression. RegEx is very powerful, so this can be very useful. It can also be very complicated, though!

Another useful, but potentially evil attribute is `autofocus`. This brings the user's focus of the page to the `input` with the `autofocus` attribute on. This can be more annoying than helpful, so be very sure that it will help your users more than hinder them!

Here's an example showing the new attributes: [form-helper-attributes.html](form-helper-attributes.html).

```html
<form action="4-new-html-form-features.html#helper-attributes" method="post">

  <label>You <strong>must</strong> fill in this one.<br />
    <input type="text" name="must" required>
  </label>

  <label>What's your favourite fruit?<br />
    <input type="text" name="fruit" placeholder="Apple, banana, pear?">
  </label>

  <label>What's your favourite number between 0 and 9?<br />
    <input type="number" name="favourite-number">
  </label>

  <label>Potentially evil! See how the cursor is in this input already? Start typing to see!<br />
    <input type="text" name="potentially-evil" autofocus>
  </label>

  <button type="submit">Send the data</button>
</form>
```
