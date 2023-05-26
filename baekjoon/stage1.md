## 백준 1단계 - 입출력과 사칙연산

> 2557. Hello World
 - 문제 : Hello World!를 출력하시오.
 - 입력 : -
 - 출력 : Hello World!를 출력하시오.
 - 예제 입력 : -
 - 예제 출력 : Hello World!

 **풀이**
```
console.log("Hello World!);
```
 
 
 
> 1000. A+B
 - 문제 : 두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.
 - 입력 : 첫째 줄에 A와 B가 주어진다.(0 < A, B < 10)
 - 출력 : 첫째 줄에 A+B를 출력한다.
 - 예제 입력 : 1 2
 - 예제 출력 : 3
 
 **풀이**
```
const input = require('fs').readFileSync('/dev/stdin').toString().trim().split(' ').map(Number);
console.log(input[0] + input[1]);
```

> 1001. A-B
 - 문제 : 두 정수 A와 B를 입력받은 다음, A-B를 출력하는 프로그램을 작성하시오.
 - 입력 : 첫째 줄에 A와 B가 주어진다.(0 < A, B < 10)
 - 출력 : 첫째 줄에 A-B를 출력한다.
 - 예제 입력 : 3 2
 - 예제 출력 : 1

 **풀이**
```
const input = require('fs').readFileSync('/dev/stdin').toString().trim().split(' ').map(Number);
console.log(input[0] - input[1]);
```
