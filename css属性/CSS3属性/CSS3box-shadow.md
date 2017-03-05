### box-shadow ������Ӱ

�﷨box-shadow: X��ƫ����(��) Y��ƫ����(Y) ��Ӱģ���뾶(��) ��Ӱ��չ�뾶(��) ��Ӱ��ɫ(��) ͶӰ��ʽ(��)Ĭ������Ӱ
�����Ӱֻ��Ҫ�ö��Ÿ�����
* ��Ӱģ���뾶 ֻ������ֵ�����Ϊ0 ��ʾ������ģ����
* ��Ӱ��չ�뾶 ����ʵ�ֶ��ر߿� 
```CSS
    box-shadow: 0 0 0 10px #000, 0 0 0 15px #f00;

    outline: #f00 solid 10px;
    outline-offset: 10px;    // �����ʾ����߿�ľ���
```
ͬʱ����ʵ��border-radius: 10px;Բ�Ǳ߿� ��Ӱ��չ�뾶Ҳ��Բ�ǡ�
ͬʱoutlineҲ����ʵ�ֶ��ر߿򡣶���֧������,ֻ������֧��Բ�ǵĶ��ر߿�

## box-shadow����
* 3DС��
```CSS
height: 100px;
width: 100px;
padding: 10px;
background-color: rgba(100, 100, 100, .2);
border-radius: 50%;
box-shadow: -14px 8px 100px #333 inset,
	0 0 2px #888,
	3px -1px 4px #444;

// CSS3 ��ֽ
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
### CSS3 ���������text-overflow �� word-wrap 
text-overflow: clip(��ʾ����) | ellipsis(��ʾ��������ʹ��ʡ�Ժű�ʾ)


```CSS
	text-overflow: ellipsis;
	overflow: hidden;    // �������Ϊ����	
	white-space: nowrap; // ǿ���ı���һ����ʾ
```




