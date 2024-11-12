# xv6-project

이 프로젝트는 2024년 부산대학교 정보컴퓨터공학부 최윤호 교수님의 운영체제 강의에서 진행된 xv6 운영체제 프로젝트입니다. xv6의 특정 기능을 구현하고 확장하는 것을 목표로 하며, 운영체제의 기초 개념을 학습할 수 있습니다. 

각 프로젝트 디렉터리에서 세부 문서와 구현 코드를 확인할 수 있습니다.

---

## 프로젝트 목록

1. [Project 0: Install xv6](#project-0-install-xv6)
2. [Project 1: System Call](#project-1-system-call)
3. [Project 2: Scheduling](#project-2-scheduling)
4. [Project 3: Stack Growth](#project-3-stack-growth)
5. [Project 4: Copy-On-Write](#project-4-copy-on-write)



## Project 0: Install xv6

**목적**: xv6 운영체제를 설치하고, QEMU 에뮬레이터를 통해 실행하는 방법을 학습합니다.

- **설치 과정**: Ubuntu 16.04.6 LTS 환경에서 `build-essential`, `gcc-multilib`, `git`, `qemu` 패키지를 설치한 후 xv6 소스를 다운로드하고 빌드합니다.
- **QEMU 실행**: xv6를 QEMU 에뮬레이터에서 실행하고, xv6 부팅 메시지에 학번과 이름을 표시하도록 수정합니다.

[자세한 내용 보기](project%20%230/README.md)


## Project 1: System Call

**목적**: xv6에 새로운 시스템 콜을 추가하고, 사용자와 커널 공간 간의 인터페이스를 이해합니다.

- **구현 기능**:
  - `getreadcount()` 시스템 콜을 추가하여, `read()` 시스템 콜 호출 횟수를 반환합니다.
- **테스트**: 사용자 프로그램을 통해 `getreadcount()` 시스템 콜의 동작을 확인합니다.

[자세한 내용 보기](project%20%231/README.md)



## Project 2: Scheduling

**목적**: xv6의 스케줄러를 수정하여 우선순위 기반 스케줄링을 구현합니다.

- **구현 기능**:
  - 프로세스 우선순위 설정(`setnice()`), 우선순위 조회(`getnice()`), 프로세스 상태 조회(`ps()`) 시스템 콜 구현
  - 낮은 `nice` 값일수록 높은 우선순위를 가지도록 우선순위 기반 스케줄러 구현
- **테스트**: `minitop` 프로그램을 통해 각 프로세스의 상태와 우선순위를 확인합니다.

[자세한 내용 보기](project%20%232/README.md)



## Project 3: Stack Growth

**목적**: xv6에서 페이지 폴트를 처리하여 스택이 동적으로 확장될 수 있도록 구현합니다.

- **구현 기능**:
  - 페이지 폴트 핸들러를 구현하여 스택 공간이 필요할 때마다 새로운 페이지를 할당
  - 스택 오버플로우가 발생하면 프로세스를 종료
- **테스트**: 잘못된 메모리 접근을 시도하여 페이지 폴트 핸들러가 올바르게 동작하는지 확인합니다.

[자세한 내용 보기](project%20%233/README.md)



## Project 4: Copy-On-Write

**목적**: xv6에 `Copy-On-Write` 메커니즘을 구현하여 메모리 효율성을 개선합니다.

- **구현 기능**:
  - `copyuvm()` 함수를 수정하여 `fork()` 시 부모와 자식 프로세스가 메모리 페이지를 공유
  - 공유된 페이지에 쓰기 시도가 발생하면 새로운 페이지를 할당하여 복사
  - 페이지 참조 카운터 관리 및 페이지 폴트 핸들러 구현
- **테스트**: `Copy-On-Write`가 제대로 작동하는지 확인하기 위한 프로그램 작성

[자세한 내용 보기](project%20%234/README.md)



## 참고 자료

- xv6 소스 코드: [GitHub 링크](https://github.com/mit-pdos/xv6-public)
- xv6 해설서: [xv6 commentary PDF](https://pdos.csail.mit.edu/6.828/2018/xv6/book-rev11.pdf)
- xv6 관련 참고서적: [xv6 source booklet PDF](https://pdos.csail.mit.edu/6.828/2018/xv6/xv6-rev11.pdf)

