### SASS & SCSS
- essentially the same
- SASS does not run in the browser, only help in development stage
- Compile into css before production

### SASS vs SCSS
- No `;`, only indentation in SASS
- `;` is fine in SCSS

### Install SASS
```sh
npm install -g sass
```

### Compile into CSS
```sh
sass main.scss main.css
# watch module just like nodemon
sass --watch main.scss:main.css
```

### Nesting
```css
.documentation-links {
	list-style: none;
	margin: 1rem 0 0 0;
	padding: 0;
	display: -webkit-box;
	display: -ms-flexbox;
	display: -webkit-flex;
	display: flex;
	flex-direction: column;

	li {
		margin: 0.2rem 0;
		background: white;
	}
}
```

### Nested Properties
```css
.container {
	display: -webkit-box;
	display: -ms-flexbox;
	display: -webkit-flex;
	display: flex;
	flex: {
		direction: column;
		wrap: nowrap;
	}
	align-items: center;
	padding: 3rem 0;
	box-sizing: border-box;
}
```

### Variables
```css
$main-color: #521751;
/* above all */
```

### List
```css
$border-default: 0.05rem  #521751;
```

### Map
```css
$colors: (main: #521751, secondary: rgb(243, 101, 101));
map-get($colors, main);
```

### [Built-in Function](https://sass-lang.com/documentation/functions)



### @import
- allows you to import another css file into one css file