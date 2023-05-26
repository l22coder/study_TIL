## ※백준에서 JavaScript 코딩테스트

 - 언어 : nodeJS 사용하기
 - 단계별로 풀어보기


## 1. 출력

 - nodeJS 출력은 console.log()를 사용하면 된다.

  > console.log("Hello World!");
  // "Hello World!" 


## 2. 입력
 
 - fs.readFileSync()를 통해 입력값을 받는다.
 - 파일 위치: '/dev/stdin' 백준 사이트의 고정값
   (로컬 환경에서 실행 시에는 자신의 입력 파일 위치)
 - 사용 목적에 따라 사용할 데이터 형태로 가공

  > const fs = require('fs');
  // 파일 시스템 모듈 임포트

  > const input = fs.readFileSync('/dev/stdin');
  // 백준의 입력값을 readFileSync 함수를 통해 파일의 입력값을 받아온다.
  
  > const input = require('fs).readFileSync('/dev/stdin');
  // 한 줄로 입력값 받기
   

## 3. 입력값 가공

 - JS의 String.split() 함수를 활용해 입력값을 배열 형태로 받아오는 방법
 - split() 매서드는 배열을 리턴하여 입력값을 다양하게 가공할 수 있다.

  > const charArray = input.toString().split('');
  // 입력값이 한 단어이고, 각 철자를 배열로 받는 경우

  > const wordArray = input.toString().split(' ');
  // 입력값이 한 줄의 여러 단어이고, 각 단어를 배열로 받는 경우

  > const numArray = input.toString().split(' ').map(Number)
  // 입력값이 한 줄의 여러 숫자이고, 각 수를 배열로 받는 경우
