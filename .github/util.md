# @include util() and util-classes()

Create media query prefixed utility classes and include utilities in classes.

## Setup

Begin by creating a `$breakpoints` map;

```scss
// rem or px allowed
$breakpoints: (
  sm: 36rem,
  md: 48rem,
  lg: 62rem,
  xl: 75rem,
  xx: 87.5rem,
);
```

Next up, create a `$utils` map with some utilities, such as commonly used flex utils;

```scss
$utils: (
  flex: (display: flex),
  flex-row: (flex-direction: row),
  flex-row-reverse: (flex-direction: row-reverse),
  flex-col: (flex-direction: column),
  flex-col-reverse: (flex-direction: column-reverse),
  flex-wrap: (flex-wrap: wrap),
  flex-no-wrap: (flex-wrap: nowrap),
  flex-wrap-reverse: (flex-wrap: wrap-reverse),
  items-stretch: (align-items: stretch),
  items-start: (align-items: flex-start),
  items-center: (align-items: center),
  items-end: (align-items: flex-end),
  items-baseline: (align-items: baseline),
  content-start: (align-content: flex-start),
  content-center: (align-content: center),
  content-end: (align-content: flex-end),
  content-between: (align-content: space-between),
  content-around: (align-content: space-around),
  self-auto: (align-self: auto),
  self-start: (align-self: flex-start),
  self-center: (align-self: center),
  self-end: (align-self: flex-end),
  self-stretch: (align-self: stretch),
  justify-start: (justify-content: flex-start),
  justify-center: (justify-content: center),
  justify-end: (justify-content: flex-end),
  justify-between: (justify-content: space-between),
  justify-around: (justify-content: space-around),
);

@include util-add($utils);
```

## Usage

#### `@include util()`

If you have used [tailwindcss](https://tailwindcss.com/), then you have likely used `@apply`. This works in the same way by including your util properties.

```scss
.flex-wrap-center-between {
  @include util(flex flex-wrap items-center justify-between);
}
```

#### `@include util-classes()`

By default, `util-classes()` will create all utils added to `util-add()`. 

```scss
@include util-classes();
```

This will generate the following classes, `flex sm:flex md:flex lg:flex xl:flex xx:flex` and so on. 

**Edge cases**

You can also pass in custom maps for both utils and breakpoints;

```scss
$custom-utils: (
  mx-auto: (margin-left: auto, margin-right: auto),
);

$custom-breaks: (
  w100: 100rem, 
  w200: 100rem
);

@include util-classes($custom-utils, $custom-breaks);
```

This will generate the following classes, `mx-auto w100:mx-auto w200:mx-auto`.
