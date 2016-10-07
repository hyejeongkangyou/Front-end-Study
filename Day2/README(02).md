## DAY 02 - FDS

#### 조건부 주석  
  조건부 주석은 IE10 미만에서 작동하는 조건문으로, 이를 이용하여 IE 브라우저별로 어떤 기능이나 파일, 디자인 등을 삽입하는 용도로 자주 사용된다.

```
  <!--[if IE]>
  	코드
  <![endif]-->
```

###### 조건부에 사용되는 기호  
- `!` : 아니라면
- `lt` : 작다(less than)
- `lte` : 작거나 같다(less than equal)
- `gt` : 크다(greater than)
- `gte` : 크거나 같다(greater than equal)
- `&` : 그리고(and)

```html
<!--[if IE 6]><html lang="ko-KR" class="ie6"><![endif]-->
<!--[if IE 7]><html lang="ko-KR" class="ie7"><![endif]-->
<!--[if IE 8]><html lang="ko-KR" class="ie8"><![endif]-->
<!--[if IE 9]><html lang="ko-KR" class="ie9"><![endif]-->
<!--[if !IE]><!--><html lang="ko-KR"><!--<![endif]-->
```
- `<html>`요소에 조건부 주석을 이용해 각각의 브라우저에 맞는 클래스명을 부여해서 이를 컨트롤하려는 방법이다.
- 이 조건을 만족할 경우, HTML코드를 렌더링하게 된다. 구문 처음의 `<!--` 부분과 마지막`>`이 적용된 부분은 타 브라우저에서 무시된다.
- 마지막줄의 구문은 기존 구문과는 좀 다른데 이는 원래 조건에 부합하는 IE 버전과 타 브라우저들도 읽어 들여야 하는 부분을 동시에 만족하기 위해 `-->` 를 조건부 뒤에 추가하는 부분이다. 다만 조건에 못미치는 IE들은 이 조건부가 끝나는 즉시 렌더링되어 `-->` 부분을 화면에 표시하게 되기 때문에 이 부분을 주석처리하기 위하여 `-->` 부분을 `<!-->`로 변경하게 된다. 마지막 부분도 이와 동일한 이유다.

    _출처  : [IE 조건부 주석 (Conditional Comment)](http://webdir.tistory.com/451)_


#### 파비콘(Favicon: Favorite Icon)  
  파비콘은 웹페이지에 접속했을 때 상단 탭에 보여지는 아이콘을 말한다.  
  이미지를 다음과 같이 넣을 수 있다.
```html
    <link rel="shortcut icon" href="images/favicon.png">
```

#### HTML 하이퍼링크  

###### 절대 경로(Server 환경에서 테스팅 가능)

    - 어떠한 웹페이지나 파일이 가지고 있는 고유한 경로

###### 상대 경로

    - 현재 위치한 곳을 기준으로 해서 그 곳의 위치를 말한다.
    - HTML파일이 위치한 폴더를 기준으로 한 상대적인 경로  

> / : 루트(가장 최상의 디렉토리)  
> ./ : 현재 위치(현재 디렉토리)  
> ../ : 현재 위치의 상단 폴더(상위 디렉토리)