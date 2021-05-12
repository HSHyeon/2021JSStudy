## 생활코딩 - Javascript 내용 정리

### 1. 자바스크립트 기본
<br>
<br>
7) 모듈<br>
사용 목적 : 코드의 재활용성 높이기 + 유지보수 쉽게 하기 위함.<br>
<br>
모듈화의 장점<br>
자주 사용되는 코드를 별도의 파일로 만들어서 필요할 때마다 재활용할 수 있다.
<br>(모듈화 목적을 이루는 법 = 코드를 여러 파일로 분리.
1개 파일 안 여러 파일과 로직들이 들어가고 프로그램을 이룸.)
<br>코드를 개선하면 이를 사용하고 있는 모든 애플리케이션의 동작이 개선된다.(메모리 낭비 감소, 시간복잡도 감소..etc)
<br>유지, 보수 간편.
<br>(한번 다운로드된 모듈은 웹브라우저에 의해서 저장되기 때문에 동일한 로직을 로드 할 때 시간과 네트워크 트래픽을 절약 할 수 있다.(브라우저에서만 제공))
<br><br>
JS는 모듈 개념 분명히 존재 x. 자바스크립트가 구동되는 환경에 따라 다른 모듈화 방법 제공.
<br>
호스트 환경 = JS가 구동되는 환경.
<br>
<br>모듈 효용에 대한 예시

```
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8"/>
    <script src="greeting.js"></script>
</head>
<body>
    <script>
        alert(welcome());
    </script>
</body>
</html>
```

<br>greeting.js

```
function welcome(){
    return 'Hello world';
}
```

이렇게 하면 greeting.js의 welcome()함수를 간단하게 원하는 페이지에서 호출 가능한다.
<br><br>

node.js에서 모듈 로드

```
var circle = require('가져오고자하는 파일의 상대 경로');
alert(circle.함수명(인자))
```

<br>
라이브러리 = 자주 사용되는 로직을 재사용하기 편리하도록 잘 정리한 코드의 집합.
<br>
모듈 = 프로그램을 구성하는 부품으로써의 로직
<br>
대표 라이브러리 : jquery(웹에서 Js를 사용하는 라이브러리)
