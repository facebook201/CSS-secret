
### currentColor 
currentColor 属性会继承当前文字颜色属性。
```CSS

.box{
	color: red;
	border: 1px solid currentColor;
}
.box:hover{
	color: pink;
}
```

这里开始边框会跟 字体颜色一样都是红色。但是在鼠标滑过的时候。
字体颜色和边框的颜色都会变成粉色。