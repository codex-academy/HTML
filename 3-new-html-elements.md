---
layout: default
title: New HTML elements
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

* `picture` and `srcset` (responsive) (look at [HTML of FEFG](http://fefg.projectcodex.co/html.html))
