# Embedded C Fundamentals
<p align="center">
  <a href="." title="Embedded C Fundamentals">
    <img src="/assets/images/embedded-c-funfamentals.png" title="Embedded C Fundamentals" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

:dart: [Embedded C Fundamentals](https://github.com/hothienai/embedded-c-fundamentals) is focusing on helping you get familiar with embedded programming world step-by-step.

:key: By having the fudamental knowledge about the embedded C, will enable you to have below skills:
* Deeply understand inside of the source code
* Confidently write your own code
* Able to debug the software and analyse the software issue
* Design and develop a robustness software
* Support you develop embedded programming skills, which is strong demanded by customers and employers

:rocket: The topics may be simple, but I believe that every topic I bring here is a step-stone enable you to approach the much higher complex technical topics in embedded programming world and help you develop your career path!

# Topics
:books: List of topics you can explore here:
| Topic     | Description |
| :-------- | :-------    |
| [Embedded C Programming](/resources/embedded-c-programming/)  | Focuses on best practices and techniques for writing efficient, reliable, and maintainable code for embedded systems |
| [Microcontroller Architecture Overview](/resources/uc-architecture/)  | What is key components of microcontroller architecture? |
| [STM32F4 Programming](/resources/stm32f4-programming/)  | Essential concepts and practical techniques for working with the STM32F4 series microcontrollers |
| [STM32F1 Programming](/resources/stm32f1-programming/)  | Essential concepts and practical techniques for working with the STM32F4 series microcontrollers |

# Requisitions
The below requistions are used for demostration only. For your case, you can choose another setup and implement the idea provided in the examples.
## Hardware
:wrench: Development Kits used in the most of topics:

* [Discovery kit with STM32F407VG MCU](https://www.st.com/en/evaluation-tools/stm32f4discovery.html). The main microcontroller on the development kit is ARM Cortex-M4 32-bit STM32F407VG. This development kit is produced by ST. Moreover, there is on-board ST-LINK programmer/debugger that enable user quickly flashes and debugs easily.
<p align="center">
  <a href="." title="Discovery kit with STM32F407VG MCU">
    <img src="/assets/images/discovery-kit-with-stm32f407vg.PNG" title="Discovery kit with STM32F407VG MCU" style="min-width: 200px"/>
  </a>
</p>

* [STM32F103C8T6Blue Pill](https://stm32-base.org/boards/STM32F103C8T6-Blue-Pill.html)

* [STM32 Nucleo-64 Development Board](https://www.st.com/en/evaluation-tools/nucleo-f401re.html). The main microcontroller on the development kit is ARM Cortex-M4 32-bit. This development kit is also produced by ST. Moreover, there is on-board ST-LINK programmer/debugger that enable user quickly flashes and debugs easily.
<p align="center">
  <a href="." title="STM32 Nucleo-64 Development Board">
    <img src="/assets/images/nucleo-f401re.png" title="STM32 Nucleo-64 Development Board" style="min-width: 200px"/>
  </a>
</p>

* [Tiva C Series TM4C123G LaunchPad Evaluation Kit - EK-TM4C123GXL](https://www.ti.com/tool/EK-TM4C123GXL). The main microcontroller on the development kit is ARM Cortex-M4F 32-bit produced by Texas Instruments. Moreover, there is on-board Debugger/Programmer (Stellaris ICDI) that enable user quickly flashes and debugs easily.
<p align="center">
  <a href="." title="Tiva C Series TM4C123G LaunchPad Evaluation Kit">
    <img src="/assets/images/ek-tm4c123gxl.png" title="Tiva C Series TM4C123G LaunchPad Evaluation Kit" style="min-width: 200px"/>
  </a>
</p>

* Additionally, during testing và debugging, I also use Logic Analyzer to measure and capture the signal of microcontroller input/output pins.
<p align="center">
  <a href="." title="Logic Analyzer">
    <img src="/assets/images/LogicAnalyzer.png" title="Logic Analyzer" style="min-width: 200px"/>
  </a>
</p>

## Software
:hammer: Software can be used to demonstrate:
* [Keil C](https://www.keil.com/demo/eval/arm.htm) is an IDE developed by ARM company. It is a very powerful tool supports software engineer to compose, edit, compile, flash code and debug. Especially, with non-comercial version, I think it fully supports all your needs to study and research.
<p align="center">
  <a href="." title="Keil C">
    <img src="/assets/images/KeilC.PNG" title="Keil C" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

* To visualize the measured signals of microcontroller pins from Logic Analyzer and easy to analyze the logs, [Logic 2](https://www.saleae.com/pages/downloads) tool is one of the suitale choice.
<p align="center">
  <a href="." title="Logic 2">
    <img src="/assets/images/Logic2.PNG" title="Logic 2" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

## Documents
:page_facing_up: You can prefer the below documents for more detailed information:
* [Discovery kit with STM32F407VG MCU](https://www.st.com/resource/en/user_manual/um1472-discovery-kit-with-stm32f407vg-mcu-stmicroelectronics.pdf)
* [STM32 Nucleo-64 boards (MB1136) User Manual](https://www.st.com/resource/en/user_manual/um1724-stm32-nucleo64-boards-mb1136-stmicroelectronics.pdf)
* [STM32F405xx STM32F407xx Mircocontroller Datasheet](https://www.st.com/resource/en/datasheet/dm00037051.pdf)
* [STM32F401xD STM32F401xE Microcontroller Datasheet](https://www.st.com/resource/en/datasheet/stm32f401re.pdf)
* [Tiva™ C Series TM4C123G LaunchPad Evaluation Board User's Guide](https://www.ti.com/lit/ug/spmu296/spmu296.pdf?ts=1751851064369&ref_url=https%253A%252F%252Fwww.google.com%252F)
* [Tiva™ TM4C123GH6PM Microcontroller Datasheet](https://www.ti.com/lit/ds/symlink/tm4c123gh6pm.pdf?ts=1751851133571&ref_url=https%253A%252F%252Fwww.ti.com%252Fproduct%252FTM4C123GH6PM%253Futm_source%253Dgoogle%2526utm_medium%253Dcpc%2526utm_campaign%253Depd-null-null-GPN_EN-cpc-pf-google-soas_en_cons%2526utm_content%253DTM4C123GH6PM%2526ds_k%253DTM4C123GH6PM+Datasheet%2526DCM%253Dyes%2526gad_source%253D1%2526gad_campaignid%253D11598374538%2526gbraid%253D0AAAAAC068F0bzZ8dihLtGrnV1NQpe3dU3%2526gclid%253DCj0KCQjwvajDBhCNARIsAEE29WqaMRC8N_5Qd0aX3VLcyh-dPe_S1-Q_Jke01T5noRDUBxR3QQkN7d4aAtmTEALw_wcB%2526gclsrc%253Daw.ds)
* [Cortex Microcontroller Software Interface Standard (CMSIS)](https://github.com/hothienai/technical-resources/tree/main/tiva-c-series/CMSIS)
* [Tiva™ TM4C123GH6PM Microcontroller Software Support Package](https://github.com/hothienai/technical-resources/tree/main/tiva-c-series/ek-tm4c123gxl)

# Assumptions
:heavy_check_mark: When I'm doing this series, I have below assumptions:
* Reader has a basic knowledge of C programming language.
* Reader has a knowledge about microcontroller hardware.

# Contact & Discussion
:e-mail: If you have anything you’d like to discuss or collaborate on, please feel free to contact me via:
* Email [Ho Thien Ai](mailto:thienaiho95@gmail.com)
* LinkedIn [Thien Ai Ho](https://www.linkedin.com/in/thien-ai-ho/)

:thumbsup: I'm always welcome your ideas and thank for your insteresting!

# Author
This page is published by Ho Thien Ai.
<p align="center">
  <a href="https://github.com/hothienai/" title="Sigma eLabs">
    <img src="/assets/images/sigma-elabs-banner.png" title="Sigma eLabs" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

# Back to Homepage
:house: [Back to Homepage](https://github.com/hothienai/embedded-c-fundamentals)

# Explore more
:point_right: [Explore more](https://github.com/hothienai)