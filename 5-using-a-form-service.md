---
layout: default
title: Using a form service
---

# Using a form service

If for some reason you can't access a server but you need to collect form data (for example, you're using [GitHub Pages](https://pages.github.com/) to host a site), you can use an external service.

[Formspree](https://formspree.io/) processes the data for you and sends it on to an email address that you supply. Have a look at [this example](formspree.html) and the [Get Started](https://formspree.io/#getstarted) section of the Formspree site.

Change the `action` in the example to include your own email address and give it a go.

```html
<form action="https://formspree.io/you@projectcodex.co"
method="POST">

    <input type="hidden" name="_subject" value="New submission!" />
    <input type="hidden" name="_next" value="" />

    <label>What is The Best Of Things?<br />
        <input type="text" name="best-of-things">
    </label>

    <label>Your email<br />
        <input type="email" name="_replyto"/>
    </label>

    <button type="submit">Spree!</button>
</form>
```

## Make some changes

Make more updates to your HTML page:

* uses formspree.io in your form's action, linked to the your email address;
* confirm your email address with formspree.io by submitting the form.
