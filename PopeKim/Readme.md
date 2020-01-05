# C# 공부하자


# 코딩 스탠다드

camelCasing 

`기본 변수명` - 두번째 단어부터는 대문자 (ex: count, rowCount, numCount)
`const` - 전체 대문자(ex: APPLE, APPLE_COUNT, POWER_ON)

# 기본 자료형

- byte - 8비트
- char - `2바이트` (다른언어는 1바이트이지만 c#에서 다름)
- int - 4바이트 정수
- long - 8바이트 정수
- float - 4바이트 실수
- double - 8바이트 실수
-


# String Format
- 포매팅 형식으로 스트링을 만들 수 있음.  
string `message`= string.Format("Name : {0}     Student ID : {1}", name, id);
`Console.WriteLine`(string.Format("Name : {0}     Student ID : {1}", name, id));
