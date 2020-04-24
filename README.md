# sass-tools

**Deprecated in favour of PostCSS plugins.**

Sass tools to help with reusability and reducing CSS codebases.

Take a look at [sass-starter](https://github.com/soberwp/sass-starter) to see how it comes together in a starter.

## Installation

Download and `@import` sass-tools;

```shell
yarn add @soberwp/sass-tools
```

```scss
@import "~@soberwp/sass-tools";
```

## Documentation

* [@include util()](https://github.com/soberwp/sass-tools/blob/master/.github/util.md) and [@include util-classes()](https://github.com/soberwp/sass-tools/blob/master/.github/util.md)
  * Define utilities and reuse in classes or create media query prefixed classes.
* [@include fl()](https://github.com/soberwp/sass-tools/blob/master/.github/fl.md)
  * Fluid rem/px values using a ratio between a min and max screen width.
* [@include fs()](https://github.com/soberwp/sass-tools/blob/master/.github/fs.md)
  * Fluid font sizes using a ratio between a min and max screen width.
* [@include mq()](https://github.com/soberwp/sass-tools/blob/master/.github/mq.md)
  * Tiny and smart @media wrapper for faster media query implementation.
