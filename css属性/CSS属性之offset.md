
## HTMLElement 属性



```HTML
<div class="block">
		<div class="box"></div>
		
</div>
```

```CSS

.block{
	position: relative;
	display: flex;
	align-items: center;
	justify-content: center;
	height: 500px;
	width: 500px;
	border: 1px solid #ccc;
}
.box{
	height: 150px;
	width: 150px;
	background-color: pink;
}

```

#### offsetTop/offsetLeft

offsetTop/offsetLeft : 只读属性。要确定这两个属性的值。首先要确定元素的offsetParent. offsetParent指的是距离元素最近的position为static的祖先元素, 如果没有就指向body。所以 offsetTop/offsetLeft 是指元素左侧/上侧偏移的距离。

```JavaScript

var element = document.querySelector('.box');
	element.offsetTop = 175;
	element.offsetLeft = 175;

```

#### offsetWidth / offsetHeight

只读属性 返回的是元素的高度或宽度。包括边框 内边距 滚动条。

```JavaScript
	element.offsetWidth = 150;
```

#### scrollheight / scrollWidth
只读属性 返回元素内容整体尺寸, 包括元素看不见的部分。

#### scrollTop / scrollLeft 
滚动条距离容器的高度。没有默认为0;

#### clientWidth / clientWidth
元素可视。不包括border 和 margin 但是包含 padding.

 
#### 网页可见区域宽： document.body.clientWidth 
#### 网页可见区域高： document.body.clientHeight 
#### 网页可见区域宽： document.body.offsetWidth (包括边线的宽) 
#### 网页可见区域高： document.body.offsetHeight (包括边线的高) 
#### 网页正文全文宽： document.body.scrollWidth 
#### 网页正文全文高： document.body.scrollHeight 
#### 网页被卷去的高： document.body.scrollTop 
#### 网页被卷去的左： document.body.scrollLeft 
#### 网页正文部分上： window.screenTop 
#### 网页正文部分左： window.screenLeft 
#### 屏幕分辨率的高： window.screen.height 
#### 屏幕分辨率的宽： window.screen.width 
#### 屏幕可用工作区高度： window.screen.availHeight 
#### 屏幕可用工作区宽度： window.screen.availWidth 

#### HTML精确定位:scrollLeft,scrollWidth,clientWidth,offsetWidth 
#### scrollHeight: 获取对象的滚动高度。 
#### scrollLeft:设置或获取位于对象左边界和窗口中目前可见内容的最左端之间的距离 
####scrollTop:设置或获取位于对象最顶端和窗口中可见内容的最顶端之间的距离 
#### scrollWidth:获取对象的滚动宽度 
#### offsetHeight:获取对象相对于版面或由父坐标 offsetParent 属性指定的父坐标的高度 
#### offsetLeft:获取对象相对于版面或由 offsetParent 属性指定的父坐标的计算左侧位置  
#### offsetTop:获取对象相对于版面或由 offsetTop 属性指定的父坐标的计算顶端位置 
#### event.clientX 相对文档的水平座标 
#### event.clientY 相对文档的垂直座标 
#### event.offsetX 相对容器的水平坐标 
#### event.offsetY 相对容器的垂直坐标 
#### document.documentElement.scrollTop 垂直方向滚动的值 
#### event.clientX+document.documentElement.scrollTop 相对文档的水平座标+垂直方向滚动的量 






