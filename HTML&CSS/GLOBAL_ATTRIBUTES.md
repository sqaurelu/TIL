# Global attributes(전역 속성) - class, id

## class

- element의 별명(여러 개 지정 가능)
```
<div class="nick1 nick2"></div>
<div class="nick1"></div>
```
- CSS, JS에서 HTML 요소를 선택해 접근할 수 있게 한다.
- CSS에서는 .을 통해 접근 가능
- JS에서는 document.querySelector('.className')을 통해 접근 가능

## id

- element의 이름, 고유한 식별자를 정의(class와 달리 여러 개 지정 불가)
```
/* 불가능 */
<div id="id1"></div>
<div id="id1"></div>
```
- CSS, JS에서 요소를 선택해 접근할 수 있게 한다.
- CSS 에서는 #을 통해 접근 가능
- JS에서는 document.getElementById('id');를 통해 접근 가능


## reference 
[HEROPY Tech](https://heropy.blog/2019/05/26/html-elements/)