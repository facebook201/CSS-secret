### CSS3 transform

常用的变形是 

* rotateX: 在X轴上旋转 指定的角度
* rotateY: 在Y轴上旋转 指定的角度
* rotateZ: 在Z轴上旋转 指定的角度



perspective属性 透视 视角。这个属性允许你改变3D元素是怎样查看透视图。定义 时的perspective属性。

它是一个元素的子元素 而不是本身。 怎么理解这句话。就是说 这个属性它定义自己没有用。要在它的子元素才有有 看例子

```css
.parent{
  perspective: 200;
  -webkit-perspective: 200;
}
/* 配合父元素的perspective 才能看出效果 */
.child{
   height: 200px;
   width: 200px;
   background-color: palevioletred;
   transform: rotateX(10deg);
}
```

perspective-origin 属性定义3D 元素所基于的X轴和Y轴。



#### 正负旋转相消

为了和文案里面的 3D 动画扯上关系，我们先给这几个元素添加 3D 转换：

```
div {
    transform-style: preserve-3d;
    perspective: 500px;
}
```

接着，尝试修改上面的旋转动画，在内层旋转上额外添加一个 rotateX：

```css
@keyframes rotate {
    0% {
        transform: rotateX(0deg) rotateZ(0deg);
    }
    /* 主要的一行 */
    50% {
        transform: rotateX(40deg) rotateZ(180deg);
    }
    100% {
        transform: rotateX(0deg) rotateZ(360deg);
    }
}
```

![border](https://user-images.githubusercontent.com/8554143/29659798-e3e366dc-88f1-11e7-98a3-3d7d913d7480.gif)



#### 动画相同 缓动不同

有的时候我们页面有相同的元素。为了不让动画那么死板 可以给与相同的动画 不同的缓动函数。达到动画效果。

```html
<div class="container">
      <div class="ball ball1"></div>
      <div class="ball ball2"></div>
      <div class="ball ball3"></div>
    </div>
```



```css
/* 动画相同 缓动不同 */
.ball {
  display: inline-block;
  height: 20px;
  width: 20px;
  border-radius: 50%;
  background-color: #000;
}
.ball1 {
  animation: move 1s ease-in infinite alternate;
}
.ball2 {
  animation: move 1s linear infinite alternate;
}
.ball3 {
  animation: move 1s ease-out infinite alternate;
}
@keyframes move{
  100% {
    transform: translateY(100px);
  }
}
```



animation: name duration timing-function delay iteration-count direction fill-mode play-state

animation-name：动画名称 

animation-duration：动画需要多少秒完成

animation-timing-function：设置动画将如何完成一个周期 linear ease-in ease-out 

animation-delay：设置动画在启动前的延迟间隔

animation-iteration-count: 定义动画的次数 infinite 可以写明次数

animation-direction ：是否应该轮流方向播放动画 alternate;



#### 奇妙的缓动

timing-function 在动画中占据了非常重要的地位。 当你不想使用CSS。可以定义

cubic-bezier(1, 1, 0, 0);  



## 动画层级的控制，保持动画层级在最上方

动画层级的控制的意思是**尽量让需要进行 CSS 动画的元素的 z-index 保持在页面最上方，避免浏览器创建不必要的图形层（GraphicsLayer）**，能够很好的提升渲染性能。

简单来说，浏览器为了提升动画的性能，为了在动画的每一帧的过程中不必每次都重新绘制整个页面。在特定方式下可以触发生成一个合成层，合成层拥有单独的 GraphicsLayer。

需要进行动画的元素包含在这个合成层之下，这样动画的每一帧只需要去重新绘制这个 Graphics Layer 即可，从而达到提升动画性能的目的。

那么一个元素什么时候会触发创建一个 Graphics Layer 层？从目前来说，满足以下任意情况便会创建层：

- 硬件加速的 iframe 元素（比如 iframe 嵌入的页面中有合成层）
- 硬件加速的插件，比如 flash 等等
- 使用加速视频解码的 元素
- 3D 或者 硬件加速的 2D Canvas 元素
- 3D 或透视变换(perspective、transform) 的 CSS 属性
- 对自己的 opacity 做 CSS 动画或使用一个动画变换的元素
- 拥有加速 CSS 过滤器的元素
- 元素有一个包含复合层的后代节点(换句话说，就是一个元素拥有一个子元素，该子元素在自己的层里)
- 元素有一个 z-index 较低且包含一个复合层的兄弟元素



- GPU 硬件加速也会有坑，当我们希望使用利用类似 `transform: translate3d()` 这样的方式开启 GPU 硬件加速，一定要注意元素层级的关系，尽量保持让需要进行 CSS 动画的元素的 `z-index` 保持在页面最上方。
- Graphics Layer 不是越多越好，每一帧的渲染内核都会去遍历计算当前所有的 Graphics Layer ，并计算他们下一帧的重绘区域，所以过量的 Graphics Layer 计算也会给渲染造成性能影响。
- 可以使用 Chrome ，用上面介绍的两个工具对自己的页面生成的 Graphics Layer 和元素层级进行观察然后进行相应修改。
- 上面观察页面层级的 chrome 工具非常吃内存？好像还是一个处于实验室的功能，分析稍微大一点的页面容易直接卡死，所以要多学会使用第一种观察黄色边框的方式查看页面生成的 Graphics Layer 这种方式。



