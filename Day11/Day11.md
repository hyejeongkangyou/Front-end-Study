## DAY 11 - FDS

#### box-sizing  

box-sizing 설명 : ![ box-sizing:border-box, box-sizing: content-box 비교 ](/Users/Laura/Desktop/FDS/Day11/images/box-sizing.png)  

* box-sizing: border-box로 설정을 하게 되면 padding이나 border를 설정하게 되어도 그림이 깨지지 않는다.  

```css
/* 해외에서 많이 사용하는 코드 */
body *, body *::before, body *::after{
box-sizing: border-box
}
/* 자신의 사이즈안에서 컨텐츠를 감싸게 됨. */
```

#### overflow-y: scroll  

* 내용이 감싸고 있는 박스보다 세로로 커지게 되었을 때 스크롤을 사용하게 되면 좌우로 스크롤이 생겨 UI가 움직이게 되기 때문에 overflow-y: scroll로 설정해 주어 스크롤을 설정해 준다.  