## ※백준에서 JavaScript 코딩테스트

 - 언어 : nodeJS 사용하기
 - 단계별로 풀어보기
 - 입출력 방법은 아래와 같이 두가지가 있는데, fs모듈이 시간효율성이 좋다고 한다.
   1. fs 모듈
   2. readline 모듈

## 1. 출력

 - nodeJS 출력은 console.log()를 사용하면 된다.

```
  console.log("Hello World!");
  // "Hello World!" 
```

## 2. 입력
 
 - fs.readFileSync()를 통해 입력값을 받는다.
 - '/dev/stdin' 백준 사이트의 입력값 경로
   (로컬 환경에서 실행 시에는 자신의 입력 파일 위치)
 - 사용 목적에 따라 사용할 데이터 형태로 가공

```
  const fs = require('fs');
  // 파일 시스템 모듈 임포트

  const input = fs.readFileSync('/dev/stdin');
  // 백준의 입력값을 readFileSync 함수를 통해 파일의 입력값을 받아온다.
  
  const input = require('fs).readFileSync('/dev/stdin');
  // 한 줄로 입력값 받기
```

## 3. 입력값 가공

아래 코드들을 참고해서 백준 문제를 풀어보도록 하자.

```
// 1. 하나의 값을 입력받을 때
const input = require('fs').readFileSync('/dev/stdin').toString().trim();

// 2. 공백으로 구분된 한 줄의 값들을 입력받을 때
const input = require('fs').readFileSync('/dev/stdin').toString().trim().split(' ');

// 3. 여러 줄의 값들을 입력받을 때
const input = require('fs').readFileSync('/dev/stdin').toString().trim().split('\n');

// 4. 첫 번째 줄에 자연수 n을 입력받고, 그 다음줄에 공백으로 구분된 n개의 값들을 입력받을 때
const [n, ...arr] = require('fs').readFileSync('/dev/stdin').toString().trim().split(/\s/);

// 5. 첫 번째 줄에 자연수 n을 입력받고, 그 다음줄부터 n개의 줄에 걸쳐 한 줄에 하나의 값을 입력받을 때
const [n, ...arr] = require('fs').readFileSync('/dev/stdin').toString().trim().split('\n');

// 6. 하나의 값 또는 공백으로 구분된 여러 값들을 여러 줄에 걸쳐 뒤죽박죽 섞여서 입력받을 때
// ex) n 입력 - 공백으로 구분된 n개의 값 입력 - m 입력 - 여러 줄에 걸쳐 m개의 값 입력
const input = require('fs').readFileSync('/dev/stdin').toString().trim().split(/\s/);
const n = input[0];
const n_arr = input.slice(1, n+1);
const [m, ...m_arr] = input.slice(n+1);

// 2~6에서 입력받는 값들을 모두 String에서 Number로 바꾸려면 split()뒤에 .map(v => +v)를 추가
```
