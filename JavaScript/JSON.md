# JSON

## JSON 개념

## 메소드
### <strong> ```JSON.stringify(value[, replacer[, space]]) ```</strong> 
- 객체를 JSON 문자열로 바꿔준다.
- 함수 프로퍼티, 심볼형 프로퍼티(심볼을 키로 가지는 프로퍼티), 값이 undefined인 프로퍼티는 stringfy 메소드로 처리할 수 없다.
- value: JSON 문자열로 변환할 객체
- replacer: 변환하고 싶은 프로퍼티를 선택하기 위한 배열 또는 함수
- space: JSON 문자열을 출력할 때 공백문자의 수(가독성)
##### <배열>
```
let user = {
  name: 'blabla',
  age: '26',
  comeFrom: { country: 'Canada', city: 'Toronto' }
}

console.log(JSON.stringify(user, ['name', 'age'])); 
// {"name":"blabla","age":"26"}

console.log(JSON.stringify(user, ['name', 'age', 'comeFrom'])); 
// {"name":"blabla","age":"26","comeFrom":{}}

console.log(JSON.stringify(user, ['name', 'age', 'comeFrom', 'country', 'city'])); 
// {"name":"blabla","age":"26","comeFrom":{"country":"Canada","city":"Toronto"}}
```
##### <함수> 
<p>
key, value를 매개변수로 받는다. <br>
JSON 문자열에 추가되어야 하는 값을 반환해야한다.
</p>

```
function replacer(key, value) {
    if (typeof value !== "string") {
        return value;
    }
    return undefined;
}

console.log(JSON.stringify(user, replacer)); // {"age":26,"comeFrom":{}}
```
### <strong> ```JSON.parse(text[, reviver]) ```</strong>
- JSON 문자열을 객체로 바꿔준다.
- text: 객체로 변환할 문자열
- reviver: 문자열에서 객체로 바뀐 '키-값' 쌍을 수정할 수 있다. 값을 반환해줘야 객체로 저장된다.
```
let user = `{
    "name": "Bruce Lee",
    "age": 26,
    "job": ["Martial arts actor", "philosopher", "martial artist"]
}`

console.log(JSON.parse(user, (key, value) => {
    if (key == 'job') {
        console.log(`JOB: ${value}`)
    }
    return value; 
}))
```
