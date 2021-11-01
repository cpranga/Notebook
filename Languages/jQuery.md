# Script Tags and Document Ready

## Script Tag
To use JS on HTML, you must add the ```<script>``` tag
ANy JS within the ```<script>``` tag will be executed including jQuery

## On Document Ready
```$(document).ready(function() {});``` will ensure that JS only executes when HTML has finished loading in browser

# Targeting Selectors

**ALL** jQuery statements begin with a ```$```
jquery will often select an HTML element with a **Selector**, then **do something** to the element
```$("button").addClass("animated bounce");```

Element Type|Format
--|--
Type|```type_name```
Class|```.class_name```
ID|```#id_name```
Body|`body`

# Common Commands
Action|Command
--|--
Add Class|```addClass```
Remove Class|```removeClass```
Change CSS|```.css("<property>","<value>")```
Change Element Prop|```.prop("<propety>",<value>)```
Edit HTML Text and Props|`.html("<em>Hello</em>")`
Edit HTML Text|`.text()`
Remove Element|`.remove()`
Move Element|`$("<source">).appendTo("<destination>")`
Copy Element|`$("<source">).clone().appendTo("<destination>")`
Access Parent Element|`.parent()`
Access Children of Element|`.children()`
Target n-th children|`$(".target:nth-child(3)")`
Target Odd Children|`$(".target:odd")`