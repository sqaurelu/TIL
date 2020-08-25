# Block element

 - DIV, H1, P
 - width를 지정하지 않으면 사용 가능한 최대 가로 너비를 사용한다.

```
/* 이렇게 하면 최대 가로 너비를 사용 */
div {
    background: yellow;
    height: 20px;
}
```
_body 태그의 default 값(margin, padding)이 있어서 0으로 초기화 시켜주면 브라우저 페이지에 가로가 꽉차게 나옴._

 - 가로(width), 세로(height) 사이즈를 지정할 수 있다.
 - ```width: 100%, height: 0; ```에서 시작 (block element안에 값이 있으면 그 값 크기만큼 height를 차지) 
 - default는 ```width: auto; height: auto; ```
 - 수직으로 쌓인다.
 - margin, padding 속성은 위 아래 좌 우 모두 사용 가능하다.
 - __레이아웃을 위한 용도__

# Inline element

 - SPAN, IMG
 - 필요한 너비만큼을 사용한다.(자신 안에 포함된 내용만큼을 inline요소의 가로 너비로 사용)
 - (가로, 세로 사이즈)크기를 지정할 수 없다.
 - ```width: 0; height: 0; ```에서 시작
- default는 ```width: auto; height: auto; ```
- 수평으로 쌓인다
- margin, padding 속성은 좌 우만 사용 가능하다.
- __TEXT를 다루기 위한 요소__

CSS의 display 속성을 이용해 block과 inline 요소 서로 변경 가능


## reference 
[HEROPY Tech](https://heropy.blog/2019/05/26/html-elements/)