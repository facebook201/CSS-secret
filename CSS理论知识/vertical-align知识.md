### vertical-align 属性



vertical-align属性只会在 inline 或 inline-block 的时候才起作用。


#### vertical-align 属性跟 line-height 的关系

vertical-align 百分比的数值是根据line-height来计算的。
```css
vertical-align: 30%; // 其实就是3像素
line-height: 10px;
```



内联元素的 vertical-align 的对其方式是 baseline为基准的。

下面是一个图片的在div的位置 我们发现图片下面会有一点点的空格

![border](https://raw.githubusercontent.com/facebook201/HTML-CSS/master/img/lineheight.png)

```html
<div class="inline">
  <img src="xxx.png" height="100px" width="100px">
</div>	
```

图片的对其方式是跟 文字的基线对其 所以下面会有小空白 如果文字越大 空白越明显 所以 如果是0 就没有空白线

> 内联元素可以块状化 vertical-align 就不会起作用。

>改变默认的对其方式 
>
>
>
>改变line-height 字符足够小 文字就没有多余的空白
>
>
>
>或者改变字符 font-size 0px;



![border](https://raw.githubusercontent.com/facebook201/HTML-CSS/master/img/baseline.png)



如上图所示。这里的一个内联盒子有文字 一个没有文字。 这里的行为表现就是 按照最后一个盒子的line box 的文字的基线对其 所以第二个盒子和第一个盒子的共同的基线对其方式就表现如此。



**inline-block 的基线是正常流中最后一个line box 的基线。 除非这个line box 里面没有 line boxes 或者本身 overflow属性的计算值不是 visible 这种情况下是 margin底边缘**



![border](https://raw.githubusercontent.com/facebook201/HTML-CSS/master/img/baselinetext.png)

这个图就展示了 最后一个标签里面的x的基线跟图片的基线对其 修改内联盒子的对其方式 line-height: 0;  vertical-align top;



### inline元素

图文表现就是 默认基线对其 下面有点小空白。



### vertical-align middle

**定义**

* inline / inline-block 元素的垂直中心点和父元素基线 的 1/ 2 x -height 处对其
* table-cell 单元格填充盒子相对于外面的表格行居中对齐



> 近似垂直居中

![border](https://raw.githubusercontent.com/facebook201/HTML-CSS/master/img/vertical.png)

```css
p {line-height: 300px;}
img { vertical-align: middle; }
```

上面的图片看似数居中对其的。但是不是的。

**元素的垂直中心点和父元素基线 的 1/ 2 x -height 处对其**  



解决方案:

* font-size: 0px;

* 都vertical-align 都是 middle



### vertical-align 的实际应用

图标和文字对其。 vertical-align: 负值; 





### 不定大小图片和多行文字垂直居中

![border](https://raw.githubusercontent.com/facebook201/HTML-CSS/master/img/middle1.png)

```css
    .line-height {background-color:blanchedalmond; height: 300px; width: 600px; }
    .line-height > img { vertical-align: middle; }
	// 辅助元素 height 100% width 0 
    .font{height: 100%; vertical-align: middle; display: inline-block;}
```





















