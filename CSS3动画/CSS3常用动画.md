#### CSS3 transform 

改变 使...变形;  转换

常用属性？

rotate() / skew() / scale() / translate(,) 

* transform: rotate(); // 表示deg 旋转的度 10deg 表示10度
* transform: rotate(); // skew() 倾斜的角度
* transform: scale(); // 缩放 法大比例 放大2倍就是 '2.0';

  可以应用在 字体缩小的情况。比如说 浏览器最小是12px。

* transform: translate(); // 位移 表示向右位移120像素 向上位移 

#### CSS3 transition

css的transition 允许css的属性值在一定时间内平滑的过渡。可以通过鼠标单击、获得焦点、被点击对元素任何改变中触发。圆滑的以动画效果改变css的属性值。

* transition-duration: <time> ; // 指定元素转换过程的持续时间  
* transition-timing-function: ease | linear | ease-in | ease-out | ease-in-out | cubic-bezier ;

  ease 逐渐变慢  linear 匀速 ease-in 加速 ease-out 减速 ease-in-out 加速然后减速 
  
* transition-delay: <time> ; // 用来指定一个动画开始执行的时间。 

#### 动画的几个关键点

* 我们可以利用opacity 透明度来设置 从0 到 1 用多久时间
* 我们可以从height 从 0 到 多少来更加描述一个从上过渡到下的动画 
  ​




#### CSS3 动画 animation @keyframe



* animation-name: 动画名称
* animation-duration: 元素播放动画所持续的时长。
* animation-tiing-function: 元素根据时间的推进来改变属性值得变化速率 动画的播放方式
* Animation-delay: 指定元素动画开始时间。
* animation-iteration-count: 指定元素播放动画的循环次数，默认值1.





















