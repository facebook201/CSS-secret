## border属性值

### border-width 不支持百分比

边框不会因为设备的变大就会变大，例如手机 和 PC。 不会因为PC变大边框就会变大。
outline box-shadow等等。border-width 还有关键字。thin(1px) medium(3px) thick(5px).

### border-style类型

* solid dashed 但是dashed 在IE(宽高 1:3) Chrome(1:2)。dotted 点线。
(在IE (圆点) 和 Chrome(方形)表现又不一样。)所以我们可以使用 dotted实现IE下面的圆

```HTML
    <div class="box">
        <div class="dotted"></div>
    </div>
```

```CSS

.box{
    height: 150px;
    width: 150px;
    /* 超出区域隐藏 只显示一个圆 */
    overflow: hidden;
}
.dotted{
    height: 100%;
    width: 100%;
    border: 149px dotted #cd0000;
}
/* 可以加两个div 来实现圆角的矩形 */

```

* border-style: double; 双边框 可以使用其绘制图形

```CSS
.icon{
    /* 移动端比较实用 */
    width: 120px;height: 20px;
    border-top: 60px double;
    border-bottom: 20px solid;
}   
```


### border-color 和 color

border-color 就是 color。就是边框的颜色会继承color颜色。
```CSS
.color{
    color: #ccc;
    border: 1px solid;
    transition: color .25s;
    /* transition: 是过渡的 只需要一个color来过渡 */
}
.color::before{
    border-top: 10px solid;
}
.color::after{
    border-left: 10px solid;
}
.color:hover{
    color: #06c;
}
```

### border 和 solid 三角形和梯形

* 三角形
```CSS
.trangle{
    height: 0px;
    width: 0px;
    border: 100px solid;
    border: red transparent transparent transparent;
}
```
* 模拟圆角

使用梯形的边缘来实现圆角边框 兼容IE6/7
```CSS
.trangle2{
	width: 300px;
	border: 100px solid;
	border-color: transparent transparent #c00;
}
```
