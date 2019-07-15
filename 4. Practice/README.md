### To Finish the Plan Section
`text-align` is used for aligning the inner content of a block element.
- left
- rigth
- center
- justify
- inherit

`background`: including the padding box, not including the margin box.
`vertical-align`: only apply to `inline` or `inline-block` element.
`box-shadow`: 1px 2px 3px 4px rgba(0,0,0,0.4);
| Setting | Description       | Explanation                                  |
| ------- | ----------------- | -------------------------------------------- |
| 1px     | horizontal offset | `+`:right, `-`:left                          |
| 2px     | vertical offset   | `+`:bottom,`-`:top                           |
| 3px     | blur radius       | the bigger, the `blurred`, the further `out` |
| 4px     | spread radius     | size of the shadow                           |
| rgba    | just color        | semi-transparent recommended                 |

`list-style:none`  to remove list style
`text-decoration:none` to remove links style (`<a>`)

#### Three ways to align element horizontaly
- `inline-block`
- Grid system
- Flexbox

`Button` element has default style by the browser. which can be overriden by `class` style.


`cursor`: the shape of cursor

#### Cancel Ugly Outline
```css
.btn:focus {
    outline: none
}
```

`margin: auto`: use available space as much as possible to center things.
`float: right`: still in the flow of document which will affect other elements' positioning.