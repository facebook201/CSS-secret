### CSS 层叠概念

重要的几个概念 

* 层叠上下文 stacking context
* 层叠等级 stacking level
* 层叠顺序 stacking Order





#### 层叠上下文 （Stacking Context）

层叠上下文是三维概念 每个元素的位置是三维的，当元素发生层叠 这时它可能覆盖了其他元素或者被其他元素覆盖。 排在Z轴越靠上的位置 距离屏幕观察者越近



- 根元素`<html></html>`
- `position`值为`absolute | relative`，且`z-index`值不为 `auto`
- `position` 值为 `fixed | sticky`
- `z-index` 值不为 `auto` 的flex元素，即：父元素`display: flex | inline-flex`
- `opacity` 属性值小于 `1` 的元素
- `transform` 属性值不为 `none`的元素
- `mix-blend-mode` 属性值不为 `normal` 的元素
- `filter`、`perspective`、`clip-path`、`mask`、`mask-image`、`mask-border`、`motion-path` 值不为 `none` 的元素
- `perspective` 值不为 `none` 的元素
- `isolation` 属性被设置为 `isolate` 的元素
- `will-change` 中指定了任意 CSS 属性，即便你没有直接指定这些属性的值
- `-webkit-overflow-scrolling` 属性被设置 `touch`的元素



1. 层叠上下文可以包含在其他层叠上下文中，并且一起组建了一个有层级的层叠上下文
2. 每个层叠上下文完全独立于它的兄弟元素，当处理层叠时只考虑子元素，这里类似于[BFC](https://link.juejin.im/?target=https%3A%2F%2Fsegmentfault.com%2Fa%2F1190000013023485)
3. 每个层叠上下文是自包含的：当元素的内容发生层叠后，整个该元素将会**在父级叠上下文**中按顺序进行层叠





### 层叠等级

决定了同一个层叠上下文中元素在Z轴上显示顺序的概念：

- 普通元素的层叠等级优先由其所在的层叠上下文决定
- 层叠等级的比较只有在同一个层叠上下文元素中才有意义
- 在同一个层叠上下文中，层叠等级描述定义的是该层叠上下文中的元素在Z轴上的上下顺序



### Z-index

z-index 只适用于定位的元素，对非定位元素无效，它可以被设置为正整数、负整数、0、auto，如果一个定位元素没有设置 z-index，那么默认为auto；

**元素的 z-index 值只在同一个层叠上下文中有意义**。如果父级层叠上下文的层叠等级低于另一个层叠上下文的，那么它 z-index 设的再高也没用。所以如果你遇到 z-index 值设了很大，但是不起作用的话，就去看看它的父级层叠上下文是否被其他层叠上下文盖住了。





### 层叠顺序

**层叠顺序** (层叠次序, 堆叠顺序, Stacking Order) 描述的是元素在同一个层叠上下文中的顺序**规则**，从层叠的底部开始，共有七种层叠顺序：

1. **背景和边框**：形成层叠上下文的元素的背景和边框。
2. **负z-index值**：层叠上下文内有着负z-index值的定位子元素，负的越大层叠等级越低；
3. **块级盒**：文档流中块级、非定位子元素；
4. **浮动盒**：非定位浮动元素；
5. **行内盒**：文档流中行内、非定位子元素；
6. **z-index: 0**：z-index为0或auto的定位元素， 这些元素形成了新的层叠上下文；
7. **正z-index值**：z-index 为正的定位元素，正的越大层叠等级越高；



![border](https://user-gold-cdn.xitu.io/2018/9/21/165fc538e321d802?imageView2)







### 张鑫旭老师的z-index 视频教程



















