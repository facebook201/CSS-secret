### box-shadow 盒子阴影

语法box-shadow: X轴偏移量(必) Y轴偏移量(Y) 阴影模糊半径(可) 阴影扩展半径(可) 阴影颜色(可) 投影方式(可)默认外阴影
多个阴影只需要用逗号隔开。
* 阴影模糊半径 只能是正值。如果为0 表示不具有模糊。
* 阴影扩展半径 可以实现多重边框 
```CSS
    box-shadow: 0 0 0 10px #000, 0 0 0 15px #f00;

    outline: #f00 solid 10px;
    outline-offset: 10px;    // 这个表示距离边框的距离
```
同时可以实现border-radius: 10px;圆角边框 阴影扩展半径也是圆角。
同时outline也可以实现多重边框。而且支持虚线,只不过不支持圆角的多重边框。

## box-shadow案例
* 3D小球
```CSS
height: 100px;
width: 100px;
padding: 10px;
background-color: rgba(100, 100, 100, .2);
border-radius: 50%;
box-shadow: -14px 8px 100px #333 inset,
	0 0 2px #888,
	3px -1px 4px #444;

// CSS3 折纸
.curved_box{
    display: inline-block;
    width: 200px;
    height: 248px;
    margin: 20px;
    background-color: #fff;
    border: 1px solid #eee;
    -webkit-box-shadow: 0 1px 4px rgba(0, 0, 0, 0.27), 0 0 60px rgba(0, 0, 0, 0.06) inset;
    -moz-box-shadow: 0 1px 4px rgba(0, 0, 0, 0.27), 0 0 40px rgba(0, 0, 0, 0.06) inset;
    box-shadow: 0 1px 4px rgba(0, 0, 0, 0.27), 0 0 40px rgba(0, 0, 0, 0.06) inset;
    position: relative;
    *zoom: 1;
}
 
.curved_box:before {
    -webkit-transform: skew(-15deg) rotate(-6deg);
    -moz-transform: skew(-15deg) rotate(-6deg);
    transform: skew(-15deg) rotate(-6deg);
    left: 15px;
}
.curved_box:after {
    -webkit-transform: skew(15deg) rotate(6deg);
    -moz-transform: skew(15deg) rotate(6deg);
    transform: skew(15deg) rotate(6deg);
    right: 15px;
}
 
.curved_box:before, .curved_box:after {
    width: 70%;
    height: 55%;
    content: ' ';
    
    -webkit-box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
    -moz-box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
    
    position: absolute;
    bottom: 10px;
    z-index: -1;    
}
```
### CSS3 文字字体和text-overflow 与 word-wrap 
text-overflow: clip(表示剪切) | ellipsis(表示超出部分使用省略号表示)


```CSS
	text-overflow: ellipsis;
	overflow: hidden;    // 溢出内容为隐藏	
	white-space: nowrap; // 强制文本在一行显示
```




