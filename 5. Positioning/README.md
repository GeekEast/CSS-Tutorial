`z-index:auto` = 0; z-index relative to its context element

`sticky`: fixed to viewport for a while until it reaches the `border` of its parent element.

`overflow:hidden`: hide the space of `direct` child element which is out of the bound of context element. doesn't apply to `position:fixed` elements. 

`static`,`relative`,`absolute`两两之间，无论谁是父谁是子，如果是直接关系，都将生效；只有`fixed`除外。但是有一种特殊情况，body设置hidden的情况下，会自动将值传给html，此时将会不会生效；若要生效，需要html和body同时设置hidden属性，避免传走值。



`static` > `absolute`: the context is `html` element.
`non-static` > `absolute`: the context is the `nearest` `non-static` parent element. 


relative > absolute: the context is the nearst relative parent. 默认对前置兄弟元素让步，即若有前置兄弟元素，top默认不为0；对后置元素不让步。
absolute > absolute: the context is the nearst absolute parent
fixed > absolute: the context is the nearest fixed parent

z-index: for non-static position element;
Compare: parent

fixed的context是html
没有前置non-static的absolute的context是html
有前置non-static的absolute的context是最近的non-static前置元素

stacking-context:
fixed元素自动创建stacking-context
absolute和relative元素需要制定z-index才会创建stacking-context

## Positioning Context
fixed: viewport
aboslute: relative or html
relative: its original position in flow
sticky: viewport and another element




