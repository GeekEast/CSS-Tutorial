### Box Model
- margin
- border
- padding
- content

#### Margin Collapsing
- In General, use eigher `margin-top` or `maring-bottom`
- not related to left or right margin
<img style="width: 80%; margin: auto" src="https://geekeaskblogpics.s3-ap-southeast-2.amazonaws.com/posts/WX20190709-144857.png">
[More](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Mastering_margin_collapsing)

#### Shorter Property
- border
```css
    section: {
        border-width: 2px;
        border-style: dashed | solid;
        border-color: orange
    }
```
```css
    section: {
        border: 2px dashed orange
    }
```
- margin
```css
    section: {
        margin-top: 5px;
        margin-right: 10px;
        margin-bottom: 5px;
        margin-left: 10px
    }
```

```css
    section: {
        margin: 5px 10px 10px 5px;
        margin: 5px 10px;
        margin: 5px
    }
```
### Height & Width
- Percentage of `parent` node
- `width`: the width of the `content`, not including the padding and border
- `height`: the height of the `content`, not including the padding and border.
- way to change this `box-sizing: border-box`, default is `cotent-box`
### Display
- `visibility:hidden`: hide the element but keep its position
- `display:none`: hide the element without keeping its position
### Important Property
- `text-decoration`: underline,deleteline and so on.
- `vertical-align`: middle
### Pseudo Class & Element
- `:hover`: state
- `::after`: part
```css
.main-nav a:hover{
    ...
}

.main-nav a::after{

}
```

### Add Picture
```css
    section: {
        background: url("freedom.jpg")
    }
```

### Tricks
- Even one space, they are quite different.
```html
    <div class="task" id="task-1">I'm a box.</div>
    <div class="task" id="task-2">I'm a box.</div>
```
```html
    <div class="task" id="task-1">I'm a box.</div><div class="task" id="task-2">I'm a box.</div>
```