### 유효범위

유효범위: 변수의 수명을 의미

전역 변수: 함수 밖에서 변수 선언
```
var vscope = 'global'; //함수 밖 전역 변수 선언
function fscope(){
    var vscope = 'local'; //함수 내에서 지역 변수 선언
    alert('함수안 '+vscope); //local 출력
}
fscope();
alert('함수밖 '+vscope); //global 출력
```

```
var vscope = 'global';
function fscope(){
    vscope = 'local'; //전역변수 vscope를 local로 변경
    alert('함수안'+vscope); //local 출력
}
fscope();
alert('함수밖'+vscope);//local 출력
```
돌겠네 진짜
