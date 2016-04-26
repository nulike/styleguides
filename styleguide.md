# Nulike Styleguide

## Naming

### Naming-conventions

For Naming the classes a slight variation of the BEM-convention will be used:

```
.block-element--modifier
```

So **no** undersores!

If a `block` has two words for the name as `.main-nav` [bad] user camelcase for this: `.mainNav` **[good]**

So for a markup as follows:

```
.block.block--modifier
  .block-element.block-element--modifier
```
Would be styled: **[good]**

```
.block {}
.block-element {}
```
Not nested as: [bad]

```
.block .block-element {}
```

Seems pretty straight forward, I will add rules as needed. I have to use this in practice more.

## Linting

Where possible the a lint should be used. There is an own `.sass-lint.yml` file where all rules followed are listed.

Sort order of all properties follows Twitters [recess](https://github.com/twitter/recess/blob/master/lib/lint/strict-property-order.js)-sort-order.

## Structure of CSS

First you need to follow the structure used to keep the CSS clear. This follows the ITCSS (Invertred Triangle CSS) approach found [as a slide](https://speakerdeck.com/dafed/managing-css-projects-with-itcss). Top to bottom, generic to explicit.

1. [Settings](#settings)
* [Tools](#tools)
* [Generic](#generic)
* [Base](#base)
* [Objects](#objects)
* [Components](#components)
* [Themes](#themes)
* [Trumps](#trumps)

### Settings

Global variables, config switches.

-
### Tools

Default mixins and functions.

-
### Generic

Ground zero styles (normalize.css, resets, box-sizing).

-
### Base

Unclassed HTML selectors (type selectors).

-
### Objects

Cosmetic-free design patterns.

-
### Components

Designed components, chunks of UI.

-
### Themes

Any themes, just visual overrides (colors, fonts).

-
### Trumps

Helpers and overrides

## Colors

There is an own [Colorguide](colorguide.md) for how to work with colors on the project. This goes from how to include colors in your CSS files and how to pick what colors to use.
