

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



#### Spacing 

Spacing is based on the value of `$base-space-value` (arcibaldo.variables.scss) and each spacing class (margin and padding) can be extended 
50 times the value of `$base-space-value`. <br>
*Eg. Having a `$base-space-value` set to 2px (`$base-space-value: 2px`),the the maximum spacing will solve at the dimension of 100px
`.mb50` will output `margin-bottom: 100px`*

 
syntax | Base | Modifiers
------------ |------------ | -------------
short | padding, margin | auto, a, h, v, t, r, b, l

At the moment just a short syntax for spacing is implemented, in a long syntax the modifiers resolves as auto, all, horizontal, vertical, top, right, bottom, left.

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

