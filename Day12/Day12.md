## DAY 12 - FDS

#### Typography System  

###### 모듈러 스케일(Modular Scale)  
관계된 객체간에 개별적으로 일정한 배율(ratio)이 반영된 수의 나열이다.  

###### 베이스 라인(Baseline)  
행(row) 사이 간격으로 글자크기를 포함하는 높이

###### 버티컬 리듬(Vertical Rhythm)  
각 요소(Element)간의 수직적인 공간 배열 관계

###### 모듈러 스케일을 반영한 제목 글자 디자인(크기/행간/마진)
> 폰트 크기(font-size) : 이전 폰트 크기(previous-font-size) x 타입 배율(type scale)

```css
/**
 * 제목 디자인
 * h1~6
 * ---------------------------------------------
 * 글자 크기 배율(Type Scale): x1.24
 * 본문 기본 글자 크기(Base Font Size): 16px = 1em
 * ※ 소수점은 4자리까지 끊고 절삭.
 * ------------------------------------------- */
h6 { font-size: 1.24em;   } /* x1.24 */
h5 { font-size: 1.5376em; } /* x1.24 */
h4 { font-size: 1.9066em; } /* x1.24 */
h3 { font-size: 2.3642em; } /* x1.24 */
h2 { font-size: 2.9316em; } /* x1.24 */
h1 { font-size: 3.6352em; } /* x1.24 */
```  


###### 행간 설정 공식

> 글자 크기에 따라 차지하는 행의 개수 = ceil( 글자 크기 비율(font-size) ÷ 기본 행간 비율(base-line-height) )<br>
> ※ ceil()은 올림 함수

> 행간 비율(line-height) = 행의 개수 × ( 기본 행간 비율(base-line-height) ÷ 글자 크기 비율(font-size) )

```css
/*
[ line-height을 구하는 공식 ]
1) ceil( 글자 크기 비율(1.24) ÷ 기본 행간 비율(1.5) ) = 글자 크기가 차지하는 행의 개수
   1.24/1.5 = .826666667 => 1개
2) 기본 행간 비율(1.5) ÷ 글자 크기 비율(1.24) × 행의 개수
   1.5/1.24 = 1.209677419 * 1
*/
```

```css
h6 {
  font-size: 1.24em;
  line-height: 1.21; /*  line-height: 1.2096; (※ 행간을 소수점 3번째 자리까지 쓰되 올림 (다소 어긋난 높이 조정)) */
}
```

-

###### 마진 설정 공식

> 기본 행간 비율(1.5) ÷ 글자 크기 비율(1.24)<br>
> ※ 소수점 4자리에서 끊고 절삭.

```css
h6 {
  font-size: 1.24em;
  line-height: 1.21;
  /*
  [ margin-bottom을 구하는 공식 ]
  기본 행간 비율(1.5) ÷ 글자 크기 비율(1.24)
  1.5/1.24 = 1.209677419
  */
  margin-bottom: 1.2096em;
}
```
-

#### 기타

###### position  

 - `static` :
  - default. 모든 요소의 기본값
 - `relative` :
  - 원래 위치에서 상대적, 주는 속성(top, left, right, bottom)에 따라 이동
  - 일반 흐름(normal flow)에 영향을 주지 않는다
 - `absolute` :
  - offsetParent
  - 부모 위치에서 상대적, relative 처럼 속성에 따라 이동
  - 부모 요소는 자격이 필요하다. position 값이 static이 아닌 가장 가까운 부모요소를 찾는다.
  - 일반 흐름(normal flow)에 영향을 준다.
  - display 값이 block으로 변경된다.
  - 일반적으로 `absolute`의 부모에 `relative`를 주는 이유는 일반흐름을 깨지 않기 때문이다.
  - `float`의 경우 부모요소가 float된 요소를 감쌀 수 있는 방법이 있으나, `absolute`는 height를 지정하여야 한다.
 - `fixed` :
  - `absolute`와 유사하게 처리되나 결과는 다르다
  - 고정형태로 위치가 설정된다. 화면 스크롤과 상관 없이 항상 그 자리를 유지한다.

 - `z-index` :
  - z-index속성은 반드시 position 속성(static 제외)과 함께 사용된다.
  - `z-index` 속성값은 양의 정수, 0, 음의 정수 사용가능
  - 1단위가 아닌 10 또는 100단위로 사용하는 것이 유지보수 관점에서 권장된다.
  - [부모 A, [자식 C]] + [부모 B, [자식 D]]

###### 그림자 효과 Shadow Effect

```css
/* box-shadow: [inset] x y blur spread color; */
box-shadow: 0 6px 5px #eaeaea; /* 그림자가 바깥쪽 방향으로 생김 */
box-shadow: inset 0 6px 5px #eaeaea; /* 그림자가 안쪽 방향으로 생김 */

/* text-shadow: x y blur spread color; */
text-shadow: 0 2px 1px #828282;
```

-

참고 [Type Scale](http://type-scale.com/)