# Bootstrap4-addon
> Extra css classes and helpers for bootstrap 4 grid system.

## ASSETS LIST
* Aspect ratio
* Backgrounds
* Extras
* Icons
* Images
* Links
* Negative margins
* Typography
* Vertical height

## HOW TO USE IT

## Aspect ratio
For each bootstrap breakpoint adds `.ar-$breakpoint-#number ` class.  
The #number is between 5-230 with step 5.  

e.g.  
Class `.ar-md-20` will add a 20% padding-top css rule to the given element.  
This will effect the height of the element depending the width, so it will maintain its aspect ratio.


## Backgrounds
This is for background images and their positions.
[data-bg-src] styles for cover images.

.bg-position-$position
$position: top
           bottom
           bottom-left


## Extras
Reset focus outline & .overflow-hidden & .h-100 classes.


## Icons
Fonticons sizes.
.icon-xs (13px)
You can edit this sizes by include a variable file before you call the specific scss file.


## Images
Usefull classes for svg images.
In addition with .img-fluid class of bootstrap the images go to the next level!
##### Use
.img-#{$number}
##### Default Variables


## Links
Set colors for the links that you will need for your project, in a variables file.
##### Use
.link-#{$name}
##### Default Variables
$link-colors: (
    white:   white,
    black:   black,
    gray:    gray,
    red:     red,
    green:   green,
    blue:    blue,
    yellow:  yellow
)