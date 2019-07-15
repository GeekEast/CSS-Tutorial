## Manipulating Styles via Javascript
- How to add Javascript?
  - Method 1: End within the `body` tag
  - Method 2: Seperate Js file and then add to the end within the `body` tag
- Things you need to know
  - Query Selector `document.querySelector('.backdrop')`
  - Event Listener ``
```javascript
var backdrop = document.querySelector('.backdrop');
// this will add style to element level
backdrop.style.display = 'block';
```
```javascript
var backdrop = document.querySelector('.backdrop');
var modal = document.querySelector('.modal');
var selectPlanButtons = document.querySelectorALL('.plan button');
for (let i=0; i< selectPlanButtons.length;i++){
    selectPlanButtons[i].addEventListener('click', function() {
        modal.style.display = 'block';
        backdrop.style.display = 'block';
    })
}
```
## Add & Remoing CSS classes via JS
```javascript
modal.className = 'open'; // overwrite way
modal.classList.add('open'); 
modal.classList.remove('open');
```

### Ways to access Style of HTML element using Javascript
1. `backdrop.style.backgroundImage`
2. `backdrop.style['backgournd-image']`

### What is a Modal?
- 对话框