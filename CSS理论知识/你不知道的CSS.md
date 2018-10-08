### CSS的盒子位置



CSS布局的核心在于如何将一系列HTML 元素映射到一组盒子上。所有的布局方案决定的。



### Position schemes

* normal flow 包括 block inline relative formatting context
* floats 与常规流互动 构成了 grid 框架的基础
* absolute 定位 处理absolute 和 fixed 元素相对于 normal flow的定位



布局的layout存在两方面起作用

* 元素的盒子大小和对其方式 通常由display的属性 width height margin 控制
* 一个特定父元素的子元素是如何相对于彼此放置的



一个父元素的子元素的相对位置是通过父元素为子元素建立的 格式化上下文控制

> BFC 块级格式化上下文 一般来说建立了一个新的块级格式化上下文。



Margin collapse 

* 两者处于同一BFC下的 in-flow block-level boxes
* 两者间不存在 line boxes clearnce padding border
* 都处于垂直相邻的盒子边缘



>第一个条件 只有处于同一个BFC的盒子才能发生 margin collapse 假如父元素创建了新的BFC  那么父元素和子元素不是同一个BFC下。 那么可以阻止 margin collpase。相反若子元素创建了新的 BFC。那么子元素和父元素仍然处于同一个BFC下 



















