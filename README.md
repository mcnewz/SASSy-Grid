# SASSy Grid
CSS Grid system written in SASS

### CDN
Include in the `<head>` of your document.
```html
<link rel="stylesheet" href="https://cdn.rawgit.com/bkwebster/SASSy-Grid/c1573ab0/dist/grid.min.css">
```

## Usage

Use the class name `grid-{number of columns}` to set the number of columns.  By default, the maximum column count is twelve, but this can be [configured in grid.sass](#configure).
```html
<div class="grid-5">
...
```

Use the class name `col-{number of columns to span}` to set the column span to individual grid items.
```html
<div class="grid-5">
  <div class="col-2">
    I span 2 of 5 columns.
  </div>
  <div class="col-3">
    I span 3 of 5 columns.
  </div>
  ...
```

Use the class name `col-pos-{column position}` to assign a specific column position to a grid item.
```html
<div class="grid-5">
  <div class="col-2 col-pos-2">
    I span 2 of 5 columns, starting on column 2.
  </div>
  <div class="col-1 col-pos-5">
    I span 1 of 5 columns, starting on column 5.
  </div>
  ...
```

Use the class name `row-{number of rows to span}` to set the row span to individual grid items.
```html
<div class="grid-5">
  <div class="row-2">
    I span 2 rows.
  </div>
  <div class="row-3">
    I span 3 rows.
  </div>
  ...
```

## Customize

### Configure
Configure the grid by editing the variables at the top of the [grid.sass](src/grid.sass) file.

```sass
// Breakpoints
$sm:    "screen and (max-width: 32em)"
$md:    "screen and (max-width: 64em)"
$lg:    "screen and (max-width: 120em)"
$xl:    "screen and (min-width: 120em)"

// Grid
$gap:     10px
$columns: 12
```

### Compile CSS
Compile the CSS using [SASS commands](https://sass-lang.com/documentation/file.SASS_REFERENCE.html#using_sass)

#### Compile
```
sass src/grid.sass dist/grid.css
```

#### Compile and Watch

```
sass --watch src/grid.sass:dist/grid.css
```

#### Minify

```
sass src/grid.sass dist/grid.min.css --style compressed
```

#### Minify and Watch

```
sass --watch src/grid.sass:dist/grid.min.css --style compressed
```

## Include
Include the CSS in the `<head>` of your document.

#### Local
```html
<link rel="stylesheet" href="dist/grid.css">
```
