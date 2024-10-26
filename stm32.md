# STM-32

## 1-1 配件介绍

### 01\. 课程简介

-   程序纯手打，手把手教学
-   STM32最小系统板+面包板硬件平台  
    ![在这里插入图片描述](pic_win/4946d58010095a5a139f776ad24fabb4.png)

> 该平台比较适合高校在校大学生学习STM32。

### 02\. 硬件设备

-   STM32最小系统+面包板
-   Windows10操作系统
-   万用表、示波器、镊子、剪刀等  
    ![在这里插入图片描述](pic_win/200140529c3efd897b83608766ec88c7.png)

### 03\. 软件工具

[Keil5](https://so.csdn.net/so/search?q=Keil5&spm=1001.2101.3001.7020) MDK  
![在这里插入图片描述](pic_win/7ac8a5b2225a07be1611883d3051c1d1.png)

### 04\. 硬件套件

![在这里插入图片描述](pic_win/a3fd25d8cde5d8ea263a5bc5a05d4615.png)

#### 4.1 面包板和跳线/飞线

![在这里插入图片描述](pic_win/989bf5c85d80bcc41a83ae9277420c60.png)

#### 4.2 杜邦线和STM32最小系统板

![在这里插入图片描述](pic_win/442d69e530a3d3563622e3e424daed7f.png)

#### 4.3 STLINK和OLED显示屏

![在这里插入图片描述](pic_win/48a2597b311ea190456e09b0167d795a.png)

#### 4.4 LED和按键

![在这里插入图片描述](pic_win/61f4ca6cde8e6331bc6b3d276319e99f.png)

#### 4.5 电位器和蜂鸣器

![在这里插入图片描述](pic_win/b6fd503a9648912f5c0f09150c9e8cce.png)

#### 4.6 传感器和旋转编码器

![在这里插入图片描述](pic_win/d325de6aa2f0244e9a9db9cd224620ec.png)

#### 4.7 USB转串口和MPU6050

![在这里插入图片描述](pic_win/ee79cebe3bd2acca61162f261d779ec3.png)

#### 4.8 Flash闪存和电机模块

![在这里插入图片描述](pic_win/ec953855b363bb9ee657509ca402bcd5.png)

#### 4.9 SG90舵机

![在这里插入图片描述](pic_win/3ed4e4e83bde299065d8b08b44a09ccc.png)

### 05\. 配件清单

![在这里插入图片描述](pic_win/d97734cd7ed675fe1d9d8ca136c95d12.png)

## 1-2 STM32简介

### 00\. 目录

#### 文章目录

-   -   [00\. 目录](https://blog.csdn.net/u010249597/article/details/134762381#00__0)
    -   [01\. STM32简介](https://blog.csdn.net/u010249597/article/details/134762381#01_STM32_3)
    -   -   [1.1 STM32是什么](https://blog.csdn.net/u010249597/article/details/134762381#11_STM32_11)
        -   [1.2 STM32应用领域](https://blog.csdn.net/u010249597/article/details/134762381#12_STM32_37)
        -   [1.3 STM32命名规则](https://blog.csdn.net/u010249597/article/details/134762381#13_STM32_52)
        -   [1.4 STM32选型](https://blog.csdn.net/u010249597/article/details/134762381#14_STM32_59)
    -   [02\. ARM简介](https://blog.csdn.net/u010249597/article/details/134762381#02_ARM_72)
    -   -   [2.1 ARM是什么](https://blog.csdn.net/u010249597/article/details/134762381#21_ARM_78)
        -   [2.2 ARM系列](https://blog.csdn.net/u010249597/article/details/134762381#22_ARM_86)
    -   [03\. STM32开发板](https://blog.csdn.net/u010249597/article/details/134762381#03_STM32_98)
    -   -   [3.1 MCU简介](https://blog.csdn.net/u010249597/article/details/134762381#31_MCU_100)
        -   [3.2 STM32开发板](https://blog.csdn.net/u010249597/article/details/134762381#32_STM32_117)
        -   [3.3 STM32硬件资源](https://blog.csdn.net/u010249597/article/details/134762381#33_STM32_126)
    -   [04\. STM32系统架构](https://blog.csdn.net/u010249597/article/details/134762381#04_STM32_133)
    -   [05\. STM32引脚定义](https://blog.csdn.net/u010249597/article/details/134762381#05_STM32_155)
    -   [06\. STM32启动配置](https://blog.csdn.net/u010249597/article/details/134762381#06_STM32_183)
    -   [07\. STM32最小系统电路](https://blog.csdn.net/u010249597/article/details/134762381#07_STM32_196)
    -   [08\. 附录](https://blog.csdn.net/u010249597/article/details/134762381#08__203)

### 01\. STM32简介

-   STM32是ST公司基于ARM Cortex-M内核开发的32位微控制器
-   STM32常应用在嵌入式领域，如智能车、无人机、机器人、无线通信、物联网、工业控制、娱乐电子产品等
-   STM32功能强大、性能优异、片上资源丰富、功耗低，是一款经典的嵌入式微控制器

#### 1.1 STM32是什么

STM32是一系列由ST Microelectronics（意法半导体公司）推出的微控制器(MCU)。这些微控制器基于ARM Cortex-M架构，并且提供各种不同的封装和引脚配置。STM32系列中一些受欢迎的微控制器包括STM32F103，STM32F407和STM32F429。 [STM32微控制器](https://so.csdn.net/so/search?q=STM32%E5%BE%AE%E6%8E%A7%E5%88%B6%E5%99%A8&spm=1001.2101.3001.7020)以其低功耗，高性能和广泛的功能而闻名。它们通常用于**物联网设备**，可穿戴技术和其他需要低功耗和高性能的应用。 总体而言，STM32微控制器是许多开发人员的首选，因为它们的多功能性，可靠性和广泛的功能。

> ST：指意法半导体  
> M：指定微处理器  
> 32：表示计算机处理器位数

【官方描述】

> STM32 is a family of microcontrollers from STMicroelectronics, a multinational semiconductor company. STM32 chips are used in a wide range of applications, from simple microcontroller-based projects to complex systems for industrial and automotive use. STM32 chips are based on the ARM Cortex-M architecture and are available in a variety of different packages and pin configurations. Some popular STM32 chips include the STM32F103, STM32F407, and STM32F429 microcontrollers. STM32 chips are known for their low power consumption, high performance, and wide range of features. They are often used in **IoT (Internet of Things)** devices, wearable technology, and other applications where low power consumption and high performance are critical. Overall, STM32 chips are a popular choice for many developers due to their versatility, reliability, and wide range of features.

【MCU】

> **MCU**：微控制器单元（MicroController Unit）：是把中央处理器、存储器、定时/计数器（timer/counter）、各种输入输出接口等都集成在一块集成电路芯片上的微型计算机。

#### 1.2 STM32应用领域

STM32的应用领域包括但不限于：

1.  嵌入式领域：如智能车、无人机、机器人、无线通信、物联网、工业控制、娱乐电子产品、医疗设备、智能家居等。
2.  高速数据采集系统：使用STM32连接高速ADC和FPGA芯片，实现对高速信号的采集和处理，例如高速摄像头、高速激光测距仪等。
3.  自动驾驶控制系统：使用STM32连接多个传感器和执行器，例如摄像头、雷达、电机、电子罗盘等，并通过算法设计和优化，实现自动驾驶控制功能。
4.  机器人视觉系统：使用STM32连接多个摄像头和处理模块，例如OpenCV、CUDA等，并通过算法设计和优化，实现机器人的视觉导航、物体识别等功能。
5.  网络安全嵌入式设备：使用STM32连接加密模块和网络模块，实现网络安全通信和数据加密等功能，例如VPN、防火墙、数据加密存储等。
6.  人工智能嵌入式设备：使用STM32连接AI模块，例如人脸识别、语音识别、自然语言处理等，并通过编程和训练，实现智能化的应用，例如智能门禁、智能家居等。

总的来说，STM32在各个领域都有广泛的应用。

#### 1.3 STM32命名规则

![在这里插入图片描述](pic_win/038c1494260015cf1c23e798d651e808.png)

#### 1.4 STM32选型

![在这里插入图片描述](pic_win/d2ffedfe17315c482c0ad7c89c883e10.png)

![在这里插入图片描述](pic_win/49541aa0b6f6eaf7778c3628eb975b02.png)

### 02\. ARM简介

-   ARM既指ARM公司，也指ARM处理器内核
-   ARM公司是全球领先的半导体知识产权（IP）提供商，全世界超过95%的智能手机和平板电脑都采用ARM架构
-   ARM公司设计ARM内核，半导体厂商完善内核周边电路并生产芯片

#### 2.1 ARM是什么

-   ARM既可以认为是一个**公司的名字** ，也可以认为是对**一类处理器的统称** ，还可以认为是**一种技术的名字** 。
-   ARM公司是专门从事基于**RISC技术芯片设计开发** 的公司，作为知识产权供应商，**本身不直接从事芯片生产，而是转让设计许可** ，由合作公司生产各具特色的芯片。
-   **ARM处理器的内核是统一的** ，由ARM公司提供，**而片内部件则是多样的** ，由各大半导体公司设计，这使得**ARM设计嵌入式系统的时候，可以基于同样的核心，使用不同的片内外设** ，从而具有很大的优势。

#### 2.2 ARM系列

![在这里插入图片描述](pic_win/74ab7edd2c06baaf75656736b30ee8b0.png)

![在这里插入图片描述](pic_win/0a45307c866abc2ba166c70c444cf10e.png)

### 03\. STM32开发板

#### 3.1 MCU简介

![在这里插入图片描述](pic_win/1da2a5626cb13f231f00ce12e71a4050.png)

**STM32F103C8T6**

-   系列：主流系列STM32F1
-   内核：ARM Cortex-M3
-   主频：72MHz
-   RAM：20K（SRAM）
-   ROM：64K（Flash）
-   供电：2.0~3.6V（标准3.3V）
-   封装：LQFP48

#### 3.2 STM32开发板

**STM32硬件**：STM32F103C8T6最小系统板

![在这里插入图片描述](pic_win/3e16ae0e01c6e673cb3bdf81c4bfeaa1.png)

#### 3.3 STM32硬件资源

![在这里插入图片描述](pic_win/5447606eddf76fb1619704963907ba78.png)

### 04\. STM32系统架构

在小容量、中容量和 大容量产品中，主系统由以下部分构成：  
● 四个驱动单元：  
─ Cortex™-M3内核DCode总线(D-bus)，和系统总线(S-bus)  
─ 通用DMA1和通用DMA2  
● 四个被动单元  
─ 内部SRAM  
─ 内部闪存存储器  
─ FSMC  
─ AHB到APB的桥(AHB2APBx)，它连接所有的APB设备

这些都是通过一个多级的AHB总线构架相互连接的，如下图所示：

![在这里插入图片描述](pic_win/947ab102f081d64efc39f8c5e14586bf.png)

### 05\. STM32引脚定义

引脚图

![在这里插入图片描述](pic_win/7d456b2b46bbaa867bb3d4dff9c34580.png)

**STM32F103C8T6引脚定义**  
![在这里插入图片描述](pic_win/48eb4b92f411d5839d9f6b00e1b6c755.png)

1.  I = 输入，O = 输出，S = 电源， HiZ = 高阻
2.  FT：容忍5V
3.  可以使用的功能依选定的型号而定。对于具有较少外设模块的型号，始终是包含较小编号的功能模块。例如，某个型号只有1个SPI和2个USART时，它们即是SPI1和USART1及USART2。
4.  PC13，PC14和PC15引脚通过电源开关进行供电，而这个电源开关只能够吸收有限的电流(3mA)。因此这三个引脚作为输出引脚时有以下限制：在同一时间只有一个引脚能作为输出，作为输出脚时只能工作在2MHz模式下，最大驱动负载为30pF，并且不能作为电流源(如驱动LED)。
5.  这些引脚在备份区域第一次上电时处于主功能状态下，之后即使复位，这些引脚的状态由备份区域寄存器控制（这些寄存器不会被主复位系统所复位）。 关于如何控制这些IO口的具体信息，请参考STM32F10xxx参考手册的电池备份区域和BKP寄存器的相关章节。
6.  与LQFP64的封装不同，在TFBGA64封装上没有PC3，但提供了V REF+ 引脚。
7.  此类复用功能能够由软件配置到其他引脚上(如果相应的封装型号有此引脚)，详细信息请参考STM32F10xxx参考手册的复用功能I/O章节和调试设置章节。
8.  VFQFPN36封装的引脚2和引脚3、LQFP48和LQFP64封装的引脚5和引脚6、和TFBGA64封装的C1和C2，在芯片复位后默认配置为OSC\_IN和OSC\_OUT功能脚。软件可以重新设置这两个引脚为PD0和PD1功能。但对于LQFP100/BGA100封装，由于PD0和PD1为固有的功能引脚，因此没有必要再由软件进行重映像设置。更多详细信息请参考STM32F10xxx参考手册的复用功能I/O章节和调试设置章节。在输出模式下，PD0和PD1只能配置为50MHz输出模式。

### 06\. STM32启动配置

在STM32F10xxx里，可以通过BOOT\[1:0\]引脚选择三种不同启动模式。

![在这里插入图片描述](pic_win/4e895ccf0e7016ac11c100cf783d652d.png)

### 07\. STM32最小系统电路

![在这里插入图片描述](pic_win/4cc636af1ccec901766ff1517e55127a.png)

### 08\. 附录

参考: [【STM32】江科大STM32学习笔记汇总](https://blog.csdn.net/u010249597/article/details/134762513)

## 2-1 软件安装

### 00\. 目录

#### 文章目录

-   -   [00\. 目录](https://blog.csdn.net/u010249597/article/details/134765079#00__0)
    -   [01\. MDK安装](https://blog.csdn.net/u010249597/article/details/134765079#01_MDK_3)
    -   [02\. Keil5注册](https://blog.csdn.net/u010249597/article/details/134765079#02_Keil5_83)
    -   [03\. 支持包安装](https://blog.csdn.net/u010249597/article/details/134765079#03___119)
    -   [04\. ST-LINK驱动安装](https://blog.csdn.net/u010249597/article/details/134765079#04_STLINK_137)
    -   [05\. USB转串口驱动](https://blog.csdn.net/u010249597/article/details/134765079#05_USB_179)
    -   [06\. 附录](https://blog.csdn.net/u010249597/article/details/134765079#06__201)

### 01\. MDK安装

MDK 源自德国的 KEIL 公司，是 RealView MDK 的简称。在全球 MDK 被超过 10 万的[嵌入式开发](https://so.csdn.net/so/search?q=%E5%B5%8C%E5%85%A5%E5%BC%8F%E5%BC%80%E5%8F%91&spm=1001.2101.3001.7020)工程师使用。目前最新版本为：

MDK6，该版本使用 uVision5 IDE 集成开发环境，是目前针对 ARM 处理器，尤其是 Cortex M 内核处理器的最佳开发工具。

[MDK5](https://so.csdn.net/so/search?q=MDK5&spm=1001.2101.3001.7020) 向后兼容 MDK4 和 MDK3 等，以前的项目同样可以在 MDK5 上进行开发(但是头文件方面得全部自己添加)， MDK5 同时加强了针

对 Cortex-M 微控制器开发的支持，并且对传统的开发模式和界面进行升级，MDK5 由两个部分组成：MDK Core 和 Software Packs。其

中，Software Packs 可以独立于工具链进行新芯片支持和中间库的升级。

1.1 双击MDK530.EXE文件，点击Next

![在这里插入图片描述](pic_win/ad81d083fafc3e863b4eee7fa61049a6.png)

1.2 接受许可协议，点击Next  
![在这里插入图片描述](pic_win/c92e97ea9b56906b5a371609460147ff.png)

1.3 选择软件安装路径，点击Next  
![在这里插入图片描述](pic_win/b0020a6d6483aaae06fc35b2eb1bdd70.png)

1.4 随便填写信息，然后点击Next  
![在这里插入图片描述](pic_win/4f717d7aba1cbc0c673bc1d28a8b2919.png)

1.5 安装过程中  
![在这里插入图片描述](pic_win/72397e5f23ca44516269fddc15754044.png)

1.6 选择安装

![在这里插入图片描述](pic_win/e6b8078410e60925be4a30d81d15287e.png)

1.7 点击Finish  
![在这里插入图片描述](pic_win/629e1fa7733ff724cca29be45e5d42a4.png)

1.8 全部点击右上角X关掉即可  
![在这里插入图片描述](pic_win/bd963a0058ec36863f528ad4a05c1856.png)

1.9 选择是  
![在这里插入图片描述](pic_win/52cddee0976594ff7cd71d764e3c75b3.png)

至此[Keil MDK](https://so.csdn.net/so/search?q=Keil%20MDK&spm=1001.2101.3001.7020)\-ARM就安装完成，可以新建工程使用了。但为了不受编译代码4K大小限制和用户体验，就需要购买授权，或注册。

### 02\. Keil5注册

2.1 以管理员的方式运行keil软件  
![在这里插入图片描述](pic_win/89f7a4af21717639691f6721b1a8cf3e.png)

2.2 选择否即可  
![在这里插入图片描述](pic_win/99e52f1babb87917d526dcdf9fa7b3a5.png)

2.3 打开注册管理窗口（File -> License Management），并复制CID。  
![在这里插入图片描述](pic_win/32f5856e5a4e6613527a5c86e7af3cac.png)

2.4 打开注册机，执行如下几步。  
![在这里插入图片描述](pic_win/85070fda0930cde54619c8c133a4e240.png)

2.5 将注册码添加到注册窗口中  
![在这里插入图片描述](pic_win/6ca93c20fe4b214f91cfc98be96ca0aa.png)

### 03\. 支持包安装

3.1 双击Keil.STM32F1xx\_DFP.2.2.0.pack  
![在这里插入图片描述](pic_win/f6cfd30dea4908a5061e71c522226092.png)

3.2 选择Finishu，完成安装  
![在这里插入图片描述](pic_win/9329c100607a16c83cf79c04c446984a.png)

### 04\. ST-LINK驱动安装

4.1 默认STM32 STLink是没有驱动的，需要安装驱动  
![在这里插入图片描述](pic_win/3b57997c2827c9eb0c31ed9ceefd82b8.png)

4.2 找到Keil安装目录下，安装64位驱动

> D:\\Keil\_v5\\ARM\\STLink\\USBDriver  
> ![在这里插入图片描述](pic_win/653ea87d709825f06305d9e27dd0cd2e.png)

4.3 选择下一页

![在这里插入图片描述](pic_win/d8f80828689926236a164876e34f7e04.png)

4.4 点击完成即可  
![在这里插入图片描述](pic_win/52fe50b015591dedb0a578011aab4ce0.png)

4.5 驱动安装好之后，黄色感叹号消失，表示安装成功

![在这里插入图片描述](pic_win/37bdbef435b71c8c93349bf40ed977d5.png)

### 05\. USB转串口驱动

5.1 双击CH341SER.EXE，点击安装

![在这里插入图片描述](pic_win/6606b2cd79b1693fb804b377c8ec31a7.png)

5.2 点击确定

![在这里插入图片描述](pic_win/fab2c4fdd9ea653637a087cacef92b2f.png)

5.3 安装好驱动之后，通过设备管理器查看如下图所示

![在这里插入图片描述](pic_win/4bfc23825d5f02956e97584c06568968.png)

### 06\. 附录

参考: [【STM32】江科大STM32学习笔记汇总](https://blog.csdn.net/u010249597/article/details/134762513)

## 2-2  创建工程

### **新建工程**

桌面新建存放STM32项目的文件夹：STM32Project

打开keil5,project,new uVersion Project，新建文件夹  2-2 STM32工程模板，其中新建工程文件Project，保存

选择芯片STM-STM32F1-STM32F103-STM32F103C8。OK，关闭弹出窗口

### **移植固件**

**启动文件**

```python
STM32F10x_StdPeriph_Lib_V3.5.0\Libraries\CMSIS\CM3\DeviceSupport\ST\STM32F10x\startup\arm
```

全选复制启动文件，在2-2 STM32工程模板中新建 Start 文件夹，放入 Start 文件夹

**外设寄存器描述文件、时钟文件**

```python
STM32F10x_StdPeriph_Lib_V3.5.0\Libraries\CMSIS\CM3\DeviceSupport\ST\STM32F10x
stm32f10x.h
system_stm32f10x.c
system_stm32f10x.h
```

复制上面三个文件，放入 Start  文件夹

**内核寄存器描述文件**

```python
STM32F10x_StdPeriph_Lib_V3.5.0\Libraries\CMSIS\CM3\CoreSupport
```

复制两个文件，放入 Start  文件夹

**keil5 添加start文件到工程**

![image-20241002003819446](pic_win/image-20241002003819446.png)

<img src="pic_win/image-20241002004322166.png" alt="image-20241002004322166"  />

![image-20241002004510536](pic_win/image-20241002004510536.png)

**添加头文件路径**

![image-20241002004828587](pic_win/image-20241002004828587.png)



**主文件**

2-2 STM32工程模板  文件夹中，新建 User 文件夹

![image-20241002005321368](pic_win/image-20241002005321368.png)

![image-20241002005437654](pic_win/image-20241002005437654.png)

![image-20241002005711568](pic_win/image-20241002005711568.png)

![image-20241002005536979](pic_win/image-20241002005536979.png)

![image-20241002005807183](pic_win/image-20241002005807183.png)

**调试器配置**

![image-20241002010140819](pic_win/image-20241002010140819.png)

![image-20241002010245989](pic_win/image-20241002010245989.png)

**基于库函数编程**

2-2 STM32工程模板  文件夹中，新建 Library 文件夹，复制下列文件到 Library 文件夹

```python
STM32F10x_StdPeriph_Lib_V3.5.0\Libraries\STM32F10x_StdPeriph_Driver\src
STM32F10x_StdPeriph_Lib_V3.5.0\Libraries\STM32F10x_StdPeriph_Driver\inc
```

后放入keil5的工程中

![image-20241002010959154](pic_win/image-20241002010959154.png)

**User中放入 头文件配置文件 与 中断文件**

```
STM32F10x_StdPeriph_Lib_V3.5.0\Project\STM32F10x_StdPeriph_Template
stm32f10x_conf.h
stm32f10x_it.c
stm32f10x_it.h
```

keil5工程中添加以上文件

![image-20241002011700959](pic_win/image-20241002011700959.png)

**设置宏定义**

![image-20241002011919516](pic_win/image-20241002011919516.png)

![image-20241002012046463](pic_win/image-20241002012046463.png)

![image-20241002012249548](pic_win/image-20241002012249548.png)

## 2-3 工程编译与下载

main.c

```c
#include "stm32f10x.h"                  // Device header
int main(void)
{
	//点亮PC13端口上的灯
	/*
	PC13由端口GPIOC端口控制，（GPIOC端口管理16个引脚：PC0~PC15）
	首先启动GPIOC时钟，调用RCC_APB2PeriphClockCmd（）函数
	RCC：（Reset and Clock Control）复位与时钟控制
	APB2：GPIOC由这条总线控制
	PeriphClockCmd：使能或禁用外围设备的时钟
	*/
	//周边时钟控制，参数：（外设，状态）
	RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOC, ENABLE);
	//配置端口模式
	GPIO_InitTypeDef GPIO_InitStructure;
	GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP;//通用推挽输出
	GPIO_InitStructure.GPIO_Pin = GPIO_Pin_13;
	GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;
	GPIO_Init(GPIOC, &GPIO_InitStructure);
	GPIO_SetBits(GPIOC, GPIO_Pin_13);//高电平
	//GPIO_ResetBits(GPIOC, GPIO_Pin_13);//低电平
	while(1)
	{
		
	}
}	
```

![在这里插入图片描述](pic_win/8c38bc24ad78900babf91ce8e2993e5d.png)

### 启动文件型号分类 根据 芯片缩写 选择

![在这里插入图片描述](pic_win/0d0508a1c010272eb314dcc7ed608832.png)

```
STM32F10x_StdPeriph_Lib_V3.5.0\Libraries\CMSIS\CM3\DeviceSupport\ST\STM32F10x\startup\arm
```

![image-20241002013552235](pic_win/image-20241002013552235.png)

### 工程结构

![在这里插入图片描述](pic_win/ab20ea0bee67465be40bb2505fc479cb.png)

**startup文件**

程序执行最基本的文件，复位中断函数：板子上电或复位按钮按下时，进入中断，先进行系统初始化，然后调用main函数

SystemInit函数定义在system_xx.c / .h

另外定义了其他中断，定义在stm32f10x_it.c / .h，达到触发条件后，自动执行

## 3-1GPIO输出

### 01\. [GPIO](https://so.csdn.net/so/search?q=GPIO&spm=1001.2101.3001.7020)简介

-   GPIO（General Purpose Input Output）通用输入输出口
-   可配置为8种输入输出模式
-   引脚电平：0V~3.3V，部分引脚可容忍5V
-   输出模式下可控制端口输出高低电平，用以驱动LED、控制蜂鸣器、模拟通信协议输出时序等
-   输入模式下可读取端口的高低电平或电压，用于读取按键输入、外接模块电平信号输入、ADC电压采集、模拟通信协议接收数据等

每个GPI/O端口有两个32位配置[寄存器](https://so.csdn.net/so/search?q=%E5%AF%84%E5%AD%98%E5%99%A8&spm=1001.2101.3001.7020)(GPIOx\_CRL，GPIOx\_CRH)，两个32位数据寄存器(GPIOx\_IDR和GPIOx\_ODR)，一个32位置位/复位寄存器(GPIOx\_BSRR)，一个16位复位寄存器(GPIOx\_BRR)和一个32位锁定寄存器(GPIOx\_LCKR)。  
根据[数据手册](https://so.csdn.net/so/search?q=%E6%95%B0%E6%8D%AE%E6%89%8B%E5%86%8C&spm=1001.2101.3001.7020)中列出的每个I/O端口的特定硬件特征， GPIO端口的每个位可以由软件分别配置成多种模式。

-   输入浮空
    
-   输入上拉
    
-   输入下拉
    
-   模拟输入
    
-   开漏输出
    
-   推挽式输出
    
-   推挽式复用功能
    
-   开漏复用功能
    

每个I/O端口位可以自由编程，然而I/0端口寄存器必须按32位字被访问(不允许半字或字节访问)。GPIOx\_BSRR和GPIOx\_BRR寄存器允许对任何GPIO寄存器的读/更改的独立访问；这样，在读和更改访问之间产生IRQ时不会发生危险。

### 02\. GPIO基本结构

**系统结构**

![在这里插入图片描述](pic_win/a978ec4384968fcc13a0bd346a455517.png)

**基本结构**

![在这里插入图片描述](pic_win/00644485e80be3c6e5599bd0816bbe1b.png)

### 03\. GPIO位结构

I/O端口位的基本结构

![在这里插入图片描述](pic_win/5f3342e4f0cda9c60a3cd49d9693c8a1.png)

5伏兼容I/O端口位的基本结构

![在这里插入图片描述](pic_win/e36e8ae034f18266b2fcfd220b4d0c08.png)

### 04\. GPIO模式

通过配置GPIO的端口配置寄存器，端口可以配置成以下8种模式

![在这里插入图片描述](pic_win/d27eda5b025a21132cf6806c52b7a075.png)

**4种输入模式**：

-   输入浮空
-   输入上拉
-   输入下拉
-   模拟输入

**4种输出模式**：

-   开漏输出
-   开漏复用功能
-   推挽式输出
-   推挽式复用功能

**3种最大翻转速度**:

-   最大输出速度为2MHz
-   最大输出速度为10MHz
-   最大输出速度为50MHz

#### 4.1 输入浮空

输入高为高，输入低为低，无输入漂浮不定。

浮空输入模式下，I/O端口的电平信号直接进入输入数据寄存器。也就是说，I/O的电平状态是不确定的，==完全由外部输入决定==；如果在该引脚悬空（在无信号输入）的情况下，读取该端口的电平是不确定的。所以在要读取外部信号时通常配置IO口为浮空输入模式。  
![在这里插入图片描述](pic_win/842f489dfbc2f43b177cb708f95c6641.png)

#### 4.2 输入上拉

**输入高为高，输入低为低，无输入拉高**

上拉输入模式下，I/O端口的电平信号直接进入输入数据寄存器。但是在==I/O端口悬空==（在无信号输入）的情况下，输入端的电平可以保持在==高电平==；并且在==I/O端口输入为低电平==的时候，输入端的电平为==低电平==。

![在这里插入图片描述](pic_win/9b79d9ed02de3ef235530781c3269e7d.png)

#### 4.3 输入下拉

**输入高为高，输入低为低，无输入拉低**

下拉输入模式下，IO口工作方式刚好和上拉模式相反。I/O端口的电平信号直接进入输入数据寄存器。但是在I/O端口悬空（在无信号输入）的情况下，输入端的电平可以保持在低电平；并且在I/O端口输入为高电平的时候，输入端为高电平。  
![在这里插入图片描述](pic_win/fc4d500bf2a23796aed1300e9c9cede8.png)

#### 4.4 模拟输入

模拟输入模式下，I/O端口的模拟信号（电压信号，而非电平信号）==直接模拟输入到片上外设模块==，比如ADC模块等等。

![在这里插入图片描述](pic_win/c15b2cc5924fc89081ee5fee82aaa1b0.png)

#### 4.5 开漏输出

p-mos不起作用，输入1时，n-mos关闭，io电平不由单片机控制，由外部电路控制；输入0时，n-mos开启，io电平为低电平

开漏输出模式下，通过设置位设置/清除寄存器或者输出数据寄存器的值，控制MOS管的导通。这里要注意N-MOS管，当设置输出的值为1的时候，N-MOS管处于关闭状态，此时I/O端口的电平就不会由输出的高低电平决定，而是由I/O端口外部的上拉或者下拉决定；当设置输出的值为0的时候，N-MOS管处于开启状态，此时I/O端口的电平就是低电平。同时，I/O端口的电平也可以通过输入电路进行读取；注意，I/O端口的电平不一定是输出的电平。通常使用开漏输出时外部要加一个上拉电阻。

![在这里插入图片描述](pic_win/5559d3d7e3ee28371188625a8e35f049.png)

#### 4.6 开漏复用功能

开漏复用输出模式，与开漏输出模式很是类似。只是输出的高低电平的来源，不是让CPU直接写输出数据寄存器，取而代之利用片上外设模块的复用功能输出来决定的。

![在这里插入图片描述](pic_win/7aa6065992f60ed389324720f255c49e.png)

#### 4.7 推挽式输出

推挽输出模式下，通过设置位设置/清除寄存器或者输出数据寄存器的值，控制P-MOS管和N-MOS管的导通来控制IO口输出高电平还是低电平。这里要注意P-MOS管和N-MOS管，当==设置输出的值为1==的时候，P-MOS管处于开启状态，N-MOS管处于关闭状态，此时==I/O端口==的电平就由P-MOS管决定为==高电平==；当==设置输出的值为0==的时候，P-MOS管处于关闭状态，N-MOS管处于开启状态，此时==I/O端口==的电平就由N-MOS管决定为==低电平==。同时，I/O端口的电平也可以通过输入电路进行读取；注意，此时I/O端口的电平一定是输出的电平。

![在这里插入图片描述](pic_win/4d569868750a0a670ae8bb946b35eb88.png)

#### 4.8 推挽式复用功能

推挽复用输出模式，与推挽输出模式很是类似。只是输出的高低电平的来源，不是让CPU直接写输出数据寄存器，取而代之利用片上外设模块的复用功能输出来决定的。

![在这里插入图片描述](pic_win/0a2032eecbc2170f4a65260bf7701d3a.png)

### 05\. LED和蜂鸣器简介

-   LED：发光二极管，正向通电点亮，反向通电不亮
-   有源蜂鸣器：内部自带振荡源，将正负极接上直流电压即可持续发声，频率固定
-   无源蜂鸣器：内部不带振荡源，需要控制器提供振荡脉冲才可发声，调整提供振荡脉冲的频率，可发出不同频率的声音  
    ![在这里插入图片描述](pic_win/53f4c7fc41af714b310e6d04c9ab187e.png)

硬件电路  
![在这里插入图片描述](pic_win/67450d6930a169812e22bd45f7697f08.png)

### 06\. 面包板

![在这里插入图片描述](pic_win/3eafba810dc2aacbe91c6ab7b9060636.png)

面包板描述

![在这里插入图片描述](pic_win/eff853b4a809052ab2bcc33d0f664fc2.png)

面包板使用示例

![在这里插入图片描述](pic_win/8452503b16acd4f4b3649f41314b6d8d.png)

![在这里插入图片描述](pic_win/23e5cbafdd27657e58e8ee1ef0c2032a.png)

### 07\. 附录

参考: [【STM32】江科大STM32学习笔记汇总](https://blog.csdn.net/u010249597/article/details/134762513)