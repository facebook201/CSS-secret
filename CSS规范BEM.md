###BEM CSS命名规范  .block_element--modifier


* 块(block) 
* 元素(element) 
* 修饰符(modifier)

block可以是由拉丁字母 数字 下划线。 下划线和搜索框 按钮可以说是一个块。都是search就是搜索块


####element 
一个元素可以是块的一部分。具有某种功能。元素是依赖上下文的。input和button都是元素。
.search_button(搜索按钮)。标致用来形容元素或块的外观，行为 状态。

####Modifier 是元素上的标志。
.block_color--black

```HTML
<form class="form form--them-xmas form-simple">
	<input class="form_input" type="text" />
	<input class="form_submit form_submit--disabled" type="submit" />
</form>
```

####如何更方便地使用BEM

以less为例。可以使用&符简化我们的代码:
```CSS
.form{
    width: 12rem;
    height: 6rem;
    &_input{
	font-size: 16px;
    }
    &_submit{
 	background: blue;
	&--disabled{
	    background: gray;
	}
    }
}
```