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

* ​









