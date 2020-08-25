# CSS_BASIC

## 사용방법
1. link 태그: HTML에서 외부 CSS 파일을 가져오는 방식
2. ```@import```: CSS 파일 안에서 외부 CSS 파일을 가져오는 방식
_이 방법들 외에도 여러 개 존재_

## 문법
```
selector {
    prop: value;
}
```

### 선택자(selector)
- CSS에서 선택자를 사용해 HTML 요소를 선택할 수 있다.
- 기본 선택자
  1. 전체 선택자 - 모든 요소를 선택 
    ```
    * {
        prop: value;
    }
    ```

  2. 태그 선택자
    ```
    TAG name 
    ```

  3. 클래스 선택자
    ```
    .classValue
    ```
  
  4. 아이디 선택자
    ```
    #idValue
    ```

- 복합 선택자
  1. 일치 선택자: 선택자 두 개를 모두 만족하는 요소를 선택
   ```
   <selector1><selector2>
   ``` 
  2. 자식 선택자
    ```
    <parentSelector> > <childSelector> /* 부모 선택자의 자식 선택자를 선택 */
    ```
  3. 후손(하위) 선택자 - __띄어쓰기를 해줘야한다.__
    _후손: 자신 밑에 있는 모든 태그들(자식 포함)_
    _조상: 자신 위에 있는 모든 태그들(부모 포함)_
    ```
    <selector> <selector> 
    ```
  4. 인접 형제 선택자
  _형제: 같은 부모(조상 아님)_
  ```
  <selector1> + <selector2> /* <selector1> 다음에 있는 형제 요소 <selector2> */
  ```
  5. 일반 형제 선택자
   ```
   <selector1> ~ <selector2> /* <selector1> 다음에 있는 모든 형제 요소 <selector2> */
   ```

- 가상 클래스 선택자

- 가상 요소 선택자

- 속성 선택자


## reference 
[HEROPY Tech](https://heropy.blog/)