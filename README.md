# PythonNotes
##### (추후 인터프리터 연결)

## 함수
#### 함수 정의
```
def 함수명(매개변수명1, 매개변수명2):
  pass
```

#### 위치 인수
- 위치 인수 (Positional Argument): 함수 호출 시 적절한 위치에 순서대로 넣는 인수 

#### 임의 인수
- 임의 인수 (Arbitrary Arguments): 위치와 개수가 정해져 있지 않아 임의로 전달할 수 있는 인수
```
def 함수명(*매개변수명):
  pass
```

#### 고정 인수 + 임의 인수
```
def 함수명(매개변수명, *args):
  pass
```

#### 키워드 인수
- 키워드 인수 (Keyword Argument): 함수 호출 시 ‘키=값’ 형태로 전달하는 인수

#### 키워드 인수와 딕셔너리 언패킹
```
def 함수명(**매개변수명):
  pass
```

#### 고정 인수 + 키워드 인수
```
def 함수명(매개변수명, **kwargs):
  pass
```

#### 임의 인수 + 키워드 인수
```
def 함수명(*args, **kwargs):
  pass
```

#### 고정 인수 + 임의 인수 + 키워드 인수
```
def 함수명(매개변수명, *args, **kwargs):
  pass
```

#### 매개변수 초기화
```
def 함수명(매개변수명=초기값):
  pass
```

## 클래스
#### 클래스 정의
```
class 클래스명:
  pass
```

#### 인스턴스 메서드 정의
```
class 클래스명:
  def 메서드명(self):
    pass
```

#### 인스턴스 속성 정의
```
class 클래스명:
  def __init__(self):
    self.속성명1 = 값1
    self.속성명2 = 값2
```

```
class 클래스명:
  def __init__(self, 매개변수명1, 매개변수명2):
    self.속성명1 = 매개변수명1
    self.속성명2 = 매개변수명2
```

```
class 클래스명:
  def __init__(self, *args):
    self.속성명1 = args[0]
    self.속성명2 = args[1]
    self.속성명3 = args[2]
```

```
class 클래스명:
  def __init__(self, **kwargs):
    self.속성명1 = kwargs[‘키명1’]
    self.속성명2 = kwargs[‘키명2’]
    self.속성명3 = kwargs[‘키명3’]
```

```
class 클래스명:
  def __init__(self, *args, **kwargs):
    self.속성명1 = args[0]
    self.속성명2 = args[1]
    self.속성명3 = args[2]
    self.속성명4 = kwargs[‘키명1’]
    self.속성명5 = kwargs[‘키명2’]
    self.속성명6 = kwargs[‘키명3’]
```

#### 인스턴스 속성 제한
```
class 클래스명:
  __slots__ = ['속성명1', '속성명2']
```

#### 클래스 메서드 정의
```
class 클래스명:
  @classmethod
  def 메서드명(cls, 매개변수명1, 매개변수명2):
    pass
```

#### 정적 메서드 정의
```
class 클래스명:
  @staticmethod
  def 메서드명(매개변수명1, 매개변수명2):
    pass
```

#### 클래스 속성 정의
```
class 클래스명:
  속성명1 = 값1
  속성명2 = 값2
```

#### 인스턴스 메서드 접근 제어
```
class 클래스명:
  def __메서드명(self):
    pass
```

#### 인스턴스 속성 접근 제어
```
class 클래스명:
  def __init__(self)
    self.__속성명 = 값
```

## 클로저
#### 클로저 정의 (함수 사용)
def 외부함수명(매개변수명):
  변수명 = 값
  def 내부함수명(매개변수명):
    return 값
  return 내부함수명
  
#### 클로저 정의 (람다식 사용)
def 외부함수명(매개변수명):
  변수명 = 값
  return lambda x: 값
  
#### 클로저 사용
변수명1 = 외부함수명(인자명)
변수명2 = 외부함수명(인자명)

변수명1(인자명)
변수명2(인자명)
