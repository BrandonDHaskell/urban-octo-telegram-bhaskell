# Code Refactor in HTML and CSS: A Review of Semantic HTML

## Description 

In this assignment, I reviewed and refactored existing code for a static webpage and added appropriate semantic HTML elements.  The core of the module was on HTML and CSS formatting and use.  For the assignment, I focused on updating the HTML fist to try and consoldiate as much as possible, as well as identify any potential semantic updates that might be needed.  This set the stage for CSS updates that ultimately made the webpage more flexible and rhobust for future updates.

In addition to the HTML and CSS updates, I also added functionality for small view ports using flexbox properties in CSS.  I also added contextual highlighting to the navbar links using pseudo-element selectors in CSS.

Checkout the live updates [here](https://bhaskell7901.github.io/urban-octo-telegram-bhaskell/)!


## Table of Contents

* [Updates to HTML](#updates-to-html)
* [Updates to CSS](#updates-to-css)
* [Bonus Items](#bonus-items)
* [Screenshots](#Screenshots)


## Updates to HTML

There were many `div` elements that were referenced as classes or some sort of ID that could be better utilized with semantic HTML elements.  The `div` elements replaced were:
| `<div>` Element | Semantic Replacement |
|-----------------|----------------------|
| `<div class="header">` | `<header>` |
| `<div>` | `<nav>` |
| `<div class="content">` | `<article>` |
| `<div class="search-engine-optimization">` | `<section>` |
| `<div class="online-reputation-management">` | `<section>` |
| `<div class="social-media-marketing">` | `<section>` |
| `<div class="benefits">` | `<aside>` |
| `<div class="benefits-lead">` | `<section>` |
| `<div class="benefits-brand">` | `<section>` |
| `<div class="benefits-cost">` | `<section>` |
| `<div class="footer">` | `<footer>` |

Additionally, I also added a `<main>` element between header and footer to wrap the `<article>` and `<aside>` elements.

Making these updates took the HTML from this structure:
```HTML
<body>
    <div class="header">
        <div></div>
    </div>
    <div class="content"></div>
    <div class="benefits"></div>
    <div class="footer"></div>
</body>

```

to this structure:
```HTML
<body>
    <header>
        <nav></nav>
    </header>
    <main>
        <article></article>
        <aside></aside>
    </main>
    <footer></footer>
</body>

```

The `<article>` and `<aside>` elements were further separated with `<section>` elements.  Making these updates simplified the CSS by reducing the need for references to classes and IDs and made the HTML more semantically readible.  Removing the reliance on the IDs reduced code duplication in the CSS file.

Additional updates were made to the `<img>` tags to include an `alt` property for accessibility.


## Updates to CSS

In the HTML, there were multiple elements with unique class properties values that were being referenced to set generic property values.  This created multiple instances of triplicated code!  These were consolidated

Several class selectors were converted to element selectors.  Below is a list of those converted to reference the semantic HTML elements that were added:
| Previous Selector | Converted To |
|-------------------|--------------|
| .header | header |
| .content | article |
| .benefits | aside |

There were also multiple selectors that implemented the same properties across multiple elements of the same type.  These were consolidated as follows:

| Previous Selectors | Consolidated Selector |
|----------|---------------|
| .search-engine-optimization, .online-reputation-management, .social-media-marketing | article section |
| .search-engine-optimization h2, .online-reputation-management h2, .social-media-marketing h2 | article section h2 |
| .search-engine-optimization img, .online-reputation-management img, .social-media-marketing img | article section img |
| .benefit-lead, .benefit-brand, .benefit-cost | aside section |
| .benefit-lead h3, .benefit-brand h3, .benefit-cost h3 | aside section h3 |
| .benefit-lead img, .benefit-brand img, .benefit-cost img | aside section img |

In addition to the clean up, I also added flexbox functionality to the CSS


## Bonus Items


### Flexbox
I added additonal functionality that allows the the `<aside>` elements to wrap around the `<article>` element allowing for more flexibility in smaller viewports.  Using `<main>` as the container and the `<article>` and `<aside>` elements as the items to flex.  As the webpage shrinks in width, eventually the `<aside>` element wrap below the `<article>` element.


### Pseudo Elements
I also enabled contextual highlighting for the navbar items using style properties on the `a:hover` pseudo element.  This will provide feedback to the user about the links in the navbar.

## Screenshots

*Large screen view*

![large screen view](https://github.com/bhaskell7901/urban-octo-telegram-bhaskell/blob/main/assets/images/ReferenceImages/urban-octo-full-screen-view.png)

-----

*Small screen view*

![large screen view](https://github.com/bhaskell7901/urban-octo-telegram-bhaskell/blob/main/assets/images/ReferenceImages/urban-octo-small-screen-view.png)