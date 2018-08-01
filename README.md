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

## Typography

## Vertical heights

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


// Link Colors
$link-colors: (
    white:   white,
    black:   black,
    gray:    gray,
    red:     red,
    green:   green,
    blue:    blue,
    yellow:  yellow
);
```