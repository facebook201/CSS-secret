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

