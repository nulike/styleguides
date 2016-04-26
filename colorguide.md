# Nulike Colorguide

## Color-Palettes

*Freely copied from [Trellicolors](https://trello.com/about/branding#colors).*


Colors are predefined in 10 shades.

```SCSS
$color-50  //lightest
$color-100
$color-200
$color-300
$color-400
$color-500 // default
$color-600
$color-700
$color-800
$color-900 // darkest
```

Only `$variables` are allowed in `.scss`-files for any colors.

**No** direct `rgba()`, `color literals` or `hex` values!

Colors **must** not contain any transparency!


### Black and White

Same variable-rules apply with the only exception of transparency:

```
black:
    rgba(0, 0, 0, .1) => rgba(0, 0, 0, 1)
white:
    rgba(255, 255, 255, .1) => rgba(255, 255, 255, 1)
```

This way black or white can be used to **darken** or **lighten** `elements`, `borders` or `shadows` no matter what underlying color.

`$black-900` and `$white-900` have no transparency.


### Don'ts

Using `lighten($color, 20%)` or `darken($color, 20%)` in your `.scss`-files is a big **no-no**. Only above color-variables with shades should be used.


## Font colors

### Font color

There are two font colors: light (white) or dark (black).

```
$dark-font-color: rgba(0, 0, 0, .8)
$light-font-color: rgba(255, 255, 255, .8)

$default-font-color: $dark-font-color
```

Both light and dark font colors have a slight transparency set to them. This is to prevent a too strong contrast or "glow" with certain background-colors.

This way font-colors automatically fit the background-color better.

### Color contrast to background

To keep text readable the color of the font should have enough contrast.

Whenever applying a `background-color` to **any** element this should only be done over following mixin:

```SASS
// pass background-color
@mixin background($color)
  color: set-text-color($color)
  background-color: $color

// depending on the lightness of the color
// a light or dark font is set
@function set-text-color($color)
  @if (lightness($color) > 40)
    @return $dark-font-color
  @else
    @return $light-font-color
```

This way there is no need to worry about the actual color behind a variable. The correct font-color is set automatically and guarantess a good contrast.

An example of setting a backgroung-color would look like this:

```
.my-class
    +background($color-500)
```

Output:

```
.my-class {
    color: rgba(255, 255, 255, .8);
    background-color: #123456;
}
```

## Nulike Brand Colors

Following above rules here is a list of current colors in use for Nulike:

```SCSS
$red-50: #fde8e4;
$red-100: #f9c7bc;
$red-200: #f69e8d;
$red-300: #f7755c;
$red-400: #ff4c29;
$red-500: #ff2900;
$red-600: #dd2604;
$red-700: #b72109;
$red-800: #921d0e;
$red-900: #671914;
```
```SCSS
$grey-50: #eaeaea;
$grey-100: #ccc;
$grey-200: #a7a7a7;
$grey-300: #858585;
$grey-400: #646464;
$grey-500: #464646;
$grey-600: #3f3f3f;
$grey-700: #373737;
$grey-800: #2e2e2e;
$grey-900: #242424;
```

#### Black and white shades
```SCSS
$black-50: rgba(0, 0, 0, .1);
$black-100: rgba(0, 0, 0, .2);
$black-200: rgba(0, 0, 0, .3);
$black-300: rgba(0, 0, 0, .4);
$black-400: rgba(0, 0, 0, .5);
$black-500: rgba(0, 0, 0, .6);
$black-600: rgba(0, 0, 0, .7);
$black-700: rgba(0, 0, 0, .8);
$black-800: rgba(0, 0, 0, .9);
$black-900: rgba(0, 0, 0, 1);
```
```SCSS
$white-50: rgba(255, 255, 255, .1);
$white-100: rgba(255, 255, 255, .2);
$white-200: rgba(255, 255, 255, .3);
$white-300: rgba(255, 255, 255, .4);
$white-400: rgba(255, 255, 255, .5);
$white-500: rgba(255, 255, 255, .6);
$white-600: rgba(255, 255, 255, .7);
$white-700: rgba(255, 255, 255, .8);
$white-800: rgba(255, 255, 255, .9);
$white-900: rgba(255, 255, 255, 1);
```

`// TODO: add link to brand colors`

I will add a link when Nulike is online where these colors will be available to see.
