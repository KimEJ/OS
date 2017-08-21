# 2장 OS개발환경을 구축하자

### Xcode Command Line Tools

Xcode Command Line Tools을 설치하지 않을 경우 Homebrew가 정상적으로 동작하지 않을 수도 있다. 따라서 Xcode Command Line Tools먼저 설치해 주자. 
```
$ xcode-select --install
```


### Homebrew

Homebrew는 macOS 용 패키지 관리자이다. nasm, qemu 모두 Homebrew를 통해 설치할 수 있다.
```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
버전 확인
```  
$ brew -v
Homebrew 1.3.1
Homebrew/homebrew-core (git revision 2893; last commit 2017-08-13)
```
이제 Homebrew 를 설치했으니 원하는 패키지를 brew 명령을 통해 설치할 수 있다.


### nasm

Netwide Assembler, 인텔 x86 아키텍처용 어셈블러이자 역어셈블러이다.
``` 
$ brew install nasm
```
버전 확인
```
$ nasm -version
NASM version 2.13.01 compiled on May  2 2017
```

### 이클립스

vim을 사용하였다.
```
$ brew install vim
```

### qemu

가상화 소프트웨어
```
$ brew install qemu
```
버전 확인
```
$ qemu-img --v
qemu-img version 2.9.0
Copyright (c) 2003-2017 Fabrice Bellard and the QEMU Project developers
```
