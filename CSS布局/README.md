
## 清除浮动 直接跳过 不常用的 例如 添加多余标签使用clear: both;

```HTML

<div class="container">
	<div class="main"></div>
	<div class="left"></div>
	<div class="right"></div>
</div>

```


#### 1 overflow: hidden;

父元素 container 使用overflow清除下面的子元素的浮动。

#### 2 clearfix:after
结合伪元素。代表一个元素后最近的元素。给浮动元素的容器添加一个clearfix类。然后给这个类添加一个:after的伪元素实现末尾添加一个看不见的块元素清理浮动

```CSS
.clearfix:after{
	content: '',
	display: block;
	height: 0;
	clear: both;
	visibility: hidde;
}
.clearfix{
	zoom: 1;
}

```


#### 关于圣杯布局
左右两边分别为200px


```CSS

.container{
	padding: 0 200px;
}
.main,
.left,
.right{
	float: left;
	position: relative;
	height: 600px;
}

.main{
	width: 100%;
}
.left:{
	width: 200px;
	margin-left: -100%;
	left: -200px;
}
.right:{
	width: 200px;
	margin-left: -200px;
	right: -200px;
}
```

### 双飞翼布局
其实就是圣杯布局的改进。将主内容放入一个容器里面。使得这个容器产生BFC.这样里面主内容就和外面隔开。不会相互影响。

```HTML

<div class="container">
	<div class="main">
		<div class="sub-mian"></div>
	</div>
	<div class="left"></div>
	<div class="right"></div>
</div>

```

```CSS

.main,.left,.right{
	float: left;
	height: 300px;
}
.main{
	width: 100%;
}
.sub-main{
	margin: 0 200px;
	height: 300px;
}
.left{
	margin-left: -100%;
	width: 200px;
}
.right:{
	margin-left: -200px;
	width: 200px;
}
```

在主要内容区块使用 margin: 0 200px; 这样通过margin-left就可以直接定位两边






















