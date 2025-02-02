# Computer Architecture

## 컴퓨터 구조와 개요
### 컴퓨터 구조란 무엇인가?
- 컴퓨터 시스템의 하드웨어 구성 요소와 그들 간의 상호작용을 다루는 분야. 
### 컴퓨터 시스템의 발전과 역사
#### 1세대 컴퓨터 (1940년대 중반~1950년대 중반)
- 특징: 회로소자로 진공관을 사용.
- 기술: 전자 회로를 통해 연산 수행. 
- 예시: 
   - ENIAC (1946): 최초의 범용 전자 디지털 컴퓨터.
   - UNIVAC(1951): 상업적으로 판매된 최초의 컴퓨터. 
- 한계: 
   - 크고 비쌌으며, 엄청난 전력을 소비. 
   - 발열이 심하고 신뢰성이 낮음.
#### 2세대 컴퓨터(1950년대 중반~1960년대 중반)
- 특징: 트랜지스터가 회로소자를 대체하기 시작. 
- 예시: IBM 7090, PDP-1
- 장점: 더 작고 빠르며, 발열 문제 감소. 
#### 3세대 컴퓨터(1960년대 중반~1970년대 중반)
- 특징: IC가 등장해 중앙처리장치가 작아지고 기억용량은 커짐. 
- 운영체제의 등장으로 멀티태스킹 가능. 
- 예시: IBM System/360 시리즈, DEC PDP-8
- 장점: 컴퓨터가 더 작아지고 저렴해짐.
#### 4세대 컴퓨터(1970년대 중반~1980년대)
- 특징: 컴퓨터의 소자들이 대규모 집적회로(LSI)로 바뀜. 
- PC 등장.
- 네트워크 기술의 발달로 인터넷 등장. 
#### 5세대 컴퓨터(1990년대 이후)
- 특징: 초고밀도 집적회로(VLSI)를 사용하여 초소형화, 초고속화가 이루어짐.
- 인공지능과 병렬 처리 기술이 적용.
- 자연어, 인공지능어 사용. 
### 컴퓨터의 구성 요소
1. 중앙처리장치(CPU)
   - 컴퓨터 시스템의 두뇌 역할을 하며, 명령어를 해석하고 실행.
2. 기억장치 (Storage)
    - 프로그램 실행에 필요한 명령어와 데이터를 저장. 
3. 입출력 장치 (I/O Devices)
   - 외부 데이터를 컴퓨터로 입력하거나, 처리 결과를 외부로 출력하며 사용자와 컴퓨터 간의 상호작용을 가능하게 함. 
- 이들 간의 상호작용:
  - CPU는 명령어를 실행하면서 기억장치에서 데이터를 가져오거나 저장. 
  - 입력 장치로부터 데이터를 받아 기억장치에 저장하고, CPU가 이를 처리.
  - 처리된 데이터를 출력 장치를 통해 사용자에게 전달.
  - 모든 구성 요소는 시스템 버스를 통해 연결되어 데이터와 명령을 주고 받음.
### 폰노이만 아키텍처  (Von Neumann Architecture)
- 정의: 프로그램과 데이터를 동일한 메모리에 저장하며, 순차적으로 명령을 실행. 
- 특징:
  1. 프로그램과 데이터를 동일한 메모리에 저장.
  2. 메모리에서 명령어와 데이터를 구분하여 처리.
  3. 명령어를 순차적으로 가져와 실행. 
  4. 데이터와 명령어가 동일한 버스를 통해 전송. 
- 장점:
  - 프로그램과 데이터가 같은 메모리를 사용하므로 하드웨어가 단순. 
  - 하나의 시스템에서 다양한 프로그램 실행 가능. 
- 단점:
  - 폰 노이만 병목현상 (Von Neumann Bottleneck): CPU와 메모리 간 데이터 전송 속도의 차이로 인해 발생하는 처리 속도 제한 
  - 병렬처리에 비효율적
  - 프로그램 명령어와 데이터가 동일한 메모리에 있어 충돌 가능. 





### 하버드 아키텍처 (Harvard Architecture)
- 정의: 프로그램 명령어와 데이터를 별도의 메모리에 저장하고, 각각 독립된 버스를 사용하여 처리하는 컴퓨터 설계 방식. 
- 특징:
  1. 명령어와 데이터를 별도의 메모리에 저장.
  2. 두 메모리에 접근하는 경로(버스)가 독립적.
  3. CPU가 명령어와 데이터를 동시에 가져올 수 있어 성능 향상.
  4. 폰 노이만 아키텍처에서 발생하는 메모리 병목현상을 줄임.
- 장점:
  - 명령어와 데이터에 동시 접근 가능하여 처리 속도 향상.
  - 명령어와 데이터가 동일한 버스를 공유하지 않아 충돌 문제가 발생하지 않음.
- 단점:
  - 메모리와 버스를 별도로 설계해야 하므로 하드웨어가 복잡. 
  - 추가적인 메모리와 버스 설계로 인해 비용이 높아짐.
  -  


### 컴퓨터 설계의 기본 원리

## 명령어 집합 구조  (ISA, Instruction Set Architecture)
### CISC (Complex Instruction Set Computer)
- 특징:
   - 복잡한 명령어
   - 명령어의 크기가 고정되지 않고, 명령어마다 길이가 달라질 수 있음.
   - 하나의 명령어로 메모리 접근과 연산을 동시에 수행할 수 있음. 
- 장점:
  - 복잡한 명령어로 인해 동일 작업을 수행하기 위해 필요한 명령어 수가 적음.
- 단점:
  - 복잡한 명령어를 처리하기 위한 하드웨어 설계가 어려움. 
  - 복잡한 명령어를 디코딩하는 데 시간이 많이 소요됨. 
- 예시: x86 아키텍처(Intel, AMD 프로세서 등).
### RISC (Reduced Instruction Set Computer)
- 특징: 
  - 단순한 명령어: 명령어 수를 줄이고, 명령어 구조를 단순화함.
  - 명령어 크기가 일정하여 디코딩이 간단.
  - 파이프라이닝에 최적화.
  - 메모리 접근은 별도의 명령어로 수행되며, 연산은 주로 레지스터 간에 이루어짐. 
- 장점: 
  - 빠른 실행 속도.
  - 간단한 명령어 구조는 파이프라이닝 성능을 극대화함. 
  - 하드웨어가 단순하여 전력 소비도 낮음. 
- 단점:
  - 코드 크기 증가: 필요한 명령어 수가 많다.
- 예시: ARM 
   
## 데이터 표현 및 연산
### 수의 체계
- 주로 기수법에 따라 구분됨.
1. 10진법 (Decimal System, Base-10)
   - 특징
     - 0부터 9까지 10개의 숫자를 사용.
     - 각 자리의 값은 10의 거듭제곱으로 표현됨. 

2. 2진법 (Binary System, Base-2)
   - 특징
     - 컴퓨터에서 가장 기본적인 수의 체계.
     - 0과 1의 두 숫자만 사용.
     - 각 자리의 값은 2의 거듭제곱으로 표현.
  
3. 8진법 (Octal System, Base-8)
   - 특징
     - 0부터 7까지 8개의 숫자를 사용.
     - 이진법을 간단히 표현하기 위해 사용됨(3비트 그룹으로 변환 가능). 
  
4. 16진법 (Hexadecimal System, Base-16)
   - 특징
     - 0부터 9까지의 숫자와 A(10), B(11), C(12), D(13), E(14), F(15)의 16개의 숫자를 사용.
     - 이진법을 간결하게 표현하기 위해 사용됨(4비트 그룹으로 변환 가능).
---진법간 수 변환 이미지 넣기 

### 정수와 실수 표현
#### 1. 정수 표현 (Integer Representation)
- 정의: 정수는 소수점이 없는 숫자를 의미하며, 양의 정수, 음의 정수, 그리고 0을 포함.
#### 1.1 고정 소수점 (Fixed-Point)
- 정의: 소수점을 고정된 위치에 배치하여 실수를 표현하는 방식. 
- 특징:
  - 실수를 표현하는 방식이지만, 컴퓨터 내부에서 정수처럼 저장되고 연산됨. 
  - 정밀도는 고정된 소수점 부분의 비트 수에 따라 결정.
  - 표현 가능한 값의 범위는 부호 비트 여부와 전체 비트 수에 따라 달라짐. 
- 장점: 부동소수점보다 연산 속도가 빠름.
- 단점: 반올림 또는 자르기 오차 발생 가능.
#### 2. 실수 표현(Floating-Point Representation)
- 정의: 소수점이 있는 숫자를 의미하며, 유리수와 무리수를 포함.
#### 2.1 부동소수점
- 정의: 소수점의 위치를 고정하징 않고, 가변적인 방식으로 숫자를 표현.
- 특징: 
  - 숫자의 크기와 범위를 지수와 유효숫자의 조합으로 나타낸다.
  - 표현 범위가 넓다.
  - 일부 실수는 정확하게 표현될 수 없으며, 근사값으로 저장. 
- 장점: 넓은 표현 범위를 가지고 유효숫자가 많아 정밀한 계산이 가능.
- 단점: 정수 연산보다 느리고 정수 표현에 비해 많은 메모리를 사용. 
#### 2.2 IEEE 754 표준
- 정의: 부동소수점의 표현, 연산, 반올림 규칙 등을 정의한 규칙. 
1. 표현
   - 부호비트 (Sign)
      - 0: 양수, 1: 음수.
   - 지수 (Exponent)
      - 지수는 Bias 값에 따라 저장.
   - 유효숫자 (Mantissa)
      - 숫자의 소수점 이하 부분을 저장.
2. 정밀도
   - 단정밀도 (Single Precision) : 총 32비트
     - 부호: 1비트/ 지수: 8비트/ 가수: 23비트.
     - 약 7자리의 유효숫자 표현 가능.
   - 배정밀도 (Double Precision) : 총 64비트
     - 부호: 1비트/ 지수: 11비트/ 가수: 52비트.
     - 약 15~16자리의 유효숫자 표현 가능. 
3. 반올림 방식 
   - 가장 가까운 값으로 반올림.
      - 가장 가까운 값으로 반올림.
      - 중간값에서는 짝수로 반올림. 
   - 0으로 수렴
      - 소수점 이하를 버려서 0에 가까운 정수 값으로 반올림.
      - 음수는 값이 증가하고, 양수는 값이 감소.
   - Round Toward Positive Infinity (+∞ 방향)
      - 항상 큰 값 쪽으로 반올림.
      - 양수는 항상 위로 올리고, 음수는 값이 감소하지 않는다.
   - Round Toward Negative Infinity (−∞ 방향)
      - 항상 작은 값 쪽으로 반올림.
      - 양수는 감소하지 않고, 음수는 항상 아래로 올린다. 
### 데이터 연산
#### 산술 연산 (Arithmetic Operations)
- 정의: 숫자 데이터에 대한 기본적인 수학적 연산을 수행. 
#### 논리 연산 (Logical Operations)
- 정의: Boolean 값을 다루는 연산. 
- 참(True)과 거짓(False)을 반환
- AND(&& 또는 &): 두 조건이 모두 참일 때만 참이 되는 연산. 
- OR(|| 또는 |): 두 조건 중 하나라도 참이면 참이 되는 연산.
- NOT(~ 또는 !): 조건을 반전시키는 연산. 
#### 시프트 연산 (Shift Operations)
- 정의: 비트를 왼쪽 또는 오른쪽으로 이동시키는 연산. 
- 배수 또는 몫을 계산하는데 사용. 
- 왼쪽 시프트, 오른쪽 시프트, 산술 오른쪽 시프트, 논리 오른쪽 시프트를 수행. 
###  Signed vs Unsigned 데이터
#### 1. Signed 데이터
- 정의: 양수와 음수를 모두 표현할 수 있는 정수 타입. 
- 특징:
  - 2의 보수법을 사용하여 음수를 표현.
  - 값의 범위는 사용되는 비트 수에 따라 다르다.
  - 부호 비트:
     - 0이면 양수, 1이면 음수.
#### 2. Unsigned 데이터 
- 정의: 음수는 표현하지 않고, 양수만을 표현할 수 있음. 
- 특징:
  - 값의 범위는 전체 비트가 숫자 표현에 사용되므로 signed 데이터보다 더 넓다.
  - 최소값은 0이고, 양수만 다룬다.

## 중앙처리장치 (CPU)
- 역할:
   - 컴퓨터 시스템의 두뇌 역할을 하며, 명령어를 해석하고 실행
   - 산술 연산, 논리 연산, 데이터 이동, 제어 신호 생성 등을 담당 
### CPU의 구조와 구성 요소
![Image](images/CPU.png)
> 위 그림은 제어장치, 연산장치, ALU, 레지스터, 내부 버스로 구성되어 있는 CPU를 보여줌 


#### 1. 연산 장치 (ALU: Arithmetic Logic Unit):
- 정의: 산술 연산과 논리 연산 등을 수행
- 역할: 입력된 데이터에 대해 연산을 수행하고, 그 결과를 레지스터로 전달하거나 메모리에 저장
- 구성: 가산기, 보수기, 누산기 , 데이터 레지스터 등

![Image](images/ALU.png)
> 위 그림은 ALU가 정수 피연산자와 연산 명령(Opcode)을 입력으로 받아 산술 및 논리 연산을 수행하고, 연산 결과와 상태 플래그를 출력하는 동작 과정을 나타냄


#### 2. 제어 장치 (CU: Control Unit):
- 정의: 프로그램 명령을 해석하고 실행 순서를 제어
- 역할: 기억 장치로부터 명령을 순차적으로 꺼내 해독하고, 해석에 따라 명령어 실행에 필요한 제어 신호를 기억 장치, 연산 장치, 입출력 장치 등으로 보내는 장치 
- 구성: 프로그램 카운터(PC), 명령 해독기, 부호기, 명령 레지스터 등

![image](images/CU.png)
> 위 그림은 CU가 플래그 레지스터와 명령 레지스터에서 입력 신호를 받아, clock에 따라 명령을 해석한 뒤, 레지스터, ALU, 메모리 및 입출력 장치로 제어 신호를 전송하여 전체 시스템을 제어하는 과정을 보임 
#### 3. 레지스터 (Register):
- 정의: CPU 내에 있는 소규모 고속 기억장치
- 역할: 명령어 주소, 코드, 연산에 필요한 데이터, 연산 결과 등을 임시로 저장
- 종류:
  - 범용 레지스터: 데이터 저장
  - 특수 레지스터: 프로그램 카운터(PC), 명령어 레지스터(IR), 스택 포인터(SP) 등
#### . 내부 버스 (CPU Internal Bus):
- 정의: ALU, 레지스터 간 데이터 이동을 위한 데이터 선들과 주소 선들, 그리고 제어 유닛으로부터 발생되는 제어 신호들을 전송하는 선들로 구성
- 특징: 외부 시스템 버스와 직접적으로 연결되지는 않음
  
### 명령어 사이클 (Instruction Cycle)
- 정의: CPU가 하나의 명령어를 처리하는 과정을 의미 
#### 명령어 사이클 단계

![image](images/instructioncycle.png)
> 위 그림은 명령어 사이클의 Fetch, Decode, Execute, Memory Access 작업 과정을 반복하는 것을 보여줌
1. Fetch
   - 목적: 메모리에서 실행할 명령어를 가져옴
   - 동작:
     - PC에 저장된 즈소를 통해 메모리에서 명령어를 읽어옴
     - 읽은 명령어는 IR(명령 레지스터)에 저장
     - PC는 그 다음 명령어의 주소를 가리키도록 증가
2. Decode
   - 목적: 가져온 명령어를 해석하여 어떤 작업을 해야 할지 결정
   - 동작:
     - CU가 명령어를 분석
     - 명령어가 산술 연산, 논리 연산, 데이터 이동 등 무엇을 해야 하는지 해석됨
     - 필요한 연산에 따라 ALU, 레지스터, 메모리 등을 결정
3. Execute
   - 목적: 명령어에 정의된 작업을 실행
   - 동작:
     - ALU가 산술 연산을 수행하거나, 논리 연산을 처리
     - 연산 결과는 레지스터나 메모리에 저장
4. Memory Access
   - 목적: 메모리에서 데이터를 읽거나 데이터를 메모리에 저장
   - 동작:
     - 읽기 또는 쓰기 작업이 필요한 경우, 메모리에 접근

### 메모리 접근 방식 (Memory Access Methods)
#### 1. 캐시 메모리 접근 방식
- 정의: CPU는 먼저 캐시 메모리에서 데이터를 찾고, 없으면 주 메모리에 접근
- 장점: 데이터 접근 속도 향상 
- 단점: 캐시 미스가 발생하면 성능 저하
  
#### 2. DMA (Direct Memory Access)
- 정의: CPU 개입 없이 메모리와 주변 장치 간 데이터 전송이 이루어지는 방법
- 특징:
  - CPU 개입 없이 주변 장치와 주기억장치와의 데이터 직접 전송
  - CPU는 DMA와 상태정보 및 제어정보만을 주고 받음 
- 장점: CPU의 부담을 줄이고 병렬 처리 가능 
- 단점: DMA 컨트롤러와의 추가적인 하드웨어 요구


## 메모리 구조
### 메모리 계층 구조 (Memory Hierarchy)
- 정의: 메모리 장치들이 성능과 비용을 기준으로 계층적으로 구성된 구조

![Image](images/MEM.png)
> 위 그림은 메모리 계층 구조를 나타내며, 상위로 갈수록 속도가 빠르고 용량이 적으며, 하위로 갈수록 속도는 느리지만 용량이 커지만 저장 장치의 계층적 구조를 보여줌 
#### 구성 요소 
#### 1. 레지스터 (Registers)
- 위치: CPU 내에 위치
- 속도: 가장 빠름
- 용량: 매우 작음
- 특징: 직접 데이터를 처리하는 가장 작은 저장 공간
- 용도: 임시 데이터, 연산 중간 겨과, PC 등의 저장

#### 2. 캐시 메모리 (Cache Memory)
- 위치: CPU와 주 메모리(RAM) 사이에 위치
- 속도: 매우 빠르지만 레지스터보다는 느림
- 용량: 작은 크기 (보통 킬로바이트에서 몇 메가바이트)
- 특징: 
  - 자주 사용하는 데이터나 명령어를 저장하여 CPU가 빠르게 접근할 수 있게 하는 고속 메모리
- 용도: 자주 사용되는 데이터나 명령어를 빠르게 공급하여 성능 향상
 
#### 3. 주 메모리 (Primary Memory / RAM)
- 위치: CPU와 보조 저장 장치(HDD,SSD) 사이에 위치
- 속도: 캐시보다는 느리지만 상대적으로 빠름
- 용량: 수 기가바이트
- 특징: 프로그램 실행 중 필요한 데이터와 명령어를 저장하는 휘발성 메모리
- 용도: 운영 체제, 실행 중인 프로그램, 시스템의 데이터 저장

#### 4. 보조 저장 장치 (Secondary Storage)
- 위치: CPU와 주 메모리보다 아래 단계에 위치
- 속도: 매우 느림
- 특징: 비휘발성 메모리로 데이터를 영구적으로 저장
- 용도: 장기적인 데이터 저장, 운영 체제

#### 5. 원격 보조 저장 장치 (Remote Secondary Storage)
- 위치: 보조 저장 장치보다 더 아래에 위치
- 속도: 가장 느림
- 용량: 대규모 저장 용량을 제공
- 특징: 장기적인 백업 및 아카이빙을 위한 저장 장치 
- 용도: 백업, 대규모 데이터 저장

### 캐시 메모리 
- 정의: CPU와 주 메모리 사이에 위치하는 고속의 작은 용량의 메모리
- 역할 
  - 속도 차이 해결: CPU와 주 메모리 간의 속도 차이를 줄여줌ㅈ
  - 자주 사용되는 데이터 저장: CPU가 자주 사용하는 데이터를 저장하며, 해당 데이터를 반복적으로 빠르게 접근할 수 있게 함
#### 캐시 적중률 (Cache Hit Rate)

![image](images/CacheHit.png)
- 정의: 캐시 메모리에서 데이터가 성공적으로 조회된 비율을 나타내는 성능 지표
#### 캐시 적중 (Cache Hit)
- 정의: CPU가 요청한 데이터가 캐시 메모리에 이미 존재하는 경우
- 캐시에서 데이터를 빠르게 읽을 수 있어 빠른 처리가 가능

#### 캐시 미스율 (Cache Miss Rate)

![image](images/CacheMiss.png)
- 정의: 캐시에서 데이터를 찾지 못하고 메인 메모리로 접근해야 하는 비율을 나타냄 
#### 캐시 미스 (Cache Miss)
- 정의: 캐시에서 CPU가 요청한 데이터가 존재하지 않을 때 발생하는 상황
- CPU는 주 메모리에서 데이터를 가져와야 하므로 시간이 더 소요됨

### 가상 메모리 (Virtual Memory)
- 정의: 컴퓨터 시스템에서 물리적 메모리보다 더 많은 메모리 공간을 사용할 수 있도록 하는 기술
#### 1. 가상 주소 공간 (Virtual Address Space)
- 정의: 각 프로세스가 독립적으로 사용할 수 있는 논리적인 메모리 주소 범위
- 특징:
  - 프로세스 간의 메모리 충돌이나 침범 방지
  - 프로세스는 가상 주소 공간만을 참조하며, 실제 물리 메모리의 위치를 알 필요가 없음
- 구성:
  1. 사용자 공간(User Space):
    - 실행하는 애플리케이션과 관련된 코드와 데이터를 저장하는 공간
    - 일반적으로 가상 주소 공간의 하위 영역 차지 
  2. 커널 공간(Kernel Space):
    - 운영체제의 커널 코드와 데이터를 저장하는 공간
    - 사용자 프로세스가 직접 접근할 수 없음
- 장점: 
  - 효율적인 메모리 사용
  - 연속적인 메모리 할당을 보장하지 않아도 됨
- 단점:
  - 물리 주소 변환 과정이 추가적인 오버헤드 발생시킴
  - 페이지 테이블 유지로 인해 메모리 공간이 많이 필요함 
#### 2. 페이지와 페이지 테이블
#### 페이지 (Page)
- 정의: 가상 메모리 시스템의 메모리 관리 단위
- 가상 주소는 페이지라는 작은 단위로 나뉘어 있으며, 각 페이지는 물리 메모리의 프레임에 매핑 
#### 페이지 테이블 (Page Table)
- 정의: 가상 주소와 물리 주소를 매핑하는 데 사용되는 자료구조
- 구성 요소:
  - 페이지 번호(Page Number): 가상 주소의 페이지를 나타냄
  - 프레임 번호(Frame Number): 물리 메모리 내 페이지가 위치한 프레임을 나타냄
#### SWAP

![image](images/swap.png)
> 위 그림은 주 메모리에 공간이 부족할 경우, 현재 실행 중이지 않은 프로세스 p1을 예비 저장 장치로 Swap out하고, 예비 저장 장치에 저장된 다른 프로세스 p2가 필요하면, Swap in하는 과정을 보여줌
- 정의: 물리 메모리가 부족할 때 일부 데이터를 디스크로 옮겨서 가상 메모리 공간을 확보하는 과정
- 스왑 공간: 디스크의 일부를 가상 메모리 시스템에서 임시 저장소로 사용하는 영역
- 스왑 아웃(Swap Out): 물리 메모리에서 사용되지 않는 데이터를 스왑 공간으로 이동시키는 작업
- 스왑 인(Swap In): 스왑 공간에 저장된 데이터를 다시 물리 메모리로 가져오는 작업
- 동작 과정:
  1. 물리 메모리가 부족하면 메모리 확보하기 위해 페이지 교체를 실행
  2. 선택된 페이지는 스왑 공간으로 이동하고, 물리 메모리에서 해당 공간을 해제
  3. 스왑 공간에 저장된 페이지가 필요해지면 디스크에서 메모리로 로드 

</div>
</details>
<details>
<summary>c언어 Swap 구현</summary>
<div markdown="1">

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#define MEMORY_SIZE 4
#define SWAP_SIZE 8

typedef struct {
    int process_id;
    char data[20];
} MemoryBlock;

MemoryBlock memory[MEMORY_SIZE];
MemoryBlock swap[SWAP_SIZE];
int memory_index = 0;
int swap_index = 0;

void initialize_memory() {
    for (int i = 0; i < MEMORY_SIZE; i++) {
        memory[i].process_id = -1; // Empty
    }
    for (int i = 0; i < SWAP_SIZE; i++) {
        swap[i].process_id = -1; // Empty
    }
}

void load_to_memory(int process_id, const char *data) {
    if (memory_index < MEMORY_SIZE) {
        memory[memory_index].process_id = process_id;
        strcpy(memory[memory_index].data, data);
        printf("Loaded process %d to memory.\n", process_id);
        memory_index++;
    } else {
        // Swap out the oldest process
        printf("Memory full. Swapping out process %d.\n", memory[0].process_id);
        swap[swap_index] = memory[0];
        swap_index++;
        
        // Shift memory
        for (int i = 1; i < MEMORY_SIZE; i++) {
            memory[i - 1] = memory[i];
        }
        
        // Add new process
        memory[MEMORY_SIZE - 1].process_id = process_id;
        strcpy(memory[MEMORY_SIZE - 1].data, data);
        printf("Loaded process %d to memory.\n", process_id);
    }
}

void print_status() {
    printf("\nMemory:\n");
    for (int i = 0; i < MEMORY_SIZE; i++) {
        if (memory[i].process_id != -1) {
            printf("Process %d: %s\n", memory[i].process_id, memory[i].data);
        }
    }

    printf("\nSwap Space:\n");
    for (int i = 0; i < swap_index; i++) {
        if (swap[i].process_id != -1) {
            printf("Process %d: %s\n", swap[i].process_id, swap[i].data);
        }
    }
}

int main() {
    initialize_memory();

    load_to_memory(1, "Data1");
    load_to_memory(2, "Data2");
    load_to_memory(3, "Data3");
    load_to_memory(4, "Data4");
    load_to_memory(5, "Data5"); // Trigger swap

    print_status();
    return 0;
}
```
</div>
</details>
</div>

</details>
<details>
<summary>java Swap 구현</summary>
<div markdown="1">

```java
import java.util.LinkedList;
import java.util.Queue;

class Process {
    int processId;
    String data;

    public Process(int processId, String data) {
        this.processId = processId;
        this.data = data;
    }

    @Override
    public String toString() {
        return "Process " + processId + ": " + data;
    }
}

public class SwapExample {
    private static final int MEMORY_SIZE = 4;
    private static final int SWAP_SIZE = 8;

    private final Queue<Process> memory = new LinkedList<>();
    private final Queue<Process> swap = new LinkedList<>();

    public void loadToMemory(int processId, String data) {
        if (memory.size() < MEMORY_SIZE) {
            memory.add(new Process(processId, data));
            System.out.println("Loaded process " + processId + " to memory.");
        } else {
            // Swap out the oldest process
            Process swappedOut = memory.poll();
            swap.add(swappedOut);
            System.out.println("Memory full. Swapped out process " + swappedOut.processId);

            // Add new process
            memory.add(new Process(processId, data));
            System.out.println("Loaded process " + processId + " to memory.");
        }
    }

    public void printStatus() {
        System.out.println("\nMemory:");
        for (Process p : memory) {
            System.out.println(p);
        }

        System.out.println("\nSwap Space:");
        for (Process p : swap) {
            System.out.println(p);
        }
    }

    public static void main(String[] args) {
        SwapExample swapExample = new SwapExample();

        swapExample.loadToMemory(1, "Data1");
        swapExample.loadToMemory(2, "Data2");
        swapExample.loadToMemory(3, "Data3");
        swapExample.loadToMemory(4, "Data4");
        swapExample.loadToMemory(5, "Data5"); // Trigger swap

        swapExample.printStatus();
    }
}
```
</div>
</details>

### TLB (Translation Lookaside Buffer)

![image](images/TLB.png)
> 위 그림은 TLB를 통해 논리적 주소를 물리적 주소로 변환을 시도하며, TLB 미스 시 페이지 테이블을 사용해 물리적 주소를 찾는 과정을 보여줌 

- 정의: 가상 메모리 시스템에서 가상 주소를 물리 주소로 빠르게 변환하기 위해 사용되는 하드웨어 캐시
- 동작 방식
  1. 가상 주소 생성: 이 가상 주소는 가상 메모리 시스템 내에서만 유효
  2. 가상 주소가 TLB에 존재한다면, TLB에서 직접 물리 주소를 얻을 수 있음
  3. 가상 주소가 TLB에 존재하지 않는다면, CPU는 페이지 테이블을 조회하여 물리 주소를 찾아야 함 
  4. 가상 주소는 TLB나 페이지 테이블을 통해 물리 주소로 변환되고 물리 주소를 통해 데이터를 가져옴
- 장점: 메모리 접근 시간 단축
- 단점: 하드웨어 캐시이므로 용량이 제한적

</div>
</details>
<details>
<summary>c언어 TLB 구현</summary>
<div markdown="1">

```c
#include <stdio.h>
#include <stdlib.h>
#include <stdbool.h>

#define TLB_SIZE 16

typedef struct {
    int page_number;
    int frame_number;
    bool valid;
} TLBEntry;

TLBEntry tlb[TLB_SIZE];

void initialize_tlb() {
    for (int i = 0; i < TLB_SIZE; i++) {
        tlb[i].valid = false;
    }
}

int search_tlb(int page_number) {
    for (int i = 0; i < TLB_SIZE; i++) {
        if (tlb[i].valid && tlb[i].page_number == page_number) {
            return tlb[i].frame_number;  // TLB hit
        }
    }
    return -1;  // TLB miss
}

void update_tlb(int page_number, int frame_number) {
    // Simple FIFO replacement
    static int next_entry = 0;
    tlb[next_entry].page_number = page_number;
    tlb[next_entry].frame_number = frame_number;
    tlb[next_entry].valid = true;
    next_entry = (next_entry + 1) % TLB_SIZE;
}

int main() {
    initialize_tlb();

    // Example usage
    update_tlb(1, 100);
    update_tlb(2, 200);

    int frame = search_tlb(1);
    if (frame != -1) {
        printf("TLB Hit: Frame number = %d\n", frame);
    } else {
        printf("TLB Miss\n");
    }

    return 0;
}
```
</div>
</details>

</div>
</details>
<details>
<summary>java TLB 구현</summary>
<div markdown="1">

```java
import java.util.LinkedHashMap;
import java.util.Map;

class TLB {
    private final int capacity;
    private final Map<Integer, Integer> tlbCache;

    public TLB(int capacity) {
        this.capacity = capacity;
        this.tlbCache = new LinkedHashMap<Integer, Integer>(capacity, 0.75f, true) {
            @Override
            protected boolean removeEldestEntry(Map.Entry<Integer, Integer> eldest) {
                return size() > capacity;
            }
        };
    }

    public Integer search(int pageNumber) {
        return tlbCache.getOrDefault(pageNumber, -1); // TLB miss -> return -1
    }

    public void update(int pageNumber, int frameNumber) {
        tlbCache.put(pageNumber, frameNumber);
    }

    public void printTLB() {
        System.out.println("Current TLB: " + tlbCache);
    }
}

public class TLBExample {
    public static void main(String[] args) {
        TLB tlb = new TLB(16); // TLB with 16 entries

        // Example usage
        tlb.update(1, 100);
        tlb.update(2, 200);

        System.out.println("Frame for page 1: " + tlb.search(1)); // TLB Hit
        System.out.println("Frame for page 3: " + tlb.search(3)); // TLB Miss

        tlb.printTLB();
    }
}
```
</div>
</details>

## 입출력 시스템
- 정의: 컴퓨터 시스템 외부와 데이터를 교환하는 장치로, 사용자와 컴퓨터 간에 정보를 전달
### 입출력 장치와 동작 원리
- 입력 장치: 데이터를 컴퓨터로 전달
- 출력 장치: 데이터를 사용자나 다른 시스템으로 전달
#### 동작 원리
1. 제어
   - 명령어를 통해 입출력 장치에 작업을 지시
2. 상태 확인
   - 장치가 준비 상태인지 확인하여 작업의 실행 가능 여부를 결정
3. 데이터 전송
   - 데이터는 CPU와 장치 간 또는 메모리와 장치 간에 이동
### 입출력 제어 방식
#### 1. 폴링 방식
- 동작 원리:
  - CPU가 주기적으로 장치의 상태를 확인하여 작업 가능 여부를 결정.
- 특징:
  - CPU가 장치 상태를 지속적으로 확인하므로 효율성이 낮고, CPU 자원 낭비가 큼.
- 예: 키보드 입력 확인.
#### 2. 인터럽트 방식
- 동작 원리:
  - 입출력 장치가 준비되면 인터럽트 신호를 CPU로 전송하여 작업 요청.
  - CPU는 작업을 중단하고 인터럽트를 처리한 뒤, 원래 작업으로 복귀.
- 특징:
  - CPU는 다른 작업을 수행할 수 있어 효율성이 높음.
  - 과도한 인터럽트 발생 시 처리 오버헤드 발생.
- 예: 네트워크 데이터 수신.
#### 3. DMA
- 동작 원리:
  - CPU 개입 없이, DMA 컨트롤러가 메모리와 입출력 장치 간의 데이터 전송을 처리.
  - CPU는 데이터 전송을 지시한 후 다른 작업을 수행하며, DMA 완료 후에만 상태 확인. 
- 특징:
  - 대량의 데이터를 빠르게 전송 가능.
  - CPU 자원 활용이 효율적.
- 예: 디스크 I/O.
### 인터럽트 (Interrupt)
- 정의: 특정 이벤트가 발생했음을 CPU에 알리고, 현재 작업을 잠시 중단하여 그 이벤트를 처리하는 메커니즘.
- 동작 원리:
  1. 이벤트 발생
  2. 작업 중단
  3. 인터럽트 처리
  4. 복귀
- 장점: 
  - CPU 효율성 향상.
  - 다양한 작업을 동시에 처리 가능.
- 단점:
  - 설계가 복잡.
  - 우선순위 관리가 필요.
### 입출력 버스와 데이터 전송
#### 입출력 버스
- 정의: CPU와 입출력 장치 간의 데이터를 전달하는 통로.
- 구성 요소
  1. 데이터 버스
     - 데이터 실제 전달 통로.
  2. 주소 버스
     - 데이터가 전송될 목적지를 지정.
     - CPU가 메모리나 장치를 식별하는 데 사용.
  3. 제어 버스
     - 데이터 전송의 타이밍과 상태를 제어.
#### 데이터 전송 방식
1. 프로그램 제어 방식
   - CPU가 모든 데이터를 직접 전송.
2. 인터럽트 방식
3. DMA
## 프로세서 설계
### 데이터 경로 설계 (Datapath Design)
- 정의: 프로세서 내부에서 데이터가 이동하는 경로 설계.
#### 1. 단일 사이클 데이터 경로 (Single-Cycle Datapath)
- 각 명령어를 하나의 클럭 사이클 내에 처리.
- 모든 연산이 동시에 완료되어야 함.
- 장점: 설계가 단순.
- 단점: 클럭 주기가 가장 느린 명령어에 맞춰져야 하므로 비효율적.
#### 2. 다중 사이클 데이터 경로 (Multi-Cycle Datapath)
- 명령어를 여러 클럭 사이클에 걸쳐 처리.
- 각 클럭 사이클에서 데이터 이동과 연산의 일부만 수행.
- 장점: 클럭 주기가 최적화됨.
- 단점: 제어 복잡.
### 제어 유닛 설계 (Control Unit Design)
- ISA(명령어 집합 구조)를 기반으로 함.
#### 1. 하드와이어드 제어 (Hardwired Control)
- 제어 신호가 논리 게이트와 플립플롭 같은 하드웨어 회로로 구현.
- 특징:
  - 설계 복잡하지만 속도가 빠름.
  - 명령어 집합 변경 시 회로 재설계 필요.
#### 2. 마이크로프로그래밍 제어 (Microprogrammed Control)
- 제어 신호가 마이크로명령어로 저장된 메모리에서 읽혀 실행.
- 특징:
  - 속도가 다소 느림.
  - 설계가 유연하고 명령어 확장이 쉬움.

### 파이프라인 처리 (Pipeline Processing)
- 정의: CPU에서 명령어 처리 단계를 병렬화하여 처리 속도를 높이는 기술. 
#### 처리 단계
1. IF (Instruction Fetch): 명령어를 메모리에서 가져옴.
2. ID (Instruction Decode): 명령어 해독.
3. EX (Execute): 연산 수행.
4. MEM (Memory Access): 메모리 접근(Read/Write).
5. WB (Write Back): 결과를 레지스터에 기록.
- 장점:
  - 병렬 처리로 CPU 성능 향상.
  - 단위 시간당 더 많은 명령어 실행 가능.
- 단점:
  - 파이프라인 해저드 발생 가능.
  - 각 단계 간의 데이터 흐름과 제어 복잡.
#### 파이프라인 해저드 (Pipeline Hazards)
1. 구조적 해저드 (Structural Hazard)
   - 동일한 자원을 여러 명령어가 동시에 사용하려고 할 때 발생.
   - 예: 메모리나 레지스터 파일의 동시 접근.
   - 해결 방법: 자원을 복제하거나 병렬 처리 가능하도록 설계.
2. 데이터 해저드 (Data Hazard)
   - 명령어 간 데이터 의존성 때문에 발생.
   - 예: 이전 명령어의 결과가 다음 명령어에서 필요하지만 아직 준비되지 않은 경우.
   - 해결 방법:
      - 포워딩(Forwarding): 결과를 즉시 다음 단계로 전달.
      - 버블 삽입(Stalling): 대기 상태를 삽입하여 데이터 준비 시간을 확보.
3. 제어 해저드 (Control Hazard)
   - 분기 명령어나 조건문 실행으로 인해 발생.
   - 예: 분기 결과가 확정되기 전에 파이프라인이 잘못된 명령어를 가져올 때.
   - 해결 방법:
      - 분기 예측(Branch Prediction): 분기 결과를 예측하여 명령어 실행.
## 성능 평가와 최적화 
### 성능 측정 자료
### Amdahl의 법칙 (Amdahl's Law)
- 정의: 병렬 처리를 통해 성능을 개선할 때, 병렬화 가능한 비율과 병렬 처리에 참여하는 프로세서의 수가 성능 향상에 어떤 영향을 미치는지 분석하는 법칙.
- 공식
  - S: 성능 향상 비율.
  - P: 병렬화 가능한 작업 비율.
  - N: 병렬 처리에 참여하는 프로세서의 수.
  - (1-P): 병렬화가 불가능한 작업 비울.
----공식 이미지 넣기 
### 시스템 성능 최적화 
#### 1. 캐시 최적화 (Cache Optimization)
- 목표: 캐시 히트율을 최대화하는 것.
#### 캐시 최적화 기법
#### 1.1 배치 처리 (Batch Processing)
- 정의: 데이터를 일괄적으로 처리하여 캐시 접근을 최적화하는 기법.
#### 1.2 반복문 최적화 (Loop Optimization)
- 정의: 반복문을 최적화하여 캐시 효율을 극대화하는 기법.
- 내부 루프 최적화: 내부 루프에서 연속된 메모리 영역을 접근하도록 배열 최적화.
- 루프 분할: 반복문을 작은 블록으로 나누어 각 블록을 처리.
- 예시
```c
int main() {
    int n = 1000;
    int result = 0;
    
    // 비효율적인 예시: 중복 계산
    for (int i = 0; i < n; i++) {
        result += i * 2;  // 'i * 2'가 반복적으로 계산됨
    }

    // 최적화된 예시: 중복 계산 제거
    int multiplier = 2;
    for (int i = 0; i < n; i++) {
        result += i * multiplier;  // 'i * 2' 대신 multiplier 사용
    }

    printf("Result: %d\n", result);
    return 0;
}
```
#### 1.3 프리페칭 (Prefetching)
- 정의: CPU가 데이터를 미리 캐시로 로드하여 캐시 미스를 줄이는 기법.

#### 2. 멀티스레딩 및 병렬 처리
- 정의: 여러 작업을 동시에 실행하여 성능을 최적화함.
- 멀티스레딩 (Multithreading)
  - 하나의 프로세스 내에서 여러 스레드를 사용하여 작업을 동시에 처리하는 기술.
- 병렬 처리 (Parallel Processing)
  - 여러 프로세서나 코어를 사용하여 하나의 작업을 분할하여 동시에 처리하는 방식.