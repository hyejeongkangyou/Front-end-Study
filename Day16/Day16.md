## DAY 16 - FDS


#### 다양한 effects

> background-clip: content-box
* background-clip은 배경색을 칠할 영역 설정(위에서는, content 영역만 배경색 적용)

> background-origin: padding-box
* 이미지 배치 영역 설정(위에서는 패딩영역부터 이미지 배치)
* 기본값은 border-box


###### cw와 ccw의 의미

* cw - clockwise(시계방향) 
* ccw - counter-clockwise(반시계방향)

#### 애니메이션

* 애니메이션 사용법

```css
@keyframes 애니메이션 이름 설정 {
  from { /* CSS 속성 */}
  to { /* CSS 속성 */}
}
@keyframes 애니메이션 이름 설정 {
  0% { /* CSS 속성 */}
  10% { /* CSS 속성 */}
  30% { /* CSS 속성 */}
  50% { /* CSS 속성 */}
  70% { /* CSS 속성 */}
  100% { /* CSS 속성 */}
}

.something:hover {
  animation: 애니메이션이름 0.3s;
}
```