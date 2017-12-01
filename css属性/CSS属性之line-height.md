## line-height

line-height 简称为行高（行间距）。用来控制两行文字垂直距离的东西。也就是行与行之间的垂直距离。

> 初始值				normal
>
> 遗传父元素
>
> 百分比				根据元素本身字体大小
>
> 计算值				数字 百分比 



一般它会搭配vertical-align 属性一起使用。 其中会涉及到 **内联格式化上下文** 

### font-size

* 相同的font-size 但是不同的font-family。渲染出来的line-height不同

  因为每个html的line-box高度不一样。 如果知道line-box 那么就会知道元素的高度。

  ​



### vertical-align 盒子的垂直对齐方式

**注意：** `vertical-align`只适用于内联和表格单元元素：不能用它来垂直对齐[块级元素](https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements)。

* 可以在包含行框内垂直对齐内联元素的框。 
* 垂直对齐表格中单元格的内容



> 初始值					baseline
>
> 遗传					没有
>
> 百分比					line-height的元素本身(独特)



#### 多行文本垂直显示

```html
<style>
 .line-div{line-height: 150px; font-size: 0; padding: 5px;}
.line-div .inner{ display: inline-block; inline-height: 14px; font-size: 14px; vertical-align: middle; }
</style>
<div class="line-div">
  <span class="inner">
  </span>
</div>
```



 