

## Arcibaldo Mixins:
- 1.0 Breakpoints
- 2.0 Size
- 3.0 Geometry

## Arcibaldo Theme:
- 1.0 Layout
  - 1.1 Layout FlexBox
- 2.0  Spacing
- 3.0 Typography
- 4.0 Buttons
- 5.0 Shadings
 


### What you will find inside Arcibaldo?

```
├── css
│   ├── arcibaldo.css
│   ├── arcibaldo.css.map
│   └── arcibaldo.min.css
└── scss
    ├── arcibaldo.scss
    ├── arcibaldo.variables.scss
    ├── _functions.scss
    ├── mixins
    │   ├── _breakpoints.scss
    │   ├── _geometry.scss
    │   └── _size.scss
    ├── _mixins.scss
    └── theme
        ├── _buttons.scss
        ├── _geometry.scss
        ├── _layout-flexbox.scss
        ├── _layout.scss
        ├── _shadings.scss
        ├── _spacing.scss
        └── _typography.scss
```

#### Layout

Keep your containers in a `.fix-container` to make sure they do not exceed a certain max-width based on the value of `$flex-fix-container-width` (arcibaldo.variables.scss).

##### width and height based on percentages (%)

syntax | base | values | example
------------ | ------------- | ------------- | -------------
short | w | 1 - 100 | w_1
short | h | 1 - 100 | h_1


#### Layout Flexbox


- Containers Block level: 

syntax | base | example
------------ | ------------- | -------------
short | rc | rc
long | row__container | row_container
short | cc | cc
long | col__container | col_container

- Flex Line Wrapping:
 
syntax | base | modifiers | example
------------ | ------------- | ------------- | -------------
short | f | wrap, nowrap, wrap-reverse | f_wrap-reverse

- Items:
 
syntax | base | values | example
------------ | ------------- | ------------- | -------------
short | f | 1 - 100 | f_1


- Axis Alignment:

syntax | base | modifiers | values | example
------------ | ------------- | ------------- | ------------- | -------------
short | f | jc | fs, fe, c, sb, sa | f_jc_fs
long | f | justify-content | flex-start, flex-end, center, space-between, space-around | f_jc_flex-start

- Cross-axis Alignment

syntax | base | values | example
------------ | ------------- | ------------- | -------------
short | f | 


#### Spacing 

Spacing is based on the value of `$base-space-value` (arcibaldo.variables.scss) and each spacing class (margin and padding) can be extended 
50 times the value of `$base-space-value`. <br>
*Eg. Having a `$base-space-value` set to 2px (`$base-space-value: 2px`),the the maximum spacing will solve at the dimension of 100px
`.mb_50` will output `margin-bottom: 100px`*

 
syntax | base | modifiers | values | example
------------ |------------ | ------------- | ------------- | -------------
short | p, m | auto, a, h, v, t, r, b, l | 1 - 50 | mb_1
long | padding, margin | auto, all, horizontal, vertical, top, right, bottom, left | |  

> At the moment just a short syntax for spacing is implemented.

### Contribute to Arcibaldo:

### Structure /src
```
── scss
    ├── arcibaldo.scss		        // Arcibaldo v.1
    ├── arcibaldo.variables.scss	// required: Core variables of Arcibaldo
    ├── _functions.scss		        // required: Core functions of Arcibaldo
    ├── mixins
    │   ├── _breakpoints.scss		// mixins for screen size and orientation breakpoints
    │   ├── _geometry.scss		// mixins for three shapes: square, rectangle, circle
    │   └── _size.scss			// mixins for managing sizes
    ├── _mixins.scss
    └── theme
        ├── _buttons.scss
        ├── _geometry.scss		// Geometry classes
        ├── _layout-flexbox.scss	// Layout Flex Box v.1
        ├── _layout.scss		// Layout
        ├── _shadings.scss		// Shadow effects
        ├── _spacing.scss		// Padding and margin
        └── _typography.scss
```

