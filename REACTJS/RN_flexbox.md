# [React Native] flexbox
- 컴포넌트들을 정렬하고 여백을 조정하는 것을 쉽게 컨트롤할 수 있도록 하는 레이아웃 구현체
- flexbox 레이아웃은 View 컴포넌트에서만 사용 가능하다
- 속성: `flex`, `flexDireaction,` `justifyContent`, `alignItems`, `alignSelf`, `flexWrap`

  
##### `flex`
- 컴포넌트가 속한 부모 컨테이너에서 컴포넌트가 차지하는 면적을 변경할 수 있게 해준다
- 같은 컨테이너에 속한 다른 컴포넌트에 지정한 flex 속성값에 상대적으로 지정한다
- `A = { flex: 1 }, B = { flex: 1 }` => 컨테이너에 1:1 비율로 차지
- `A = { flex: 1 }, B = { flex: 2 }` => 컨테이너에 1:2 비율로 차지

##### `flexDirection`
- 자식 컴포넌트가 쌓이는 방향을 지정할 수 있다
- 부모 View 컨테이너에 지정한다
- 기본값은 `column`: 수직으로 쌓임
- `row`: 수평으로 쌓임
  
##### `justifyContent`
- 컨테이터에 속한 컴포넌트들간의 간격과 여백을 지정할 수 있다
- 부모 컨테이너에 적용한다
- `center`: 부모 컨테이너 내의 자식 컴포넌트를 중앙에 배치. 남는 여백은 모여 있는 자식 요소들의 양 측면에 배치
- `flex-start`: `flexDirection` 속성에 지정된 값을 기준으로 행이나 열의 시작점부터 자식 요소들을 배치
- `flex-end`: 'flex-start'와 반대로 동작. 자식 요소들을 부모 컨테이너의 끝에 배치
- `space-around`: 각 요소 주변으로 공간을 고르게 배치. (여백을 자식요소들 주변으로 배치)
- `space-between`: 컨테이너의 시작과 끝에 여백을 주지 않는다. 연속된 요소들 사이의 여백은 동일하게 배치

##### `alignItems`
- 부모 컨테이너의 보조 축을 따라 자식 요소들을 어떻게 정렬할 것인지를 지정
- 부모 View 컴포넌트에 선언
- flex가 적용 가능한 자식 요소들에게 영향을 미친다
- 속성값: `stretch`, `center,` `flex-start`, `flex-end`
- `stretch`는 기본값

##### `alignSelf`
- 위 속성들은 부모 컨테이너에 적용했다. `alignSelf`는 자식 요소에 직접 적용한다.
- 부모 컨테이너에 지정된 정렬 기준을 재정의
- 속성값: `auto`, `stretch`, `center,` `flex-start`, `flex-end`
- `auto`는 기본값. 부모 컨테이너의 alignItems 속성값 그대로 사용

##### `flexWrap`
