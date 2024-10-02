# fluid-typography

This CSS Library leverages [CSS Container Queries](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_container_queries) to dynamically alter `font-size` and `line-height` values in response to resizing of elements. There is no JavaScript involved, only liberal use of CSS Container Queries, Custom Properties and the `calc` function.

Credit for the math belongs to [Chris Pearson](https://pearsonified.com/about/), creator of the [Golden Ratio Typography Calculator](https://grtcalculator.com/).

## Usage

Just include `fluid-typography.css` in the `<head>` of your html document, and add the `fluid` attribute to the DOM elements you would like to exhibit the fluid behavior. See `example.html` for an example implementation.

For the algorithm to work in CSS, the following values are necessary:

- min and max viewport width (`--vp_minWidth` and `--vp_maxWidth`)
- min and max font-size (`--fontSize_min` and `--fontSize_max`)
- min and max line-height (`---lineHeight_min` and `---lineHeight_max`)
- desired CPL (Characters Per Line) (`--cpl`)
- Character Width (`---char_width`)

See `fluid-typography.css` for the default values.

> **NOTE:** The default Character Width is `2.27`. This value was chosen because it is the [average character width of 135+ fonts](https://grtcalculator.com/math/#section-width-factor). This value should work well in most cases, but tweaking it can sometimes provide better results. Changes to this value will affect the way `line-height` is calculated, in concert with `--cpl`.

## Coming Soon

- Automatic calculation of `h1 - h6` `font-size` and `line-height` values
