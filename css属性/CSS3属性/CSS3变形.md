## CSS3变形

* rotate() 函数通过指定的角度参数使元素相对原点进行旋转。旋转默认中心点
```CSS
    transform: rotate(45deg);
    transform-orangin: 50% 50%; //默认50% 安装中心点旋转
```

* skew() 扭曲 沿着X轴和Y轴倾斜的角度
* translate(X, Y) 将元素向指定的方向移动 类似于 position中的relative。
* scale(X,Y) 元素在水平和垂直方向上缩放。如果只有一个值表示水平和垂直方向都缩放
* 矩阵 matrix() 是一个含6个值的变换矩阵。用来指定一个2D变换 相当于直接应用一个[a b c d e f]
* 原点 transform-origin 原点位置
* 过渡 transition

##CSS3 中的变形与动画
@keyframes 关键帧 后面跟着是动画名称加上一对花括号{}
@keyframes changcolor{
	0% {background: red;}
	100% {background: green;}
}

animation: 调用动画。

* animation-name		动画名称
* animation-duration    	动画完成一个周期所花费的秒
* animation-timing-function	动画的速度曲线
* animation-delay		动画开始时间
* animation-iteration-count	动画被播放的次数
* animation-direction		动画是否在下一周期逆向播放
* animation-play-state		动画是否运行或暂停

