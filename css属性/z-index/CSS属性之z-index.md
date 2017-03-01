## CSS之z-index深入理解

###1 z-index的基础

* z-index取值：auto(默认) <integer>整数值 inherit(继承)
* z-index特性：支持负值 支持CSS3 animation动画 需要跟定位元素配合(relative absolute fixed)

###2 z-index与定位元素

* 后来居上。
* 那个z-index的值大 哪个在上面

如果z-index发生了嵌套。
```HTML
<div style="position: relative;z-index:1;">
	<img src="mm0.jpg" style="position:absolute;z-index: 2;"></img>
</div>
<div style="position: relative;z-index:1;">
	<img src="mm0.jpg" style="position:relatives;z-index: 1;"></img>
</div>

```
这里不管里面的z-index有多大，只看父级元素的z-index值。谁大谁在上面。但是z-index要是数值。
* 祖先优先原则 

###3 层叠上下文 和 层叠水平

层叠上下文(stacking context)相当于一个z轴。我们所看到的东西都是z轴上面的。
#### 具有层叠上下文
* 页面更元素天生具有层叠上下文
* z-index值为数值的定位元素也有层叠上下文
* 其他属性

### 层叠顺序 小到大 内容在上 布局在中 装饰在在下 

* background/color 颜色背景描述
* 负z-index。
* block块状水平盒子
* float浮动盒子
* inline/inline-block	
* z-index:auto/0;
* z-index: 正数

#### 层叠水平
层叠上下文中的元素都有层叠水平。决定同一个层叠上下文中在z轴上面的显示数据。
遵循 "后来居上" "谁大谁上"

