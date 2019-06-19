# C-sharp


CLI(Common Language Infrastructure) 제공  
여러 언어로 개발해도 .NET 위에서는 동일하게 구동 한다.  

class library = dll로 만듬.  



캐스팅 = boxing(담을때) +unboxing(꺼낼때) ->  `성능 저하`  
```
object a = 10
object b = "hello"
object c = 3.14f
```

- var타입(auto) 가능 -> `컴파일러 시점에서 결정`
```
var a = 10;
var b = "hello";
var c = 3.14f;
```




# 문법

- `라이브러리 이름 바꾸기` : using my_lib = ClassLibrary1; 




# 형식

byte , int , float, char , bool = stack (함수 종료 시점, 지역변수)  
string, object = heap ( 가비지 컬렉터가 알아서 처리)  


