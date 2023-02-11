本文档整理了龙芯平台嵌入式和教学OS资料，更多龙芯平台OS或软件发行动态见[社区](https://preview.loongarch.dev/33/zh-cn/posts/2022year/)。

# mit xv6-实验和参考书(开发中)

xv6是MIT在2006年开发的一个类Unix教学操作系统，与Linux或BSD不同，xv6非常简单，足以在一个学期内讲完，但仍包含Unix的重要概念和组织结构。

**开发者：** 罗老师

**仓库地址：** https://github.com/skt-cpuos/xv6-loongarch-exp

**主要特性：**

* 基于v2.0 ABI的新世界系统
* 仓库含OS代码、实验代码、实验指导书和PPT演示资料
* 实验的具体实现，参考邓老师的[仓库](https://github.com/Fan33oo/xv6-labs-loongarch)

# mit xv6-参考实现(开发中)

本项目是罗老师[基于LoongArch构建xv6实验](https://github.com/skt-cpuos/xv6-loongarch-exp)的参考实现。

**实现者：** 邓老师

**仓库地址：** https://github.com/Fan33oo/xv6-labs-loongarch

**主要特性：**

* 完成utils，syscall，pgtbl，trap，cow，thread，mmap实验
* net实验，pci设备支持，有待完善
* lock实验，龙芯qemu还不支持多核
* fs实验，龙芯qemu内存限制，有待完善

# uCore(维护中)

uCore OS Labs是用于清华大学计算机系本科操作系统课程的教学试验内容。本项目基于[ucore-thumips](https://github.com/z4yx/ucore-thumips)，现移植到LoongArch 32。并成功跑通了所有的用户进程。

**开发者：** 陈老师

**仓库地址：** https://github.com/cyyself/ucore-loongarch32

**实验指导书：** https://cyyself.github.io/ucore_la32_docs

**主要特性：**

* 基于v2.0 ABI的新世界系统
* 可运行在LoongArch[开源Soc平台](https://gitee.com/loongson-edu/chiplab)
* 成功跑通所有的用户进程
* 实验环境有Docker镜像支持，使用`docker pull chenyy/la32r-env`进行安装，在该容器编译

# rCore(移植完成，待合并)

rCore是THU基于Rust语言开发的类Unix教学操作系统。

**开发者：** 陈老师

**仓库地址：** https://github.com/Godones/rCoreloongArch

**主要特性：**

* 基于v2.0 ABI的新世界系统
* 支持ch0-ch8实验
* 支持简易内核栈回溯
* 项目荣获2022年全国大学生操作系统大赛-功能挑战赛二等奖。

# Yocto(移植完成，待合并)

Yocto是用于定制嵌入式Linux系统的主流工具之一。龙芯相关团队基本完成了yocto的LoongArch支持工作，可以在x86平台和LoongArch平台从零构建定制的Linux/LoongArch嵌入式系统，并生成相应的SDK。

**开发者：** 龙芯团队

**参考仓库地址：** https://github.com/foxsen/meta-loongson

https://github.com/foxsen/poky

https://github.com/yoctoproject/poky

主要特性：

* 基于v2.0 ABI的新世界系统
* poky的基础支持代码大部分已被上游接受

# seL4(移植完成，待合并)

seL4是首个经过形式化验证的微内核，是经典的L4系列微内核的一种实现，具有安全、高性能、高可靠等特色。已在2022年.09移植到了LoongArch架构，并通过了测试程序。

**开发者：** [tyyteam](https://github.com/tyyteam)

**主仓库地址：** https://github.com/tyyteam/la-seL4

**主要特性：**

* 基于v2.0 ABI的新世界系统
* 陈老师重新整理，已向上游提PR
* 移植或使用了10个官方仓库
* 项目[视频](https://www.bilibili.com/video/BV1Mt4y1j7Gx/?vd_source=c0ebc331ee63978f26b2050109cc5826)，通过了sel4test测试用例
* 项目[文档](https://github.com/tyyteam/OS-comp-pdfdoc-videos/blob/main/proj97-la-seL4-tyyteam-%E5%86%B3%E8%B5%9B%E9%A1%B9%E7%9B%AE%E6%96%87%E6%A1%A3.pdf)
* 项目荣获2022年全国大学生操作系统大赛-功能挑战赛一等奖

# fuchsia的zircon(开发中)

zircon是fuchsia系统的微内核，官方尚未给出zircon的代码仓库，此移植工作基于[PanQL](https://github.com/PanQL)分离的[zricon代码](https://github.com/PanQL/zircon)。

**开发者：** 徐老师 耿老师

**仓库地址：** 代码完善后即将公开

**主要特性：**

* 基于v2.0 ABI的新世界系统
* 可以shell，支持简单的cd，ls等命令

# NuttX(开发中)

NuttX是完全兼容Posix和ANSI标准的嵌入式实时系统，有着轻量级、定制化的特点，已被广泛应用在成熟的商业系统或软件中，如小米Vela系统、三星Tizen RT系统、px4飞行控制软件。

**开发者：** 刘老师

**仓库地址：** https://github.com/LA-NuttX

**主要特性：**

* 基于v2.0 ABI的新世界系统
* 正在移植flat build模式的nsh64程序

* 计划移植kernel build模式
* 计划移植knsh64、smp64、net64程序
