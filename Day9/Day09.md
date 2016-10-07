## DAY 09 - FDS  


### 타이포그래피 속성  

#### 행간(line-height): normal(default)  
* 1.5~2 사이 값을 권장(상대값을 사용하여 font-size 변동에 자동으로 반응하도록 설정)

###### font 속기 작성법
```css
p{
	font: [style] [weight] [variant] size[/line-height] family;
	/* []괄호속성은 옵션 */
	/* variant, style, weight는 순서가 바뀌어도 상관 없다. */
}
```  

#### IR기법(Image Replacement)  
* 의미가 포함되어 있는 image를 배경으로 표현하고, 그에 상응하는 내용을 text로 전경에 기입하는 방법
* 비장애인의 경우 이미지로 처리된 화면을 볼 수 있지만 화면 낭독기를 사용하는 시작장애인의 경우 css제거 및 인쇄시에는 문자에 접근하거나 문자를 볼 수 있는 형태로 설계하는 기법을 의미한다.

```html
<h1 class="brand-tweetle"><a href>Web Design</a></h1>
```

```css
.brand-tweetle {
    display: block;
    width: 32px;
    height: 32px;
    background-image: url('...');
    background-repeat: no-repeat;
    text-indent: -9999em;
}
/* 이미지와 겹친 텍스트를 보이지 않게 하지만 스크린리더가 읽을 수 있다. 접근성 이슈가 있다. */
```

#### CSS 레이아웃

###### display  

  * block: 폭은 부모만큼, 높이는 자식만큼 갖는다.
  * inline: 폭, 높이를 자식만큼 갖는다.
  * inline-block: 외부는 inline처럼, 내부는 block처럼 작동한다.
  * none: 보이지 않는다. 스크린리더에도 읽히지 않음

###### overflow  

  * visible: 기본값
  * hidden: 부모보다 넘치는 자식은 보이지 않음
  * auto: 내용이 넘칠경우 스크롤이 생김
  * scroll: 내용이 넘치지 않아도 스크롤이 보임

###### float  

  * 본래 목적은 이미지 주변으로 텍스트를 둘러싸기 위함이다.
  * float속성을 보여하면 모니터 위쪽으로 부유하게 된다.
  * 여러 박스의 높낮이를 다르게 설정한 후 float을 주면 테트리스처럼 float drop현상이 일어난다.
  * 실제 레이아웃을 위한 목적이 아니므로 float속성을 이용할 경우 다양한 경험을 할 수 있다.