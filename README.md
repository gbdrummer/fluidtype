# fluid-typography

This CSS Library leverages [CSS Container Queries](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_container_queries) to dynamically alter `font-size` and `line-height` values in response to resizing of elements. There is no JavaScript involved, only liberal use of CSS Container Queries, Custom Properties and the `calc` function.

Credit for the math belongs to [Chris Pearson](https://pearsonified.com/about/), creator of the [Golden Ratio Typography Calculator](https://grtcalculator.com/).

## Usage

Just include `fluid-typography.css` in the `<head>` of your html document, and add the `fluid` attribute to the DOM elements you would like to exhibit the fluid behavior.

## How it works

For the algorithm to work in CSS, it is necessary to specify the following values:

- min and max viewport width (`--vp-width_min` and `--vp-width_max`)
- min and max font-size (`--font-size_min` and `--font-size_max`)
- min and max line-height (`--line-height_min` and `--line-height_max`)
- desired CPL (Characters Per Line) (`--cpl`)
- Character Width (`---char-width`)

The default Character Width value is `2.27`. This value was chosen because it is the [average of 135+ fonts](https://grtcalculator.com/math/#section-width-factor). This value should work well in most cases, but tweaking it can sometimes provide better results. Changes to this value will affect the way `line-height` is calculated in concert with `--cpl`.

These values can be altered by changing the CSS Custom Properties in `fluid-typography.css`. However, the default values should work well for common scenarios.

**To learn more about CSS Container Queries, see:**

- [MDN Article](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_container_queries)
- [The Spec](https://www.w3.org/TR/css-contain-3/#container-queries)

## Coming Soon

- Automatic calculation of `h1 - h6` `font-size` and `line-height` values
