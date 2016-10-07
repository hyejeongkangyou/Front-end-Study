## DAY 20 - FDS

#### Flexible Video  

##### HTML5 <video>
##### Youtube, Vimeo 비디오 파일(iframe, object, embed)  
* `<video>`와 달리 `<iframe>`은 `<iframe>`을 감싸는 컨테이너 요소가 필요
* position 속성 필요(iframe요소는 absolute 부모요소는 relative)
* iframe요소에 `top: 0; width: 100%; height: 100%;`
* 부모 컨테이너 요소에는 `height: 0; padding-bottom: 스크린비율`

-

#### 미디어 쿼리

```css
@media only screen and (조건문) {실행문}
```

* screen: screen 키워드는 미디어 쿼리를 해석해야 할 대상 미디어를 선언한 것이다. 
* all 이면 모든 미디어가 이 구문을 해석해야 한다. all 키워드 대신 screen 또는 print와 같은 특정 미디어를 구체적으로 언급할 수도 있다. 
* all 키워드는 생략 가능하고 생략했을 때 기본 값은 all 으로 처리된다. 
* 이 밖에도 다양한 미디어 타입(all, aural, braille, embossed, handheld, print, projection, screen, speech, tty, tv)이 있다. 
* all, screen, print를 가장 널리 쓴다.


###### orientation

* 뷰포트의 너비와 높이 비율을 이용하여 세로 모드인지 가로 모드인지를 판단한다.

* Value : portrait | landscape

```css
@media all and (orientation:portrait) { … } 
// 세로 모드. 뷰포트의 높이가 너비에 비해 상대적으로 크면 실행

@media all and (orientation:landscape) { … } 
// 가로 모드. 뷰포트의 너비가 높이에 비해 상대적으로 크면 실행
```

##### aspect-ratio  

* 뷰포트의 너비와 높이에 대한 비율. '너비/높이'순으로 조건을 작성.
* min/max 접두사를 사용하여 너비 값의 최소/최대 비율을 설정.
* Value: <ratio>

```css
@media all and (aspect-ratio:5/4) { … } 
// 뷰포트 너비가 5, 높이가 4 비율이면 실행

@media all and (min-aspect-ratio:5/4) { … } 
// 뷰포트 너비가 5/4 비율 이상이면 실행

@media all and (max-aspect-ratio:5/4) { … } 
// 뷰포트 너비가 5/4 비율 이하면 실행
```
-
##### 참고  

[CSS 미디어쿼리 이해](http://naradesign.net/wp/2012/05/30/1823/)