# SASS Inline Grid

A small library to create fluid thumbnail or tile grids using inline-block display.

## Usage

Use the mixin on your container (probably a `<ul>`), and tell it which child elements you'd like it to use.

````css
.my-awesome-thumbnail-grid { @include grid-inline(1 2 3, $gutter: 1em, $child: "& > li"); }
````

**Note:** Your container will be given a negative margin on the right side to keep row width even. You may need to wrap it in another container if, for instance, you're using a centered layout.

## Options

### Variables

- `$type-size--default` (number, any unit) Your default font size (default: 1em)
- `$breakpoints` (list) The breakpoints you'd like to use for the grid.

### Mixin parameters

All parameters have default values (and are therefore optional).

- `$cols` (list of numbers) The number of columns to create at each breakpoint. Best practice is to go from smallest to largest screen (ie, mobile first). (default: 1 2 3)
- `$gutter` (number, any unit) The width of the gutters between each column. (default: 0)
- `$child` (css selector) The child elements of the grid (default: "& > li").

