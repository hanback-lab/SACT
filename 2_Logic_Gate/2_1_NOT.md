# 2.Logic Gate

## 2.1 Not Gate

### **2.1.1.이론**

NOT 연산은 입력 논리  값의 반대가 출력되는 연산이다. 출력 값을 입력 값의 역 또는 보수라고 말할 수도 있다.

다음 그림은 NOT 게이트의 논리 기호로 인버터(inverter)라고 부르기도 한다. 

이 회로는 항상 1개의 입력을 가지고 있으며, 출력은 입력 논리 값의 반대 값을 가지게 된다. 

즉 High의 값이 입력되면, Low의 값이 출력 된다.


<img src="./pds/not01.png" alt="not01" style="width: 30%;">

NOT 연산 진리표
|A|X = /A  (not A)|
|:---:|:---:|
|0|1|
|1|0|

<img src="./pds/not02.png" alt="not02" style="width: 50%;">



### **2.1.2.실습**


**실험 목표**

1. 다음의 회로를 설계하여 실험해 보자.

<img src="./pds/not03.png" alt="not03" style="width: 70%;">


이 회로의 진리표은 다음과 같다. 


|A|X = /A |Y = /(/A) = A|
|:---:|:---:|:---:|
|0|1|0|
|1|0|1|

SACT 장비에서 확인하기 위하여 연결된 장치는 다음과 같다. 

|A|X|Y|
|:---:|:---:|:---:|
|SLIDE7|LED7|LED6|

**설계**

2. 실험을 위해 아래 링크를 눌러, 프로젝트 파일을 다운로드 한다. 

<a href="./pds/GATEpds.zip" download>여기를 클릭하여 프로젝트 다운로드</a>



3. 다운로드된 프로젝트의 압축 파일을 d:\work에 이동시킨 후, 압축을 푼다.

<img src="./pds/not04.png" alt="not04" style="width: 50%;">
 

4. Quartus II를 실행키고, File> Open Project 메뉴를 선택한다. 

<img src="./pds/ex01.png" alt="ex01" style="width: 50%;">


5. 위에서 압축을 푼 위치인, d:\work\GATE_NOT 폴더로 이동 후,GATE_NOT 프로젝트를 OPEN한다. 

<img src="./pds/not05.png" alt="not05" style="width: 70%;">

6. File > Open 메뉴를 선택하여 GATE_NOT.bdf 파일을 불러오거나, 프로젝트 왼쪽의 GATE_NOT 부분을 마우스로 더블 클릭한다. 

<img src="./pds/ex02.png" alt="ex02" style="width: 50%;">

<img src="./pds/not06.png" alt="not06" style="width: 70%;">


7. 아래 그림과 같이 미완성된 도면이 보이는데, 1번에서 설명한 도면으로 완성시키자. 

<img src="./pds/not07.png" alt="not07" style="width: 70%;">

<img src="./pds/not03.png" alt="not03" style="width: 70%;">

8. 아래 그림과 같이 도면을 마우스로 더블 클릭하거나, 마우스 오른쪽 버튼을 누르고 Insert > Symbol 메뉴를 선택한다. 

<img src="./pds/not08.png" alt="not08" style="width: 70%;">

9. 심볼 창에서 왼쪽 아래 부분의 -Name- 부분에 not이라고 심볼명을 입력하고, OK 버튼을 누른다. 

<img src="./pds/not09.png" alt="not09" style="width: 70%;">

10. NOT 게이트 심볼을 도면에 위치시킨다. 다시 한 번 진행하여 총 2개의 심볼을 도면에 위치시킨다. 

<img src="./pds/not10.png" alt="not10" style="width: 70%;">

11. 심볼의 선 분에 마우스 포인터를 가져가면 아래 그림과 같이 wire를 그리는 것으로 바뀌는데, 마우스의 드래그 & 드롭을 이용해서 회로를 완성해 보자.

회로의 Wire가 정확하게 연결되지 않았을 경우에는 원하는 동작이 되지 않을 수 있기 때문에 주의하자. 

<img src="./pds/not11.png" alt="not11" style="width: 70%;">

<img src="./pds/not12.png" alt="not12" style="width: 70%;">


**컴파일**


12. File > Save 메뉴를 선택하여 저장하고, Processing > Start Compilation 메뉴를 선택하여 컴파일을 진행한다. 

이 컴파일 과정은 설계한 논리 회로에 오류가 없는 지를 검증하고, 프로그래밍 파일과 시뮬레이션 파일을 만드는 과정이다. 


<img src="./pds/ex03.png" alt="ex03" style="width: 30%;">

<img src="./pds/ex04.png" alt="ex04" style="width: 30%;">

13. 아래 그림은 컴파일이 진행되어 완료된 상태이다.  

<img src="./pds/not13.png" alt="not13" style="width: 80%;">


**시뮬레이션**

14. 아래 그림과 같이 File > Open 메뉴를 선택하고, 나타나는 Open File 창에서 오른쪽 아래 부분의 File Type을 All File(*.*)로 변경한 후, Waveform.vwf 파일을 선택한다. 

<img src="./pds/not14.png" alt="not14" style="width: 70%;">

<img src="./pds/ex06.png" alt="ex06" style="width: 80%;">

<img src="./pds/not15.png" alt="not15" style="width: 70%;">

15. 아래 그림과 같이 Waveform 창에서, Simulation > Run Functiona Simulation 메뉴를 선택하여 Functional Simulation을 진행한다. 

<img src="./pds/not16.png" alt="not16" style="width: 70%;">

16. 아래 그림은 시뮬레이션 한 결과이다. 앞의 실험 목표에서 설명한 진리표와 맞게 시뮬레이셔 되었는지 확인한다. 

<img src="./pds/not17.png" alt="not17" style="width: 70%;">


**하드웨어 동작 확인**

17. SACT 장비를 준비한다. 

18. 장비의 중앙 위쪽의 USB B Type Connector에 USB 케이블을 PC와 연결한다. 

19. 장비의 왼쪽 Power Connector에 전원 케이블을 연결하고, 전원 스위치를 눌러 장비에 전원을 인가시킨다. 

20. Quartus 소프트웨어에서 Tool > Programmer 메뉴를 선택한다.

<img src="./pds/ex07.png" alt="ex07" style="width: 50%;">

21. 앞의 그림과 같이 Programmer창의 Hardware Setup  부분이 No Hardware로 되어 있다면, 장비와 PC간에 USB 케이블이 바르게 연결되어 있는지 확인하고 Hardware Setup 버튼을 눌러, USB Blaster를 선택한다. 

<img src="./pds/ex08.png" alt="ex08" style="width: 70%;">

<img src="./pds/ex09.png" alt="ex09" style="width: 50%;">

22. 아래 그림과 같이 USB Blaster가 연결되어 있다면, Start 버튼을 눌러 프로그래밍 하고 장비에서 NOT 게이트의 동작을 확인한다. 

<img src="./pds/not18.png" alt="ex18" style="width: 70%;">




 









