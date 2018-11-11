---
layout: default
title: Arcibaldo v1.0
---

### What you will find inside Arcibaldo?

```
├── css
│   ├── arcibaldo.css                  // Arcibaldo v.1 CSS
│   ├── arcibaldo.css.map               
│   └── arcibaldo.min.css              // Arcibaldo v.1 minified CSS 
├── LICENSE
├── package.json
├── README.md
└── scss
    ├── arcibaldo.scss                  // Arcibaldo v.1 SCSS
    ├── arcibaldo.variables.scss        // required: Core variables of Arcibaldo
    ├── _functions.scss                 // required: Core functions of Arcibaldo
    ├── mixins
    │   ├── _breakpoints.scss           // mixins for screen size and orientation breakpoints
    │   ├── _geometry.scss              // mixins for three shapes: square, rectangle, circle
    │   └── _size.scss                  // mixins for managing sizes
    ├── _mixins.scss                    // Arcibaldo - Import all mixins
    └── theme
        ├── _buttons.scss
        ├── _geometry.scss              
        ├── _layout-flexbox.scss        // Layout: Flexbox
        ├── _layout.scss                // Layout
        ├── _shadings.scss              
        ├── _spacing.scss               // Padding and margin
        └── _typography.scss
```
 
##### Installation:

```
$ npm install --save arcibaldo
```

 
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


| **base**      |**values**| **example** |
| ------------- |:--------:| -----------:|
| w             | 1 - 100  | class="w_1" |
| h             | 1 - 100  | class="h_1" |



### Layout: Flexbox


##### Containers Block level: 

| **short**    | **long**      | **base**          | **example**                 |
| ------------ |:-------------:|:-----------------:| ---------------------------:|
| rc           | row-container | rc, row-container | class="rc"                  |
| cc           | col-container | cc, col-container | class="cc"                  |

##### Flex Line Wrapping:
 
| **short**         | **base**      |**modifiers**               | **example**                 |
| ----------------- |:-------------:|:--------------------------:| ---------------------------:|
| flex_wrap         | flex          | wrap                       | class="flex_wrap"           |
| flex_wrap-nowrap  | flex          | nowrap                     | class="flex_wrap-nowrap"    |
| flex_wrap-reverse | flex          | wrap-reverse               | class="flex_wrap-reverse"   |

##### Items:

| **short**       | **base**      |**modifiers**               | **values**     | **example**                  |
| --------------- |:-------------:|:--------------------------:|:---------------| ----------------------------:|
| flex_{n}        | flex          |                            | 1 - 100        | class="flex_1"               |
| flex_shrink_{n} | flex          | shrink                     | 1 - 100        | class="flex_shrink_1"        |

##### Axis Alignment:

| **short**     | **long**                          | **base**              |**modifiers**                  | **example**                   |
| ------------- |:---------------------------------:|:---------------------:|:-----------------------------:| -----------------------------:|
| jc_fs         | justify-content_flex-start        | jc, justify-content   | fs, flex-start                | class="jc_fs"                 |
| jc_fe         | justify-content_flex-end          | jc, justify-content   | fe, flex-end                  | class="jc_fe"                 |
| jc_c          | justify-content_center            | jc, justify-content   | c, center                     | class="jc_c"                  |
| jc_sb         | justify-content_space-between     | jc, justify-content   | sb, space-between             | class="jc_sb"                 |
| jc_sa         | justify-content_space-around      | jc, justify-content   | sb, space-around              | class="jc_sa"                 |


##### Cross-axis Alignment

@todo: work in progress


#### Spacing 

Spacing is based on the value of `$base-space-value` (arcibaldo.variables.scss) and each spacing class (margin and padding) can be extended 
50 times the value of `$base-space-value`. <br>
*Eg. Having a `$base-space-value` set to 2px (`$base-space-value: 2px`),the the maximum spacing will solve at the dimension of 100px
`.mb_50` will output `margin-bottom: 100px`*


| **base**                                       |**modifiers**  | **values**  | **example**                   |
|:----------------------------------------------:|:-------------:|:------------| -----------------------------:|
| pt, pr, pb, pl, <br> p-horizontal, p-vertical  | auto          |             | class="pt_auto"               |
| p-all                                          |               | 1 - 50      | class="p-all_1"               |
| p-horizontal                                   |               | 1 - 50      | class="p-horizontal_1"        |
| p-vertical                                     |               | 1 - 50      | class="p-vertical_1"          |
| pt                                             |               | 1 - 50      | class="pt_1"                  |
| pr                                             |               | 1 - 50      | class="pr_1"                  |
| pb                                             |               | 1 - 50      | class="pb_1"                  |
| pl                                             |               | 1 - 50      | class="pl_1"                  |
| mt, mr, mb, ml, <br> m-horizontal, m-vertical  | auto          |             | class="mt_auto"               |
| m-all                                          |               | 1 - 50      | class="m-all_1"               |
| m-horizontal                                   |               | 1 - 50      | class="m-horizontal_1"        |
| m-vertical                                     |               | 1 - 50      | class="m-vertical_1"          |
| mt                                             |               | 1 - 50      | class="mt_1"                  |
| mr                                             |               | 1 - 50      | class="mr_1"                  |
| mb                                             |               | 1 - 50      | class="mb_1"                  |
| ml                                             |               | 1 - 50      | class="ml_1"                  | 

> At the moment just a short syntax for spacing is implemented.



<hr>

## Contribute to Arcibaldo:

Any help is more than welcome, file a bug, contribute some code, or improve documentation. 
