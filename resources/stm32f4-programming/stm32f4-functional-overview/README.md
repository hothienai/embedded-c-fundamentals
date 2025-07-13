# STM32F40xxx Functional Overview
<p align="center">
  <a href="." title="STM32F40xxx Functional Overview">
    <img src="/resources/stm32f4-programming/stm32f4-functional-overview/images/STM32F40xxx_Functional_Overview.png" title="STM32F40xxx Functional Overview" style="min-width: 200px"/>
  </a>
</p>

:dart: Hello everyone, in this article, I would like to share you an overview of STM32F40xxx functionalities. To be honest, I do not work with all the functionalities it has, but I will try explain them based on my understand and research. 

:triangular_flag_on_post: The motivation here is when you are working with a specific microcontroller or plan to select it for your embedded system, you should know a big picture about the features it supports. By knowing that, you can wisely select it and wisely use it to develop your embedded system.

# Table of contents
:books: This article will cover the below topics:
| Chapter     | Description                                                 |
| :--------   | :-------                                                    |
| 1           | [# STM32F40xxx Block Diagram](#stm32f40xxx-block-diagram)   |

Reference documents I use in this article are provided by [ST Company](https://www.st.com/content/st_com/en.html). You can find here:
* [STM32F405xx STM32F407xx Datasheet](https://www.st.com/resource/en/datasheet/dm00037051.pdf)
* [RM0090 Reference Manual](https://www.st.com/resource/en/reference_manual/dm00031020-stm32f405-415-stm32f407-417-stm32f427-437-and-stm32f429-439-advanced-arm-based-32-bit-mcus-stmicroelectronics.pdf)

# STM32F40xxx Block Diagram
<p align="center">
  <a href="." title="STM32F40xxx Block Diagram">
    <img src="/resources/stm32f4-programming/stm32f4-functional-overview/images/STM32F40xxx_block_diagram.PNG" title="STM32F40xxx Block Diagram" style="min-width: 200px"/>
  </a>
</p>

:mag_right: By looking into this block diagram, what are the insides you can find? I hope that you can find some very common components as below:
* Arm Cortex-M4 and internal peripherals (NVIC, MPU, FPU)
* Memory related components: Flash, SRAM, External Memory Controller
* Gneral Purpose IO Ports
* Analog-to-Digital Converters and Digital-to-Analog Coverters
* Timers and Watch Dog components
* Communication related components: USARTs, SPIs, I2Cs, CANs...
* Direct Memory Access components
* Internal Busess: AHB1, AHB2, AHB3, APB1, APB2
* And other components

:mag_right: Every component reposibles for a specific functions in microcontroller. It is depend on the embedded system you develop, some components can be used and some are not.

:mag_right: I am sorry that I could not go in details about each component in this article because there are a lot of thing I have to study and explain to you. Additionally, in the reference documents, ST has documented very detailed about the functionality of the STM32F40xxx, you can go and find out.

:mag_right: I promise you to write another article with more detailed about one component with the practical demostrantion.

# Contact & Discussion
:e-mail: If you have anything you’d like to discuss or collaborate on, please feel free to contact me via:
* Email [Ho Thien Ai](mailto:thienaiho95@gmail.com)
* LinkedIn [Thien Ai Ho](https://www.linkedin.com/in/thien-ai-ho/)

:thumbsup: I always welcome your ideas and appreciate your interest!

# Author
This article is published by Ho Thien Ai.
<p align="center">
  <a href="https://github.com/hothienai/" title="Sigma eLabs">
    <img src="/assets/images/sigma-elabs-banner.png" title="Sigma eLabs" style="min-width: 200px"/>
  </a>
</p>

# Back to Homepage
:house: [Back to Homepage](https://github.com/hothienai/embedded-c-fundamentals)

# Explore more
:point_right: [Explore more](https://github.com/hothienai)