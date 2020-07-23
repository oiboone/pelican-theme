# Using sass

Use command line:

```bash
sass --watch --no-source-map scss:css
```

from the static directory to automatically convert scss files in the static/scss directory to css files in the static/css directory whenever they change.

same command without --watch does conversion once.

# Features

## variables

Sass uses $var: to signify variables definitions and $var for use.

Sass variables can be used in odd places using interpolation. e.g. 

 #{$top-or-bottom}: 0;

sets top=0 or bottom=0 depending on teh value of top-or-bottom.

unit arithmetic is available, so you can write $width * 1px;

## Nesting of selectors

## Partials/Modules

filenames start with _ like _typography.scss
they are not generated into css files automatically but included in other files via 
@use typography as *

## Mixins

Functions that allow you to simplify css code by reducing redundancy:

```scss
@mixin transform($property) {
  -webkit-transform: $property;
  -ms-transform: $property;
  transform: $property;
}
.box { @include transform(rotate(30deg)); }
```

## Inheritance and placeholder classes 

