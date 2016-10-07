## DAY 13 - FDS

#### background  

###### background-size: cover
 * 이미지가 요소보다 크다는 가정하에 가로, 세로 길이가 요소를 가득 채우게 된다.(이미지가 잘릴 수 있음)
 * 가로 세로 비율이 유지된다.  

###### background-size: contain
 * 이미지가 가로, 세로 길이 모두 엘리먼트 안에 들어온다는 조건하에 가능한한 배경 이미지를 크게 조정한다. 
 * 가로, 세로 비율이 유지된다. 따라서 배경 이미지 크기는 cover와 다르게 요소보다 항상 작거나 같다.  

###### 기타
01-grid.html의 class가 footer인 `<section>`에 empty라는 class명을 가진 `<div>`를 배치시키려고 했을 때 발생한 문제점 및 해결방안

- margin-top과 margin-bottom이 그 상위 요소인 footer에 적용이 됨.
- margin-collapsing 현상
  [조건]부모요소의 패딩(혹은 보더)가 없을 경우:  
  - 자식 마진이 부모의 마진보다 클 경우 부모 바깥 범위에 영향을 끼친다.
  - 부모요소에 패딩(혹은 보더) 값을 주어 자식요소의 마진이 부모요소 내부에만 영향을 주도록 한다.
- 부모인 .footer에 border: 1px solid transparent와 box-sizing: border-box를 설정하여 문제를 해결함.


###### 참고
[1. CSS 단위 관련 사이트]
http://webdesign.tutsplus.com/ko/articles/7-css-units-you-might-not-know-about--cms-22573
[2. Grid 관련 사이트]
http://pixelbuddha.net/ui-tiles/