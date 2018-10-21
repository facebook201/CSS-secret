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

![border](https://github.com/facebook201/HTML-CSS/blob/master/img/lineheight.png)

```html
<div class="inline">
  <img src="xxx.png" height="100px" width="100px">
</div>	
```

图片继承了一下属性。例如 font-size: 24px; 后面的空白字符的也是基线对其。下面会有一点空白。

> 内联元素可以块状化 vertical-align 就不会起作用。

>改变默认的对其方式 
>
>改变line-height 字符足够小 文字就没有多余的空白
>
>或者改变字符 font-size 0px;

**inline-block 的基线是正常流中最后一个line box 的基线。 除非这个line box 里面没有 line boxes 或者本身 overflow属性的计算值不是 visible 这种情况下是 margin底边缘**

