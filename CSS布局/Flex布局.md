## flex布局

### 容器的属性


#### 1 (主轴的方向 项目的排列方向) flex-direction: row | row-reverse | column | column-reverse
![border](http://www.ruanyifeng.com/blogimg/asset/2015/bg2015071005.png)

#### 2 (项目排在轴线上) flex-warp：nowrap | wrap | wrap-reverse
![border](http://www.ruanyifeng.com/blogimg/asset/2015/bg2015071006.png)


#### 3 (flex-direction 和 flex-flow的简写) flex-flow: flex-start | flex-end | center | space-between | space-around

#### 4 (项目在主轴上的对齐方式) justify-content: flex-start | flex-end | center | space-between | space-around

* flex-start（默认值）：左对齐
* flex-end：右对齐
* center： 居中
* space-between：两端对齐，项目之间的间隔都相等。
* space-around：每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍。

#### 5 项目在交叉轴怎么对齐 align-items: flex-start | flex-end | center | baseline | stretch;
* flex-start：交叉轴的起点对齐。
* flex-end：交叉轴的终点对齐。
* center：交叉轴的中点对齐。
* baseline: 项目的第一行文字的基线对齐。
* stretch（默认值）：如果项目未设置高度或设为auto，将占满整个容器的高度。



## 项目的属性

#### order 定义项目的排列顺序 数值越写 越靠前。默认为0 

![border](http://www.ruanyifeng.com/blogimg/asset/2015/bg2015071013.png)

#### flex-grow 定义项目的放大比例 默认0 
![border](http://www.ruanyifeng.com/blogimg/asset/2015/bg2015071014.png)
如果所有项目的flex-grow属性都为1，则它们将等分剩余空间（如果有的话）。如果一个项目的flex-grow属性为2，其他项目都为1，则前者占据的剩余空间将比其他项多一倍。

#### flex-shrink属性 定义了项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。

![border](http://www.ruanyifeng.com/blogimg/asset/2015/bg2015071013.png)

#### flex-basis属性定义了在分配多余空间之前，项目占据的主轴空间（main size）。浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为auto，即项目的本来大小。

#### flex属性 flex-grow, flex-shrink 和 flex-basis的简写，默认值为0 1 auto。后两个属性可选。

#### align-self属性允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。默认值为auto，表示继承父元素的align-items属性，如果没有父元素，则等同于stretch。

![border] (http://www.ruanyifeng.com/blogimg/asset/2015/bg2015071016.png)