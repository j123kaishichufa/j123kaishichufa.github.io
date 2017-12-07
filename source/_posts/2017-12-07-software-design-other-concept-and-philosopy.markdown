---
layout: post
title: "软件设计的其它概念和设计哲学"
date: 2017-12-07 11:16:09 -0500
comments: true
categories: 软件设计基础
---

在设计软件的时候，为了保证软件的质量，需要遵循一定的设计原则。这些设计原则（或者设计概念）是什么呢？有什么用呢？设计概念的最高抽象层次其实就是站在哲学思想的角度，有哪些哲学思想可以指导我们设计软件？
<!-- more -->

## 软件设计的其它概念
### Conceptual integrity
Conceptual integrity，即概念完整性。下述列出了两种“概念完整性”的概念：

[Conceptual integrity](http://cseweb.ucsd.edu/~wgg/CSE131B/Design/node6.html) is the principle that anywhere you look in your system, you can tell that the design is part of the same overall design.

[Conceptual integrity](http://architecture.typepad.com/architecture_blog/2011/10/the-importance-of-conceptual-integrity.html) is the quality of a system where all the concepts and their relationships with each other are applied in a consistent way throughout the system.

总之，概念完整性就是指一个系统的各个方面不是零散的、独立的、不协调的，而是所有的一切都是一致性的贯穿于整个系统。无论以哪个视角看待一个设计，我们都可以感知到这个设计是同样一个系统的整体的一部分。

### Cohesion
Cohesion，内聚度。内聚度描述的是单个组件的特性。一个组件的内聚度指该组件内部所有元素相互依赖的程度。从量化的角度看，内聚度越高越好。在研究领域，已有研究提出了不同的内聚度指标来量化度量组件的内聚性。例如：针对面向对象的软件的度量指标，分布式软件的度量指标，基于服务的软件的度量指标。具体可以参考文章：[https://link.springer.com/article/10.1023/A:1009783721306](https://link.springer.com/article/10.1023/A:1009783721306)； [https://link.springer.com/article/10.1007/s11219-017-9369-3](https://link.springer.com/article/10.1007/s11219-017-9369-3)
### Coupling
coupling，耦合度。耦合度描述的是组件之间的关系。两个组件之间的耦合度是指互相依赖的程度。从量化的角度看，耦合性越低越好。研究领域，已有研究提出了不同的耦合性指标来量化度量组件的耦合性。例如：针对面向对象的软件的度量指标，分布式软件的度量指标，基于服务的软件的度量指标。具体可以参考文章：[https://link.springer.com/article/10.1023/A:1009783721306](https://link.springer.com/article/10.1023/A:1009783721306); [https://link.springer.com/article/10.1007/s11219-017-9369-3](https://link.springer.com/article/10.1007/s11219-017-9369-3)

### Information hiding
Information hiding，信息隐藏。将模块的具体信息和实现封装起来，对外只暴露接口，这就是信息隐藏。 当具体实现发生修改的时候，不会影响接口，从而不会影响客户代码的实现。

### Abstraction and refinements
程序语言就是一个抽象机制。比如程序语言中的很多概念都是抽象化：声明（是什么而不是怎么做），聚集（容器的概念而不是内容），泛化（类的概念而不是实例），参数化（真正调用的时候，才绑定数值）


## 软件设计哲学
### 设计美学
美具有三个特点：完整wholeness、和谐harmony、光辉radiance。

软件设计的美，我们称为**软件美学（Software Aesthetics**），也可以类似包括三点：完整性completeness、一致性consistency、概念完整性conceptual integrity。
### 设计哲学
从哲学的角度如何理解软件设计，可以参考[Piete En](http://www.pietervermaas.nl/Pieter_Vermaas_Design_Research_publications.html) 的相关研究。

哲学的层次看，很多东西都是相通的。例如：

Descartes的哲学思想 VS 基于模型的分析

Marx的理论 VS 理解上下文 (比如：以用户为中心)

Heidegger的思想 VS 提供可用的工具 (比如：IDE)

Wittgenstein的思想 VS 隐喻 (比如：计算机的垃圾箱，文件夹，邮箱的概念)
