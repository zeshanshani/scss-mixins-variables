# Sass (SCSS) Mixins & Variables

This package offers various mixins and variables I use all the time in my personal projects.

## Installation

### NPM

1. Install using NPM:

    `npm install --save sass-mixins-variables`

2. Import into your main SCSS file:

    ```SCSS
    // Import Variables (beta)
    @import 'node_modules/sass-mixins-variables/variables';
    // Import Mixins
    @import 'node_modules/sass-mixins-variables/mixins';
    ```

### Overwrite default variables
All the variables mixins use are set with !default so can easily be overwritten.

```SCSS
$primary                 : #00deff
$secondary               : #0050ff

$path--image             : 'assets/images'
$path--font              : 'assets/fonts'

$font__size--root        : 16px

$breakpoint__extra-large : 1400px
$breakpoint__large       : 991px
$breakpoint__medium      : 767px
$breakpoint__small       : 480px
$breakpoint__extra-small : 320px

$container__width        : 1040px
```

## Mixins & Functions
These are the available mixins you can use in your SCSS project.

Name | Type | Description
------ | ----- | -----
spacing | mixin | Creates spacing classes for paddings and margins
bg-img-full | mixin | Expands full background image CSS with background-size.
bg-img-only | mixin | Expands only background-image CSS
all-colors | mixin | Changes the color of all the child themes, including main element and: a, h1-h6
all-headings-colors | mixin | Changes color of all the headings from h1-h6
calc-rem | funciton | Convert pixel into 'rem'. Root size is based on $font__size--root value. Multiple values are accepted, e.g., 10px 20px 10px 20px
calc-em | funciton | Convert pixel into 'em'. Root size is based on $font__size--root value. Multiple values are accepted, e.g., 10px 20px 10px 20px
font-size | mixin | Generates font-size from pixel into 'rem' with 'px' as fallback.
margin | mixin | Generates margin from pixel into 'rem' with 'px' as fallback. e.g., `@include margin( 10px 20px );`
padding | mixin | Generates padding from pixel into 'rem' with 'px' as fallback. e.g., `@include padding( 10px 20px );`
size-rem | mixin | _Description yet to be provided._
width | mixin | Generates width from pixel into 'rem' with 'px' as fallback.
height | mixin | Generates height from pixel into 'rem' with 'px' as fallback.
media | mixin | Opens responsive media.
bp-x-large | mixin | Opens max-width responsive `@media` with size based on $breakpoint__extra-large variable
bp-large | mixin | Opens max-width responsive `@media` with size based defined in $breakpoint__large variable
bp-medium | mixin | Opens max-width responsive `@media` with size based defined in $breakpoint__medium variable
bp-small | mixin | Opens max-width responsive `@media` with size based defined in $breakpoint__small variable
bp-x-small | mixin | Opens max-width responsive `@media` with size based on $breakpoint__extra-small
bp-x-large-min | mixin | Opens min-width responsive `@media` with size based defined in $breakpoint__extra-large-min variable
bp-large-min | mixin | Opens min-width responsive `@media` with size based defined in $breakpoint__large-min variable
bp-medium-min | mixin | Opens min-width responsive `@media` with size based defined in $breakpoint__medium-min variable
bp-small-min | mixin | Opens min-width responsive `@media` with size based defined in $breakpoint__small-min variable
bp-x-small-min | mixin | Opens min-width responsive `@media` with size based defined in $breakpoint__extra-small-min variable
opacity | mixin | Generates opacity CSS with fallback for older browsers.
vertical-center | mixin | Makes child elements vertically centerd. Applied on the parent element. e.g., `@include vertical-center( 100px, '.child-item' );`
position | mixin | Shorthand for position CSS properties.
background | mixin | Shorthand for individual background properties. It's used to avoid using `background` property that overrides all previous background properties.
background-opacity | mixin | Background opacity using SCSS `rgba` function with fallback background color for older browsers. e.g., `@include background-opacity(#000, 0.5);`
per-calc | function | Converts pixel into percentage based on container's size. e.g., `width: per-calc(250px, 1000px);` ---> `width: 25%`
center-with-width | mixin | Center align block-level element using margin-x auto method. e.g., `@include center-with-width( 250px );`
grid | mixin | Generates custom grid classes with row and columns. e.g., `@include grid( $number: 12, $gutter: 30px );`
font-per-base | function | Converts pixel to '%' for font size based on $font__size--root size. e.g., `font-size: font-per-base( $size: 20px, $base: $font__size--root );`
strip-unit | function | Strips a unit from number. e.g., `12px` will become `12`
flex-container | mixin | _Description yet to be provided._
primary-gradient | mixin | _Description yet to be provided._
aspect-ratio | mixin | Convert pixel into aspect ratio in percentage. e.g., `aspect-ratio( 16px 9px );` will convert into `56.25%`
single-button | mixin | _Description yet to be provided._
