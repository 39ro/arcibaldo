---
layout: default
title: Arcibaldo v1.0
---

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



**Arcibaldo Mixins:**
- 1.0 Breakpoints
- 2.0 Size
- 3.0 Geometry

**Arcibaldo Theme:**
- 1.0 Layout
  - 1.1 Layout FlexBox
- 2.0  Spacing
- 3.0 Typography
- 4.0 Buttons
- 5.0 Shadings
 
 
 
##### Import all Arcibaldo:

```
// Arcibaldo
@import '~node_modules/arcibaldo/scss/arcibaldo';
```


##### Import just what you need from Arcibaldo:

```
// Arcibaldo variables
@import '~node_modules/arcibaldo/scss/arcibaldo.variables';

// Custom variables: will overwrite Arcibaldo default variables
$base-space-value: 10px;

// Required
@import '~node_modules/arcibaldo/scss/functions';
@import '~node_modules/arcibaldo/scss/mixins';

// Optional
@import '~node_modules/arcibaldo/scss/theme/layout';
@import '~node_modules/arcibaldo/scss/theme/layout-flexbox';
@import '~node_modules/arcibaldo/scss/theme/spacing';
@import '~node_modules/arcibaldo/scss/theme/typography';
@import '~node_modules/arcibaldo/scss/theme/buttons';
@import '~node_modules/arcibaldo/scss/theme/shadings';
@import '~node_modules/arcibaldo/scss/theme/geometry';
```




## Layout

Keep your top level container wrapped in a `.fix-container` to make sure the flexed items do not exceed a certain max-width based on the value of `$flex-fix-container-width` (arcibaldo.variables.scss).


##### width / height based on percentages (%)


| **syntax**    | **base**      |**values**| **example** |
| ------------- |:-------------:|:--------:| -----------:|
| **short**     | w             | 1 - 100  | w_1         |
| **short**     | h             | 1 - 100  | h_1         |



### Layout: Flexbox


##### Containers Block level: 

| **syntax**    | **base**      | **example**   |
| ------------- |:-------------:| -------------:|
| **short**     | rc            | rc            |
| **long**      | row-container | row-container |
| **short**     | cc            | cc            |
| **long**      | col-container | col-container |

##### Flex Line Wrapping:
 
| **syntax**    | **base**      |**modifiers**               | **example**         |
| ------------- |:-------------:|:--------------------------:| -------------------:|
| **short**     | flex          | wrap                       | flex_wrap           |
| **short**     | flex          | nowrap                     | flex_wrap-nowrap    |
| **short**     | flex          | wrap-reverse               | flex_wrap-reverse   |

##### Items:

| **syntax**    | **base**      |**modifiers**               | **values**     | **example**         |
| ------------- |:-------------:|:--------------------------:|:---------------| -------------------:|
| **short**     | flex          |                            | 1 - 100        | flex_1              |
| **short**     | flex          | shrink                     | 1 - 100        | flex_shrink_1       |

##### Axis Alignment:

| **syntax**    | **base**        |**modifiers**               | **example**                   |
| ------------- |:---------------:|:--------------------------:| -----------------------------:|
| **short**     | jc              | fs                         | jc_fs                         |
| **short**     | jc              | fe                         | jc_fe                         |
| **short**     | jc              | c                          | jc_c                          |
| **short**     | jc              | sb                         | jc_sb                         |
| **short**     | jc              | sa                         | jc_sa                         |
| **long**      | justify-content | flex-start                 | justify-content-flex-start    |
| **long**      | justify-content | flex-end                   | justify-content-flex-end      |
| **long**      | justify-content | center                     | justify-content-center        |
| **long**      | justify-content | space-between              | justify-content-space-between |
| **long**      | justify-content | space-around               | justify-content-space-around  |


##### Cross-axis Alignment

@todo: work in progress


#### Spacing 

Spacing is based on the value of `$base-space-value` (arcibaldo.variables.scss) and each spacing class (margin and padding) can be extended 
50 times the value of `$base-space-value`. <br>
*Eg. Having a `$base-space-value` set to 2px (`$base-space-value: 2px`),the the maximum spacing will solve at the dimension of 100px
`.mb_50` will output `margin-bottom: 100px`*


| **syntax**    | **base**                                       |**modifiers**  | **values**  | **example**         |
| ------------- |:----------------------------------------------:|:-------------:|:------------| -------------------:|
| **short**     | pt, pr, pb, pl, <br> p-horizontal, p-vertical  | auto          |             | pt_auto             |
| **short**     | p-all                                          |               | 1 - 50      | p-all_1             |
| **short**     | p-horizontal                                   |               | 1 - 50      | p-horizontal_1      |
| **short**     | p-vertical                                     |               | 1 - 50      | p-vertical_1        |
| **short**     | pt                                             |               | 1 - 50      | pt_1                |
| **short**     | pr                                             |               | 1 - 50      | pr_1                |
| **short**     | pb                                             |               | 1 - 50      | pb_1                |
| **short**     | pl                                             |               | 1 - 50      | pl_1                |
| **short**     | mt, mr, mb, ml, <br> m-horizontal, m-vertical  | auto          |             | mt_auto             |
| **short**     | m-all                                          |               | 1 - 50      | m-all_1             |
| **short**     | m-horizontal                                   |               | 1 - 50      | m-horizontal_1      |
| **short**     | m-vertical                                     |               | 1 - 50      | m-vertical_1        |
| **short**     | mt                                             |               | 1 - 50      | mt_1                |
| **short**     | mr                                             |               | 1 - 50      | mr_1                |
| **short**     | mb                                             |               | 1 - 50      | mb_1                |
| **short**     | ml                                             |               | 1 - 50      | ml_1                | 

> At the moment just a short syntax for spacing is implemented.



<hr>

## Contribute to Arcibaldo:

##### Structure /src

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

