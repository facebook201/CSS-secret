## CSS֮z-index�������

###1 z-index�Ļ���

* z-indexȡֵ��auto(Ĭ��) <integer>����ֵ inherit(�̳�)
* z-index���ԣ�֧�ָ�ֵ ֧��CSS3 animation���� ��Ҫ����λԪ�����(relative absolute fixed)

###2 z-index�붨λԪ��

* �������ϡ�
* �Ǹ�z-index��ֵ�� �ĸ�������

���z-index������Ƕ�ס�
```HTML
<div style="position: relative;z-index:1;">
	<img src="mm0.jpg" style="position:absolute;z-index: 2;"></img>
</div>
<div style="position: relative;z-index:1;">
	<img src="mm0.jpg" style="position:relatives;z-index: 1;"></img>
</div>

```
���ﲻ�������z-index�ж��ֻ������Ԫ�ص�z-indexֵ��˭��˭�����档����z-indexҪ����ֵ��
* ��������ԭ�� 

###3 ��������� �� ���ˮƽ

���������(stacking context)�൱��һ��z�ᡣ�����������Ķ�������z������ġ�
#### ���в��������
* ҳ���Ԫ���������в��������
* z-indexֵΪ��ֵ�Ķ�λԪ��Ҳ�в��������
* ��������

### ���˳�� С���� �������� �������� װ�������� 

* background/color ��ɫ��������
* ��z-index��
* block��״ˮƽ����
* float��������
* inline/inline-block	
* z-index:auto/0;
* z-index: ����

#### ���ˮƽ
����������е�Ԫ�ض��в��ˮƽ������ͬһ���������������z���������ʾ���ݡ�
��ѭ "��������" "˭��˭��"

