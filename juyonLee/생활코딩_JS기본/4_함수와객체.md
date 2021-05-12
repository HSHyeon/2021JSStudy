## 생활코딩 - Javascript 내용 정리

### 1. 자바스크립트 기본

5) 함수
<br>
로직을 재실행할 수 있도록 해 코드의 재사용성을 높여주는 코드 작성 기법.
<br><br>
javascript에서 함수 작성 형식

```
function 함수명( [인자...[,인자]] ){
   코드
   return 반환값
}


//해당 인자의 값을 반환해주는 함수
function number(num){
  return num;
}
```

<br>함수의 이용 목적
<br>반복문 : 기계적으로 일정한 반복을 그 자리에서 실행할 때 사용.(해당 위치에서만 사용 가능)
<br>함수 : 여러 맥락에서 반복되는 로직을 사용해야 할 경우(여기저기서 호출해서 사용 가능)
<br>함수를 사용하는 근본적 이유 = 재사용성을 크게 하기 위해. (여러 곳에서 함수 유지보수가 용이.)
##### 재사용성, 유지보수의 용이, 가독성

<br>
함수의 핵심 = 입출력. 입력된 값을 연산해서 출력하는 것이 기본적 역할.

<br>
출력 : return문 사용. 결과 반환과 동시에 종료. 함수는 한 번에 1개 값만 리턴 가능.
<br>
입력 : 인자(argument)로 이루어짐.
<br>함수로 유입되는 입력값. 인자로 전달되는 값 따라 리턴값을 다르게 조작할 수 있다.

<br><br>자바스크립트에서 또다른 함수 선언 방법
<br>함수는 변수가 갖는 값으로 선언할 수도 있다.

```
var numbering = function (){
    i = 0;
    while(i < 10){
        document.write(i);
        i += 1;
    }
}
numbering(); //numbering은 변수이지만 함수인 것처럼 사용 가능하다.
```

<br>함수는 이름이 없는 익명함수로도 사용할 수 있다.

```
(function (){
    i = 0;
    while(i < 10){
        document.write(i);
        i += 1;
    }
})(); //함수 정의 + 정의한 함수 호출이 한 문장 내에 들어감.
```

<br><br><br>6) 배열
<br>연관된 데이터들을 담는 그릇. 여러 데이터를 1개의 변수에 저장하기 위함.
<br>
<br> 배열 내 원소를 element, 해당 원소를 구분하기 위해 순서로 정의한 식별자를 Index라고 칭한다.

```
var mem = ['aa', 'bb','cc'];
//index(순서)에 따라 해당 element들 도출 가능.
```

<br>배열 선언 및 사용 방법

```
function get_members(){
    return ['egoing', 'k8805', 'sorialgi'];
}
members = get_members();
//element들의 구별은 index를 사용한다. 해당 함수는 members의 문자들을 대문자로 변환하는 함수이다.
for(i = 0; i < members.length; i++){
    // members[i].toUpperCase()는 members[i]에 담긴 문자를 대문자로 변환해준다.
    document.write(members[i].toUpperCase());
    document.write('<br />');
}
```

<br>배열을 다루기 위해 주로 사용되는 명령어

```
배열명.length = 배열의 크기
배열명.push(값) = 배열 뒤쪽에 값 추가
배열명.concat([값들]) = 배열 뒤쪽에 값 추가
배열명.unshift(값) = 배열 가장 앞에 값 추가
배열명.splice(index, index에서부터 제거될 원소들의 수, 첫번째 Index에 넣을 값들(복수 가능)
배열명.shift() = 배열의 첫 번째 원소 제거. 반환값 없음.
배열명.pop() = 배열의 마지막 원소 제거하고 제거된 결과 반환.

배열명.sort() = 오름차순으로 정렬.
배열명.reverse() = 내림차순으로 정렬.
```

<br><br><br>7) 객체(설명은 추후 더 추가 예정)
<br>배열과 유사. 식별자가 숫자가 아닌 것들.
<br>식별자가 문자 = dictionary<br>다른 언어 - associative array, map, dictionary

##### (+객체에 대한 공부는 추후 더 깊게 해야 할 예정)

<br>자바스크립트 선언문 예시

```
var grades = {'egoing': 10, 'k8805': 6, 'sorialgi': 80};
egoing : key, 10: value
grades['egoing'] = 10;
grades.egoing = 10;
```

<br>객체를 이용하는 반복문 만들기

```
var grades = {'egoing': 10, 'k8805': 6, 'sorialgi': 80};
for(key in grades) {
    document.write("key : "+key+" value : "+grades[key]+"<br />");
}


var grades = {
    'list': {'egoing': 10, 'k8805': 6, 'sorialgi': 80},
    'show' : function(){
        for(var name in this.list){
            document.write(name+':'+this.list[name]+"<br />");
        }
    }
};
grades.show();
grades['list']['egoing'] = 10;
```

객체 안에 함수가 담길 수도 있음.
this = 약속된 변수. 이 함수가 속해 있는 객체를 가리키는 변수
여기서 this = grades
