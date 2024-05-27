# 리눅스 명령어(1) - top


## 📌top이란?
top 명령어는 리눅스 계열 서버의 OS 상태를 호가인할 수 있는 CLI어플리케이션이라고 할 수 있다.
CPU사용량, 메모리 사용량 등을 확인할 수 있고, 서버에서 구동 중인 모든 어플리케이션들을 CPU 사용률이나 메모리 사용률이 많은 순서대로 나열하여 모니터링이 가능한 명령어이다.

## 💡옵션
- shift + t ( 대문자 T ): 실행된 시간이 큰 순서로 정렬합니다.
- shift + m ( 대문자 M ) : 메모리 사용량이 큰 순서로 정렬합니다.
- shift + p ( 대문자 P ): cpu 사용량이 큰 순서로 정렬합니다.
- d [sec] : 설정된 초단위로 화면이 갱신됩니다.
---
- q : top 를 종료


![top 명령어](https://github.com/onyune/OP-SW/assets/166621162/50e3aac7-581a-4c38-8bdd-a74bc6141c0f)

---
>top - 시스템의 현재시간, os가 살아 있는 시간, 유저 세션 수
>load average: cpu load의 이동 평균 / 차례대로 1분, 5분, 15분에 대한 평균값
* cpu load란 cpu가 수행하는 작업의 양

task : 현재 프로세스들의 상태를 나타내주는 영역

- total : 전체 프로세스
- running : running상태인 프로세스
- sleeping : 대기상태인 프로세스
- stopped : 종료된 프로세스
- zombies : 좀비상태인 프로세스 수

%Cpu(s) : cpu가 어떻게 사용되고 있는지 그 사용율을 보여주는 영역
모든 값의 총 합은 100% 

- us : 프로세스의 유저 영역에서의 CPU 사용률
- sy : 프로세스의 커널 영역에서의 CPU 사용률
- ni : 프로세스의 우선순위(priority) 설정에 사용하는 CPU 사용률
- id : 사용하고 있지 않는 비율
- wa : IO가 완료될때까지 기다리고 있는 CPU 비율
- hi : 하드웨어 인터럽트에 사용되는 CPU 사용률
- si : 소프트웨어 인터럽트에 사용되는 CPU 사용률
- st : CPU를 VM에서 사용하여 대기하는 CPU 비율

---
그 밑으로는 메모리 사용량이다.

- MiB Mem : RAM의 메모리 영역으로 Mem이라 표시되어있는 부분
- MiB Swap : 디시크를 메모리처럼 이용하는 Swap 메모리 영역
일반적으로 Mem의 사용량이 거의 가득 찼을 때 Swap메모리 영역을 사용한다. 
하지만 디스크 부분이기때문에 RAM 메모리보다 속도가 느림.

- total : 총 메모리 양
- free : 사용가능한 메모리 양
- used : 사용중인 메모리 양

디테일 영역
- PID : 프로세스 ID, 프로세스를 구분하기 위한 겹치지않는 고유한 값이다.
- USER : 해당 프로세스를 실행한 USER 이름 또는 효과를 받는 USER의 이름이다.
- PR & NI : 커널에 의해서 스케줄링되는 우선순위 & PR에 영향을 주는 nice라는 값
- VIRT : 프로세스가 소비하고 있는 총 메모리이다. 프로그램이 실행중인 코드, heap, stack과 같은 메모리, IO buffer 메모리를 포함한다.
- RES : RAM에서 사용중인 메모리의 크기를 나타낸다.
- SHR : 다른 프로세스와의 공유메모리를 나타낸다.
- %MEM : RAM에서 RES가 차지하는 비율을 나타낸다.
- S : 프로세스의 현재 상태를 나타낸다.
- TIME+ : 프로세스가 사용한 토탈 CPU 시간
- COMMAND : 해당 프로세스를 실행한 커맨드를 나타낸다.



 
