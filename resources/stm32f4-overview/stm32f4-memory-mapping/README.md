# STM32F4 Memory Mapping
<p align="center">
  <a href="." title="STM32F4 Memory Mapping">
    <img src="/resources/stm32f4-overview/stm32f4-memory-mapping/images/mem_map_cover.png" title="STM32F4 Memory Mapping" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

:dart: Hello everyone! In this article, I will introduce some important memory blocks within a microcontroller. Understanding the location and purpose of each memory block will help you become a more skilled engineer — enabling you to quickly adapt to new projects, efficiently debug software, and develop robust applications.

:question: What motivated me to write this article? These points are based on my own experiences in both work and interviews. Can you answer the following questions?
* What are the sizes of RAM and ROM in the microcontroller? Does it have enough resources for your embedded software?
* Where are different types of variables stored in the program?
* Where are the program code and non-volatile data located?
* How do you configure a peripheral to perform a specific function?
* If a program crashes, is it accessing memory locations it shouldn't?
* Could the microcontroller be running out of resources during operation, causing critical issues?
* For safety-critical software, can we implement mechanisms to protect memory from unauthorized access?

# Table of contents
:books: This article will cover the below topics:
| Chapter    | Description |
| :-------- | :------- |
| 1 | [STM32F40xxx memory map](#stm32f40xxx-memory-map) |
| 2 | [512-Mbyte Block 0 - Code](#512-mbyte-block-0---code) |
| 3 | [512-Mbyte Block 1 - SRAM](#512-mbyte-block-1---sram) |
| 4 | [512-Mbyte Block 2 - Peripherals](#512-mbyte-block-2---peripherals) |
| 5 | [512-Mbyte Block 3 - FSMC Bank 1 & Bank 2](#512-mbyte-block-3---fsmc-bank-1--bank-2) |
| 6 | [512-Mbyte Block 5 - FSMC Registers](#512-mbyte-block-5---fsmc-registers) |
| 7 | [512-Mbyte Block 6 - Not used](#512-mbyte-block-6---not-used) |
| 8 | [512-Mbyte Block 7 - Cortex-M4's Internal Peripherals](#512-mbyte-block-7---cortex-m4s-internal-peripherals) |
| 9 | [Register boundary addresses](#register-boundary-addresses) |

Reference documents I use in this article are provided by ST. You can find here:
* [STM32F405xx STM32F407xx Datasheet](https://www.st.com/resource/en/datasheet/dm00037051.pdf)
* [RM0090 Reference Manual](https://www.st.com/resource/en/reference_manual/dm00031020-stm32f405-415-stm32f407-417-stm32f427-437-and-stm32f429-439-advanced-arm-based-32-bit-mcus-stmicroelectronics.pdf)

# STM32F40xxx memory map
:mag_right: STM32F40xxx is a 32-bit microcontroller with a 32-bit address space ranging from 0x0000 0000 to 0xFFFF FFFF. This address space is structured and segmented into blocks, each serving a specific function. The following figure illustrates the memory map of the STM32F40xxx.
<p align="center">
  <a href="." title="STM32F40xxx memory map">
    <img src="/resources/stm32f4-overview/stm32f4-memory-mapping/images/STM32F40xxx_memmap.PNG" title="STM32F40xxx memory map" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

:rocket: Now, let's explore each of the 8 main memory blocks and their specific functions in detail. Note that some of these blocks are further divided into sub-blocks to serve different purposes.
# 512-Mbyte Block 0 - Code
<p align="center">
  <a href="." title="Code">
    <img src="/resources/stm32f4-overview/stm32f4-memory-mapping/images/Block0.png" title="Code" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

:point_right: When you flash the software, it is stored in this block (commonly referred to as code flash). Additionally, data that needs to be retained after uC power-off can also be stored here (known as data flash).
| Start Address    | End Address |
| :-------- | :------- |
| 0x0000 0000 | 0x1FFF FFFF |

# 512-Mbyte Block 1 - SRAM
<p align="center">
  <a href="." title="SRAM">
    <img src="/resources/stm32f4-overview/stm32f4-memory-mapping/images/Block1.png" title="SRAM" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

:point_right: This block is used during program execution. The call stack, heap, and variables are allocated and initialized in this memory region.
| Start Address    | End Address |
| :-------- | :------- |
| 0x2000 0000 | 0x3FFF FFFF |

# 512-Mbyte Block 2 - Peripherals
<p align="center">
  <a href="." title="Peripherals">
    <img src="/resources/stm32f4-overview/stm32f4-memory-mapping/images/Block2.png" title="Peripherals" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

:point_right: Peripheral-related registers reside in this block. Both functional and data registers can be configured, read, or written by accessing their addresses within this memory region.
| Start Address    | End Address |
| :-------- | :------- |
| 0x4000 0000 | 0x5FFF FFFF |

# 512-Mbyte Block 3 & 4 - FSMC Banks
<p align="center">
  <a href="." title="FSMC Banks">
    <img src="/resources/stm32f4-overview/stm32f4-memory-mapping/images/Block34.png" title="FSMC Banks" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

:point_right: This address region is intended for interfacing with external memory devices that interface with the controller through shared address, data, and control signals, including:
* Static random access memory (SRAM)
* NOR/OneNAND flash memory
* PSRAM (4 memory banks)

| Block             | Start Address     | End Address     |
| :--------         | :--------         | :-------        |
| 3                 | 0x6000 0000       | 0x7FFF FFFF     |
| 4                 | 0x8000 0000       | 0x9FFF FFFF     |

# 512-Mbyte Block 5 - FSMC Registers
<p align="center">
  <a href="." title="FSMC Registers">
    <img src="/resources/stm32f4-overview/stm32f4-memory-mapping/images/Block5.png" title="FSMC Registers" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

:point_right: This address region is reserved for FSMC registers, which are used to define the type of external device and its associated characteristics.
| Start Address     | End Address     |
| :--------         | :-------        |
| 0xA000 0000       | 0xBFFF FFFF     |

# 512-Mbyte Block 6 - Not used
:point_right: This block is not used.
| Start Address     | End Address     |
| :--------         | :-------        |
| 0xC000 0000       | 0xDFFF FFFF     |

# 512-Mbyte Block 7 - Cortex-M4's Internal Peripherals
<p align="center">
  <a href="." title="Cortex-M4's Internal Peripherals">
    <img src="/resources/stm32f4-overview/stm32f4-memory-mapping/images/Block7.png" title="Cortex-M4's Internal Peripherals" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

:point_right: This block is reserved for internal controller peripherals, including:
* Nested Vectored Interrupt Controller (NVIC)
* Memory Protection Unit (MPU)
* System Timer (SysTick)
* Floating-Point Unit (FPU)

| Start Address     | End Address     |
| :--------         | :-------        |
| 0xE000 0000       | 0xFFFF FFFF     |

# Register boundary addresses
:point_right: In the ARM Cortex-M architecture, there are multiple address buses, each designed to access different peripherals. When accessing a peripheral, ensure you are using the correct bus. Refer to the Register boundary addresses table for more details.

<p align="center">
  <a href="." title="Register boundary addresses">
    <img src="/resources/stm32f4-overview/stm32f4-memory-mapping/images/address_bus1.png" title="Register boundary addresses" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

<p align="center">
  <a href="." title="Register boundary addresses">
    <img src="/resources/stm32f4-overview/stm32f4-memory-mapping/images/address_bus2.png" title="Register boundary addresses" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

<p align="center">
  <a href="." title="Register boundary addresses">
    <img src="/resources/stm32f4-overview/stm32f4-memory-mapping/images/address_bus3.png" title="Register boundary addresses" style="width: 100vw; min-width: 200px"/>
  </a>
</p>


# Contact & Discussion
:e-mail: If you have anything you’d like to discuss or collaborate on, please feel free to contact me via:
* Email [Ho Thien Ai](mailto:thienaiho95@gmail.com)
* LinkedIn [Thien Ai Ho](https://www.linkedin.com/in/thien-ai-ho/)

:thumbsup: I always welcome your ideas and appreciate your interest!
# Buy me a coffee
If you find these topics helpful, you can support me by buying a coffee :coffee: using the button below :point_down:. Your support motivates me to create more valuable content. Thank you! :pray:
<p align="center">
  <a href="https://github.com/hothienai/donate-me-a-coffee" title="Buy me a coffee">
    <img src="/assets/images/buy-me-a-coffee.png" title="Buy me a coffee" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

# Author
This page is authorized by Ho Thien Ai.
<p align="center">
  <a href="https://github.com/hothienai/" title="Sigma eLabs">
    <img src="/assets/images/sigma-elabs-banner.png" title="Sigma eLabs" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

# Back to Homepage
:house: [Back to Homepage](https://github.com/hothienai/embedded-c-fundamentals)

# Explore more
:point_right: [Explore more](https://github.com/hothienai)