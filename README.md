---
layout: post
title: stm8blue_blink
date: 2024-12-23 13:41:09 +0800
categories: [stm8s, STM8BLUE, STM8S103F3P6, sdcc]
tags: [stm8s, STM8BLUE, STM8S103F3P6, sdcc, gcc, make]
image: https://yooaroma.com/mm/image/stm8/stm8blue/mm_stm8blue_set.jpg
# ------------------------------------------------------------------
# 포스트 작성 시 참고 URL
---

## ST 마이컴 개발시 설치 TOOLS

- vscode download : <https://code.visualstudio.com/download>
- 칩(chip) 프로그래머 : ST Visual Programmer : <https://www.st.com/en/development-tools/stvp-stm8.html>
- GNU/LINUX에서 STM8 개발 도구 시작하기 : <https://www.codementor.io/@hbendali/getting-started-with-stm8-development-tools-on-gnu-linux-zu59yo35x>
- stm8flash : <https://github.com/vdudouyt/stm8flash>
- STM8S105K4T6 - stm8flash 에 대한 설명 : <https://blog.naver.com/chcbaram/222688164090>
- 최종 stm8flash : <https://github.com/chcbaram/stm8flash_win>
- st 컴파일러 : sdcc download : <https://sourceforge.net/projects/sdcc/files/snapshot_builds/x86_64-w64-mingw32/>
  - snapshot 의 빌더 버젼(\*.zip)을 다운로드 받아서 unzip하고 나서 c:/tools 아래에 카피한다. 그리고 시스템 환경변수 path 에 위 c:\tools\sdcc\bin 폴더를 추가한다.
- make : download : <https://github.com/xpack-dev-tools/windows-build-tools-xpack/releases>
  - 최신 버젼을 (\*.zip) 화일을 unzip 하여 c:/tools/make 아래에 카피한다. 그리고 시스템 환경변수 path 에 위 c:\tools\make\bin 폴더를 추가한다.
- gcc 컴파일러 설치 : <https://www.mingw-w64.org/>
  - 다운로드로 가서 : <https://www.mingw-w64.org/downloads/> -> <https://github.com/niXman/mingw-builds-binaries/releases> 즉 Mingw-builds installation: GitHub 를 선택해서
    <x86_64-14.2.0-release-win32-seh-msvcrt-rt_v12-rev0.7z> path는 c:\tools\mingw64 에 설치하고 사용하기를 권장...
  - path c:\tools\mingw64\bin 를 추가하면 실행이 가능합니다.
- vscode extention program : Serial Monitor

---

## STM8S_DISCOVERY

- site : <https://www.st.com/en/evaluation-tools/stm8s-discovery.html>
- vscode key : <https://keycombiner.com/collections/vscode/>

---

![STM8S-DISCOVERY](https://www.st.com/bin/ecommerce/api/image.PF247087.en.feature-description-include-personalized-no-cpn-large.jpg)

---

## All features

- <https://www.st.com/content/ccc/fragment/product_related/rpn_information/product_circuit_diagram/group3/95/7f/7f/bb/d4/44/4d/e4/bd-stm8s105x6-32k/files/bd-stm8s105x6-32k.jpg/jcr:content/translations/en.bd-stm8s105x6-32k.jpg>
- STM8S105C6T6 microcontroller, 32 KB Flash, 2 KB RAM, 1 KB EEPROM
- Powered by USB cable between PC and STM8S-DISCOVERY
- Selectable power of 5 V or 3.3 V
- Touch sensing button
- User LED
- Extension header for all I/Os
- Wrapping area for users own application
- Embedded ST-Link
- USB interface for programming and debugging
- SWIM debug support

---

## 참고 문서

- STM8S-DISCOVERY User Manual : <https://www.st.com/resource/en/user_manual/um0817-stm8sdiscovery-stmicroelectronics.pdf>
- Developing and debugging : <https://www.st.com/resource/en/user_manual/um0834-developing-and-debugging-your-stm8sdiscovery-application-code-stmicroelectronics.pdf>
- debugging and writer : <https://www.devicemart.co.kr/goods/view?no=11871401>
- 부품 사양
- STM8S105C6T6 : <https://www.st.com/en/microcontrollers-microprocessors/stm8s105c6.html>
  - STM8S Reference Manuals : <https://www.st.com/resource/en/reference_manual/rm0016-stm8s-series-and-stm8af-series-8bit-microcontrollers-stmicroelectronics.pdf>
  - pdf <https://www.st.com/resource/en/datasheet/stm8s105c6.pdf>
  - doc link : <https://www.st.com/en/microcontrollers-microprocessors/stm8s105c6.html#documentation>
  - Programming Manuals : <https://www.st.com/resource/en/programming_manual/pm0044-stm8-cpu-programming-manual-stmicroelectronics.pdf>
  - PB5 : PORT : VCC - PU - VOUT - SW - GND / VOUT - LED - 100R - GND
- The STM8S Series and STM8AF Series Flash programming manual (PM0051)
  - <https://www.st.com/resource/en/programming_manual/pm0051-how-to-program-stm8s-and-stm8a-flash-program-memory-and-data-eeprom-stmicroelectronics.pdf>
- The STM8 SWIM communication protocol and debug module user manual (UM0470)
  - <https://www.st.com/resource/en/user_manual/cd00173911-stm8-swim-communication-protocol-and-debug-module-stmicroelectronics.pdf>
- STM8 bootloader user manual (UM0560)
  - <https://www.st.com/resource/en/user_manual/cd00201192-stm8-bootloader-stmicroelectronics.pdf>
- STM8 CPU programming manual (PM0044)
  - <https://www.st.com/resource/en/programming_manual/pm0044-stm8-cpu-programming-manual-stmicroelectronics.pdf>
- STM8 in-application programming example (AN2659)
  - <https://www.st.com/resource/en/application_note/an2659-stm8-inapplication-programming-iap-using-a-customized-userbootloader-stmicroelectronics.pdf>
- Micro USB STM8S103F3P6 초소형 개발보드 (SZH-AT041)
  - <https://www.devicemart.co.kr/goods/view?no=1361337> <br>

<!--  # <https://www.devicemart.co.kr/data/collect_img/kind_0/goods/detail/1361337_1.jpg> -->

[//]: # "https://www.devicemart.co.kr/data/collect_img/kind_0/goods/detail/1361337_1.jpg"
[//]: # "https://www.devicemart.co.kr/data/collect_img/kind_0/goods/detail/1361337_1.jpg"
[//]: # "https://www.devicemart.co.kr/data/collect_img/kind_0/goods/detail/1361337_1.jpg"

---

- Micro USB STM8S103F3P6 초소형 개발보드 <br>

  - [Micro USB STM8S103F3P6 초소형 개발보드](https://www.devicemart.co.kr/goods/view?no=1361337) <br>
    ![Micro USB STM8S103F3P6 초소형 개발보드](https://yooaroma.com/mm/image/stm8/stm8blue/STM8S103F3P6_BOARD.png) <br>
  - [**circuitstate.com** 보드 설명 사이트](https://www.circuitstate.com/pinouts/stm8s-blue-generic-stm8s103f3p6-development-board-pinout-diagram-and-pin-reference/#Schematic) <br>
  - [보드 pinout 및 reference](https://www.circuitstate.com/wp-content/uploads/2023/10/STM8S-Blue-STM8S103F3P6-Microcontroller-Development-Board-Pinout-Diagram-and-Pin-Reference-Featured-Image-CIRCUITSTATE-Electronics-2.jpg) <br>
    ![보드 pinout 및 reference](https://yooaroma.com/mm/image/stm8/stm8blue/STM8S-Blue-STM8S103F3P6-Microcontroller-Development-Board-Pinout-Diagram-and-Pin-Reference-Featured-Image-CIRCUITSTATE-Electronics-2.jpg) <br>
  - [보드 사진 앞면과 뒷면](https://www.circuitstate.com/wp-content/uploads/2023/10/STM8S-Blue-STM8S103F3P6-Generic-Microcontroller-Development-Board-Top-and-Bottom-Views-CIRCUITSTATE-Electronics-1.jpg) <br>
    ![보드 사진 앞면과 뒷면](https://yooaroma.com/mm/image/stm8/stm8blue/STM8S-Blue-STM8S103F3P6-Generic-Microcontroller-Development-Board-Top-and-Bottom-Views-CIRCUITSTATE-Electronics-1.jpg) <br>
  - [보드 회로도](https://www.circuitstate.com/wp-content/uploads/2023/10/STM8S-Blue-STM8S103F3P6-Generic-Development-Board-Schematic-Diagram-R0.1-CIRCUITSTATE-Electronics-1_1.png) <br>
    ![보드 회로도](https://yooaroma.com/mm/image/stm8/stm8blue/STM8S-Blue-STM8S103F3P6-Generic-Development-Board-Schematic-Diagram-R0.1-CIRCUITSTATE-Electronics-1_1.png) <br>
  - [보드 pinout](https://www.circuitstate.com/wp-content/uploads/2023/10/STM8S-Blue-Generic-STM8S103F3P6-Microcontroller-Board-Pinout-Diagram-R0.1-CIRCUITSTATE-Electronics-1.png) <br>
    ![보드 pinout](https://yooaroma.com/mm/image/stm8/stm8blue/STM8S-Blue-Generic-STM8S103F3P6-Microcontroller-Board-Pinout-Diagram-R0.1-CIRCUITSTATE-Electronics-1.png) <br>
  - [보드 IC pinout](https://www.circuitstate.com/wp-content/uploads/2023/10/STM8S-Blue-STM8S103F3P6-Generic-Microcontroller-Development-Board-IC-Pinout-CIRCUITSTATE-Electronics-1.png) <br>
    ![보드 IC pinout](https://yooaroma.com/mm/image/stm8/stm8blue/STM8S-Blue-STM8S103F3P6-Generic-Microcontroller-Development-Board-IC-Pinout-CIRCUITSTATE-Electronics-1.png) <br>

---

---

## 기타 자료

- stm8flash : <https://github.com/hbendalibraham/stm8_started>
- 디버거 : <https://marketplace.visualstudio.com/items?itemName=CL.stm8-debug>

---

## 참고자료

- snippets : 사용법 <https://youtu.be/EVxCdenPbFs> 드림코딩 <br>
- devicemart 구매 <br>
- [SMG] Micro USB STM8S103F3P6 초소형 개발보드 [SZH-AT041] <https://www.devicemart.co.kr/goods/view?no=1361337> <br>
- [SMG] STM8S105K4T6 초소형 개발보드 [SZH-DVBP-002] <https://www.devicemart.co.kr/goods/view?no=1326909> <br>
- [SMG] ST-LINK V2 호환 STM8/STM32 프로그래머/에뮬레이터 [SZH-PRBP-004] <https://www.devicemart.co.kr/goods/view?no=1326910> <br>
- [SMG] CH340G USB to TTL 컨버터 모듈 [SZH-EK092] <https://www.devicemart.co.kr/goods/view?no=1321026> <br>
- <https://tenbaht.github.io/sduino/hardware/stm8blue/> <br>
- <https://tenbaht.github.io/sduino/> <br>
- <https://github.com/roybaer/sduino_mb> <br>
- <https://github.com/roybaer/sduino_uno> <br>

---

## 실행 순서

- 하고자 하는 디렉토리로 이동한다.
- make 하면 makefile을 참고하여 실행한다.
- 결과 화일은 obj 와 exe에 생성된다.
- xx.hex 화일을 다운로드한다.
- ST Visual Programmer 을 통해서 화일을 읽어 들인다.
- File -> Open (xx.hex)
- Configure 선택 (ST-LINK - USB - SWIM - STM8S105x6) OK
- Program -> Current Tab (Ctl-P)
- File -> Exit

---

Use SDCC Toolchain :
Notice: make sure you can find your 'target' and 'interface' in OpenOcd config folder !, like: 'target/stm8s003.cfg'

```c
{
"version": "0.2.0",
"configurations": [
  {
    "type": "stm8-debug",
    "request": "launch",
    "name": "Launch Program",
    "serverType": "stm8-sdcc",
    "executable": ".\\out\\Debug\\stm8_demo.elf",
    "openOcdConfigs": [
    "interface/stlink.cfg",
    "target/stm8s003.cfg"
    ]
  }
]
}
```

git hub example
===

```git
// 일반적으로 계속 할 때 사용
git add -A -- 작업 디렉토리 모든 변경내용
or
git add .
git commit -m "readme text"
git push
// 추가 사용하는 명령어
git status
git config
git add file/dir
```

=======
