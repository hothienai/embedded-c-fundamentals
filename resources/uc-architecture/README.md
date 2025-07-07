# Microcontroller Architecture
<p align="center">
  <a href="." title="Microcontroller Architecture">
    <img src="/resources/uc-architecture/images/uc_architecture.png" title="Microcontroller Architecture" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

:dart: In this post, I let you the basic components of microcontroller architecture design.

# Table of contents
:books: This post will cover the below topics:
| Chapter    | Description |
| :-------- | :------- |
| 1 | [Microcontroller Architecture Overview](#microcontroller-architecture-overview) |
| 2 | [Central Processing Unit (CPU)](#central-processing-unit-cpu) |
| 3 | [Interrupt Control](#interrupt-control) |
| 4 | [Memory Units](#memory-units) |
| 5 | [I/O Ports](#io-ports) |
| 6 | [Communication Port](#communication-port) |
| 7 | [Other components](#other-components) |

# Microcontroller Architecture Overview
Nowadays, there is a interesting thing is every thing will follow an standards. And the microcontroller architecture is not an exception. They are designed based on some architecture patterns like Harvard Architecture or Von Neumann Architecture.

Here, I won't go into details about of these 2 architectures. I will go straight forward to the very common used architecture in morden embedded world, that is Von Neumann Architecture.

So, what is exactly it looked like? In a simple form, you can see it as below:
<p align="center">
  <a href="." title="8051 Microcontroller Architecture">
    <img src="/resources/uc-architecture/images/8051_architecture.jpg" title="8051 Microcontroller Architecture" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

* Source: [www.tutorialspoint.com](https://www.tutorialspoint.com/microprocessor/microcontrollers_8051_architecture.htm)
Take a look on that you can see, there are serval components:
* Central Processing Unit (CPU)
* Interrupt Control
* Memory Unit (ROM, RAM)
* I/O Ports
* Timers
* Serial Port

So, what is the functionality of these components in the microcontroller?
# Central Processing Unit (CPU)
<p align="center">
  <a href="." title="Central Processing Unit">
    <img src="/resources/uc-architecture/images/8051_architecture_cpu.jpg" title="Central Processing Unit" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

It is the most important component and plays as a "brain" of the microcontroller. It receives the input as the information from the internal or external environment, performs calculation and provide the output back to internal or external environment.

The CPU interacts with other components, example: Interupt Control, Timers, Memory Units, to collect the information and processes these information following the programmable logic and then provide the output to other compoments.

# Interrupt Control
<p align="center">
  <a href="." title="Interrupt Control">
    <img src="/resources/uc-architecture/images/8051_architecture_interrupt.jpg" title="Interrupt Control" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

This compoment handles all internal/external interruption events. In case an event happenned, this component will notify and guilde the CPU to stop the current calculation and perform another calculation for it.

# Memory Units
<p align="center">
  <a href="." title="Memory Units">
    <img src="/resources/uc-architecture/images/8051_architecture_memory.jpg" title="Memory Units" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

## ROM
This a permanent memory to store the program code. What is the program code? It actually the program written by software developer to instruct how the microcontroller should do. This program is complied to the code that can be flashed to ROM.

The CPU will read out this code and performs the logic as the requirements of the software developer.

## RAM
This the temporary memory helps to store the temporary information (like variables, call-stack) when the program is running. All information in RAM will be lost after the power is cut off.

# I/O Ports
<p align="center">
  <a href="." title="IO Ports">
    <img src="/resources/uc-architecture/images/8051_architecture_io.jpg" title="IO Ports" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

Input Ports support the microcontroller to read the information from the external environment by converting them in to electric signals.

In the other hand, Output Ports support the microtroller to control the external objects by sending out the electric signals.

# Communication Port
<p align="center">
  <a href="." title="Communication Port">
    <img src="/resources/uc-architecture/images/8051_architecture_com.jpg" title="Communication Port" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

This component supports the microtroller to communicate with other devices and exchange the information between them.

# Other Components
In the morden and complex microcontroller architecture, there are a lot of components which are not mentioned here. You can go and explore them by yourself.

# Outcomes
I hope that now you already have an overview of microcontroller architecture:
* You know what the important components inside of it.
* You're know where is the first place you can start with a very new microcontroller.
* After you have a overview, then you can continue to investigate more detailed parts.

# Contact & Discussion
:e-mail: If you have any thing would like to discuss or cooperate with me, please don't hesitate to contact me via:
* Email [Ho Thien Ai](mailto:thienaiho95@gmail.com)
* LinkedIn [Thien Ai Ho](https://www.linkedin.com/in/thien-ai-ho/).

:thumbsup: I'm always welcome your ideas and thank for your insteresting!
# Buy me a coffee
If you see the topics are useful, you can support me a coffee :coffee: by clicking the button below :point_down:. It will be a big motivation for me to bring more wonderful topics. Thank you! :pray:
<p align="center">
  <a href="https://github.com/HoThienAi/donate-me-a-coffee" title="Buy me a coffee">
    <img src="/assets/images/buy-me-a-coffee.png" title="Buy me a coffee" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

# Authors
This page is authorized by Ho Thien Ai.
<p align="center">
  <a href="https://github.com/HoThienAi/" title="Sigma eLabs">
    <img src="/assets/images/sigma-elabs-banner.png" title="Sigma eLabs" style="width: 100vw; min-width: 200px"/>
  </a>
</p>

# Back to Homepage
:house: [Back to Homepage](https://github.com/HoThienAi/embedded-c-fundamentals)

# Explore more
:point_right: [Explore more](https://github.com/HoThienAi)