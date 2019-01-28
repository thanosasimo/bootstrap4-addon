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

cp node_modules/bootstrap4-addon/sass/_variables.scss ./your/local/folder

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
/////////////////////////////////////////////////////////////////////////// GRID 
$grid-columns:                16 !default;
$grid-gutter-width:           10px !default;
 
$container-max-widths: (
  sm: 540px,
  md: 720px,
  lg: 960px,
  xl: 1180px
) !default;
 
/////////////////////////////////////////////////////////////////////////// COLORS
$white:    #fff !default;
$gray-100: #f5f5f5 !default;
$gray-200: #ebebeb !default;
$gray-300: #ddd !default;
$gray-400: #d8d8d8 !default;
$gray-500: #bcbcbc !default;
$gray-600: #919191 !default;
$gray-700: #4a4a4a !default;
$gray-800: #212121 !default;
$gray-900: #030303 !default;
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
 
$blue:           #345799 !default;
$indigo:         #6610f2 !default;
$purple:         #6f42c1 !default;
$pink:           #e83e8c !default;
$red:            #af282b !default;
$orange:         #ff8405 !default;
$yellow:         #ffca05 !default;
$green:          #c8f000 !default;
$teal:           #20c997 !default;
$cyan:           #367fbb !default;
$acadia:         #2f2d28 !default;
$dune:           #514e47 !default;
$masala:         #5f5c55 !default;
$lotus:          #8a4f48 !default;
$night-rider:    #353333 !default;
$porcelain:      #e3e3e2 !default;
 
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
  "lighter":        $gray-100,
  "light":          $gray-200,
  "medium":         $gray-400,
  "gray":           $gray-600,
  "dark":           $gray-700,
  "darker":         $gray-800
), $colors);
 
$primary:       $dune !default;
$secondary:     $lotus !default;
$success:       $green !default;
$info:          $cyan !default;
$warning:       $orange !default;
$danger:        $red !default;
$lighter:       $gray-100 !default;
$light:         $gray-200 !default;
$medium:        $gray-400 !default;
$gray:          $gray-500 !default;
$dark:          $gray-600 !default;
$darker:        $gray-800 !default;
 
$theme-colors: () !default;
$theme-colors: map-merge((
  "primary":      $primary, 
  "secondary":    $secondary, 
  "acadia":       $acadia, 
  "masala":       $masala, 
  "porcelain":    $porcelain, 
  "night-rider":  $night-rider, 
  "success":      $success, 
  "info":         $info, 
  "warning":      $warning, 
  "red":          $red, 
  "danger":       $danger, 
  "lighter":      $lighter, 
  "light":        $light, 
  "medium":       $medium, 
  "gray":         $gray, 
  "dark":         $dark, 
  "darker":       $darker, 
  "black":        $black 
), $theme-colors);
 
$body-bg: $white !default;
 
/////////////////////////////////////////////////////////////////////////// FONTS
$font-family-sans-serif:      "brother-1816", sans-serif !default;
$font-family-monospace:       "trailmade", script !default;

$font-weight-thin:            100 !default;
$font-weight-light:           300 !default;
$font-weight-book:            300 !default;
$font-weight-normal:          400 !default;
$font-weight-regular:         400 !default;
$font-weight-medium:          500 !default;
$font-weight-bold:            700 !default;
$font-weight-exbold:          800 !default;
$font-weight-black:           900 !default;
$font-weight-heavy:           900 !default;

$font-size-base:              .87rem !default;

$display1-size:               6.25rem !default;
$display2-size:               3.375rem !default;
$display3-size:               2.625rem !default;
$display4-size:               2.375rem !default;
$display5-size:               2.25rem !default;
$display6-size:               2rem !default;
 
$display1-weight:             $font-weight-thin !default;
$display2-weight:             $font-weight-thin !default;
$display3-weight:             $font-weight-thin !default;
$display4-weight:             $font-weight-thin !default;
$display5-weight:             $font-weight-thin !default;
$display6-weight:             $font-weight-thin !default;
 
$display-line-height:         1.2 !default;

$h1-font-size:                1.9375rem !default;
$h2-font-size:                1.87rem !default;
$h3-font-size:                1.6875rem !default;
$h4-font-size:                1.53rem !default;
$h5-font-size:                1.375rem !default;
$h6-font-size:                1.26rem !default;
 
$headings-margin-bottom:      0rem !default;
$headings-font-weight:        $font-weight-book;
$headings-color:              $primary !default;

$font-size-xxxlg:             1.1875rem !default;
$font-size-xxlg:              1.125rem !default;
$font-size-xlg:               1.0625rem !default;
$font-size-lg:                1rem !default;
$font-size-sm:                0.87rem !default;
$font-size-xsm:               0.82rem !default;
$font-size-xxsm:              0.76rem !default;
$font-size-xxxsm:             0.6875rem !default;

$small-font-size:             96% !default;
 
$font-weight-base:            $font-weight-normal !default;
$font-spacing-base:           0rem !default;
$line-height-base:            1.6 !default;
$paragraph-margin-bottom:     0rem !default;

$body-color:                  $primary;
 
/////////////////////////////////////////////////////////////////////////// LINKS 
$link-color:                  $secondary !default;
$link-hover-color:            $primary !default;
$link-hover-decoration:       none !default;

$link-colors: (
    primary:    $primary,
    secondary:  $secondary 
);
 
/////////////////////////////////////////////////////////////////////////// SPACERS 
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
  41: ($spacer * 20),
  42: ($spacer * 20.5),
  43: ($spacer * 21),
  44: ($spacer * 21.5),
  45: ($spacer * 22),
  46: ($spacer * 22.5),
  47: ($spacer * 23),
  48: ($spacer * 23.5),
  49: ($spacer * 24),
  50: ($spacer * 25.5)
), $spacers);
 
/////////////////////////////////////////////////////////////////////////// ICONS 
$icon-size-xxl:         70px !default;
$icon-size-xl:          35px !default;
$icon-size-l:           33px !default;
$icon-size-m:           20px !default;
$icon-size-s:           15px !default;
$icon-size-xs:          13px !default;
 
/////////////////////////////////////////////////////////////////////////// IMAGES 
$image-width:           380 !default;
$image-width-step:      5 !default;
 
/////////////////////////////////////////////////////////////////////////// NEGATIVE MARGINS
$negative-margins-max:      230 !default;
$negative-margins-step:     5 !default;
 
/////////////////////////////////////////////////////////////////////////// VERTICAL HEIGHTS
$vertical-heights-max:      230 !default;
$vertical-heights-step:     5 !default;

/////////////////////////////////////////////////////////////////////////// TYPOGRAPHY
$text-wings-height:       2px !default;
```

## Update package
npm version [<newversion> | major | minor | patch | premajor | preminor | prepatch | prerelease [--preid=<prerelease-id>] | from-git]  
npm version [major | minor | patch] -m "Upgrade to %s for reasons"  
npm publish  
