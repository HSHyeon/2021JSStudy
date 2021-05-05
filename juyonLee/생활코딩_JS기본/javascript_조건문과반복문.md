## 생활코딩 - Javascript 내용 정리

### 1. 자바스크립트 기본

4) 조건문(conditional statement)
<br>
주어진 조건에 따라 다르게 동작하는 명령문. if로 시작함.
<br>
조건문 형식

```
if(true){//조건이 true면 해당 주석의 명령문이 실행됨.}
else if(true){//if의 조건은 false지만 해당 조건문에 true일 경우 실행됨.}
else {//위 조건들 중 어디에도 만족하지 않을 때 실행됨.}
```

<br>
코드 예시

```
id = prompt('아이디를 입력해주세요.')
        if(id=='egoing'){
            alert('아이디가 일치 합니다.')
        } else {
            alert('아이디가 일치하지 않습니다.')
        }
```

<br>
prompt('당신의 나이는? '); // 출력창에 당신의 나이는?이라는 문장이 뜨면서 값을 Input할 수 있음.
<br>//해당 값을 가져와 변수의 값에 대입해주는 api.

<br>조건문은 중첩이 가능하다.

```
id = prompt('아이디를 입력해주세요.')
pw = prompt('비밀번호를 입력해주세요. ')
        if(id=='egoing'){
            alert('아이디가 일치 합니다.')
            if(pw=='1233'){
            alert('비밀번호와 아이디가 일치합니다. 로그인되었습니다.')
            }
        } else {
            alert('아이디가 일치하지 않습니다.')
        }
```

<br>
논리연산자. boolean 대체제
<br>&& = 좌우항이 모두 참일 때 true값 출력.
<br>|| = or, 좌우항 중 하나가 참일 때

<br><br><br>
5) 반복문(loop, iterate)
<br>특정한 명령문을 특정한 위치에서 계속 반복하기 위해 사용함.
<br>기본적으로 while, for 2가지 형태가 있음.

<br>while문 형식

```
while(boolean 데이터타입 조건문) {
반복 실행 코드 위치할 좌표
}


var i = 0; //i는 식별자. 반복문을 몇 번 했는지 명시함.
// 종료조건으로 i의 값이 10보다 작다면 true, 같거나 크다면 false가 된다.
while(i < 10){
    // 반복이 실행될 때마다 coding everybody <br />이 해당 웹페이지에 출력된다.
    document.write('coding everybody'+i+<br />');
    // i의 값이 1씩 증가한다.
    i++
}
```

<br>for문 형식

```
for(초기화; 반복조건; 반복이 될 때마다 실행되는 코드){
    반복해서 실행될 코드
}

//위 while문 코드와 같은 역할을 함.
for(var i = 0; i < 10; i++){
    document.write('coding everybody'+i+'<br />');
}
```

<br>그 외 반복문을 제어하는 명령어들
<br>
break : 반복문 내 실행을 중지하고 즉시 반복문을 빠져나옴.
<br>continue : 반복문 내 해당 실행을 중단하면서 반복을 지속되게 만듦.
<br>
i++와 ++i의 차이
<br>
