# CSS ��ֱ����

<div class="center">
	<main>
		<p>Center me, please</p>
	</main>
<center>

##���ھ��Զ�λ�Ľ������ ��֪���߿�
```CSS
main{
	position: absolute;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
}
```
## ��ʹ��absolute�Ľ������
```CSS
main1{
	width: 18em;
	padding: 1em 1.5em
	margin: 50vh auto 0;
	transform: translateY(-50%);
	color: #fff;
}
```
##FlexBox  ���ȸ���Ԫ�ؼ���flex, ��Ԫ��ֻ��Ҫ����margin: auto;�������Ҫ�����p��ǩ�������ݴ�ֱ���С��Ǿ�Ҫָ����� ����ͽ������λ�á�
```CSS
main{
	align-items: center;
	justify-content: center;
	display: flex;
	height: 18em;
	width: 18em;
	margin: auto;
}
```
