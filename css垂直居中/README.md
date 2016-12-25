# CSS 垂直居中

<div class="center">
	<main>
		<p>Center me, please</p>
	</main>
<center>

##基于绝对定位的解决方案 不知道高宽
```CSS
main{
	position: absolute;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
}
```
## 不使用absolute的解决方案
```CSS
main1{
	width: 18em;
	padding: 1em 1.5em
	margin: 50vh auto 0;
	transform: translateY(-50%);
	color: #fff;
}
```
##FlexBox  首先给父元素加上flex, 子元素只需要加上margin: auto;如果你想要里面的p标签里面内容垂直居中。那就要指定宽高 主轴和交叉轴的位置。
```CSS
main{
	align-items: center;
	justify-content: center;
	display: flex;
	height: 18em;
	width: 18em;
	margin: auto;
}
```
