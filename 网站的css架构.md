### 模块化

**样式分离是应用到模块化的独立元素上。** 模块化指的是页面元素 例如 通用按钮 图标 页面的固定框架



### CSS分离和CSS合并

**分离** 一般是指那些非模块化的元素。 **合并** 多针对模块化的元素。 因为模块化是多处共用的东西。如果某天 产品 或者设计或者你的老板说 这里地方要改一下 那么你开始在模块化做好语义化的东西 你都要改 这是很糟糕的事情。维护起来也很麻烦



![border](http://image.zhangxinxu.com/image/blog/201007/2010-07-08_202843.png)

这里有个张鑫旭老师的图。文本框的宽度大小不一。不可能针对每个宽度独立写一个样式。 需要将公共的样式独立出来。

```css
.inset{
    height:16px;
    background-position:0 -220px; 
    background-color:white;
    border:1px solid #D3D2D4; 
    padding:3px 0 2px 2px;
}
/* 这里看起来是分离了公共样式 其实是合并了 那我接下来只要设置宽度属性了 例如*/
.w340{width: 340px;}
.w287{width: 287px;}
```



```html
<input type="text"  class="inset w163" />
<input type="text"  class="inset w297" />
<input type="text"  class="inset w397" />
```



上面的做法是不可取的。如果某天要重改 w340的语义化 那就很难改了。所以这里注意 模块化元素不分离。

分离的意识在于 分离命名。比如我们取一个类似以下的命名

```css
.txtwname { width: 340px; }
.txtwpass { width: 289px; }
```

但是这里的txtname 明明是独立样式 但是不能作为分离样式使用。

```css
.txtname, .w340 {width: 340px;}
```



