


## How to Add CSS to HTML
### 1. Inline
- Not Recommended.
```html
<div style="background: #cac02f" />
```
### 2. Head
- Not Recommended.
```html
<head>
    <style>
        section { background: #b43838; }
    </style>
</head>
```

### 3. CSS file
- Best Practice.
- two parts: link html with css, css itself.
```css
/* index.css */
section {
    background: #b43838;
}
```
```html
<head>
    <link rel="stylesheet" href="./index.css">
</head>
```


## Selectors, Combinator, Cascading
- Cascading: allow for multiple style on the same element.
### Multiple class name
```html
<div class="a b c"/>
```
- [Selector && Combinator](https://geekeast.github.io/css-tricks.html)




### Inheritance
- Child element will **automatically** inherit style from parent element.
```css
  section: {
      background: inherit
  }
```
