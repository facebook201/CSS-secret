## Flex布局

### 1 基本概念
任何一个容器都可以设为flex容器。display: flex; 容器默认两根轴 水平主轴 (main axis) 和垂直的交叉轴 (cross axis)。
![flex容器](http://www.ruanyifeng.com/blogimg/asset/2015/bg2015071004.png)

### 2 容器的属性
有下面6个属性设置在容器上。

1. flex-direction: 决定主轴的方向 (项目的排列方向)

     * row： (默认值 就是我们不显示的写明的时候 就自己默认为这个排列方向)：主轴为水平方向。起点在左端。
     * row-reverse： 主轴为水平方向 起点在右端
     * column：主轴为垂直方向 起点在上沿
     * column-reverse：主轴为垂直方向 起点在下沿

2. flex-wrap：默认情况下 项目排在一条线上。flex-wrap属性定义 如果一条轴线排不下 如何换行。

    * nowrap：默认 不换行
    * wrap：换行 第一行在上面
    * wrap-reverse: 换行 第一行在下面

3. flex-flow: 是上面两个属性的简写。 默认 row nowrap

4. justify-content: 定义了项目在主轴上的对齐方式

    * flex-start: 默认值 左对齐
    * flex-end: 右对齐
    * center: 居中
    * space-between: 两端对齐 项目之间的隔间都相等
    * space-around: 每个项目两侧的间隔相等 所以项目之间的间隔比项目与边框的间隔大一倍

5. align-items: 定义项目在交叉轴上如何对齐

    * flex-start：交叉轴的起点对齐。
    * flex-end：交叉轴的终点对齐。
    * center：交叉轴的中点对齐。
    * baseline: 项目的第一行文字的基线对齐。
    * stretch（默认值）：如果项目未设置高度或设为auto，将占满整个容器的高度


### 项目的属性

1. order: 定义项目的排列顺序 数值越小 排列越靠前 默认0

```CSS
.items{
    /* 假设items 是子项目 */
     order: -1;     /* 就会排列到前面 类似float的一点特性 但是会跟其他统计的项目比较。越小排的越前 */
}
```

2. flex-grow： 属性定义项目的放大比例 默认0 如果存在剩余空间 也不放大
    * 如果项目属性值为 1, 则它们将等分剩余空间(如果有的话) 如果父容器 1200px。现在三个子项目 宽度200px;
      那么剩余600px;那么剩余 600px会平分给他们三个 那他们就是400px;
      如果单独一个项目为1 那么它就会分剩下的空间。如果一个项目为2 其他项目为1  那么前者比后者多1个。

3. flex-shrink： 定义项目的缩小比例 默认1 如果空间不足 项目缩小

4. flex-basis：  定义了在分配多余空间之前 项目占据主轴空间。浏览器根据这个属性 计算主轴是否有多余空间。 默认auto
                比如 flex-basis: 500px; 可以设置像素值

5. flex：是 flex-grow flex-shrink flex-basis 简写。默认0 1 auto。后两个属性可选。

```HTML

<div class="container">
    <div class="box green"></div>
    <div class="box yellow"></div>
    <div class="box black"></div>
</div>

```
 ```CSS
/* 这里加入有三个子项目width 是200px,  父容器1200px 剩余600px */
.container{
    width: 1200px;
    .box{
        width: 200px;
    }
    /* 假如red的div */
    .red{
        flex: 1; /* 这里就会将剩下的600px分给红色的盒子 那么它就会变成800px */
        flex: 0 0 400px; /* 这里就会变成400px */
    }
}
 ```







*
