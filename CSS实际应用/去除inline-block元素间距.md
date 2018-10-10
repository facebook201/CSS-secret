#### 问题描述

一般inline-block 水平呈现的元素之间 都有一点空白间隙。 其实这是符合规范的表现。也就是说 规范如此。



> 有可能是我们在写代码的时候html中有空格 换种书写方式会去掉间隙

```html
<div>
    <a>李四</a
    ><a>张三</a
    ><a>王二</a>
</div>
```



> margin 负值

```css
.space a {
    margin-left: -3px;
}
```

但是字体不一样 margin-left 负值也不一样。不适合使用



> font-size: 0px;

```css
.space { font-size: 0; -webkit-text-size-adjust: none;}
.space a { font-size: 12px; }
```



> 使用letter-spacing

```css
.space {
    letter-spacing: -3px;
}
.space a {
    letter-spacing: 0;
}
```

































