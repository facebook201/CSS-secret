## line-height

行高 两行文字基线的距离。

* 基线？baseline

   英语里面 学习的时候有个标准线 在字母的下方。 根据这个线来决定文字的高度

* 为什么是基线？

* 需要两行吗？




#### line-height 与盒模型

```html
<p>
    pp
    <em>em</em>
</p>
```

上面的文字虽然简单 但是有四种盒子

* 内容区域 content-area

  是一种围绕文字看不见的盒子。大小跟font-size有关

* 内联盒子 inline-boxs

  内容不会成块显示 一行排列。内联标签 em storng span 等

* 行框盒子

  每一行就是一个行框盒子

* 内容盒子




### line-height的 高度基理

**内联元素的高度是由行高决定的，即使font-size为0 也是有高度的。但是如果line-height 没有的话 就是 0**



* 行高由于其继承性 影响无处不在 即使单行文字

* **高度的表现不是行高 而是内容区域和行间距** 内容区域高 + 行间距 = 行高

  * 内容区域高度只和字号和字体有关系 跟line-height 无关
  * 行间距 = line-height - font-size


**行高决定内联盒子高度。行间距可大可小 保证高度正好等同于行高** 



### 行高支持的属性值

* normal
* number 根据字体大小计算 
* length 20px 具体的长度 跟一个数值单位
* precent 150% 根据字体的大小计算
* inherit 



1.5 150% 1.5 em 有什么区别吗？

* 计算没有差别
* 元素应用有差别 可以继承的元素根据font-size 重新计算行高。当前元素根据font-size计算行高 继承给下面的元素。

```css
body { font-size: 14px; line-height: 1.4286;}
```



### line-height 和图片的关系

下面是一张图片。发现图片下面有一点空隙。并没有占满。这是什么原因。**隐匿文本节点**  后面跟着看不到的文字。因为文本是根据baseline对其的。

![border](https://github.com/facebook201/HTML-CSS/blob/master/img/lineheight.png)

如何消除？

* 图片块状化 img { display: block; }
* 底线对其 img { vertical-align: bottom;}
* 行高足够小 基线上移动 .box { line-height: 0; }



### 实际应用

>  水平垂直居中

```css
.box { line-height: 300px; text-align: center; }
.box > img { vertical-align: middle; display: inline-block; }
```



> 多行文本水平垂直居中

```css
.line-height {background-color:blanchedalmond; text-align: center; line-height: 300px; }
.line-height > .txt { display: inline-block; vertical-align: middle; line-height: normal; text-align: left;}
```

把文字用个标签包起来 跟图片类似





