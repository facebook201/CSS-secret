###BEM CSS�����淶  .block_element--modifier


* ��(block) 
* Ԫ��(element) 
* ���η�(modifier)

block��������������ĸ ���� �»��ߡ� �»��ߺ������� ��ť����˵��һ���顣����search����������


####element 
һ��Ԫ�ؿ����ǿ��һ���֡�����ĳ�ֹ��ܡ�Ԫ�������������ĵġ�input��button����Ԫ�ء�
.search_button(������ť)��������������Ԫ�ػ�����ۣ���Ϊ ״̬��

####Modifier ��Ԫ���ϵı�־��
.block_color--black

```HTML
<form class="form form--them-xmas form-simple">
	<input class="form_input" type="text" />
	<input class="form_submit form_submit--disabled" type="submit" />
</form>
```

####��θ������ʹ��BEM

��lessΪ��������ʹ��&�������ǵĴ���:
```CSS
.form{
    width: 12rem;
    height: 6rem;
    &_input{
	font-size: 16px;
    }
    &_submit{
 	background: blue;
	&--disabled{
	    background: gray;
	}
    }
}
```