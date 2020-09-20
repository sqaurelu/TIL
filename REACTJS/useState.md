# React Hook useState

- 함수형 컴포넌트에서도 상태를 관리할 수 있게 해주는 리액트 훅
- 클래스형 컴포넌트의 this.state와 똑같은 기능을 가진다.
- setState(클래스형 컴포넌트)는 기존 상태값과 새로운 상태값을 병합, 상태값 변경함수(함수형 컴포넌트)는 이전 상태값에 새로운 상태값을 덮어쓴다.
- state 변수가 객체나 배열일 경우 __상태값 변경 함수는 spread 문법을 이용해 기존의 객체나 배열(이전 상태값)을 복사한 후__ 값을 수정해야 한다.

##### 사용 예시
1. useState를 사용하기 위해 import 해준다.
    ```
    import React, { useState } from 'react'; 
    ```
2. useState 함수에 초기 상태값을 넣어준다.
    ```
    useState(defaultValue);
    ```
3. 배열 구조분해를 이용해 useState 함수의 반환값을 받는다. 
첫번째 변수는 state 변수, 두번째 변수는 상태값 변경함수이다.
    ```
    const [state, setState] = useState(defaultValue);
    ```
    상태값 변경함수는 비동기로 동작한다. but 순서는 바뀌지 않는다.
    여러 개의 상태값 변경 요청을 배치로 처리한다.

    ```
    function Counter() {
        const [count, setCount] = useState(0)
        function upCount() {
            setCount(prev => prev + 1) // 첫번째
            setCount(prev => prev + 2) // 두번째
        }
        return (
            <>
                <button onClick={upCount}>+</button>
            </>
        )
    }
    ```



## reference 
[실전 리액트 프로그래밍](http://www.yes24.com/Product/Goods/74223605)
