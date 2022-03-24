MIPS(Million Instructions Per Second) : 초 당 백만 연산 속도  

전력 소비  
CPU CORE 8+4  
8 -> Big : 전력소비가 큰 부분  
4 -> Little : 전력소비가 작은 부분  
열 -> 효율감소 -> 수명에 직결됨  
  
P = C *V *I *f (상수, 전압, 전류, 주파수)  
  

파운드리 : 반도체 생산 - 삼성, TSMC   
팹리스   : 반도체 설계 - 애플, 컬컴, ARM, Intel  
IP      :  지식 재산권(Intellectual Property rights)  
  
CISC(Complex Instruction Set Computer)  
복잡 명령어 집합 컴퓨터  
RISC(Reduced Instruction Set Computer)
축소 명령어 집합 컴퓨터 -> 전력소모 줄이기 위해  
  
작성된 프로그램 -> Flash -> 읽어올 때 RAM 으로  

RAM(unvolatile) : 휘발성  
ROM(volatile)   : 비휘발성  

Micro - Controller (마이컴)  
: 마이크로프로세서와 메모리, 입력장치 등 기능이 함께 있음  
: 혼자서 다함(CPU + 메모리 + I/O + peripherals)
: 통신 i2c, spi
: GPIO 
: ADC DAC 
등이 메인칩 안에 들어가있음

Micro - Processor  
: CPU, 주변 장치(I/O등)가 필요함,  제어장치, 연산장치, 레지스터    
: 혼자서 못함(CPU)

CPI : Cycles(Clock) per Instruction   
1MHZ   
-> 1이면 -> 1초에 한 사이클 백만  
-> 2이면 -> 1초에 2번 사이클 50만  


 IMU(Inertial Measurement Unit) '관성 측정 장치'



### Memory map 보기

Base Address   : 시작 주소
offset Address 
c언어 구조체를 가지고 클래스처럼 사용한다.
-> int 4byte

구조체 비트 합에서 4byte씩 옮겨가며 주소입력


&= ~() : RESET  
|=     : SET  
^      : Toggle  

[Go to top](#){: .btn .btn--primary }{: .align-right}