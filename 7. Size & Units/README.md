## Percentage
How is it calculated?
- the percentage of the containing block
- case 1: position: fixed -> the viewport
- case 2: position: absolute -> parent who has a **position** property
- case 3: static/relative -> parent who is a block element


## Scrollbar in Windows
Question: When you set width as `1vw`, it might see the scrollbars appeared in a windows computer.
Reason: In windows, 1vw include the viewport and the scrollbar width
Solutions:
1. use `width:100%`
2. add `overflow-x:hidden;` to body selector or add `overflow-y:hidden` to the body selector
3. add `-webkit-scrollbar { width: 0}` to the body selector

## Recommended Units
Property | Unit
---------|-----
font-size(root element) | % or **don't set**
font-size |  rem(em only for children)
padding/margin | rem
border | px
width/height | %(position property)/vw/vh
top/bottom/left/right | %