# scss-mq

Tiny and smart media query wrapper for faster coding.

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

## Usage

The mixin uses map `$breakpoints` by default;

```scss
@include mq(md) {}
```

You can also just pass in a custom rem/px value;

```scss
@include mq(100rem) {}
```

**Edge-cases**

While it is always encourged to develop from small screen sizes upwards, in some cases you may require `@media (max-width: $breakpoint)`.

```scss
@include mq-down(md) {}
```
