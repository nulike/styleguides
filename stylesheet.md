## CSS Styleguide

So just that all has it's order, here I will be keeping all rules needed.


### Naming conventions

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

### Structure of CSS

First you need to follow the structure used to keep the CSS clear. This follows the ITCSS (Invertred Triangle CSS) approach found [as a slide](https://speakerdeck.com/dafed/managing-css-projects-with-itcss). Top to bottom, generic to explicit.

1. [Settings](#settings)
* [Tools](#tools)
* [Generic](#generic)
* [Base](#base)
* [Objects](#objects)
* [Components](#components)
* [Themes](#themes)
* [Trumps](#trumps)

#### Settings

Global variables, config switches.

-
#### Tools

Default mixins and functions.

-
#### Generic

Ground zero styles (normalize.css, resets, box-sizing).

-
#### Base

Unclassed HTML selectors (type selectors).

-
#### Objects

Cosmetic-free design patterns.

-
#### Components

Designed components, chunks of UI.

-
#### Themes

Any themes, just visual overrides (colors, fonts).

-
#### Trumps

Helpers and overrides
