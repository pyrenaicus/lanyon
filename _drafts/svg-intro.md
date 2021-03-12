---
layout: "post"
title: "svg-intro"
date: "2021-03-12 13:02"
---
## SVG, Scalable Vector Graphics

Following [SVG tutorial on MDN Web Docs][eb7b29e8]

Language to draw vector graphics. We can also apply transformation to all its components.

SVG is supported by all major browsers.

An SVG document consists in a `<svg>` root element and elements to draw basic geometric shapes. In addtion there is the `<g>` element which groups different basic shapes together.

[Inkscape][3a9bf671] uses SVG as it's native format.

Attribute values in SVG must be placed inside quotes, even in the case of numbers.

Order of rendering the elements: later elements are rendered atop previous elements.

### Positioning the elements
SVG uses a coordinate system, top left corner is the point of origin (0, 0).

One unit in the coordinate system equals one screen unit (pixel). For example `<svg width="800" height="600"></svg>` defines a 800x600px canvas.

With `viewbox` attribute we can define a portion of that canvas to display.

```
<svg width="800" height="600" viewbox="0 0 400 300"></svg>
```
The whole canvas is 800x600px but the `viewbox` attibute defines the part of the canvas that will be visible.

### Basic shapes
**Rectangle**
```
<rect x="10" y="10" rx="6" ry="6" width="80" height="60"/>
```
**Circle**
```
<circle cx="40" cy="40" r="60"/>
```
**Ellipse**
```
<ellipse cx="40" cy="40" rx="60" ry="30"/>
```
**Line**
```
<line x1="10" y1="40" x2="60" y2="30"/>
```
**Polyline**
A group of connected straight lines, all the points (x, y) are included in a ist as `points` attribute. numbers separated by comma, space, EOL or LF.
```
<polyline points="40 60, 80 90, 115 125"/>
```


  [3a9bf671]: http://www.inkscape.org/ "Inkscape"


  [eb7b29e8]: https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Introduction "SVG tutorial on MDN Web Docs"