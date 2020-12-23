2020년도 빅데이터 수업 (데이터 분석)
=============
## 10월 19일

#### 변수
변수명 대소문자 구분
변수명은 영문자와 숫자, 밑줄 로 구성
변수명 중간에 공백 허용하지 않음

__따라서, 구분하기 위해서는 밑줄을 사용하거나 중간에 대문자로 시작__

#### 예약어 
이미 용도가 정해져 있는 단어 

#### 식별자 
변수, 상수, 함수, 사용자 정의 타입 등에서 
다른 것과 구분하기 위해 사용되는 이름

- id(a) #id 는 변수가 가리키는 메모리의 주소 반환
- print(a) #변수가 가리키는 객체의 값 출력#변수에 값 저장
- 변수 = 값#여러개의 변수에 여러개의 값 저장
- 변수 1, 변수 2, 변수 3 ..... = 값 1, 값 2, 값 3 ..........
- 여러개의 변수에 한 개의 값 저장
- 변수 1 = 변수 2 = 변수 3 = 값 

#### 두 변수 값의 교환
a= 10
b = 20
위 두 변수의 값을 교환 하세요.
a,b = b,a #동적 할당을 하기 때문에
print(a, b)

#### 변수 삭제 
del 명령어 사용
del 변수 
del a #a 변수 삭제
print(a)

#### 문자열 사용 
문자열에 큰 따옴표 사용
name = "홍길동"
age = 23
print(name, age)

#### 작은 따옴표도 사용 가능
``` 
address = '서울시 강남구'
print(address)
```
__문자열에 + 연산자를 사용하면 문자열 결합 연산자로 취급__
  ```print(name + "은 " + address + "에 삽니다");```

숫자를 문자열과 연결하기 위해서는 숫자를 문자열 타입으로 형변환을 해야한다 
  ```
  str(str)
  name, no, year, grade, average = "홍길동", 2016001, 4, "A", 93.5
  print("성명 : " + name)
  print("학번 : " + str(no)
  print("학년 : " + str(year))
  print("학점 : " + grade)
  print("평균 : " + str(average))
```

#### 포맷 코드 사용
  ```print("이름 % 입니다 " %)```

#### 포맷 코드
```
  print("성명 : %s" % name) #문자열 포맷 코드  
  print("학번 : %s" %str(no))  
  print("학년 : %d"  %year)#정수형 포맷 코드  
  print("학점 : %c" %grade) #한문자 포맷 코드  
  print("평균 : %f" % average) # 실수형 포맷 코드 
```
## 10월 20일
#### if 문 
조건식이 참이면 주어진 문장 수행
조건식이 거짓이면 아무것도 수행하지 않음
- if ~ else 문
- 조건식이 참이면 if 문 수행
- 조건식이 거짓이면 else 문 수행
```
if 조건식 :
else : 
```
#### 로그인 프로그램
```
id = 'flower'
password = '1234'
```
###### 사용자로부터 키보드를 통해 값을 입력 받기
```
input_id = input("아이디 입력 : ") #입력되는 data는 문자열로 처리
input_pass = input("비밀번호 입력")
```
###### 두 값이 모두 일치하면 로그인 성공
```
if (id == input_id )and( password == input_pass) :
    print('로그인 성공')
else :
    print('로그인 실패')
password = 1234

if password == 12341 : 
    print('비밀번호 일치')
else : 
    pass #아무것도 수행하지 않을 경우 
```
###### 사용자로부터 두 수를 입력받아 더한 결과를 출력하는 코드 작성
```
su1 = int(input('첫번째 수 입력 : '))
su2 = int(input('두번째 수 입력 : '))

print(su1 + su2)
```
###### 또 다른 조건이 있을 때 elif 사용
```
if (조건식 1) :
   1이 참
elif (조건식 2) : 
   2이 참
else :
  아무것도 아닐경우
```
###### if~elif~else
```
num = int(input('정수 입력'))

if num < 0 :
    print('음수')
elif num > 0 :
    print('양수')
else :
    print('0')
``` 

###### 정수 3개를 입력 받아서 제일 큰 수 출력
```
f = int(input('첫번째 수 : '))
s = int(input('두번째 수 : '))
t = int(input('세번째 수 : '))
array = [f, s , t]
maxNum = max(array)
print(maxNum)
```
###### for 문 
```
정해진 횟수만큼 반복

for name in ["홍길동", "이몽룡", "성춘향", "변학도" ] :
    print(name)
for i in range(0, 10):
    print(i)
```
###### range() 함수 
특정 범위의 정수 생성
```
range(start, stop)
start 에서 stop-1까지의 정수

range(start, stop, step)
start 에서 stop-1까지의 정수를 step 씩 

for x in range(0, 10, 2) :
    print(x)
```

##### 숫자 11부터 21까지를 한줄에 출력하시오 .
###### 단, 한칸 띄어서 출력 할 것

```
for x in range(11 , 22) :
    print(x, end= " ")

```

###### 1부터 10까지 합을 출력
```
sumx = 0;
for num in range(1, 11) :
    sumx += num
print(sumx)
```

- 문자열 인덱스 (indexing)
- 인덱스로 문자의 위치를 나타내는 것
- 인덱스 (첨자) : 문자의 위치, 0부터 시작
- string[0] : 인덱스의 0번째 문자

###### 슬라이싱 (slicing)
문자열 중에서 일부분을 추출하는 것
인덱스 사용
```
print(crawling) 
print(crawling[0:4]) #0~3
print(crawling[5:16]) #5~15
print(crawling[17:]) #17~끝
print(crawling[19]) #19(20번째 글자) ~ 인덱스는 0부터 시작
print(crawling[-1:]) # 마지막에서 끝까지 (마지막 문자)
print(crawling[:-1]) # 처음부터 마지막 -1 까지
print(crawling[16:16+4]) # 16 ~ 19
parsing[5] = '가' #문자열 인덱싱에는 대입연산자를 사용할 수 없다 .
```

- 문자열 연산자 in / not in 연산자
- 특정 문자열이 포함되어 있는지 여부 확인
- 결과 T/F
- 대소문자는 구별해서 찾는다.
```
string = 'python programing'
print('python' in string)
print('Python' in string)


if 'python' in string :
    print('있음')
else : 
    print('없음')
```

#### 문자열 관련 메소드(함수)
- len() # 문자열 전체 길이 반환
- count() #문자열 내에 들어있는 특정 문자(열)의 개수 반환, 문자열 또는 변수.
- find()
- index()
- split : 구문자를 기준으로 문자열을 나누고 리스트 형태로 반환
- 구분자 : 기본 공백, 옵션으로 구분자를 지정할 수 있음. - / , . 
- replace() : 전체문자열에서 특정 문자열을 찾아 다른 문자열로 변경
- join() : 각 문자사이에 특정 문자(열) 삽입
- upper() : 전부 대문자로
- lower() : 전부 소문자로
- capitalize() : 문자의 첫 번째 문자를 대문자로 
- title() : 각 단어의 첫 글자를 대문자로 변경

- split : 구문자를 기준으로 문자열을 나누고 리스트 형태로 반환
- 구분자 : 기본 공백, 옵션으로 구분자를 지정할 수 있음. - / , . 
```
string = 'python programming'
split_str = string.split()
print(split_str) # 결과는 리스트 형태로 반환
names  ='홍길동,이몽룡,성춘향,변학도'
names_split = names.split(",")
print(names_split)

colors = 'red:blue:yellow:green'
colors_split = colors.split(":")
print(colors_split)
```
replace() : 전체문자열에서 특정 문자열을 찾아 다른 문자열로 변경

문자열.replace(찾는문자열,변경할 문자열)
```
course = 'Java programing'

//Java 를 Python 으로 변경
course_replace = course.replace("Java", "Python")
print(course_replace)
//기존 course 변수의 값은 변경되는가 ? (f)
print(course)
```
join() : 각 문자사이에 특정 문자(열) 삽입
```
a = 'aa'
a.join('bbb')# a 변수의 값을 bbb 사이에 삽입
# 문자열 사이에 구분자 삽입 사용
# 리스트에 있는 모든 문자를 하나로 구성할때 사용(리스트 함수)
a = '-'
print(a.join('abcd'))
```
리스트에 join 함수 사용
```
sep = '-'
names = ['홍길동', '이몽룡', '성춘향', '변학도']
print(sep.join(names))
```

- 대소문자 전환 함수
- upper() : 전부 대문자로
- lower() : 전부 소문자로
- captialize() : 문자의 첫 번째 문자를 대문자로 
- title() : 각 단어의 첫 글자를 대문자로 변경
```
string = 'this is MY DOG'
string.upper()
string.lower()
string.capitalize()
string.title()
```

- isalpha() : 문자여부 결과 반환 (t/f)
- isdigit() : 숫자여부 결과 반환
- isspace() : 공백여부 결과 반환 (t/f)
- isalnum() : 문자 또는 숫자여부 결과 반환


###### 사용자로부터 문장을 입력 받는다
```
string = input("문장을 입력하세요.")
al = 0
di = 0
sp = 0
aln = 0

for i in string :
    if i.isalpha() :
        al+= 1
    elif i.isdigit() :
        di+= 1
    elif i.isspace() :
        sp += 1
    else :
        aln += 1
print("알파벳 : " + str(al))
print("숫자 : " + str(di))
print("스페이스 : " + str(sp))
print("기타 : " + str(aln))
```
#### 리스트 

동일한 이름을 갖는 원소들의 연속 저장 영역

여러 개의 데이터가 저장되어 있는 장소
- 각 원소는 인덱스(index) 로 구분 
- 원소(값) 변경 가능
- 대괄호 사용

##### 리스트의 특징
- 리스트의 크기는 가변적
- 다양한 종류의 데이터를 하나의 리스트 안에 저장 가능 
- 리스트의 각 원소 출력 : range() 함수 사용


###### 리스트 생성
```
numbers = [100, 200, 300, [10,20,30]]
numbers[3][1]

for n in range(0, len(numbers)) :
    print(numbers[n])
```
###### 리스트의 값을 각 변수에 저장하는 코드 
```
nums = [1,2,3]
a,b,c = nums #리스트 모든 원소를 각 변수에 대입
print(a)
```
###### 인덱싱
- a[0] : 첫번째 요소
- a[-1] : 마지막 요소
- a[-2] : 뒤에서 두번째 요소
```
b = [1,2,3,[10,20]]
b[-1][0] # 반환되는 값

a = [1,2,3,4,5]
c = [1,2,3,[10,20],4,5]

all_list = [a,b,c]
print(all_list)
```
###### 슬라이싱 (slicing)
리스트 안에서 범위를 지정하여서 원하는 요소들을 선택하는 연산
- 리스트[start,end] : start 에서 end -1 요소까지 선택

## 10월 21일

#### 튜플
리스트와 유사한 집합적 자료형이지만 리스트와 달리 원소 변경 불가
- 추가 / 수정 / 삭제 불가능 , 소괄호를 사용해서 만든다

###### 튜플 생성 () 이용
```
t1 = (1,2,3)
t2 = 4,5,6 #소괄호 없어도 튜플로 생성이 된다 
t3 = t1,(7,8,9) #튜플 내에 또 다른 튜플 생성
t4 = [1,2], [4,5] #리스트로 튜플 생성
t5 = tuple([5,6,7,8]) #tuple 함수 사용 - 기존 구조(리스트)를 튜플로 변환
t6 = ([5,6,7,8]) #리스트 하나를 원소로 갖는 튜플

print(t4)
t4[0]
print(t5)
```
###### 튜플을 리스트로 변환 
```
#(1,2,3) -> [1,2,3]
to_list1 = list(t1)
to_list1
```
###### 튜플 내 튜플 원소는 변환 후에도 그대로 튜플로 유지
```
to_list2 = list(t3)
to_list2
```

###### 튜플은 변경할 수 없다
```
t=(1,2,3)
t[0] = 5 #에러발생 : 변경 불가 
```

###### 소괄호 없이 튜플을 생성할 때 원소가 1개인 튜플을 생성하는 방법
```
t8 = 2,
t8
```

#### 딕셔너리
키(key)와 값(value)의 한 쌍을 요소로 갖는 자료형
- 딕셔너리 = [키1:값1, 키2:값2]

##### 딕셔너리의 특징
순서가 없다. 따라서, 인덱스로 접근할 수 없다
- 중괄호 {} 사용
- key를 통해서만 접근

###### 딕셔너리의 주요 함수
- 딕셔너리.keys() : key만 추출해서 리스트로 반환
- 딕셔너리.values() : values만 추출해서 리스트로 반환
- 딕셔너리.items() : (key,value)형태로 모든 item을 리스트로 반환

###### 딕셔너리에 값(item) 추가 
딕셔너리 변수 [새로추가될 key] = 키에 대응하는 값

###### 딕셔너리 item 의 value에 접근
딕셔너리명[키값]

###### 딕셔너리 예제
```
naver = {
    "name" : "naver",
    "url" : "www.naver.com",
    "userId" : "nv",
    "password" : "1234"   
}
print(naver)
print(type(naver))
print(naver.keys()[0])
```

반환 객체가 list를 포함하는 dict_keys 형태로 반환

사용하려면 list로 변환시켜서 사용해야 함

###### 딕셔너리 파생 객체들은 list로 변환 후 사용
```
list(naver.keys())
```

- 반복문을 이용해서 naver 딕셔너리의 각 요소 출력
- 반복문에서 딕셔너리 파생 객체를 사용할 때는 리스트 변환이 필요 없음
```
for key in naver.keys():
    print(key)
```
###### 문제 : naver 딕셔너리의 values 를 모두 출력하시오
__단 , 반복문과 딕셔너리 관련 함수를 사용 할 것__
```
for value in naver.values() :
    print(value)
```
###### key로 value 찾기 
```
print(naver["userId"])
print(naver.get("password")) # get 함수를 이용해서 value 찾기

# print(naver["link"]) #키가 없으므로 에러 발생
print(naver.get('link')) #키가 없으면 None
print(naver.get('link', '없음')) #없음 출력

#키에 대응하는 값의 존재여부만 확인 : in / not in
print('link' in naver)
print('link' not in naver)
```
