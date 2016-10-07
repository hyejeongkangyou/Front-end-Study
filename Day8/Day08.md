## DAY 08 - FDS

#### 속기 스타일  

* 속기 스타일은 명시적이지 않아 명시적인 방법을 더 권고한다.
* margin: 100px auto = margin-top: 100px
					   margin-right: auto
					   margin-left: auto

  ```css
  margin: top right bottom left
  margin: top right(left) bottom
  margin: top(bottom) right(left)
  margin: top(top, right, bottom, left)
  ```

#### 세로 중앙 정렬  

* [IE 비표준 모드]에서 박스의 폭은 padding과 border 값을 포함한다. margin: auto 또한 작동하지 않는다.
* IE에서 레이아웃이 꺠진다면 이러한 이슈를 고려할 수 있다.

#### Margin collapsing  

* 세로로 2개 이상 블록요소의 마진이 만났을 때, 마진이 겹쳐지는 현상
* 부모 요소 안에 자식 요소의 경우, 부모에게 padding, border의 값이 없을 때 발생

  ###### [부모요소의 패딩(혹은 보더)값이 없을 경우]
   * 자식 마진이 부모의 마진보다 클 경우 부모 바깥 범위에 영향을 미친다.
   * 부모요소에 패딩(혹은 보더) 값을 주어 자식요소의 마진이 부모요소 내부에만 영향을 주도록 한다.



#### Font  

```css
p {
    /* 띄어쓰기가 들어갈 경우 쌍따옴표로 묶어준다. 앞선 순서대로 폰트 적용 */
    font-family: "Times New Roman", Times,"Nanum Gothic", "나눔 고딕", 돋움, Dotum, san-serif}
}
```