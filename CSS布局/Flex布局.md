## flex����

### ����������


#### 1 (����ķ��� ��Ŀ�����з���) flex-direction: row | row-reverse | column | column-reverse
![border](http://www.ruanyifeng.com/blogimg/asset/2015/bg2015071005.png)

#### 2 (��Ŀ����������) flex-warp��nowrap | wrap | wrap-reverse
![border](http://www.ruanyifeng.com/blogimg/asset/2015/bg2015071006.png)


#### 3 (flex-direction �� flex-flow�ļ�д) flex-flow: flex-start | flex-end | center | space-between | space-around

#### 4 (��Ŀ�������ϵĶ��뷽ʽ) justify-content: flex-start | flex-end | center | space-between | space-around

* flex-start��Ĭ��ֵ���������
* flex-end���Ҷ���
* center�� ����
* space-between�����˶��룬��Ŀ֮��ļ������ȡ�
* space-around��ÿ����Ŀ����ļ����ȡ����ԣ���Ŀ֮��ļ������Ŀ��߿�ļ����һ����

#### 5 ��Ŀ�ڽ�������ô���� align-items: flex-start | flex-end | center | baseline | stretch;
* flex-start��������������롣
* flex-end����������յ���롣
* center����������е���롣
* baseline: ��Ŀ�ĵ�һ�����ֵĻ��߶��롣
* stretch��Ĭ��ֵ���������Ŀδ���ø߶Ȼ���Ϊauto����ռ�����������ĸ߶ȡ�



## ��Ŀ������

#### order ������Ŀ������˳�� ��ֵԽд Խ��ǰ��Ĭ��Ϊ0 

![border](http://www.ruanyifeng.com/blogimg/asset/2015/bg2015071013.png)

#### flex-grow ������Ŀ�ķŴ���� Ĭ��0 
![border](http://www.ruanyifeng.com/blogimg/asset/2015/bg2015071014.png)
���������Ŀ��flex-grow���Զ�Ϊ1�������ǽ��ȷ�ʣ��ռ䣨����еĻ��������һ����Ŀ��flex-grow����Ϊ2��������Ŀ��Ϊ1����ǰ��ռ�ݵ�ʣ��ռ佫���������һ����

#### flex-shrink���� ��������Ŀ����С������Ĭ��Ϊ1��������ռ䲻�㣬����Ŀ����С��

![border](http://www.ruanyifeng.com/blogimg/asset/2015/bg2015071013.png)

#### flex-basis���Զ������ڷ������ռ�֮ǰ����Ŀռ�ݵ�����ռ䣨main size�������������������ԣ����������Ƿ��ж���ռ䡣����Ĭ��ֵΪauto������Ŀ�ı�����С��

#### flex���� flex-grow, flex-shrink �� flex-basis�ļ�д��Ĭ��ֵΪ0 1 auto�����������Կ�ѡ��

#### align-self������������Ŀ����������Ŀ��һ���Ķ��뷽ʽ���ɸ���align-items���ԡ�Ĭ��ֵΪauto����ʾ�̳и�Ԫ�ص�align-items���ԣ����û�и�Ԫ�أ����ͬ��stretch��

![border] (http://www.ruanyifeng.com/blogimg/asset/2015/bg2015071016.png)