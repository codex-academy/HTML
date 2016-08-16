---
layout: default
title: New HTML elements
unitstandard: 115368
---

# New HTML elements

The new HTML elements offer improved semantics and accessibility. Here are some of them, in the order that you might be likely to use them as you build up a page.

## Structural elements

### &lt;main&gt;

The `<main>` element is used to show to where the main content of a page begins. You can only use it once per page. Before this element existed, we might have used `<div class="main">`

### &lt;article&gt;

The `<article>` element is used for a stand-alone piece of content. Popular examples are blog posts, news items, forum posts, and user comments. The content of an `<article>` must make sense if distributed or reused on its own, for example in syndication. It may or may not have a header and / or footer.

### &lt;section&gt;

The `<section>` element is used for sectioning content (a page or an article) into different topics. A `<section>` might contain paragraphs, articles. A `<section>` must contain a `<header>`. Consider if `<article>`, `<aside>` or `<nav>` would be a more appropriate element choice.

### &lt;nav&gt;

The `<nav>` element is used for major navigation sections of a document. It contains links to other documents, or to other parts of the current document. It could be used for a navigation list, a table of content, previous/next buttons, or breadcrumbs.

### &lt;header&gt;

The `<header>` element is used for the header of the document or section of the document. It can be used multiple times in a document. It usually contains some `<h1>`-`<h6>` elements. It doesn't mark a new section: it functions as the head of the section it's inside.

### &lt;footer&gt;

The `<footer>` element is used for the footer of the document or section of the document. It can be used multiple times in a document. It usually contains metadata. It doesn't mark a new section: it functions as the footer of the section it's inside.

### &lt;aside&gt;

The `<aside>` element has two uses. When inside an article, it's used for content related to the article. When used outside of an article, it's used for content that's separate from the article, but related to the site.

### Example

`new-html-elements.html` is a large example showing how the elements fit together on a page. [View the source](view-source:http://html.projectcodex.co/new-html-elements.html) of the page.

## Images

Every day a wider range of devices with varying screen sizes, and varying support for web technologies, is accessing the web. Two major changes / trends over the past few years have been: the rise of [Responsive web design](http://fefg.projectcodex.co/responsive-web-design.html); the increased use of images.

Images take up a large proportion of the weight of a web page. It’s important to [use the right format](http://designingforperformance.com/optimizing-images/#choosing-an-image-format) for the type of image, and to provide the smallest size that you can using [responsive images](https://responsiveimages.org/). Otherwise we end up sending huge, data-heavy, images to small screen devices that only needed small, data-light(er) images.

We can use the `srcset` and `sizes` attributes for `img`s to provide different size images for different size screens. If you need to show different pictures (such as different crops of the same image) at different screen sizes, look at the `<picture>` element.

The [Responsive Image Breakpoints Generator](http://www.responsivebreakpoints.com/) is a handy tool that generates a set of images for you from one, large, original. You give it a handful of parameters to work with, and it gives you the best spread of images sizes. Choosing images sizes is more complicated than it might seem at first.

### srcset and sizes

The `srcset` and `sizes` attributes are the right choice if you want to provide the same image at different sizes, depending on the screen size.

```html
<img src="small.jpg"
     srcset="large.jpg 1024w, medium.jpg 640w, small.jpg 320w"
     sizes="(min-width: 36em) 33.3vw, 100vw"
     alt="A rad wolf">
```

Example from [responsiveimages.org](https://responsiveimages.org/)

### &lt;picture&gt;

The `<picture>` element is the right choice for "art direction" use cases: where you want to supply different crops of an image (or different images entirely), depending on the screen size.

```html
<picture>
  <source media="(min-width: 40em)"
    srcset="big.jpg 1x, big-hd.jpg 2x">
  <source
    srcset="small.jpg 1x, small-hd.jpg 2x">
  <img src="fallback.jpg" alt="">
</picture>
```

Example from [responsiveimages.org](https://responsiveimages.org/)

If the `<picture>` element is not supported by the browser, the `<img src="fallback.jpg" alt="">` is loaded.

The `<picture>` element can also be used to supply a list of different image formats. You can supply a WebP format image for browsers that support it ([Chrome on desktop, Chrome on Android, and Opera Mini](http://caniuse.com/#feat=webp) at time of writing), and jpg format to everyone else.

### Further reading

* [Responsive Images Done Right: A Guide To picture And srcset](https://www.smashingmagazine.com/2014/05/responsive-images-done-right-guide-picture-srcset/) by Eric Portis, on Smashing Magazine.
* [Responsive Images - The srcset and sizes Attributes](https://bitsofco.de/the-srcset-and-sizes-attributes/).
* [Responsive Images 101, Part 4: Srcset Width Descriptors](https://cloudfour.com/thinks/responsive-images-101-part-4-srcset-width-descriptors/) by Jason Grigsby of Cloud Four.
* [Keeping srcset and sizes under control](https://mattwilcox.net/web-development/keeping-srcset-and-sizes-under-control) by Matt Wilcox.
* [Picturefill](https://scottjehl.github.io/picturefill/) is a JavaScript polyfill that enables `<picture>` support in browsers that don't support it natively. It also has some excellent advice on how to choose [which markup patter to use](https://scottjehl.github.io/picturefill/#examples): `srcset` and `sizes` or `<picture>`.

## Make some changes

Make more updates to your HTML page:

* add several of the new HTML elements;
* add either an `img` using `srcset` and `sizes` or a `picture` element. Or both!
