---
layout: post
title: "软件设计初识"
date: 2017-12-07 09:05:09 -0500
comments: true
categories: 软件设计基础
---

软件设计是软件开发周期的早期阶段。那么，什么是软件设计？设计包括哪些方面？设计方法有哪些呢？设计的时候要注意什么呢？
<!-- more -->

## 什么是软件设计？
软件设计是构造（不是实现）一个程序的过程，该程序能够满足待解决问题的功能方面的需求，同时不会违背其它非功能的需求。整个构造过程是一个权衡（tradeoff）的过程。

## 什么是架构设计和详细设计？
软件设计通常包括架构设计和详细设计。

**架构设计**：将程序雕刻成几个组件，并且给每个组件的行为方面分配职责，以及讨论各个组件之间如何交互的过程。

**详细设计**：深入到每个组件内部，针对每个组件进行处理。设计每个组件内部的数据结构，以及具体算法等。比如编写伪代码，结构化编程，算法的流程图表示等，都属于详细设计。

## 软件设计存在哪些问题？
**短期的项目计划安排与软件的长期的可维护性**。一个软件项目都有进度安排计划，要求在一定的时间内完成软件。而软件一旦投入运行，是要求软件具有长期可维护性。 但实际上，在有限的时间内完成软件，是牺牲了一定软件的可维护性的。因此，软件的可维护性一直都是很大的问题，已有很多相关研究，如：如何评估软件的质量（可维护性属于质量的一种）；在软件的生命周期内，如何尽早的发现软件质量下降的时间点以及引起质量下降的根因所在。特别是最近几年，[技术债（technical debt）](https://en.wikipedia.org/wiki/Technical_debt)和[架构债（architectural technical debt）](https://www.sei.cmu.edu/architecture/research/arch_tech_debt/index.cfm)的研究非常火热。

**架构设计与详细设计**。软件的架构设计与详细设计存在一定的gap。

**软件的功能行为与非功能约束**。需求不仅包括功能方面的需求，也包括非功能方面的需求。比如，性能、可伸缩性属于非功能需求。特别是，性能需求往往与其它需求之间存在一定的冲突，需要根据具体情形进行权衡。

**软件的需求说明与软件的设计**。软件的需求说明书指出要解决的问题是什么（what），而软件设计指出如何解决问题（how）。

## 如何进行软件设计？- Design method
**结构化设计（structured design）**。即面向功能的设计（function-oriented design）。

**面向对象设计（object-oriented design，OOD）**。 历史上是先有结构化设计，再有OOD。从软件生命期来看，object比功能更稳定。OOD是我们的系列文章的主要关注点。

**基于角色的设计（role-based design）**。

## 如何表示一个软件设计？- Design representative
**UML**（Unified Modeling Language）是面向对象软件设计的建模语言，有很多工具可以帮助人使用UML表示软件设计，并可视化。比如[**ArgoUML**](http://argouml.tigris.org/)。
## 如何验证一个软件设计？- Design validation
及时验证软件设计结果是否符合客户的需求，是性价比高的（cost-effective）且具有时效性的（time-effective）做法。验证评估软件设计，一旦发现问题，就可在编码之前解决问题。若在实现代码时候才发现当初的设计与客户需求不符合，这时候重新设计再实现，为时太晚，需投入更多的精力和财力。
## 如何记录一个软件设计？- Design documentation
软件设计的文档化，能够保存此软件设计的原理、前提假设、架构等，便于团队长期理解和维护软件。

软件设计文档，包含的内容一般有：组件描述（包括数据和处理），控制流，性能，资源，设计者是谁，客户是谁，这样设计的前提假设是什么，所依赖的其它组件（库）有哪些，使用的技术栈，隐式的依赖，配置，内部约束条件，外部约束条件等等。此外，设计文档包含的内容也可以参考Leonardo project记录的内容，比如：stakeholders(views)，issue bases(decision，reasons，influences，conflict)，temporal relation(version，history)，aggregates(package，components，configuration)，internal constraints, external constraints。

总之，文档需要详细记录**设计机理（design rationale）**，也就是：为什么这样设计，设计的方案是什么。
