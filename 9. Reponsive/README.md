## Reponsive Design
- How to make the page look awesome in all devices？
### Hardware vs Software Pixels
[Absolute Length](https://www.w3.org/TR/css-values-3/#absolute-lengths)


## Two ways to make site responsive
### viewport meta tag
- used to adjust site to device viewport
  - translate the website according to the pixel ratio
```html
<meta name='viewport' content='width=device-width, initial-scale=1.0'>
```
- **name**: target
- **content**: value of the target
- **width=device-width**: tell the browser the actuall size of the device
- **initial-scale=1.0**: zoom in or zoom out; the default value - no zoom
- **user-scalable=no**: don't allow user to zoom in or out.
- **maximum-scale=2.0**: the maximum value of scale
### Media Query with @media
- used to adjust element according different devices - media.
```css
/* when the width is above 40rem */
@media (min-width: 40rem) {
    #product-overview h1 {
        font-size: 3rem;
    }
}

/* you could set multiple -  cascading */
@media (min-width: 40rem) {
    #product-overview h1 {
        font-size: 3rem;
    }
}
```

- How to find right breaking point?
  - [Device length All in One](https://www.mydevice.io/)

- Logical Operators
```css
/* and */
@media (min-width: 40rem) and (orientation: landscape) {
    #product-overview h1 {
        font-size: 3rem;
    }
}
/* or */
@media (min-width: 40rem), (orientation: landscape) {
    #product-overview h1 {
        font-size: 3rem;
    }
}
```
## Links
[Web Design Resources](http://floatingboxes.com/resources/)

## Hints
- Design Method: Mobile First