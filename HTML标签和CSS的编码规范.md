### HTML

```html
<!DOCTYPE html>
<html lang="zh-CN">

</html>
```



#### 元素以及标签闭合

* 空元素 area、br、hr、img、input、link、source **只有开始标签 没有闭合标签**
* 原始文本元素：script、style
* 常规元素：其他HTML允许的元素都称为常规元素



代码缩进 四个空格。 纯数字输入框 type="tel"





### CSS

**属性书写顺序**

* 布局定位属性 display float position overflow 等
* 自身属性 width border margin
* 文本属性 color text-align vertical-align
* 其他属性 content cursor box-shadow 

```css
.css{
    display: block;
    position: relative;
    float: left;
    width: 100px;
    height: 100px;
    margin: 0 10px;
    padding: 20px 0;
    font-family: Arial, 'Helvetica Neue', Helvetica, sans-serif;
    color: #333;
    background: rgba(0,0,0,.5);
    border-radius: 10px;    
}
```



### SCSS规范

```css
/**
 * @desc File Info
 * @author syo
 * @date 2010-10-10
 */

/*  Module A
------------------------------ */
.mod-a {}

```



#### 嵌套规范

```scss
/* 选择器嵌套 */
.jd {}
.jd-cover {}
.jd-info

/* scss */
.jd {
  &-cover{}
  &-info{}
}

/* 属性嵌套 */
.jd{
  background: {
    color: red;
    repeat: no-repeat;
  }
}

/* 变量 */
$base-color: red;
.jd{
  color: $color;
}

/* 混合mixin */
@mixin radius($radius: 5px) {
  -webkit-border-radius: $radius;
  border-radius: $raduis;    
}

.jd {
  @include: radius; // 参数使用默认值
}



```















