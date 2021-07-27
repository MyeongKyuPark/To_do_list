### 파이썬 코딩 무료 강의 (기본편) - 6시간 뒤면 여러분도 개발자가 될 수 있어요 [나도코딩] 

### 정리본

-----



TOC

[1-1. 소개](1\-1.-소개)

[1-2. 환경설정](#---------)



> **\-** (hypene) 포함해서 링크를 거는 방식을 찾아야함



1-1. 소개

Python은 Most Wanted Languages에서 1위 차지. 25.7%를 차지함. 구글 유튜브 나사 넷플릭스 인스타 등 다양한 회사에서 쓰이는 언어. 

기본편 구성은 기본문법, 실생활 기반 예제, 퀴즈. 활용편은 라이브러리 기초 사용법, 8개의 실전 프로젝트(머신러닝, 데이터 분석, 업무 자동화, 아두이노 RC Car, 얼굴 인식 등)



1-2. 환경설정

skip. (Jupyter Notebook 사용했음)



2-1 숫자 자료형

print() 문을 활용하여 다양한 사칙연산이 가능함. e.g. print(5+3*(4\*2)) => 29



2-2 문자열 자료형

print() 문을 통해 문자열 같은 경우 `''` 와 `""` 로 표현이 가능하고 더했을 때는 내용이 뒤에 덧붙혀짐. 곱셈은 덧셈을 여러번 한 거와 동일하게 뒤에 n번 덧붙임. e.g. print("ㅋ"*3) => ㅋㅋㅋ



2-3 boolean 자료형

boolean (참 거짓 판단)

e.g1. print(5 < 10) => False

e.g2. print(not True) => False



2-4 변수

``````python
'''
print("우리집 강아지의 이름은 연탄이예요")
print("연탄이는 4살이며, 산책을 아주 좋아해요")
print("연탄이는 어른일까요? True")
위 내용을 변수로 활성화
'''

animal = "강아지"
name = "연탄이"
age = 4
hobby = "산책"
is_age = age >= 3

print("print("우리 집 " + animal + "의 이름은 " + name + "예요")")
print(name + "는 " + str(age) + "살이며, " + hobby + "을 아주 좋아해요")
print(name + "는 " "어른일까요? "+ str(is_adult))
``````

프린트문에 변수를 더하기 위해서 `+ +` 또는 `, ,`를 사용. 단 `, ,` 사용하면 띄어쓰기가 적용 됨. 또한 `, ,` 사용시에는 문자열 str로 표현하겠다는 표시를 안해도 됨. e.g. str(age)를 age로 기재해도 괜찮음.

> cf) 맨 앞에 더할 경우 앞에 + 붙이면 오류. 마찬가지로 맨 마지막에도 + 더하면 오류



2-5 주석

한 문장 주석처리: #

여러문장 주석처리: 전후로 ''' (백틱 \``` 아님)

선택한 문장 주석처리: ctrl + /



2-6 퀴즈 #1

`````python
# Quiz) 변수를 이용하여 다음 문장을 출력하시오
# 변수명 : station
# 변수값: "사당", "신도림", "인천공항" 순서대로 입력
# 출력문장: XX 행 열차가 들어오고 있습니다.

station = "사당"
print(station + " 행 열차가 들어오고 있습니다.")
station = "신도림"
print(station + " 행 열차가 들어오고 있습니다.")
station = "인천공항"
print(station + " 행 열차가 들어오고 있습니다.")
`````



3-1 연산자

`````python
print(5 % 3) => 나머지 2
print(5 // 3) => 몫 1
print(5 ** 3) => 5^3 = 125
print(5 != 3) => True
print(not(5 != 3)) => False
print(2+3 == 5) => True
print((3>0) and (3 < 5)) => True
`````



3-2 간단한 수식

```python
number = 2 + 3 * 4 #14
print(number) # 14
number += 2 # 16
number *= 2 # 32
number /= 2 # 16
number -= 2 # 14
number %= 2 # 0
```



3-3 숫자처리함수

```python
print(abs(-5)) # 5
print(pow(4,2)) # 16
print(max(5,12)) # 12
print(min(5,12)) # 5
print(round(3.14)) # 3
print(round(4.99)) # 5

from math import *
print(floor(4.99)) # 내림. 4
print(ceil(3.14)) #올림. 4
print(sqrt(16)) #제곱근. 4
```



3-4 랜덤함수

```python
from random import *
print(random()) # 0.0 ~ 1.0 미만의 임의의 값 생성
print(random() * 10) # 0.0 ~10.0 미만의 임의의 값 생성
print(int(random() * 10)) # 0 ~ 10 미만의 임의의 값 생성
print(int(random() * 10) + 1) # 1 ~ 10 이하의 임의의 값 생성
print(int(random() * 45) + 1) # 1 ~ 45 이하의 임의의 값 생성
print(randrange(1,46)) # 1 ~ 46 미만의 임의의 값 생성
print(randint(1,45)) # 1 ~ 45 이하의 임의의 값 생성
```



3-5 퀴즈 #2

```python
'''
Quiz) 당신은 최근에 코딩 스터디 모임을 새로 만들었습니다.
월 4회 스터디를 하는데 3번은 온라인으로 하고 1번은 오프라인으로 하기로 했습니다.
아래 조건에 맞는 오프라인 모임 날짜를 정해주는 프로그램을 작성하시오.

조건1: 랜덤으로 날짜를 뽑아야함
조건2: 월별 날짜는 다름을 감안하여 최소 일수인 28이내로 정함
조건3: 매월 1~3일은 스터디 준비를 해야 하므로 제외

(출력문 예제)
오프라인 스터디 모임 날짜는 매월 x 일로 선정되었습니다.
'''

print("오프라인 스터디 모임 날짜는 매월 " + str(randint(4,28)) + "일로 선정되었습니다.")

print("오프라인 스터디 모임 날짜는 매월" ,randint(4,28),"일로 선정되었습니다.")

date = randint(4,28)
print("오프라인 스터디 모임 날짜는 매월 " + str(date) + "일로 선정되었습니다.")
```



4-1 문자열

> 2-2 참조



4-2 슬라이싱

```python
pmk = "960107-1234567"
print("성별 : " + pmk[7]) # 7번째 자리 알려줘 => 1
print("연도 : " + pmk[0:2]) # 0 부터 2 직전까지 => 96
print("월 : " + pmk[2:4]) # 2 부터 4 직전까지 => 01
print("일 : " + pmk[4:6]) # 4 부터 6 직전까지 => 07
print("생년월일 : " + pmk[:6]) # 처음부터 6 직전까지 => 960107
print("뒤 7자리 : " + pmk[7:]) # 처음부터 끝까지 => 1234567
print("뒤 7자리 (뒤에부터): " + pmk[-7:]) # 맨 뒤에서 7번째부터 끝까지 => 1234567
```



4-3 문자열처리함수

```python
python = "Python is Amazing"
print(python.lower()) # 소문자 출력 => python is amazing
print(python.upper()) # 대문자 출력 => PYTHON IS AMAZING
print(python[0].isupper()) # 첫번째 문자열이 대문자인지 => True
print(len(python)) # 문자열 길이 출력. => 17
print(python.replace("Python", "Java")) # 단어를 교체 => Java is amazing
print(python) # => Python is Amazing. cf. 위에서 변수를 바꾼게 아니라 print문 써서 출력한거라

index = python.index("n") # n의 위치는 몇번째인지 = 5
print(index) # 5
index = python.index("n", index + 1) # index + 1번째 부터 n의 위치는 어디인지
print(index) # 15 (16번째에 위치한다)

print(python.find("n")) # 위치를 찾음. => 5
print(python.find("Java")) # => 없어서 -1을 반환함.
print(python.index("Java")) # => 없어서 에러가 발생함. 아래 내용으로 안 이어짐

print(python.count("n")) # n이 몇번 있는지 => 2
```



4-4 문자열 포맷

```python
#방법 1
print("나는 %d살입니다." % 20) 
print("나는 %s을 좋아해요." % "파이썬") # 문자열 가져올게요
print("Apple 은 %c로 시작해요." % "A") # 한 글자 가져올게요
print("나는 %s살입니다." % 20) # 숫자도 가능
print("나는 %s색과 %s색을 좋아해요." %("파란", "빨간"))

#방법 2
print("나는 {}살입니다." .format(20))
print("나는 {}색과 {}색을 좋아해요." .format("파란","빨간"))
print("나는 {0}색과 {1}색을 좋아해요." .format("파란","빨간"))
print("나는 {1}색과 {0}색을 좋아해요." .format("파란","빨간"))

#방법 3
print("나는 {age}살이며, {color}색을 좋아해요." .format(age = 20, color = "빨간"))
print("나는 {age}살이며, {color}색을 좋아해요." .format(color = "빨간", age = 20))

#방법 4 (v3.6 이상~)
age = 20
color = "빨간"
print(f"나는 {age}살이며,{color}색을 좋아해요.")
```



4-5. 탈출문자

```python
''' 
\n : 줄바꿈
\ : 탈출. 특수문자 앞에 쓰면 있는 그대로 쓸 수 있음.
\r : 커서를 맨 앞으로 이동
\b : 백스페이스(한 글자 삭제)
\t : 탭

'''

print("백문이 불여일견 \n 백견이 불여일타")
print("저는 \"박명규\"입니다.")
print("C:\\Users\\WALNUT\\To_do_list") # C:\Users\WALNUT\To_do_list
print("Red Apple\rPine") # => PineApple
print("Redd\bApple") # => RedApple
print("Red\tApple") # => Red	Apple
```



4-6 퀴즈 #3

```python
'''
Quiz) 사이트별로 비밀번호를 만들어 주는 프로그램을 작성하시오

예) http://naver.com
규칙1: http:// 부분은 제외 => naver.com
규칙2: 처음 만나는 점(.) 이후 부분은 제외 => naver
규칙3: 남은 글자 중 처음 세자리 +  글자 갯수 + 글자 내 'e' 갯수 + "!" 로 구성
			(nav)				  (5)			(1)			  (!)
예) 생성된 비밀번호 : nav51!
'''
 
url = "http://naver.com"
my_str = url.replace("http://", "") # 규칙1
print(my_str)

my_str = my_str[0:my_str.index(".")] # 규칙2 my_str[0:5]와 같음
print(my_str)

pw = my_str[:3] + str(len(my_str)) + str(my_str.count("e")) + "!"
print("{0}의 비밀번호는 {1}입니다" .format(url,pw))
```



 5-1 리스트

```python
# 지하철 칸 별로 10명, 20명, 30명
subway1 = 10
subway2 = 20
subway3 = 30

subway = [10, 20, 30]
print(subway)

subway=["유재석","조세호","박명수"]
print(subway)

# 조세호씨가 몇 번째 칸에 타고 있는가?
print(subway.index("조세호"))

# 하하씨가 다음 정류장에서 다음 칸에 탐
subway.append("하하")
print(subway)

# 정형돈씨를 유재석 / 조세호 사이에 태워봄
subway.insert(1,"정형돈")
print(subway)

# 지하철에 있는 사람을 한 명씩 뒤에서 꺼냄
print(subway.pop())
print(subway)

# 같은 이름의 사람이 몇 명 있는지 확인
subway.append("유재석")
print(subway)
print(subway.count("유재석"))

# 정렬도 가능
num_list = [5,2,4,3,1]
num_list.sort()
print(num_list)

# 순서 뒤집기 가능
num_list.reverse()
print(num_list)

# 모두 지우기
num_list.clear()
print(num_list)

# 다양한 자료형 함께 사용
mix_list = ["조세호", 20, True]
print(mix_list)

# 리스트 확장
num_list = [5,4,3,2,1]
num_list.extend(mix_list)
print(num_list)
```



5-2 딕셔너리

```python
cabinet = {3:"유재석", 100:"김태호"} # 3번 키를 유재석씨가 가지고 갔다.
print(cabinet[3]) # 3번 키 가지고 간 사람 => 유재석
print(cabinet[100]) 
print(cabinet.get(3)) # 3번 키 가지고 간 사람 => 유재석
print(cabinet.get(5)) # 5번 키 가지고 간 사람 => None 
# print(cabinet[5]) 5번 키 가지고 간 사람이 없는데 왜 달라해 => 오류 
print(cabinet.get(5, "사용 가능")) # => 사용 가능

print(3 in cabinet) # True
print(5 in cabinet) # False

cabinet = {"A-3":"유재석", "B-100":"김태호"}
print(cabinet)
print(cabinet["A-3"])
print(cabinet["B-100"])

# 새 손님
print(cabinet)
cabinet["A-3"] = "김종국"
cabinet["C-20"] = "조세호"
print(cabinet)

# 간 손님
del cabinet["A-3"]
print(cabinet)

# key 들만 출력
print(cabinet.keys())

# value 들만 출력
print(cabinet.values())

# key, value 쌍으로 출력
print(cabinet.items())

# 목욕탕 폐점
cabinet.clear()
print(cabinet)
```



5-3 튜플

```python
menu = ("돈까스", "치즈까스")
print(menu[0])
print(menu[1])

# menu.add("생선까스") => tuple은 add 못 씀

name = "김종국"
age = 20
hobby = "코딩"
print(name, age, hobby)

(name, age, hobby) = ("김종국", 20, "코딩")
print(name, age, hobby)
```



5-4 세트 (집합)  

```python
# 집합 (set)
# 중복 안 됨, 순서 없음
my_set = {1,2,3,3,3}
print(my_set)

java = {"유재석","김태호","양세형"}
python = set(["유재석","박명수"])

# 교집합 (java와 python을 모두 할 수 있는 개발자)
print(java & python)
print(java.intersection(python))

# 합집합 (java를 할 수 있거나 python을 할 수 있는 개발자)
print(java | python)
print(java.union(python))

# 차집합 (java는 할 수 있지만 python을 할 줄 모르는 개발자)
print(java - python)
print(java.difference(python))

# python을 할 줄 아는 사람이 늘어남
python.add("김태호")
print(python)

# java를 잊었어요
java.remove("김태호")
print(java)
```



5-5 자료구조의 변경

```python
# 자료구조의 변경
# 커피숍
menu = {"커피", "우유", "주스"}
print(menu, type(menu))

menu = list(menu)
print(menu, type(menu))

menu = tuple(menu)
print(menu, type(menu))

menu = set(menu)
print(menu, type(menu))
```



5-6 퀴즈 #4

```python
'''
Quiz) 당신의 학교에서는 파이썬 코딩 대회를 주최합니다.
참석률을 높이기 위해 댓글 이벤트를 진행하기로 하였습니다.
댓글 작성자들 중에 추첨을 통해 1명은 치킨, 3명은 커피 쿠폰을 받게 됩니다.
추첨 프로그램을 작성하시오

조건1: 편의상 댓글은 20명이 작성하였꼬 아이디는 1~20이라고 가정
조건2: 댓글 내용과 상관 없이 무작위로 추첨하되 중복 불가
조건3: random 모듈의 shuffle과 sample을 활용

(출력 예제)
- - 당첨자 발표 - -
치킨 당첨자 : 1
커피 당첨자 : [2, 3, 4]
- - 축하합니다 - -

(활용 예제)
from random import *
lst = [1,2,3,4,5]
print(lst)
shuffle(lst) => 임의로 순서 섞기
print(lst) 
print(sample(lst,1))  => lst 에서 샘플 1개 랜덤으로 뽑기
'''

'''
내가 작성한 1차 답안
from random import *

lst = range(1,21) # 1부터 20까지 숫자를 생성. 단 type은 range로 형성됨
# print(lst,type(lst)) => range(1,21) <class 'range'> 로 나타남
lst = list(lst) # range 형식 그리고 set 형식은{} shuffle이 안됨
shuffle(lst) 
lst = set(lst) # 리스트로[] 가져가면 집합 개념이 적용이 안됨. 조건2

chicken = sample(lst,1)
chicken = set(chicken)

lst2 = lst - chicken

coffee = sample(lst2,3)

print("- - 당첨자 발표 - - \n" 
      "치킨 당첨자 : %s \n"
      "커피 당첨자 : %s \n"
      "- - 축하합니다 - -" %(chicken, coffee))
      
=> 결과값 
- - 당첨자 발표 - - 
치킨 당첨자 : {13} 
커피 당첨자 : [1, 18, 20] 
- - 축하합니다 - -

치킨 당첨자에 중괄호{세트} 생김.
'''

# 수정 답안
from random import *

lst = range(1,21) 
lst = list(lst) 
shuffle(lst) 
lst = set(lst)

winner = sample(lst,4)

''' 
내가 쓴 수정 답안
print("- - 당첨자 발표 - - \n" 
      "치킨 당첨자 : %s \n"
      "커피 당첨자 : %s \n"
      "- - 축하합니다 - -" %(winner[0], winner[1:]))
'''

# 영상이 쓴 답안
print("- - 당첨자 발표 - - ") 
print("치킨 당첨자 : {0}" .format(winners[0]))
print("커피 당첨자 : {0}" .format(winners[1:]))
print("- - 축하합니다 - -")
```



6-1. if

```python
weather = input("오늘 날씨는 어때요? ")
if weather == "비" or "눈":
    print("우산을 챙기세요.")
    
elif weather == "미세먼지":
    print("마스크를 챙기세요")
    
else:
    print("준비물 필요 없어요.")

temp = int(input("기온은 어때요? "))
if 30 <= temp:
    print("너무 더워요, 나가지 마세요")
    
elif 10 <= temp < 30:
    print("괜찮은 날씨예요")
    
elif 0 <= temp and temp < 10:
    print("외투를 챙기세요")
    
else:
    print("너무 추워요. 나가지 마세요")
```



6-2. for 

```python
print("대기번호 : 1")
print("대기번호 : 2")
print("대기번호 : 3")
print("대기번호 : 4")

for waiting_no in range(0,5): # 0, 1, 2, 3, 4
    print("대기번호 : {0}" .format(waiting_no))

starbucks = ["아이언맨","토르","아이엠 그루트"]
for customer in starbucks:
    print("{0}, 커피가 준비되었습니다." .format(customer))
```



6-3 while

```python
 # while
customer = "토르"
index = 5
while index >=1 :
    print("{0}, 커피가 준비 되었습니다. {1} 번 남았어요." .format(customer,index))
    index -= 1
    if index == 0:
        print("커피는 폐기처분되었습니다.")

'''    
customer = "아이언맨"
while True:
    print("{0}, 커피가 준비 되었습니다. 호출 {1} 회" .format(customer, index))
    index += 1 #강제 종료하기 위해 ctrl + c
''' 
    
customer = "토르"
person = "Unknown"

while person != customer :
    print("{0}, 커피가 준비 되었습니다." .format(customer))
    person = input("이름이 어떻게 되세요? ")
```



6-4 continue 와 break

```python
absent = [2,5] # 결석
no_book = [7] # 책을 깜빡했음
for student in range(1,11): # 1,2,3,4,5,6,7,8,9,10
    if student in absent:
        continue
    elif student in no_book:
        print("오늘 수업 여기까지. {0}는 교무실로 따라와" .format(student))
        break
    print("{0}, 책을 읽어봐" .format(student))
```



6-5. 한 줄 for

```python
# 출석번호가 1 2 3 4, 앞에 100을 붙이기로 함 -> 101 102 103 104.
students = [1,2,3,4,5]
print(students)
students = [i+100 for i in students]
print(students)

# 학생 이름을 길이로 변환
students = ["Iron man", "Thor", "I am groot"]
students = [len(i) for i in students]
print(students)

# 학생 이름을 대문자로 변환
students = ["Iron man", "Thor", "I am groot"]
students = [i.upper() for i in students]
print(students)
```



6-6. 퀴즈 #5

```python
'''
Quiz) 당신은 Cocoa 서비스를 이용하는 택시 기사입니다.
50명의 승객과 매칭 기회가 있을 때, 총 탑승 승객 수를 구하는 프로그램을 작성하시오.

조건1 : 승객별 운행 소요 시간은 5분 ~ 50분 사이의 난수로 정해집니다.
조건2 : 당신은 소요 시간 5분 ~ 15분 사이의 승객만 매칭해야 합니다.

(출력문 예제)
[0] 1번째 손님 (소요시간 : 15분)  # 동그라미는 선택이 됐다는 뜻임.
[ ] 2번째 손님 (소요시간 : 50분)
[0] 3번째 손님 (소요시간 : 5분)
...
[ ] 50번째 손님 (소요시간 : 16분)

총 탑승 승객 : 2 분

'''
'''
#내가 푼 답안
from random import *
count = 0
for i in range(0,51):
    print("[{0}] {1}번째 손님 (소요시간 : {2}분)" .format(select,i,minute))
    minute = randint(5,50)
    if 5 <= minute <= 15:
        select = "0"
        count += 1
    else:
        select = " "

print("총 탑승 승객: {0} 분".format(count))
'''
# 영상 답안
from random import *
cnt = 0 # 총 탑승 승객 수
for i in range(1,51): # 1 ~ 50 이라는 수 (승객)
    time = randrange(5,51) # 5분 ~ 50분 소요 시간
    if 5 <= time <= 15: # 5분 ~ 15분 이내의 손님(매칭 성공), 탑승 승객 수 증가처리
        print("[O] {0}번째 손님 (소요시간 : {1}분)".format(i,time))
        cnt +=1
    else: # 매칭 실패한 경우
        print("[] {0}번째 손님 (소요시간 : {1}분)".format(i,time))
        

print("총 탑승 승객 : {0} 분".format(cnt))
```



7-1 함수

```python
def open_account():
    print("새로운 계좌가 생성되었습니다.")  # open_account() 함수를 정의할거야: print
    
open_account() # 함수를 실행해줘
```



7-2 전달값과 반환값

```python
def open_account():
    print("새로운 계좌가 생성되었습니다.")  # open_account() 함수를 정의할거야: print
    
def deposit(balance, money): # balance : 잔액, money : 입금할 돈
    print("입금이 완료되었습니다. 잔액은 {0} 원입니다." .format(balance + money))
    return balance + money

balance = 0 # 잔액
balance = deposit(balance, 1000) # return 값인 1000원을 balance에 넣어줌
print(balance) # 1000

def withdraw(balance,money): #출금
    if balance >= money: # 잔액이 출금보다 많으면
        print("출금이 완료되었습니다. 잔액은 {0} 원입니다.".format(balance-money))
        return balance - money
    else:
        print("출금이 완료되지 않았습니다. 잔액은 {0} 원입니다." .format(balance))
        return balance

balance = 0 # 잔액
balance = deposit(balance, 1000) # return 값인 1000원을 balance에 넣어줌
balance = withdraw(balance, 2000) # 출금이 완료되지 않았습니다. 잔액은 1000 원입니다.
balance = withdraw(balance, 500) # 출금이 완료되었습니다. 잔액은 500 원입니다.

def withdraw_night(balance, money) : # 저녁에 출금
    commission = 100 # 수수료 100원, balance 보다 많은 돈 출금하는 if 문은 생략
    return commission, balance - money - commission # tuple 값으로 반환됨
    
balance = 0 # 잔액
balance = deposit(balance, 1000)
commission, balance = withdraw_night(balance, 500)
print("수수료는 {0} 원이며, 잔액은 {1} 원입니다." .format(commission, balance))   # 수수료는 100 원이며, 잔액은 400 원입니다.
```



7-3 기본값

```python
'''def profile(name, age, main_lang):
    print("이름: {0}, \t나이: {1}\t주 사용 언어: {2}" \
         .format(name,age,main_lang))
# \t 은 탭키, \ + 엔터는 한칸띄어져있지만 실제로는 한 문장 취급
    
profile("유재석", 20, "파이썬")
profile("김태호", 25, "자바")
'''
# 같은 학교 같은 학년 같은 반 같은 수업.
def profile(name, age = 17, main_lang = "파이썬"):
    print("이름: {0}, \t나이: {1}\t주 사용 언어: {2}" \
         .format(name,age,main_lang))
profile("유재석", 18) # 이름: 유재석, 	나이: 18	주 사용 언어: 파이썬
profile("김태호") # 이름: 김태호, 	나이: 17	주 사용 언어: 파이썬

# 입력하면 입력값 호출 가능. 입력 안하면 기본값 호출.
```



7-4. 키워드값

```python
def profile(name, age, main_lang):
    print(name, age, main_lang)
        
profile(name="유재석", main_lang="파이썬", age=20)
profile(main_lang = "자바", age=25, name="김태호")
#순서 상관 없이 입력하면 입력값 넣을 수 있음
```



7-5. 가변인자

```python
'''def profile(name, age, lang1, lang2, lang3, lang4, lang5):
    print("이름: {0}\t나이 : {1}\t".format(name,age), end="") 
    # end="" 는 한칸 띄어쓰기 없이 뒤에 붙여서 쓸 때 유용하게 쓰임.
    print(lang1, lang2, lang3, lang4, lang5)
    
profile("유재석", 20, "Python", "Java", "C", "C++", "C#")
profile("김태호", 25, "Kotlin", "Swift", "", "", "")
'''
# 가변인자 : 서로 다른 갯수의 값을 넣어 줄 때 *가변인자를 활용
def profile(name, age, *language):
    print("이름: {0}\t나이 : {1}\t".format(name,age), end="") 
    for lang in language:
        print(lang, end =" ")
    print()
    
profile("유재석", 20, "Python", "Java", "C", "C++", "C#", "JavaScript")
profile("김태호", 25, "Kotlin", "Swift", "", "", "")
```



7-6. 지역변수와 전역변수

```python
# 지역변수 : 함수 내에서만 쓸 수 있음. 함수 호출 될 때 만들어졌다가 호출 끝나면 사라짐
# 전역변수 : 프로그램 내에 어디서든지 부를 수 있는 변수


'''
STEP 1
gun = 10 # 총 10자루

def checkpoint(soldiers): # 경계근무 나가는 군인 수
    gun = gun - soldiers # checkpoint 내에서 만들어진 지역변수
    print("[함수 내] 남은 총 : {0}".format(gun))
    
print("전체 총 : {0}".format(gun))
checkpoint(2)
print("남은 총 : {0}".format( gun))

# 실행해보면 함수 내에서 gun이 초기화, 할당 안돼서 오류가 뜸

'''

'''
STEP 2
# 지역 변수 gun = 20이라 할당해보자.
gun = 10 # 총 10자루

def checkpoint(soldiers): # 경계근무 나가는 군인 수
	gun = 20 # 
    gun = gun - soldiers # checkpoint 내에서 만들어진 지역변수
    print("[함수 내] 남은 총 : {0}".format(gun))
    
print("전체 총 : {0}".format(gun))
checkpoint(2) # 2명이 경계 근무 나감
print("남은 총 : {0}".format( gun))

# 결과값
전체 총 : 10
[함수 내] 남은 총 : 18
남은 총 : 10

checkpoint() 함수 안에서만 2개가 빼짐.
'''
# STEP 3
gun = 10 # 총 10자루

def checkpoint(soldiers): # 경계근무 나가는 군인 수
    global gun # 전역 공간에 있는 gun 사용
    gun = gun - soldiers # checkpoint 내에서 만들어진 지역변수
    print("[함수 내] 남은 총 : {0}".format(gun))
    
print("전체 총 : {0}".format(gun))
checkpoint(2) # 2명이 경계 근무 나감
print("남은 총 : {0}".format( gun))

'''
# 결과값
전체 총 : 10
[함수 내] 남은 총 : 8
남은 총 : 10
'''

gun = 10 # 총 10자루

def checkpoint(soldiers):  # 경계근무 나가는 군인 수
    global gun # 전역 공간에 있는 gun 사용
    gun = gun - soldiers # checkpoint 내에서 만들어진 지역변수
    print("[함수 내] 남은 총 : {0}".format(gun))
    
print("전체 총 : {0}".format(gun))
checkpoint(2) # 2명이 경계 근무 나감
print("남은 총 : {0}".format( gun))

# 일반적으로는 전역변수를 많이 쓰게 되면 코드 관리가 어려워짐으로 권장하지 않음. 가급적 함수의 전달값 PARAMETER로 던져서 계산하고 반환값을 받아서 사용하는 방법을 권장함. => STEP 4

# STEP 4
gun = 10 # 총 10자루

def checkpoint(soldiers):  # 경계근무 나가는 군인 수
    global gun # 전역 공간에 있는 gun 사용
    gun = gun - soldiers # checkpoint 내에서 만들어진 지역변수
    print("[함수 내] 남은 총 : {0}".format(gun))
    
def checkpoint_ret(gun, soldiers):
    gun = gun - soldiers
    print("[함수 내] 남은 총 : {0}".format(gun))
    return gun
    
print("전체 총 : {0}".format(gun))
# checkpoint(2) # 2명이 경계 근무 나감
gun = checkpoint_ret(gun,2)
print("남은 총 : {0}".format(gun))
```



7-7. 퀴즈 #6

```python
'''
Quiz) 표준 체중을 구하는 프로그램을 작성하시오

* 표준 체중 : 각 개인의 키에 적당한 체중
    
(성별에 따른 공식)
	남자 : 키(m) x 키 (m) x 22
	여자 : 키(m) x 키 (m) x 21
	
조건1 : 표준 체중은 별도의 함수 내에서 계산
		* 함수명 : std_weight
		* 전달값 : 키(height), 성별(gender)
조건2 : 표준 체중은 소수점 둘째자리까지 표시

(출력 예제)
키 175cm 남자의 표준 체중은 67.38kg 입니다.

'''

height = input("height: ")
gender = input("성별(남/여): ")
               
if gender == "남"
    std_weight = height * height * 22
    
elif gender == "여"
    std_weight = height * height * 21
        
else:
    print("다시 입력해주세요")
        
# print("키 {0}cm {1}의  표준 체중은 {3}kg 입니다" .format(height,gender,std_weight))

# gender = ""

# def normal_man(height):
#     std_weight = height * height * 22
#     return std_weight


# def normal_woman(height):
#     std_weight = height * height * 21
#     return std_weight
```



7-7. 퀴즈 #6

```python
'''
Quiz) 표준 체중을 구하는 프로그램을 작성하시오

* 표준 체중 : 각 개인의 키에 적당한 체중
    
(성별에 따른 공식)
	남자 : 키(m) x 키 (m) x 22
	여자 : 키(m) x 키 (m) x 21
	
조건1 : 표준 체중은 별도의 함수 내에서 계산
		* 함수명 : std_weight
		* 전달값 : 키(height), 성별(gender)
조건2 : 표준 체중은 소수점 둘째자리까지 표시

(출력 예제)
키 175cm 남자의 표준 체중은 67.38kg 입니다.

'''

''' 
모범답안
def std_weight(height, gender): # 키 m 단위 (실수), 성별 "남자" / "여자"
    if gender == "남자":
        return height * height * 22
    else :
        return height * height * 21
    
height = 175 # cm 단위
gender = "남자"
weight = round(std_weight(height / 100, gender),2)
print("키 {0}cm {1}의 표준 체중은 {2}kg 입니다."  .format(height, gender, weight))
'''

```



8-1. 표준입출력

```python
print("Python", "Java") # Python Java
print("Python" + "Java") # PythonJava
print("Python", "Java", sep=",") # separate => Python,Java
print("Python", "Java", "JavaScript", sep=" vs ") # Python vs Java vs JavaScript

print("Python", "Java", sep=",", end="?")
print("무엇이 더 재밌을까요?") # Python,Java?무엇이 더 재밌을까요?

print("Python", "Java", sep=",")# Python,Java
print("무엇이 더 재밌을까요?") # 무엇이 더 재밌을까요?

import sys

print ("Python", "Java", file=sys.stdout) # std out 표준 출력
print ("Python", "Java", file=sys.stderr) # std err 표준 에러

#시험 성적
scores = {"수학":0, "영어":50, "코딩":100}
for subject, score in scores.items():
    #print(subject, score)
    print(subject.ljust(8), str(score).rjust(4), sep=":")

# .ljust(8) 8킨 확보한상태에서 왼쪽 정렬 .rjust(4) 4칸 확보한 상태에서 오른쪽 정렬

# 은행 대기순번표
# 001, 002, 003, ...

for num in range(1, 21):
    print("대기번호: " + str(num).zfill(3))
    # .zfill 3 공간을 확보하고 값 없는 빈 공간은 0으로 채우기

answer = input("아무 값이나 입력하세요 : ")
print(type(answer)) # 사용자 입력을 통해서 값을 받으면 항상 문자열 형태로 저장됨
print("입력하신 값은 " + answer + "입니다.")    
```



8-2. 다양한 출력포맷

```python
# 빈 자리는 빈 공간으로 두고, 오른쪽 정렬을 하되, 총 10자리 공간을 확보
print("{0: >10}".format(500))

# 양수일 땐 +로 표시, 음수일 땐 -로 표시
print("{0: >+10}".format(500)) # > : 오른쪽으로, + : 양수면 +, 음수면 -표시
print("{0: >+10}".format(-500))

# 왼쪽 정렬하고, 빈칸으로 _로 채움
print("{0:_<10}".format(500))

# 3자리 마다 콤마를 찍어주기
print("{0:,}".format(100000000000)) # 100,000,000,000

# 3자리 마다 콤마를 찍어주기, +- 부호도 붙이기
print("{0:+,}".format(-100000000000)) # -100,000,000,000

# 3자리 마다 콤마를 찍어주기, 부호도 붙이고, 자릿수도 확보하기
# 돈이 많으면 행복하니까 빈 자리는 ^로 채워주기, 왼쪽정렬 30자리확보
print("{0:^<+30,}".format(100000000000))

# 소수점 출력
print("{0:f}".format(5/3))

# 소수점 특정 자리수까지만 표시
print("{0:.2f}".format(5/3)) #.2 소수점 3번째자리에서 반올림. 2째자리까지만
```



8-3. 파일입출력

```python
# score_file = open("score.txt","w", encoding = "utf8") # score_file 이라는 변수는 어떤거냐면 score.txt를 열고 write인 덮어쓰기 하겠다. utf8로 인코딩 하겠다. (한국말 쓸 때)
# print("수학 : 0", file=score_file) # 프린트문은 자동으로 줄바꿈이 됨
# print("영어 : 50", file=score_file)
# score_file.close()

# score_file = open("score.txt","a", encoding = "utf8") # append 
# score_file.write("과학 : 80") 
# score_file.write("\n코딩 : 100")
# score_file.close()

# score_file = open("score.txt","r", encoding = "utf8") # read
# print(score_file.read()) # 파일의 모든 내용을 읽어와서 출력
# score_file.close()

# score_file = open("score.txt", "r", encoding = "utf8")
# print(score_file.readline(), end="") # 줄 별로 읽기, 한 줄 읽고 커서는 다음 줄로 이동
# print(score_file.readline(), end="")
# print(score_file.readline(), end="")
# print(score_file.readline(), end="")
# score_file.close()

# score_file = open("score.txt", "r", encoding = "utf8")
# while True: # 라인이 몇 줄인지 모를 때 끝까지 출력하려고 할 때
#     line = score_file.readline()
#     if not line:
#         break
#     print(line, end="") #end = "" 줄바꿈 없이 출력
# score_file.close()

# score_file = open("score.txt", "r", encoding = "utf8")
# lines = score_file.readlines() # list 형태로 저장
# for line in lines: # list에서 한 줄씩 불러와서
#     print(line,end="") # 출력한다
    
# score_file.close() 
    
```



8-4. pickle

```python
# pickle이란: 프로그램 상에서 사용하는 데이터를 파일 형태로 저장.
# 그 파일을 누군가에게 주면 그분이 파일을 열어서 피클을 사용해서 데이터를 가져와서 또 쓸 수 있음

import pickle
# profile_file = open("profile.pickle","wb") # wb는 write binary. pickle은 항상 binary 타입으로 정리해줘야함. 피클은 따로 인코딩 설정은 안해줘도 됨
# profile = {"이름":"박명수", "나이":30, "취미":["축구","골프","코딩"]}
# print(profile)
# pickle.dump(profile, profile_file) # profile 에 있는 정보를 file 에 저장
# profile_file.close()

profile_file = open("profile.pickle","rb") # rb는 read binary
profile = pickle.load(profile_file) # 파일에 있는 정보를 profile 에 불러오기
print(profile)
profile_file.close()
```



8-5. with

```python
import pickle

# with open("profile.pickle", "rb") as profile_file: # profile.pickle 파일을 열어서 profile_file이라는 변수에 저장
#     print(pickle.load(profile_file)) # 파일 내용을 pickle.load 통해 불러와서 출력
# # close 따로 안해줘도 됨.

# with open("study.txt", "w", encoding="utf8") as study_file:
#     study_file.write("파이썬을 열심히 공부하고 있어요")
    
with open("study.txt", "r", encoding = "utf8") as study_file:
    print(study_file.read())

```



8-6. 퀴즈 #7

```python
'''
Quiz) 당신의 회사에서 매주 1회 작성해야 하는 보고서가 있습니다.
보고서는 항상 아래와 같은 형태로 출력되어야 합니다.

- X 주차 주간보고 -
부서 :
이름 :
업무요약 :

1주차부터 50주차까지의 보고서 파일을 만드는 프로그램을 작성하시오

조건 : 파일명은 '1주차.txt', '2주차.txt', ... 와 같이 만듭니다.
'''
# 모범답안
for i in range(1,51):
    with open(str(i) + "주차.txt", "w", encoding="utf8") as report_file:
        report_file.write("- {0} 주차 주간보고 -".format(i))
        report_file.write("\n부서 :")
        report_file.write("\n이름 :")
        report_file.write("\n업무요약 :")
        
'''
내가 쓴 답안 #보완


weeknum = 0

while True:
    week_num += 1
    report_file = open('report.txt', "w", encoding = "utf8")
    print("- {0} 주차 주간보고 -", .format(week_num), file=report_file)
    print("부서 : ", file=report_file)
    print("이름 : ", file=report_file)
    print("업무요약 : ", file=report_file)
    
    if week_num == 51:
    break
    
'''
```



9-1. 클래스

```python
'''
# 마린 : 공격 유닛, 군인, 총을 쏠 수 있음
name = "마린" # 유닛의 이름
hp = 40 # 유닛의 체력
damage = 5 # 유닛의 공격력

print("{0} 유닛이 생성되었습니다.".format(name))
print("체력 {0}, 공격력{1}\n".format(hp,damage))

# 탱크 : 공격 유닛, 탱크. 포를 쏠 수 있는데, 일반 모드 / 시즈 모드.
tank_name = "탱크"
tank_hp = 150
tank_damage = 35

print("{0} 유닛이 생성되었습니다.".format(tank_name))
print("체력 {0}, 공격력{1}\n".format(tank_hp,tank_damage))

tank2_name = "탱크"
tank2_hp = 150
tank2_damage = 35

print("{0} 유닛이 생성되었습니다.".format(tank2_name))
print("체력 {0}, 공격력{1}\n".format(tank_hp,tank2_damage))

def attack(name, location, damage):
    print("{0} : {1} 방향으로 적군을 공격합니다. [공격력 {2}]".format(\
                                                       name,location,damage))
    
attack(name, "1시", damage)
attack(tank_name, "1시", tank_damage)
attack(tank_name, "1시", tank2_damage)


# 매 번 탱크 생성될때마다 숫자 붙이기 그러니까 클래스가 필요함
# 클래스는 붕어빵 틀에 비유됨

'''

# 위 내용을 클래스로

class Unit: 
    def __init__(self, name, hp, damage):
        self.name = name
        self.hp = hp
        self.damage = damage
        print("{0} 유닛이 생성 되었습니다.".format(self.name))
        print("체력 {0}, 공격력 {1}".format(self.hp, self.damage))
        
marine1 = Unit("마린",40,5)
marine2 = Unit("마린",40,5)
tank = Unit("탱크",40,5)
```



