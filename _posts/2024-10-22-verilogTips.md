---
title: verilog小Tips
date: 2024-10-22
---

# verilog简介
Verilog HDL（简称 Verilog ）是一种*硬件描述语言*，用于数字电路的系统设计。可对算法级、门级、开关级等多种抽象设计层次进行建模。
Verilog 继承了 C 语言的多种操作符和结构，与另一种硬件描述语言 VHDL 相比，语法不是很严格，代码更加简洁，更容易上手。
# 请不要将verilog与c混淆！
虽然Verilog很多东西继承于C语言，但是他们两者**完全不一样！完全不一样！！完全不一样！！！**
- C语言作为软件语言，其运行逻辑是串行的，它关心的是如何通过算法逻辑解决问题。
- Verilog作为硬件描述语言，其运行逻辑是并行的，它关心的不仅是从功能逻辑这个问题如何解决，更关心这些功能如何实现，关心最终的电气连接。*可综合的Verilog代码经过综合后，最终会转化为实际电路。*
硬件**描述**语言，望文生义，其是为了描述具体电路的功能、连接和时序，重在描述。需要预先对电路进行设计，而非想到啥写啥。
# Verilog的并行执行
Verilog所有always块都是并行执行的，并不存在写在哪的顺序问题。这也是因为电路都是“同时”发生变化而导致的。
# 可综合与不可综合
Verilog中存在一些用于仿真验证的子集，属于仿真验证语言，只在仿真时候使用，不能被综合成电路，因为没有相应的硬件元件与其对应，比如$display函数、initial初始化块等。
*具体哪些不可综合可自行百度。*