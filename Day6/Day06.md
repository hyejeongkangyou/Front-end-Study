## DAY06 - FDS

#### 선택자

###### CSS SELECTOR LIST

   유형    |    선택자    | 	설명
----------|------------|----------- 
일반 선택자|E|요소 선택자
		|E'(P)'' E'(C)'|자손선택자
		|*| 전체 선택자(Universal)
		|E[F]| F라는 속성을 가진 경우 선택
		|E[attr="bar"]|속성 값이 'bar'인 경우 선택
		|E[attr^="bar"]|속성의 값이 'bar'로 시작하는 경우 선택
		|E[attr~="bar"]|공백으로 구분되는 단어 중 'bar'가 일치할 때 선택
		|E[attr$="bar"]|속성의 값이 'bar'로 끝나는 경우 선택
		|E[attr|="en"]|하이픈(-)으로 구분되는 단어 중 'en'이 첫번재로 올 때 선택
		|E[attr*="bar"]|속성값을 포함하는 경우 선택
가상 클래스|E:root|루트 요소 선택
		|E:nth-child(n)|부모 요소의 자식 요소 중,(n)번째 자식 선택
		|E:nth-last-child(n)|부모 요소의 자식 요소 중, 뒤에서부터 (n)번째 자식 선택
		|E:first-child|부모 요소의 자식 중 첫번째 자식일 경우 선택
		|E:last-child|부모 요소의 자식 중 마지막 자식일 경우 선택
		|E:first-of-type|동일한 유형 중 첫번째 일 경우 선택
		|E:last-of-type|동일한 유형 중 마지막 일 경우 선택
		|E:only-child|부모 요소의 유일한 자식 요소일 경우 선택
		|E:only-of-type|동일한 유형 중 유일한 자식일 경우 선택
		|E:empty|자식이 없을 경우 선택
		|E:link|요소의 기본 상태
		|E:visited|요소의 방문한 상태
		|E:hover|요소에 마우스 커서가 올라간 상태
		|E:active|요소를 마우스 커서로 누른 상태
		|E:focus|요소에 키보드 포커스가 적용된 상태
		|E:not(selector)|()안의 선택자를 제외한 나머지 대상 요소 선택
가상 요소|E::before|요소 전에 내용을 만들어낸다
		|E::after|요소 다음에 내용을 만들어낸다
		|E::fisrt-line|요소 첫번째 라인에 속성을 적용한다
		|E::first-letter|요소 첫번째 글자에 속성을 적용한다

* 일반형제 선택자 VS 인접형제 선택자
  * 일반 형제 선택자는 인접 형제와 달리 인접하지 않아도 된다.
  * 인접 형제가 1개인데 반해, 일반 형제는 1개 이상이 될 수 있다.

```css
 #shoppingGrpTab> #shopping1 + h3 a{color:red;} /*이 경우 div의 직계 h3만을 찾아 적용한다*/
 #shoppingGrpTab> #shopping1 ~ h3 a{color:yellow;} /*이 경우 div에 인접한 h3를 모두 찾아 적용한다*/
```
