# Code Refactor in HTML and CSS: A Review of Semantic HTML

## Description 

In this assignment, we reviewed and refactored existing code for a static webpage and added appropriate semantic HTML elements.


## Table of Contents

* [Updates to HTML](#updates-to-html)
* [Updates to CSS](#updates-to-css)


### Updates to HTML

There were many `div` elements that were referenced as classes or some sort of ID that could be better utilized with semantic HTML elements.  The `div` elements replaced were:
* `<div class="header">` --> `<header>`
* `<div>` --> `<nav>`
* added a `<main>` element between header and footer
* `<div class="content">` --> `<main>`
* `<div class="search-engine-optimization">` --> `<section>`
* `<div class="online-reputation-management">` --> `<section>`
* `<div class="social-media-marketing">` --> `<section>`
* `<div class="benefits">` --> `<aside>`
* `<div class="benefits-lead">` --> `<section>`
* `<div class="benefits-brand">` --> `<section>`
* `<div class="benefits-cost">` --> `<section>`
* `<div class="footer">` --> `<footer>`

Making these updates gave the `<body>` of the page the following structure:

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


### Updates to CSS



### Review of Refactor



## Installation

What are the steps required to install your project? Provide a step-by-step description of how to get the development environment running.


## Usage 

Provide instructions and examples for use. Include screenshots as needed. 

To add a screenshot, create an `assets/images` folder in your repository and upload your screenshot to it. Then, using the relative filepath, add it to your README using the following syntax:

```md
![alt text](assets/images/screenshot.png)
```


## Credits

List your collaborators, if any, with links to their GitHub profiles.

If you used any third-party assets that require attribution, list the creators with links to their primary web presence in this section.

If you followed tutorials, include links to those here as well.


## License

The last section of a good README is a license. This lets other developers know what they can and cannot do with your project. If you need help choosing a license, use [https://choosealicense.com/](https://choosealicense.com/)


---

🏆 The sections listed above are the minimum for a good README, but your project will ultimately determine the content of this document. You might also want to consider adding the following sections.

## Badges

![badmath](https://img.shields.io/github/languages/top/nielsenjared/badmath)

Badges aren't _necessary_, per se, but they demonstrate street cred. Badges let other developers know that you know what you're doing. Check out the badges hosted by [shields.io](https://shields.io/). You may not understand what they all represent now, but you will in time.

## Features

If your project has a lot of features, consider adding a heading called "Features" and listing them there.

## Contributing

If you created an application or package and would like other developers to contribute it, you will want to add guidelines for how to do so. The [Contributor Covenant](https://www.contributor-covenant.org/) is an industry standard, but you can always write your own.

## Tests

Go the extra mile and write tests for your application. Then provide examples on how to run them.

---

© 2022 Trilogy Education Services, LLC, a 2U, Inc. brand. Confidential and Proprietary. All Rights Reserved.
