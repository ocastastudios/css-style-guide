# CSS Style Guide

This is a guide for writing consistent and aesthetically pleasing CSS code. It is inspired by what is popular within the community.

This guide is inspired by the following style guides:

* [GitHub](https://github.com/styleguide/css)
* [Idiomatic CSS](https://github.com/necolas/idiomatic-css)
* [CSS Wizardry](http://csswizardry.com/2012/04/my-html-css-coding-style/)
* [ThinkUp](https://github.com/ginatrapani/ThinkUp/wiki/Code-Style-Guide:-CSS)
* [Google](http://google-styleguide.googlecode.com/svn/trunk/htmlcssguide.xml)

## Spacing

* Use soft-tabs with a 2 space indent.
* Put spaces after `:` in property declarations.
* Put spaces before `{` in rule declarations.
* Put line breaks between rulesets.
* When grouping selectors, keep individual selectors to a single line.
* Place closing braces of declaration blocks on a new line.
* Each declaration should appear on its own line for more accurate error reporting.
* Include a space after each comma in comma-separated property or function values.

## Formatting

* Use hex color codes `#000` unless using `rgba()`.
* When denoting color using hexadecimal notation, use all capital letters. Both three-digit and six-digit hexadecimal notation are acceptable; if it’s possible to specify the desired color using three-digit hexadecimal notation, do so as you’ll save the end-user a few bytes of download time.
* Avoid specifying units for zero values, e.g., `margin: 0;` instead of `margin: 0px;`, *where allowed*.
* Strive to limit use of shorthand declarations to instances where you must explicitly set all the available values.
* Include a semi-colon at the end of the last declaration in a declaration block.
* Put declarations in alphabetical order in order to achieve consistent code in a way that is easy to remember and maintain (ignoring vendor-specific prefixes for sorting purposes).

## Exceptions and slight deviations

Long, comma-separated property values - such as collections of gradients or
shadows - can be arranged across multiple lines in an effort to improve
readability and produce more useful diffs. There are various formats that could
be used; one example is shown below.

```css
.selector {
    background-image:
        linear-gradient(#fff, #ccc),
        linear-gradient(#f3c, #4ec);
    box-shadow:
        1px 1px 1px #000,
        2px 2px 1px 1px #ccc inset;
}
```

Write vendor prefixes so that the values all line up vertically; it allows you to can scan them quicker (to check they’re all identical) and to alter them all in one go if the editor supports typing in columns.

```css
body {
  -webkit-box-sizing: border-box;
     -moz-box-sizing: border-box;
          box-sizing: border-box;
}
```

## Hacks

Avoid user agent detection as well as CSS "hacks". Consider them a last resort. Instead try to use conditional comments when possible.

## Inclusion

Do not write inline styles or embedded styles unless unavoidable. Inlining or embedding styles is most likely avoidable.

For performance reasons (see [Steve Souder’s blog](http://www.stevesouders.com/blog/2009/04/09/dont-use-import/)), always link to external stylesheets using the `<link>` syntax rather than the `@import` syntax.

## Naming convention

Use BEM naming convention.

Useful resources: [Nicolas Gallagher](http://nicolasgallagher.com/about-html-semantics-front-end-architecture/) and [CSS Wizardry](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/)

Use the double separator (`__` and `--`) for class.
