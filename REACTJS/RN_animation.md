# [React Native] Animated

- 애니메이션을 만들기 위해서는 먼저 `Animated.Value` 값을 설정 하고, `Animated.timing()`을 사용하여 애니메이션을 만든다.
- 예시
  ```
  const exAnimation = new Animated.Value(애니메이션 초기값);
  
  const animate = () => {
    Animated.timing(
      exAnimation, // 시작값
      { // 설정 객체
        toValue: 100, // 애니메이션 종료값
        duration: 300, // 애니메이션 길이(ms)
      }
    )
  }
  ```

---------

## Animated.timing
 - `static timing(value, config)`
## Animated.loop
- `static loop(animation, config?)`
- 무한 반복되는 애니메이션을 만들 수 있다.
- `loop.Animated.loop` static 메소드를 이용한다.
- 위 메소드는 지정된 애니메이션을 반복해서 실행하고, 애니메이션이 끝나면 처음부터 다시 반복해서 실행한다.
## interpolate
- 애니메이션 효과 조정 가능.
- `inputRange`와 `outputRange` 2개의 키로 구성된 설정 객체를 인수로 사용한다.
- `inputRange`: 현재 작업하는 원래 애니메이션 효과
- `outputRange`: 앞으로 변경될 애니메이션 효과
- 예시
  ```
  const animatedRotation = new Animated.Value(0);
  
  const rotation = animatedRotation.interpolate({
    inputRange: [0, 1], // 애니메이션의 시작값과 종료값(0과 1)
    outputRange: ['0deg', '360deg'], // 애니메이션의 진행 변화(inputRange 값으로 매핑할 값: 시작값은 0도 종료값은 360도)
  });
  ```
