## 백준 1단계 - 입출력과 사칙연산

> 2557. Hello World
 - 문제 : Hello World!를 출력하시오.
 **풀이**
```
console.log("Hello World!);
```
##
> 1000. A+B
 - 문제 : 두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.
 **풀이**
```
const input = require('fs').readFileSync('/dev/stdin').toString().trim().split(' ').map(Number);
console.log(input[0] + input[1]);
```
##
> 1001. A-B
 - 문제 : 두 정수 A와 B를 입력받은 다음, A-B를 출력하는 프로그램을 작성하시오.
 **풀이**
```
const input = require('fs').readFileSync('/dev/stdin').toString().trim().split(' ').map(Number);
console.log(input[0] - input[1]);
```
##
> 10998. AxB
 - 문제 : 두 정수 A와 B를 입력받은 다음, AxB를 출력하는 프로그램을 작성하시오.
 **풀이**
```
const input = require('fs').readFileSync('/dev/stdin').toString().trim().split(' ').map(Number);
console.log(input[0] * input[1]);
```
##
> 1008. A/B
 - 문제 : 두 정수 A와 B를 입력받은 다음, A/B를 출력하는 프로그램을 작성하시오.
 **풀이**
```
const input = require('fs').readFileSync('/dev/stdin').toString().trim().split(' ').map(Number);
console.log(input[0] / input[1]);
```
##
> 10869. 사칙연산
 - 문제 : 두 자연수 A와 B가 주어진다. 이때, A+B, A-B, A*B, A/B(몫), A%B(나머지)를 출력하는 프로그램을 작성하시오.
 **풀이**
```
const input = require('fs').readFileSync('/dev/stdin').toString().trim().split(' ').map(Number);
console.log(input[0] / input[1]);
```
