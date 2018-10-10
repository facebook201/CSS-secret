# z-index

* z-index 在跟css3之前 只有跟定位元素属性配合才有效 relative absolute fixed sticky。





### 如果定位元素没有发生嵌套

* 后来居上原则 
* 那个大 那个上

**后来居上 后面的会在前面的上面**



### 如果发生了嵌套

* 祖先优先原则

  ```html
  <div style="position: relative; z-index: 1;">
    <img src="pkq.jpg" style="position: absolute; z-index: 2;">
  </div>
  <div style="position: relative; z-index: 1;">
    <img src="pkq.jpg" style="position: absolute; z-index: 1;">
  </div>
  ```

  **z-index值不能为auto。当它为auto时。不会创建一个层叠上下文。**




#### z-index 实践分析

> 1、最小化影响原则

* 避免z-index 嵌套混乱
* 元素的层叠水平主要有层叠上下文决定

**避免使用定位属性 定位属性从大容器分离为小容器**



> 不犯二原则

避免z-index 混乱。一层盖住一层。

**对于非浮层元素 避免设置z-index。其值不要超过2**



> 组件层级计数器

通过js获取body下元素的最大z-index值。 外来的组件获取z-index 让浮层最大。



> z-index 负值在背景之上

可以使用这个特性来做提交按钮

```html
  <form>
    <input type="text">
    <input type="submit" id="submit">
    <label for="submit" class="label-btn">提交</label>
  </form>
```



```css
  .input[type="submit"] {
      position: absolute;
      z-index: -1;
    }
 .label-btn {
     cursor: pointer;
     border-radius: 5px;
     background-color:tomato;
     color: #fff; 
     padding: 8px 15px;
}
```

















