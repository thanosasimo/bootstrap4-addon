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
`.line-height-$number` ($number: 07-20)  
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
// Grid
$grid-columns:                16 !default;
$grid-gutter-width:           10px !default;

$container-max-widths: (
  sm: 540px,
  md: 720px,
  lg: 960px,
  xl: 1180px
) !default;

// Colors
// stylelint-disable
$white:    #fff !default;
$gray-100: #eeeeee !default;
$gray-200: #e8e7e7 !default;
$gray-300: #dee2e6 !default;
$gray-400: #d8d8d8 !default;
$gray-500: #969696 !default;
$gray-600: #676767 !default;
$gray-700: #4a4a4a !default;
$gray-800: #333333 !default;
$gray-900: #212529 !default;
$black:    #000 !default;

$grays: () !default;
$grays: map-merge((
  "100": $gray-100,
  "200": $gray-200,
  "300": $gray-300,
  "400": $gray-400,
  "500": $gray-500,
  "600": $gray-600,
  "700": $gray-700,
  "800": $gray-800,
  "900": $gray-900
), $grays);

$blue:       #2f4486 !default;
$indigo:     #6610f2 !default;
$purple:     #6f42c1 !default;
$pink:       #e83e8c !default;
$red:        #e1251b !default;
$orange:     #fd7e14 !default;
$yellow:     #ffc107 !default;
$green:      #7aaf08 !default;
$teal:       #20c997 !default;
$cyan:       #68c9c9 !default;

$colors: () !default;
$colors: map-merge((
  "blue":           $blue,
  "indigo":         $indigo,
  "purple":         $purple,
  "pink":           $pink,
  "red":            $red,
  "orange":         $orange,
  "yellow":         $yellow,
  "green":          $green,
  "teal":           $teal,
  "cyan":           $cyan,
  "white":          $white,
  "gray-light":     $gray-100,
  "gray-medium":    $gray-400,
  "gray":           $gray-500,
  "gray-dark":      $gray-700,
  "gray-darker":    $gray-800
), $colors);

$primary:       $red !default;
$secondary:     $cyan !default;
$success:       $green !default;
$info:          $cyan !default;
$warning:       $yellow !default;
$danger:        $red !default;
$light:         $gray-100 !default;
$lighter:       $gray-200 !default;
$medium:        $gray-400 !default;
$gray:          $gray-500 !default;
$dark:          $gray-700 !default;
$darker:        $gray-800 !default;

$theme-colors: () !default;
$theme-colors: map-merge((
  "primary":    $primary,
  "secondary":  $secondary,
  "success":    $success,
  "info":       $info,
  "warning":    $warning,
  "danger":     $danger,
  "light":      $light,
  "lighter":    $lighter,
  "medium":     $medium,
  "gray":       $gray,
  "dark":       $dark,
  "darker":     $darker,
  "black":      $black
), $theme-colors);

$body-bg: $white !default;

// Fonts
$font-family-sans-serif:      "roboto-slab",sans-serif !default;

$font-weight-light:           200 !default;
$font-weight-normal:          400 !default;
$font-weight-medium:          500 !default;
$font-weight-bold:            700 !default;

$font-size-base:              1rem !default; // Assumes the browser default, typically `16px`

$display1-size:               12.8571rem !default;
$display2-size:               6.2142rem !default;
$display3-size:               5rem !default;
$display4-size:               3.3571rem !default;
$display5-size:               2.5rem !default;

$display1-weight:             800 !default;
$display2-weight:             800 !default;
$display3-weight:             800 !default;
$display4-weight:             800 !default;
$display5-weight:             800 !default;

$display-line-height:         .9 !default;

$small-font-size:             83% !default;

$font-weight-base:            $font-weight-normal !default;
$font-spacing-base:           0.00rem !default;
$line-height-base:            1.2 !default;
$paragraph-margin-bottom:     0rem !default;

$h1-font-size:                $font-size-base * 4.2857 !default;
$h2-font-size:                $font-size-base * 3.0 !default;
$h3-font-size:                $font-size-base * 1.875 !default;
$h4-font-size:                $font-size-base * 2.0714 !default;
$h5-font-size:                $font-size-base * 1.7142 !default;
$h6-font-size:                $font-size-base * 1.5 !default;

$headings-margin-bottom:      0rem !default;
$headings-font-weight:        $font-weight-bold;

$body-color:                  $black;

// Links
$link-color:                  $black !default;
$link-hover-color:            $red !default;
$link-hover-decoration:       none !default;

// Spacers
$spacer: 1rem !default;
$spacers: () !default;
$spacers: map-merge((
  0: 0,
  1: ($spacer * .25),
  2: ($spacer * .5),
  3: $spacer,
  4: ($spacer * 1.5),
  5: ($spacer * 2),
  6: ($spacer * 2.5),
  7: ($spacer * 3),
  8: ($spacer * 3.5),
  9: ($spacer * 4),
  10: ($spacer * 4.5),
  11: ($spacer * 5),
  12: ($spacer * 5.5),
  13: ($spacer * 6),
  14: ($spacer * 6.5),
  15: ($spacer * 7),
  16: ($spacer * 7.5),
  17: ($spacer * 8),
  18: ($spacer * 8.5),
  19: ($spacer * 9),
  20: ($spacer * 9.5),
  21: ($spacer * 10),
  22: ($spacer * 10.5),
  23: ($spacer * 11),
  24: ($spacer * 11.5),
  25: ($spacer * 12),
  26: ($spacer * 12.5),
  27: ($spacer * 13),
  28: ($spacer * 13.5),
  29: ($spacer * 14),
  30: ($spacer * 14.5),
  31: ($spacer * 15),
  32: ($spacer * 15.5),
  33: ($spacer * 16),
  34: ($spacer * 16.5),
  35: ($spacer * 17),
  36: ($spacer * 17.5),
  37: ($spacer * 18),
  38: ($spacer * 18.5),
  39: ($spacer * 19),
  40: ($spacer * 19.5),
  50: ($spacer * 29)
), $spacers);

// Cards

$card-spacer-y:                     0 !default;
$card-spacer-x:                     0 !default;
$card-border-width:                 0 !default;
$card-border-radius:                0 !default;
$card-border-color:                 $white !default;
$card-inner-border-radius:          calc(#{$card-border-radius} - #{$card-border-width}) !default;
$card-cap-bg:                       rgba($black, .03) !default;
$card-bg:                           $white !default;

$card-img-overlay-padding:          0 !default;

$card-group-margin:                 0 !default;
$card-deck-margin:                  $card-group-margin !default;

$card-columns-count:                2 !default;
$card-columns-gap:                  0em !default;
$card-columns-margin:               $card-spacer-y !default;

/*
***
***
/* ********* BOOTSTRAP4-ADDON
***
***
***
*/

// Icons
$icon-size-xxl:         40px !default;
$icon-size-xl:          30px !default;
$icon-size-l:           25px !default;
$icon-size-m:           20px !default;
$icon-size-s:           15px !default;
$icon-size-xs:          13px !default;

// Images
$image-width:           230 !default;
$image-width-step:      5 !default;

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

// Negative margins
$negative-margins-max:      230 !default;
$negative-margins-step:     5 !default;

// Typography
$font-size-base:        1rem !default;

$font-weight-thin:      200 !default;
$font-weight-light:     300 !default;
$font-weight-book:      300 !default;
$font-weight-normal:    400 !default;
$font-weight-medium:    500 !default;
$font-weight-bold:      700 !default;
$font-weight-exbold:    800 !default;
$font-weight-black:     900 !default;

$display4-size:         3.3571rem !default;
$display4-weight:       $font-weight-bold;
$display5-size:         2.5rem !default;
$display5-weight:       $font-weight-bold;

$font-size-xxlg:        ($font-size-base * 1.2857) !default;
$font-size-xlg:         ($font-size-base * 1.1428) !default;
$font-size-lg:          ($font-size-base * 1.0625) !default;
$font-size-sm:          ($font-size-base * .8125) !default;
$font-size-xsm:         ($font-size-base * .6875) !default;
$font-size-xxsm:        ($font-size-base * .7857) !default;
$font-size-xxxsm:       ($font-size-base * .7142) !default;

// Vertical heights
$vertical-heights-max:      230 !default;
$vertical-heights-step:     5 !default;
```