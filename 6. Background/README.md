## Background
```css
.class {
    /* this is shorthand */
    background: url("freedom.jpg");
    /* this is seperate */
	background-image: url("freedom.jpg");
	background-size: cover;
	/* left and top offset */
	/* background-position: 10px 10px; */
	background-position: center;
	background-repeat: no-repeat;
	background-origin: border-box;
    background-clip: border-box;
    background-attachment: fixed;
    
}
```
## Image
[background-size](https://developer.mozilla.org/zh-CN/docs/Web/CSS/background-size)
[background-position](https://developer.mozilla.org/zh-CN/docs/Web/CSS/background-position)
### 设置图片container的高度对图片大小没有影响，应该如何解决？
- 问题分析：**图片的大小不受其surrounding container的高度宽度的限制**，这是默认设定，无法改变；如果想要改变图片的大小，有两种方法，一种是设定图片的绝对高度和绝对宽度；另外一种是设定图片相对于surround container的高度和宽度，但是有个前提： surrounding container的display属性为`非inline`
  - 方法一： 直接给`img`以固定高度
  - 方法二： `container`设定为非`inline`属性，并且附加`高度`；img附加`百分比高度`；
- 小知识点：`height`默认值为`auto`，即根据`content`调整

### CSS中图片需要与文字左右排列，应该如何做？
- `<img>`外面加一个`div`做container
- container设置为inline0-block属性
- 可以调整图片的宽度来适应文字

### 图片添加阴影效果后，下方多出来一个空白条，如何解决？
- 方法一：为`img`添加`vertical-align`为`top`或`bottom`
- 方法2：设置`img`为block属性
## Gradients
### Linear Gradient
```css
.overview {
    background-image: linear-gradient(to bottom, red, blue);
    background-image: linear-gradient(to left bottom, red, blue);
    background-image: linear-gradient(to right top, red, blue);

    background-image: linear-gradient(0deg, red, blue);
    background-image: linear-gradient(30deg, red, blue);

    background-image: linear-gradient(30deg, red, transparent);
    background-image: linear-gradient(30deg, red, rgba(0,0,0,0.5));
}
```
### Radial Gradient
```css
.overview {
    background-image: radial-gradient(circle, red, blue);
    background-image: radial-gradient(circle at top, red, blue);
    background-image: radial-gradient(circle at top left, red, blue);
    background-image: radial-gradient(circle at 20% 15%, red, blue);
    background-image: radial-gradient(circle 20px at 20% 15%, red, blue);
    background-image: radial-gradient(ellipse 20px 30px at 20% 15%, red, blue);
    background-image: radial-gradient(ellipse farthest-side at 20% 15%, red, blue);
    background-image: radial-gradient(ellipse farthest-corner at 20% 15%, red, blue);
    background-image: radial-gradient(ellipse closest-side at 20% 15%, red, blue);
    background-image: radial-gradient(ellipse closest-corner at 20% 15%, red, blue);

}
```
### Multiple Backgrounds
```css
.overview{
    /* read from left to right: from top to bottom */
    background: linear-gradient() + prop, url() + prop, red;
}
```
## Filters
```css
div {
    /* this would blue the element */
    filter: blur(10px);
    filter: grayscale(50%)
}
```


### SVG Styling
```css
element.style {
    fill: red;
    stroke: black;
    stroke-width: 10px
}
```

## Summary
- shorthand overwrites other properties.
- 
