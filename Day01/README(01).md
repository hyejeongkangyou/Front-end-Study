## Day 1 - FDS



### `<meta>`태그  

- `<meta>`태그는 문서 그 자체를 설명하는 태그이다.
- `<meta>`태그는 HTML 문서가 어떤 내용을 담고 있고, 문서의 키워드는 무엇이며, 누가 만들었는지 등에 대한 문서 자체의 특성을 담고 있다.
- `<meta>`태그는 문서의 헤더부분(`<head></head>`)에 위치한다.
```html
 <meta http-equiv="X-UA-Compatible" content="IE=Edge"> 
```
- http-equiv속성은 meta요소에서 정의된 명령을 먼저 실행한 후 페이지를  로딩한다.

```html
 <meta name="viewport" content="width=device-width, initial-scale=1.0">
```

###### viewport란?  
  
  - viewport란 우리말로 보임창, 즉 화면상의 화상 표시 영역을 뜻한다.
  - viewport설정을 하게 되면 다양한 모바일 기기에서도 페이지의 너비나 화면 배율을 설정할 수 있다.
  - 보통 viewport meta태그는 뷰포트의 너비와 초기 배율(zoom 레벨)을 설정하기 위해 사용한다.
  - 그러므로 모바일 장치에 최적화된 웹페이지를 만들려면 HTML문서 `<head></head>`에 뷰포트 설정을 포함해야 한다.  


### dir  

dir은 문서가 읽히는 방향을 말한다. 

```html
 <html lang="ko-KR" dir="ltr">
```

- ltr은 left to right(왼쪽에서 오른쪽으로)이다.
- rtl은 right to left(오른쪽에서 왼쪽으로)이다.
rtl은 right to left(오른쪽에서 왼쪽으로)이다.  

### UTF-8  
```html
<meta charset="UTF-8">
```
텍스트 언어 인코딩을 UTF-8로 설정하여 모든 유니코드 문자를 표현할 수 있도록 설정하고, 깨지는 한글 문제를 해결한다.