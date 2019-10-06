# sass-tools

Four useful tools for creating config and utility first frameworks. 

Take a look at the [sass-starter](https://github.com/soberwp/sass-starter) to see how it comes together.

## Installation

Download and `@import` sass-tools;

```shell
yarn add @soberwp/sass-tools
```

```scss
@import "~@soberwp/sass-tools";
```

## Documentation

* [@include util()](https://github.com/soberwp/util) and [@include util-classes()](https://github.com/soberwp/util)
  * Define utilities and reuse in classes or create media query prefixed classes.
* [@include fl()](https://github.com/soberwp/sass-tools/fl)
  * Fluid rem/px values using a ratio between a min and max screen width.
* [@include fs()](https://github.com/soberwp/sass-tools/fs)
  * Fluid font sizes using a ratio between a min and max screen width.
* [@include mq()](https://github.com/soberwp/sass-tools/mq)
  * Tiny and smart @media wrapper for faster media query implementation.
