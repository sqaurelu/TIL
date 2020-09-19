# React Element(리액트 요소)

- 리액트 요소는 리액트에서 UI를 표현하는 것이다. 불변객체이므로 element를 생성한 이후에는 자식이나 속성을 변경할 수 없다.
- JSX는 바벨(Babel)을 통해 React.createElement()를 호출해 리액트 요소를 반환받게 된다.
```
const element = <h2>Hello world</h2>; // JSX
// 바벨이 해줌
const element = React.createElement('h2', {}, 'Hello world'); // Javascript
```
- 리액트 요소가 모여 돔이 만들어진다. 리액트는 렌더링을 할 때마다 가상 돔을 만든다. 가상 돔의 변경 사항이 있는 경우 돔을 업데이트해, UI를 변경한다.
    - 돔을 구성하는 리액트 요소는 type 속성값이 문자열이어야 한다.
    - JSX는 HTML 태그 또는 컴포넌트로 구성된다. HTML 태그인 경우 type 속성값은 문자열이고, 컴포넌트인 경우에는 함수형태이다. 따라서 컴포넌트인 경우 그 함수를 호출해 렌더링 결과를 가져와야 한다. 
- 데이터 변경에 의한 화면 업데이트: ReactDOM.render 함수(최초 렌더링)나 상태값이 변경될 때 일어난다.
    1. 렌더 단계: 실제 돔에 반영할 변경 사항을 파악하는 단계
    2. 커밋 단계: 변경 사항을 실제 돔에 반영하는 단계



## reference 
[실전 리액트 프로그래밍](http://www.yes24.com/Product/Goods/74223605)

[[React] 리액트를 처음부터 배워보자. — 02. React.createElement와 React.Component 그리고 ReactDOM.render의 동작 원리](https://medium.com/react-native-seoul/react-%EB%A6%AC%EC%95%A1%ED%8A%B8%EB%A5%BC-%EC%B2%98%EC%9D%8C%EB%B6%80%ED%84%B0-%EB%B0%B0%EC%9B%8C%EB%B3%B4%EC%9E%90-02-react-createelement%EC%99%80-react-component-%EA%B7%B8%EB%A6%AC%EA%B3%A0-reactdom-render%EC%9D%98-%EB%8F%99%EC%9E%91-%EC%9B%90%EB%A6%AC-41bf8c6d3764)