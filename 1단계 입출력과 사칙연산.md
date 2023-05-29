# 2557. Hello World
## 문제 : Hello World!를 출력하시오.
## 문제풀이
```
console.log("Hello World!);
```
## 공부한 것
출력 시 console.log() 사용하기


# 1000, 1001, 10998, 1008, 10869. 사칙연산 (문제 중복으로 합침)
## 문제 : 두 정수 A와 B를 입력받은 다음, A+B, A-B, AxB, A/B(몫), A%B(나머지)를 출력하는 프로그램을 작성하시오.
## 문제풀이
```
const input = require('fs').readFileSync('/dev/stdin').toString().trim().split(' ').map(Number);
console.log(input[0] + input[1]);
console.log(input[0] - input[1]);
console.log(input[0] * input[1]);
console.log(Math.floor(input[0] / input[1]));
console.log(input[0] % input[1]);
```
## 공부한 것
입력값을 String에서 Number로 변경할때 split() 뒤에 .map(v => +v) 말고 .map(Number)를 넣어도 변경된다.
Math.floor()는 내림함수로 소숫점을 제외할 때 사용됨 (Math.ceil(): 올림, Math.round():반올림)
참고 : https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Math/floor


# 10926. ??!
## 문제 : 준하는 사이트에 회원가입을 하다가 joonas라는 아이디가 이미 존재하는 것을 보고 놀랐다. 준하는 놀람을 ??!로 표현한다. 준하가 가입하려고 하는 사이트에 이미 존재하는 아이디가 주어졌을 때, 놀람을 표현하는 프로그램을 작성하시오.
## 문제풀이
```
const input = require('fs').readFileSync('/dev/stdin').toString().trim();
console.log(`${input}??!`);
```
## 공부한 것
 - 백틱(\`) : ES6부터 새로 도입된 문자열 표기법으로 문자열 생성시 따옴표 대신, 백틱(\`)을 사용한다. 
 - 표현식 삽입(${}) : ${} 사이에 변수나 연산 등을 삽입할 수 있다.
 ex) 
```
var name = `사과`
var price = 100
var num = 5;

console.log(`${name}의 구매가는 ${price * num}원 입니다.`) // 사과의 구매가는 500원 입니다.
```
참고 : https://curryyou.tistory.com/185


# 18108. 1998년생인 내가 태국에서는 2541년생?!
## 문제 : ICPC Bangkok Regional에 참가하기 위해 수완나품 국제공항에 막 도착한 팀 레드시프트 일행은 눈을 믿을 수 없었다. 공항의 대형 스크린에 올해가 2562년이라고 적혀 있던 것이었다. 불교 국가인 태국은 불멸기원(佛滅紀元), 즉 석가모니가 열반한 해를 기준으로 연도를 세는 불기를 사용한다. 반면, 우리나라는 서기 연도를 사용하고 있다. 불기 연도가 주어질 때 이를 서기 연도로 바꿔 주는 프로그램을 작성하시오.
## 예제 입력 : 2541 / 예제 출력 : 1998
## 문제 풀이
```
const input = require('fs').readFileSync('/dev/stdin').toString().trim();
console.log(+input - 543);
```
## 공부한 것
단항연산자 '+/-'는 피연산자를 Number 타입('+'는 양수, '-'는 음수)으로 변환한다.
참고 : https://developer-talk.tistory.com/299


# 10430. 나머지
## 문제 : (A+B)%C는 ((A%C) + (B%C))%C 와 같을까? (A×B)%C는 ((A%C) × (B%C))%C 와 같을까? 세 수 A, B, C가 주어졌을 때, 위의 네 가지 값을 구하는 프로그램을 작성하시오.
## 출력 : 첫째 줄에 (A+B)%C, 둘째 줄에 ((A%C) + (B%C))%C, 셋째 줄에 (A×B)%C, 넷째 줄에 ((A%C) × (B%C))%C를 출력한다.
## 문제풀이
```
const input = require('fs').readFileSync('/dev/stdin').toString().trim().split(' ').map(Number);
console.log((input[0] + input[1]) % input[2]);
console.log(((input[0] % input[2]) + (input[1] % input[2])) % input[2]);
console.log((input[0] * input[1]) % input[2]);
console.log(((input[0] % input[2]) * (input[1] % input[2])) % input[2]);
```
## 공부한 것
나머지 연산의 분배법칙
참고 : https://lypicfa.tistory.com/638


# 2588. 곱셈
## 문제 : (세 자리 수) × (세 자리 수)는 다음과 같은 과정을 통하여 이루어진다. (1)과 (2)위치에 들어갈 세 자리 자연수가 주어질 때 (3), (4), (5), (6)위치에 들어갈 값을 구하는 프로그램을 작성하시오.
![image](https://github.com/JavaScript-Coding-Test-Study/lsh/assets/133360417/2df76533-ceb8-4e54-8021-dec359a6f1fe)
## 문제풀이
```
const input = require('fs').readFileSync('/dev/stdin').toString().trim().split('\n');
// input[0] = (1), input[1] = (2)
console.log(+input[0] * +input[1][2]); // (3) - input[1][2] : 일의 자리
console.log(+input[0] * +input[1][1]); // (4) - input[1][1] : 십의 자리
console.log(+input[0] * +input[1][0]); // (5) - input[1][0] : 백의 자리
console.log(+input[0] * +input[1]); // (6)
```
## 공부한 것
단항연산자를 통해 Number로 변환 후 연산 시 한쪽에만 단항연산자를 작성해도 계산은 된다.
그런데, 둘다 적용하는게 계산 시간이 빠르다. Number() == 양쪽다 '+' > 한쪽만 '+'


# 11382. 꼬마 정민
## 문제 : 꼬마 정민이는 이제 A + B 정도는 쉽게 계산할 수 있다. 이제 A + B + C를 계산할 차례이다!
## 문제풀이
```
const input = require('fs').readFileSync('/dev/stdin').toString().trim().split(' ');
console.log(input.reduce((acc, cur) => +acc + +cur, 0));
```
## 공부한 것
reduce()를 활용하여 배열의 합을 구해보았다.
acc는 누적값이 저장되고, cur은 현재값을 의미하고, 0은 acc의 초기값이다.
위 문제와 코드대로보면, 입력값 : [A, B, C]
 - 1회차 : acc = 0, cur = A / +acc + +cur = A 값이 acc에 저장
 - 2회차 : acc = A, cur = B / +acc + +cur = A+B 값이 acc에 저장
 - 3회차 : acc = A+B, cur = C / +acc + +cur = A+B+C 값이 acc에 저장
 
더이상 cur이 없기때문에 최종 acc 값인 A+B+C를 출력
변수를 선언하지 않고, 바로 출력도 가능하긴 하다. 코드길이가 줄었는데, 미세한 차이긴 하지만 계산 시간은 늘었다. 왜지? 흠..ㅋㅋ


# 10171. 고양이
## 문제 : 아래 예제와 같이 고양이를 출력하시오.
## 예제 출력 : ![image](https://github.com/JavaScript-Coding-Test-Study/lsh/assets/133360417/b909ef24-6590-44d8-a951-923a605f4caa)
## 문제풀이
```
console.log(`
\\    /\\
)  ( ')
(  /  )
 \\(__)|
`)
```
## 공부한 것
JS 문자열 내에서 특수기호를 표시하려면 '이스케이프 시퀀스'를 사용해야 한다.
사용 방법은 해당 특수 기호 앞에 역슬래시(\\)를 붙여주면 된다.
백틱(`)으로 템플릿 리터럴을 사용하면, 줄바꿈 및 특정 특수 기호 앞에 '\\'를 하지 않고 쉽게 표현할 수 있다.
고양이 문제에서는 '\\' 앞에만 '\\'를 추가해주면 된다.


# 10172. 개
## 문제 : 아래 예제와 같이 개를 출력하시오.
## 예제 출력 : ![image](https://github.com/JavaScript-Coding-Test-Study/lsh/assets/133360417/19983bcc-9ce0-49be-a5d9-52759333312d)
## 문제풀이
```
console.log(`|\\_/|
|q p|   /}
( 0 )"""\\
|"^"\`    |
||_/=\\\\__|`)
```
##  공부한 것
개 문제에서는 '\\(역슬래시), `(백틱)' 앞에 '\\'를 추가해주면 된다.
