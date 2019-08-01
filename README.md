# switch문 vs if-else

- `switch` - 점프테이블(jump statement 기반)을 만들어서 입력된 값을 보고 특정 위치로 점프(인덱싱,해시 개념)  
오버헤드에 대한 리스크가 있음(메모리 번지 전부 기억)

- `if-else` - 이진 분리(branch statement)를 기반으로 값 두개를 비교하며 실행여부를 계속 판단

```
ex) 임베디드 장치 문제
D사의 하드웨어 마우스를 연결하면 소프트웨어에서 인식을 해야하는데
switch문에서 상단에 있는 소프트웨어면 금방 처리하지만
case 맨끝에 있는 A사의 마우스를 연결시키면 D사보다 느려지는 현상이 발생함.
(그래서 참조테이블(해시)를 만들어 빠른 속도로 접근 가능)  
```

- 최적화 방법 : if문에서 사용자가 자주 사용하는 기능을 순서대로 설정하면 성능 개선에 큰 도움.
여담 : switch문은 case가 4개 이상이면 점프테이블을 사용하고, 4개 미만이면 if else와 똑같이 진행.













# C-sharp



CLI(Common Language Infrastructure) 제공  
여러 언어로 개발해도 .NET 위에서는 동일하게 구동 한다.  

class library = dll로 만듬.   


# 간단한 윈폼의 이해

- `program.cs` : 메인문
- `Form1.cs / Form1.Designer.cs` : 소스코드파일,UI모드

- `Application.Run()` : 파라미터로 넣고, UI쓰레드에 전달.


 





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




# 함수

- `sleep, 슬립 함수` : using System.Threading; Thread.Sleep(1000);  

- `scanf` : System.Console.WriteLine("hello");

- `printf` : var str = Console.Readline();


# 구조


```
namespace WindowsFormsApplication2
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
            this.button1.Click += new System.EventHandler(this.button1_Click);
            Thread.Sleep(5000);
            System.Console.WriteLine("1");

            this.button1.Click -= new System.EventHandler(this.button1_Click2);
          
        }

        private void button1_Click(object sender, EventArgs e)
        {
            MessageBox.Show("에러");
            Thread.Sleep(5000);
            
        }
        private void button1_Click2(object sender, EventArgs e)
        {
            MessageBox.Show("에러22");

        }

    }
}
``` 
위와 같은 구조에서 Form1은 한번만 초기화되고 이벤트 헨들러가 대기함.  
UI 스레드 = 메인 쓰레드에서 공유함.

