# 12-Column-Grid-Framework & CSS-Reset
The project includes a _12-column grid-framework_ & _css reset._

##### Built With
+ HTML5
+ CSS3

# Author
+ Saintaze [https://github.com/saintaze/](https://github.com/saintaze/)

## 12 Column Grid Framework

It is a simple 12 column grid layout system, inspired by bootstrap. 
- It takes mobile first approach.
- It allows to define 12 column grid for different screen sizes.
- It allows to define offsets for different screen sizes.
- Its allows to customize the total number of columns (12 default), vertical and horizontal gutter (1.5rem default for both). 

### Getting Started

Start by including `grid.css` file 

```html
<link rel="stylesheet" href="grid.css">
```

### Create Container

In order to use the grid system, the grid must be inside one of the two container classes.

#### Fixed Width container (size changes at breakpoints)
&nbsp;
 You can create a fixed width container, that will change width at different breakpoints.

```html
<div class="container"></div>
```
#### Fluid Width Container
&nbsp;
 You can create a fluid container, that will always be 100% width of its parent.

```html
<div class="container-fluid"></div>
```

### Create Row

The row can be created with `.row` class. Row must be inside of the `.container` or `.container-fluid` class. All columns are defined inside of a row.

```html
<div class="container">
    <div class="row"></div>
</div>
```

### Create Columns

This grid system supports **12 column grid** by default. But it can be customized to your needs. 

#### Change No. Of Columns In The Grid
&nbsp;
All you have to do is change the value of `--total-columns` variable inside of `.grid.css` to the number of columns you like.

```css
:root{
    --total-columns: 12;  /* default */
    --total-columns: 16;  /* customized */
}
```
#### Change Vertical or Horizontal Gutter Size
&nbsp;
All you have to do is change the value of `--horizontal-gutter` or`--vertical-gutter` variable inside of `.grid.css` to the `rem` size you like.

```css
:root{
    --horizontal-gutter: 1.5rem;  /* default */
    --horizontal-gutter: 2rem;  /* customized */
    
    --vertical-gutter: 1.5rem;  /* default */
    --vertical-gutter: 2rem;  /* customized */
}
```
#### Equal Width Column At All Screen Sizes
&nbsp;
You can create an equal width column at all screen sizes by simply using `.col` class
```html
<div class="container">
  <div class="row">
    <div class="col">col-1</div>
    <div class="col">col-2</div>
  </div>    
</div>
```
#### Defining Column Size At Mobile Screen (< 576px)
&nbsp;
You can define the width of a column at mobile screens by defining column size `{1-12}` after `.col-` class as `col-{1 to 12}`.
_Note: For the grid to work properly, the number of columns must add up to 12. Or total column number when grid is customised._ 
```html
<div class="container">
  <div class="row">
    <div class="col-7"></div>
    <div class="col-3"></div>
    <div class="col-2"></div>
  </div>    
</div>
```
#### Defining Column Size With Breakpoints (> 576px)
&nbsp;
This grid system uses following media breakpoints.

`sm (> 576px)`
`md (> 768px)`
`lg (> 992px)`
`xl (> 1200px)`

_Note: For screen size below `sm (< 576px)` no breakpoint label is required._

You can define the width of a column at differnt breakpoints `(> 576px)` by using breakpoint label `sm, md, lg, xl` after `.col-` and before size of column `{1-12}`, such as `col-sm-8`

_Note: Whatever the column size, it will be applied from that screen size and up._ 
```html
<div class="container">
  <div class="row">
    <div class="col-sm-12 col-md-10 col-lg-8 col-xl-6">col-1</div>
    <div class="col-sm-12 col-md-2 col-lg-4 col-xl-6">col-2</div>
  </div>
</div>
```
### Create Column Offset
You can define the column offset size, by which column should be moved to the right side of a row.
#### Defining Column Offset At Mobile Screen (< 576px)
&nbsp;
You can define a column offset size at a mobile screen `(< 576px)` with a class `col-offset-{1-11}`
```html
<div class="container">
  <div class="row">
    <div class="col-6 col-offset-3"></div>
  </div>    
</div>
```

#### Defining Column Offset With Breakpoints (> 576px)
&nbsp;
You can define the offset size at differnt breakpoints `(> 576px)` by using breakpoint label `sm, md, lg, xl` after `.col-offset-` and before size of column `1-11`. Such as `col-offset-md-5`

```html
<div class="container">
  <div class="row">
    <div class="col-md-10 col-offset-md-2</div>
  </div>
</div>
```


## CSS Reset

`reset.css` is a very basic reset, that includes following.
-  Box-sizing for all elements set to `border-box`
-  Root font-size set to `10px`
-  Font family set to `Raleway` (default). Can be switched to `Roboto`
-  Overall font color set to `#333`
-  Font size set for `h1`, `h2`, `h3`, `h4`, `h5`, `h6`
-  Margin and Padding set for all lists `ol`, `ul`, `dl`
-  Unhovered and hovered color for `<a>` tag
- Three contextual text color classes `.text-primary`, `.text-success` and  `.text-danger` 

### Getting Started

Start by including `reset.css` file 

```html
<link rel="stylesheet" href="reset.css">
```
## Grid-Debug
`grid-debug.css` adds row and column background color to visually see and debug rows and columns.

### Getting Started

Start by including `grid-debug.css` file 

```html
<link rel="stylesheet" href="grid-debug.css">
```



