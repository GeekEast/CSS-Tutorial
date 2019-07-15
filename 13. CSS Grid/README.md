<img style="width: 60%; margin: auto" src="https://qph.fs.quoracdn.net/main-qimg-273858213285396edb57d9bb175825d6"></img>

```html
<div class="container">
    <div class='el1'> Element 1 </div>
    <div class='el2'> Element 2 </div>
    <div class='el3'> Element 3 </div>
    <div class='el4'> Element 4 </div>
</div>
```

```css
.container {
    display: grid;

    /* define number of columns */
    /* fr: fraction, takes up the remaining space */
    grid-template-columns: 200px 150px 20% 1fr;
    /* create 16 columns in total */
    grid-template-columns: repeat(4, 25% 25% 25% 25%);

    grid-template-rows: 5rem 2.5rem;
    /* minmax function: try to fill up as much as possible */
    grid-template-rows: 5rem minmax(10px,200px);

    /* add gaps between columns */
    grid-column-gap: 20px;
    /* add gaps between rows */
    grid-row-gap: 20px;
    /* add the  row and column gap*/
    grid-gap:10px 20px;
    /* add the same value for row and column gap */
    grid-gap:10px;

    /* sepcify item position using area name */
    grid-template-areas : "header header header header"
                          "side side main main"
                          "footer footer footer footer"

}

.el3 {
    /* start from line number 3 */
    grid-column-start: 3;
    /* end in line number 5 */
    grid-column-end: 5;
    grid-row-start: 1;
    grid-row-end:2;
    /* good pratice to the end */
    grid-row-end: -1;

    /* you should first name area in containing element css settings */
    grid-area: header;
}
```

### Debug
- Firefox
- Inspect -> Layout: extend lines infinitely

### Columns and Rows
- CSS grid thinks in `lines`
- Firefox
- Inspect -> Layout: display line numbers

### auto in css
- if the height or width of containing element is specified, auto means take as much as space.
- if the height or width of containing element is missing, auto means fit the content.
- 具体也要看情况进行试验

### Overlap
- Element could overlap each other in grid system if you clearly set their starting and ending position, otherwise the system would automatically to avoid overlapping.


### Important Properties
- grid-auto-flow
- grid-auto-rows
- grid-auto-columns
- auto-fill
- auto-fit

- align grid items
justify-items:
align-items
- align entire gird content
justify-content
align-content