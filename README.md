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

