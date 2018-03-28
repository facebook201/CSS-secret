##### 实现的效果

![border](https://user-images.githubusercontent.com/8554143/37917279-8f6fd236-3150-11e8-8b8d-fca96d1d6001.gif)

上面这个动态的效果图 怎么实现。



> 首先可以看到是在hover的时候实现的。其次我们可以是border-bottom 来表示下划线。但是如果直接隐藏的话 li是无法移动的。所以我们可以尝试其他方法 伪元素。

```Css
li:before {
    constent: '';
    position: absolute;
    top: 0;
    left: 100%;
    width: 0;
    height: 100%;
    transition: 0.2s all linear;
    border-bottom: 2px solid #ccc;
}
li:hover::before {
    left: 0;
    width: 100%;
}
li:hover ~ li::before {
    left: 0;
}
```







