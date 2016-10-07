##Day 10

#### float된 하위요소에 대처하는 상위요소  
* HTML 모든 요소는 float속성 기본값이 none으로 설정되어 있다.
* 이를 사용자가 필요에 따라 float 방향을 왼쪽(left), 오른쪽(right)로 설정할 수 있다.
* 이에 따라 float이 적용된 요소의 뒤에 마크업(구조화)된 요소는 float의 영향을 받는다.

###### 첫번째 방법: 부모요소도 float으로 띄우기
* 이 방식은 무한 float에 빠지는 치명적인 결함이 있어 권장하지 않음

###### 두번째 방법: 새로운 요소를 사용해 클리어 하기
```html
<div class="parent">
    <div class="child">Child Element 1</div>
    <div class="child">Child Element 2</div>
    <div class="child">Child Element 3</div>
    <div class="clear"></div>
</div>
```
```css
.clear{
	clear: both;
}
```
* 마지막 하위요소가 clear속성을 가지게 되면 상위 요소가 나머지 하위 요소들을 자식으로 감싸게 된다.
* 이 방식은 무의미한 요소를 추가하게 되어 좋은 구현이라 하기 어렵다.

###### 세번째 방법: overflow 속성값을 hidden 또는 auto로 설정
```css
.float-container {
    overflow: hidden;
    overflow: auto;
}
```  
* 많이 쓰이는 코드이나 권장하지 않는다.
* 문제사항을 수반한 해결방법이다.

###### 네번째 방법: ::after 가상요소를 이용하라(.clearfix) - 권장
```css
.clearfix::after {
    clear: both;
    display: block;
    content: '';
}

css
.lt-ie8.new-clearfix{
	zoom:1;
}
/* E 6,7고려한 방식 */

```  
* 최적의 방식
* cler: both의 의미는 float:left, float:right 둘 다를 해제하겠다는 의미이다.


#### 기타

###### overflow:hidden  

* 이미지 하단에 공백을 형성하여 옆으로 배치되는 글들이 동일한 공간을 가질 수 있게 한다.
* div로 글을 묶어서 css 속성에 overflow를 주게 되면 하나의 덩어리로 표현이 가능하다. 즉, 그림 밑으로 글이 들어가지 않고 한 라인으로 글이 들어가게 된다.




