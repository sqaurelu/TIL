# [코딩테스트 대비를 위한 백준 문제](https://covenant.tistory.com/224)

## Part 1 - 기본기

### [약수 구하기](https://www.acmicpc.net/problem/2501)

숫자의 절반 만큼만 반복문을 돌아서 약수를 배열에 저장한다. 

나머지가 0인 경우 약수가 되는데, 약수인 경우 나누는 수와 몫을 같이 저장해서 반복문이 도는 횟수를 줄였다.

```javascript
let fs = require('fs');
let input = fs.readFileSync('/dev/stdin').toString().split(' ');

let n = Number(input[0]);
let k = Number(input[1]);
let result = new Set();

for (let i = 1; i <= n / 2; i++) {
    if (n % i === 0) {
        result.add(i);
        result.add(n / i);
    }
}

result = Array.from(result).sort((a, b) => a - b);

if (result.length < k) console.log(0);
else console.log(result[k - 1]);
```
