# Project 0: xv6 설치

이 프로젝트는 부산대학교 정보컴퓨터공학부의 운영체제 과목에서 진행하는 과제로, 교육 목적으로 개발된 Unix 기반 운영체제인 xv6를 설치하고 설정하는 것을 목표로 합니다.



---

## 목차

- [xv6 소개](#xv6-소개)
- [시작하기](#시작하기)
  - [사전 준비](#사전-준비)
  - [환경 설정](#환경-설정)
  - [xv6 설치](#xv6-설치)
  - [xv6 실행](#xv6-실행)
- [커스터마이징](#커스터마이징)
- [참고 자료](#참고-자료)

---



## xv6 소개

xv6는 MIT에서 교육용으로 개발된 Unix 기반 운영체제로, 초기 Unix Version 6(V6)을 x86 기반 멀티프로세서 환경에서 재구현한 운영체제입니다. 이 프로젝트에서는 QEMU 에뮬레이터를 이용해 xv6를 실행합니다.



## 시작하기

### 사전 준비

- **운영체제**: Ubuntu 16.04.6 LTS
- **필수 패키지**: `build-essential`, `gcc-multilib`, `git`, `qemu`

### 환경 설정

1. Ubuntu 업데이트:
   ```bash
   sudo apt-get upgrade

2. 필수 패키지 설치:
   ```bash
   sudo apt-get install build-essential gcc-multilib git qemu
   
### xv6 설치

1. xv6 소스 코드 다운로드 및 압축 해제:
   ```bash
   tar -xzvf xv6-public.tar.gz
   cd xv6-public

2. 빌드:
   ```bash
   make

### xv6 실행

1. QEMU 에뮬레이터에서 xv6를 실행:
   ```bash
   make qemu-nox

2. 종료: Ctrl-A + X를 누르기


## 커스터마이징

xv6의 부팅 메시지에 본인의 학번과 이름을 출력하도록 초기 프로그램 코드를 수정하세요.

## 참고 자료

- xv6 소스 코드: [GitHub 링크](https://github.com/mit-pdos/xv6-public)
- xv6 해설서: [xv6 commentary PDF](https://pdos.csail.mit.edu/6.828/2018/xv6/book-rev11.pdf)
- xv6 관련 참고서적: [xv6 source booklet PDF](https://pdos.csail.mit.edu/6.828/2018/xv6/xv6-rev11.pdf)




