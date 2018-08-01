# Bootstrap4-addon
> Extra css classes and helpers for bootstrap 4 grid system.

### ASSETS LIST
* [Aspect ratio](#aspect-ratio)
* [Backgrounds](#backgrounds)
* [Extras](#extras)
* [Icons](#icons)
* [Images](#images)
* [Links](#links)
* [Negative margins](#negative-margins)
* [Typography](#typography)
* [Vertical heights](#vertical-heights)

### HOW TO USE IT

## Aspect ratio
For each bootstrap breakpoint adds .ar-$breakpoint-$number class.  
Class `.ar-md-20` will add a 20% padding-top css rule to the given element.  
This will effect the height of the element depending the width, so it will maintain its aspect ratio.  
###### USE
`.ar-$breakpoint-$number`
###### DEFAULT VARIABLES
$number: 5-230 with step 5.  

## Backgrounds
This is for background images and their positions.  
###### USE
`[data-bg-src]` or `[bg-img-src]` background size cover.  
``` scss
.bg-position-$position
$position: top
           bottom
           bottom-left
```

## Extras
Reset focus outline & .overflow-hidden & .h-100 classes.
###### USE
`.overflow-hidden`  
`.h-100` height 100%  

## Icons
Fonticons sizes.
###### USE
`.icon-xs`  
###### DEFAULT VARIABLES
```scss
$icon-size-xxl:      40px !default;
$icon-size-xl:       30px !default;
$icon-size-l:        25px !default;
$icon-size-m:        20px !default;
$icon-size-s:        15px !default;
$icon-size-xs:       13px !default;
```
You can edit this sizes by include a variable file before you call the specific scss file.

## Images
Adds width to images.  
Usefull for svg images.  
Use it with bootstrap's .img-fluid class and with caution!
###### USE
`.img-$number`
###### DEFAULT VARIABLES
$number: 5-230 with step 5.  

## Links
Set colors for the links that you will need for your project, in a variables file.
###### USE
.link-$color-name
###### DEFAULT VARIABLES
$link-colors: (
    white:   white,
    black:   black,
    gray:    gray,
    red:     red,
    green:   green,
    blue:    blue,
    yellow:  yellow
)

## Negative margins
Adds .mt#{$infix}--#{$i} classes for negative margins.  
Works like bootstrap's margins and paddings classes.  
###### USE
`.mt-$breakpoint-$number`
###### DEFAULT VARIABLES
$number: 5-340 with step 5.  

## Typography
###### USE
`.text-wings`  
`.text-underline`  
`.text-underline-simple`  
`.line-height-$number`  
`.font-weight-$weight`  
`.display-4` & `display-5`  
`.xxlarge`, `.xlarge`, `.large`, `.xsmall`, `.xxsmall`, `.xxxsmall`  
###### DEFAULT VARIABLES

## Vertical heights
###### USE
`.vh-$breakpoints-$number`  
`.vh-max-$breakpoints-$number`  
###### DEFAULT VARIABLES
$number: 5-230 with step 5.  

### VARIABLES
Copy paste this vars in a file.  
Change the variables according to your needs.  
Call this file before the scss assets.

``` scss
// Icons
$icon-size-xxl:      40px !default;
$icon-size-xl:       30px !default;
$icon-size-l:        25px !default;
$icon-size-m:        20px !default;
$icon-size-s:        15px !default;
$icon-size-xs:       13px !default;

// Images
$image-width:        230 !default;
$image-width-step:   1 !default;

// Links
$link-colors: (
    white:   white,
    black:   black,
    gray:    gray,
    red:     red,
    green:   green,
    blue:    blue,
    yellow:  yellow
);

// Typography
$font-weight-book:      300 !default;
$font-weight-medium:    500 !default;
$font-weight-exbold:    800 !default;
$font-weight-black:     900 !default;

$display4-size:         3.3571rem !default;
$display4-weight:       $font-weight-bold;
$display5-size:         2.5rem !default;
$display5-weight:       $font-weight-bold;

$font-size-xxlg:        ($font-size-base * 1.2857) !default;
$font-size-xlg:         ($font-size-base * 1.1428) !default;
$font-size-lg:          ($font-size-base * 1.0714) !default;
$font-size-xsm:         ($font-size-base * .8571) !default;
$font-size-xxsm:        ($font-size-base * .7857) !default;
$font-size-xxxsm:       ($font-size-base * .7142) !default;
```