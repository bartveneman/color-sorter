# color-sorter [![Build Status](https://travis-ci.org/bartveneman/color-sorter.svg?branch=master)](https://travis-ci.org/bartveneman/color-sorter) [![Known Vulnerabilities](https://snyk.io/test/github/bartveneman/color-sorter/badge.svg)](https://snyk.io/test/github/bartveneman/color-sorter) ![Dependencies Status](https://img.shields.io/david/bartveneman/color-sorter.svg) ![Dependencies Status](https://img.shields.io/david/dev/bartveneman/color-sorter.svg)

Sort CSS colors by hue, then by saturation. Black-grey-white colors (colors with 0% saturation) are shifted to the end.

This sorting algorithm is very opinionated and might not fit *your* needs!

## Usage

```js
var sortColors = require('color-sorter');
var colors = [
  '#000',
  'red',
  'hsl(0, 10%, 60%)'
];

// Method 1: wrap array in a sort function
var sorted = sortColors(colors);

// Method 2: use Array.sort with a sort function
var sorted = colors.sort(sortColors.sortFn)

// => sorted:
// [
//  'red',
//  'hsl(0, 10%, 60%)',
//  '#000'
// ]
```

## Examples

These examples can be seen on [Project Wallace](https://projectwallace.com) where this package is used for sorting the colors.

### CSS-Tricks

![CSS Tricks color sort example](/examples/css-tricks.png)

### Smashing Magazine

![Smashing Magazine color sort example](/examples/smashing-magazine.png)

### Bootstrap

![Bootstrap color sort example](/examples/bootstrap.png)

### Zurb Foundation

![Zurb Foundation color sort example](/examples/foundation.png)

### Project Wallace

![Project Wallace color sort example](/examples/project-wallace.png)