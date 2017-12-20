---
layout: post
title: "软件说明书（specification）及其形式化描述"
date: 2017-12-20 01:31:55 +0800
comments: true
categories: 软件设计基础
---
在编写程序之前，我们需要知道这个程序的功能是什么，才能进行编程。这就是功能说明书（specification）所扮演的角色。Specification可以有多种形式，比如：无结构化的文本、结构化的文本、数学描述等。本文将简单介绍一下如何使用数学符号来形式化的描述specification。
<!-- more -->

##软件说明书（specification）是什么？

在编写程序之前，我们需要知道这个程序的功能是什么，才能进行编程。这就是功能说明书（specification）所扮演的角色。Specification就是详细的说明软件或者程序要实现的功能。
Specification可以有多种形式： 无结构的文本语言（informal text）、 结构化的文本语言（structured document）、 形式化的数学表示（formal mathematical notation）。

##如何准确的表达specification？
在本文中，我们将主要关注如何使用**mathematical notation** 来准确的描述specification。
数学的好处就是可以进行准确的、无歧义的描述。

其中，有2种mathematical notation，一种是[**FOL**](https://en.wikipedia.org/wiki/First-order_logic)（一阶逻辑，First Order Logic）；另一种是[**OCL**](https://en.wikipedia.org/wiki/Object_Constraint_Language)（对象描述语言，Object Constraints Language）。

FOL可以准确的表示命题（proposition）。

OCL是UML语言的一个扩展，OCL提供了一种语法对UML图进行注释，OCL往往是出现在UML图中。


## 如何将text specification表示为mathematic specification？
这部分我们**以SQRT为例**，来展示如何使用数学表示（FOL或者OCL）来描述specification。
SQRT功能是求X的平方根。

### (1)文本描述SQRT功能

* ***输入***：X，非负数。
* ***输出***：Y，是X的平方根。
* ***约束***：Y * Y  = X

	[**注意**]：在使用文本描述功能的时候，避免出现循环描述。一定要详细的说明输出与输入之间的关系。

### (2)将上述文本描述拆分成三部分

根据上述的文本描述，我们拆分出三部分内容：

* ***名字***（signature）：由程序的名字、输入参数及类型、输出参数及类型组成。

	例如：Real Y =  Sqrt(Real X).  

* ***前置条件***（Precondition）: 输入参数的声明，用于检查输入参数是否符合程序的要求。

	例如：Sqrt(int x)的precondition是：x>=0。

	再举个例子：如果除了对输入参数有类型约束之外，没有其他约束，那么，precondition总为True。
* ***后置条件***（Postcondition）: 输出结果的声明，用于表达输出结果与输入参数的关系。

	[**注意**]：有一些程序的功能（pure function），其输出结果完全由输入参数决定；而也有一些程序的功能（impure function）是有副作用的，或者，其输出结果不完全由输入参数来决定。在这里，我们是针对pure function。         
	例如，SQRT的后置条件为： Y * Y = X


### (3)使用FOL或者OCL描述
经过上述分析出SQRT的名字、前置条件、后置条件之后，就可以使用FOL或者OCL进行形式化描述了。

例如，对SQRT使用OCL描述为：

```
Context REAL::SQRT(): Real

Pre: self >= 0

Post: result * result = self
```

例如，对排序功能ISORDERED使用OCL描述为:

```
Context Vector:: ORDER(): Boolean

Pre: true

Post: self -> forAll (i: integer | i >0 and i < self.length  implies

self.at[i] <= self.at[i+1])
```


## 后记
其实在学术论文中，也会经常使用数学符号来描述问题、建模等。不论使用FOL形式，还是OCL形式，一定要在论文中保持一致，至始至终使用同一种语言形式来表示，切勿混用。
