## DAY 17 - FDS

#### Media Query  

```css  

 @media only screen and (min-width: 25rem) {
        .masonry-container {
            -moz-column-count: 1;
            -webkit-column-count: 1;
            column-count: 1;
        }
    }
```

* `only` 키워드는 미디어쿼리를 지원하는 웹브라우저에서만 조건을 인식하도록 하는 키워드. 미디어쿼리를 지원하지 않는 웹브라우저의 경우 ONLY 키워드가 있으면 미디어 쿼리가 무시되어 실행되지 않아야 한다.

###### CSS Multi Columns  

* `column-count` : 화면에 보일 column의 수를 설정한다.
* `column-gap` : column 사이 간격(GAP) 
* `column-rule` : 컬럼 사이 간격의 중앙에 배치되는 수직 선
* `column-span`: 
	- all : 제목을 모든 컬럼 위로 빼낸다.
	- 1 : default value(기본값). 1개 컬럼 위로 제목이 온다.
	- initial : 기본값으로 설정된다.
	- inherit : 부모 값을 상속받는다.

