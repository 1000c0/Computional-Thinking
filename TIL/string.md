# string

## cf) byte와 bit
1byte = 8bit = 2^8 = 256 : 0 ~ 256까지 저장 가능

1bit는 0 또는 1

U 는 1000011 로 변환 되어 저장 (UTF-8기준)

정수형 
- int
    
     크기 : 4바이트, 표현범위(32bit) : -2^31 ~ 2^31 -1
- long

     크기 : 무제한, 표현범위(32bit) : 무제한

실수형
- float
     크기 : 8바이트, 표현범위(32bit) : 약 -10^-308 ~ 10^308

4byte = 32bit = 2^32 = 4,294M = -2,147M ~ 2,147M 까지 표현

#
## 문자열의 특징
- list와 같은 시퀀스형 자료의 특징을 가진다.
     - 각 문자열의 오프셋은 왼쪽에선 0 오른쪽에선 -1로 시작
     - 문자열의 주소값을 기반으로 문자열의 부분 값을 반환
     - 덧셈과 뺄셈 연산 가능
     - in 명령으로 포함여부 체크 가능
    ```python
    x = "apple"
    y = "Dell"
    if 'a' in x:
        print(x)
    else:
        print(y)
    #>>> apple
    ```   
#
## 문자열 함수
- len(a) : 문자열의 문자 개수 반환
- a.upper() : 대문자로
- a.lower() : 소문자로
- a.capitalize() : 첫 문자를 대문자로
- a.title : 띄어쓰기 후 첫 글자만 대문자로
- a.count('abc') : 'abc' 들어간 횟수 반환
- a.find('abc') : 왼쪽부터 'abc' 가 들어간 위치(오프셋) 찾아서 반환
- a.rfind('abc') : 오른쪽부터 'abc' 가 들어간 위치(오프셋) 찾아서 반환
- a.startswith('abc') : 문자열 a가 'abc'로 시작하는지 확인 True, False 반환
- a.endswitch('abc') : 문자열 a가 'abc'로 끝나는지 확인 True, False 반환
- a.strip() : 좌우 공백 제거
- a.rstrip() : 오른쪽 공백 제거
- a.lstrip() : 왼쪽 공백 제거
- a.split() : 공백을 기준으로 나눠 리스트로 변환
- a.split('abc') : abc를 기준으로 나눠 리스트로 변환
- a.isdigit() : 문자열이 숫자인지 여부 반환
- a.islower() : 문자열이 소문자인지 여부 반환
- a.isupper() : 문자열이 대문자인지 여부 반환
- ''.join(리스트) : 리스트를 문자열로 합쳐서 반환
- '구분자'.join(리스트) : 리스트 값 사이에 구분자를 넣어서 리스트로 합쳐서 반환
#


## 문자열 표현
- '' 작은 따옴표       
    문자열 안에서 작은 따옴표를 사용하고 싶을 때는 역스래시\사용
    
    ex)  'It\' ok.' -> 'It's ok.'
- "" 큰 따옴표  

두줄 이상 저장
- """ 큰 따옴표 3번
- \n 
    ```python
    a = " 코딩하기 아주 즐겁다. \n 행복하다."
    print(a)
    # >>> 코딩하기 아주 즐겁다.
    #     행복하다. 
    ```

특수 문자
- \ [Enter] : 다음 줄과 연속임을 표현
- \n : 줄 바꾸기
- \\\\ : \ 문자 자체 # 역슬래시 두개 써야하지만 md에서 표현하기 위해 4개를 씀
- \t : TAB 키
- \` : ` 문자
- \e : ESC 키
- \" : " 문자
- \b : 백 스페이스
  
### raw_string
- 특수문자 특수 기호인 \ escape 글자를 무시하고 그대로 출력함
  ```python
  a = " 코딩하기 아주 즐겁다. \n 행복하다."
  print(a)
  #>>> 코딩하기 아주 즐겁다. \n 행복하다.
  ```
#
