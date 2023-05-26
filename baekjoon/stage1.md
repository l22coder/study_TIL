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
console.log(input[0] + input[1]);
console.log(input[0] - input[1]);
console.log(input[0] * input[1]);
console.log(Math.floor(input[0] / input[1]));
console.log(input[0] % input[1]);
```
##
> 10926. ??!
 - 문제 : 준하는 사이트에 회원가입을 하다가 joonas라는 아이디가 이미 존재하는 것을 보고 놀랐다. 준하는 놀람을 ??!로 표현한다. 준하가 가입하려고 하는 사이트에 이미 존재하는 아이디가 주어졌을 때, 놀람을 표현하는 프로그램을 작성하시오.
 **풀이**
```
const input = require('fs').readFileSync('/dev/stdin').toString().trim();
console.log(`${input}??!`);
```
##
> 18108. 1998년생인 내가 태국에서는 2541년생?!
 - 문제 : ICPC Bangkok Regional에 참가하기 위해 수완나품 국제공항에 막 도착한 팀 레드시프트 일행은 눈을 믿을 수 없었다. 공항의 대형 스크린에 올해가 2562년이라고 적혀 있던 것이었다.
불교 국가인 태국은 불멸기원(佛滅紀元), 즉 석가모니가 열반한 해를 기준으로 연도를 세는 불기를 사용한다. 반면, 우리나라는 서기 연도를 사용하고 있다. 불기 연도가 주어질 때 이를 서기 연도로 바꿔 주는 프로그램을 작성하시오.
 - 예제 입력 : 2541 / 예제 출력 : 1998
 **풀이**
```
const input = require('fs').readFileSync('/dev/stdin').toString().trim();
console.log(+input - 543);
```
##
> (A+B)%C는 ((A%C) + (B%C))%C 와 같을까?
 (A×B)%C는 ((A%C) × (B%C))%C 와 같을까?
 세 수 A, B, C가 주어졌을 때, 위의 네 가지 값을 구하는 프로그램을 작성하시오.
 **풀이**
```
const input = require('fs').readFileSync('/dev/stdin').toString().trim();
console.log(+input - 543);
```
