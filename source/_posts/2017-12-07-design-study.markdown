---
layout: post
title: "Design study"
date: 2017-12-07 09:28:08 -0500
comments: true
categories: 软件设计基础
---

每个软件项目应该最终包含3个交付物：解决问题的source code，项目的具体报告，design study。那么，什么是design study？它有什么用呢？如何严谨的记录归档design study呢？
<!-- more -->

## 为什么需要Design study？
设计的过程就是一个决策的过程，分析探索可能的解决方案（design space）。这个决策的过程往往需要分析各方、权衡利弊。

那么如何帮助决定选择哪种方案呢？其中一个可选的方法就是进行design study。通过量化的分析，直观地揭示哪些因素会影响我们的设计，揭示这些因素如何影响设计。可见，design study 是一个软件设计阶段的早期活动。

## Design study是什么？
从定义上来看，design study是：严谨的且系统化地评估那些影响设计的因素的过程。

既然是一个评估过程，那么需要涉及评估的标准、度量的指标等。评估的内容可以包括客观目标的评估以及美学方面的评估等等。

## 如何记录Design study？
Design study与科学实验其实很类似，展示分析评估结果的同时，也要具备可重复性（repeatability）。为了保证评估过程与结果的可重复性，那么就需要详细的记录整个过程，即编写严谨的report - the report of a design study 。report必须严谨、专业、无歧义、浅显易懂、简洁明了。

## 记录哪些内容？
Design study的report应该记录哪些内容呢？与科学的实验报告类似，也要包括下面几部分：

### （1）上下文-Context
这部分内容主要提供该design study的背景、动机、专业词汇释义。即使没有任何相关先验知识的人，看到这部分内容后，都能了解该study的背景和目的。

### （2）研究问题-Research questions
研究问题可以是针对不同非功能需求之间的tradeoff关系的疑问。

每个研究问题应该以中立的视角明确阐述、或者公式化的表示。清晰的阐述变量是什么，自变量是什么。

### （3）对象-Subject
在design study中，比较的对象有哪些？各个对象是什么？这都要进行简单描述。

### （4）实验条件-Experimental conditions
实验运行了多少次，实验运行的环境。如：运行程序的机器型号、架构类型、内存大小、网络带宽信息等。

### （5）变量-Variables
变量包括：自变量-independent variables，因变量-dependent variables。

变量有哪些？每个变量的度量指标、度量单位、对应与每个研究问题的自变量和因变量是什么？

### （6）数据收集和分析方法-Method
使用的工具，度量采用的设备，统计分析技术，使用到的具体参数值等。

### （7）实验结果-Results
使用各种图表展示收集到的数据和评估结果。

### （8）讨论-Discussion
解释实验数据，揭示暗示的含义并讨论， 解释异常结果， 反省本次study的不足之处和待提高之处， 计划未来等。

### （9）结论-Conclusions
总结上述的结果和得出的结论，明确的回答上述提出的研究问题。
