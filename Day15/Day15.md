## DAY15 - FDS  


#### 다양한 효과  


##### Effect 스타일링  


```css
a[class*="slide-"]{
	display: inline-block;
	position: relative;
	vertical-align: bottom;
	padding-bottom: 0.06em;
	border-bottom: none;
	overflow: hidden;
}

a[class*="slide-"]::after{
	position: absolute;
	content: attr(data-linktext);
	width: 100%;
	background: #1f74bf;
	color: #fff;
	transition: all 0.25s;
	text-align: center;
}

a.slide-from-top::after{
	top: -110%;
}

/* 
가상요소를 적용할 때 ::after이기 때문에 글자가 옆으로 치우쳐 있다. 그렇기 때문에 left: 0값을 줘서 설정해 줘야 hover,focus했을 때 글자가 보이게 된다. 
*/

a.slide-from-top:hover::after,
a.slide-from-top:focus::after{
	top: 0;
	left: 0;
}
```  


##### Grid System : push, pull, prefix, suffix  

* prefix, suffix는 축 자체를 움직일 때 사용한다.
* margin, padding 모두 사용 가능
```css
.grid .push-1 { left: 160px; }
.grid .push-2 { left: 320px; }
...  

.grid .pull-1 { right: 160px; }
.grid .pull-2 { right: 320px; }
...  

.grid .prefix-1 { margin-left: 160px; }
.grid .prefix-2 { margin-left: 320px; }
.grid .padding-prefix-1 { padding-left: 160px; }
.grid .padding-prefix-2 { padding-left: 320px; }
...  

.grid .suffix-1 { margin-right: 190px; }
.grid .suffix-2 { margin-right: 350px; }
.grid .padding-suffix-1 { padding-right: 160px; }
.grid .padding-suffix-2 { padding-right: 320px; }
...
```