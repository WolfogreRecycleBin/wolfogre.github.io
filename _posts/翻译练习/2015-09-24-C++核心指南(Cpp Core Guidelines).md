---
layout: post
title: "C++核心指南(Cpp Core Guidelines)"
description: "内层C++是一门努力摆脱困境，追求更精巧，更安全，更安全的语言。"
category: 翻译练习
tags: [C++]
---

{% include JB/setup %}

*声明：本文为笔者为练习用于所做的翻译练习，原文所属者与笔者没有任何关系，翻译结果不代表原文所属者的观点。笔者不保证翻译的正确性，任何人以任何形式的对本文的引用，都是不负责任和荒谬的行为，造成的后果笔者不予负责。*


**[原文链接](https://github.com/isocpp/CppCoreGuidelines/blob/dde3cc5c20d85f0f0186d85e20eb62c80e296ed7/README.md)**  
**所属:[isocpp/CppCoreGuidelines](https://github.com/isocpp/CppCoreGuidelines/)**  

> "Within C++ is a smaller, simpler, safer language struggling to get out." -- Bjarne Stroustrup  

内层C++是一门努力摆脱困境，追求更精巧，更安全，更安全的语言。—— 本贾尼·斯特劳斯特卢普  

> The C++ Core Guidelines are a collaborative effort led by Bjarne Stroustrup, much like the C++ language itself. They are the result of many person-years of discussion and design across a number of organizations. Their design encourages general applicability and broad adoption but they can be freely copied and modified to meet your organization's needs.  

C++核心指南如同C++语言本身一样，是由本贾尼·斯特劳斯特卢普博士领导的共同协作的成果。它是许多人花费数年的时间，跨越许多组织，共同讨论、设计的成果。它的设计提倡普遍使用和广泛采用，但是它可以被自由的复制和修改，来迎合你的组织的实际需要。  

> The aim of the guidelines is to help people to use modern C++ effectively. By "modern C++" we mean C++11 and C++14 (and soon C++17). In other words, what would you like your code to look like in 5 years' time, given that you can start now? In 10 years' time?  

 这份指南的目标是帮助人们有效地使用现代C++语言。这里的“现代C++”指的是C++11和C++14（以及即将发布的C++17）。换句话说，假如从现在开始你就可以考虑，你希望未来五年里你写的代码是什么样的？未来十年呢？  

> The guidelines are focused on relatively higher-level issues, such as interfaces, resource management, memory management, and concurrency. Such rules affect application architecture and library design. Following the rules will lead to code that is statically type safe, has no resource leaks, and catches many more programming logic errors than is common in code today. And it will run fast - you can afford to do things right.  

这份指南专注于相对来说比较高级的问题，比如接口，资源管理，内存管理，以及并发性。这些规则会影响应用的架构和库的设计。遵循这些规则将带来静态类型安全的代码，避免资源泄露，并捕获更多在当今代码中常见的编程逻辑错误。而且代码将运行地更快——你将有条件做一些正确的事。  

> We are less concerned with low-level issues, such as naming conventions and indentation style. However, no topic that can help a programmer is out of bounds.

我们不太关心低级的问题，比如命名约定或代码缩进风格。然而事实是，没有任何一个专题能帮到一个不遵守约定的程序员。  

> Our initial set of rules emphasize safety (of various forms) and simplicity. They may very well be too strict. We expect to have to introduce more exceptions to better accommodate real-world needs. We also need more rules.  

我们最初设定的规则强调安全（包括多种形式的）和简单。它很可能过于严格。我们希望引入更多的例外来更好的适应现实的需求。我们同样也需要引入更多的规则。  

> You will find some of the rules contrary to your expectations or even contrary to your experience. If we haven't suggested you change your coding style in any way, we have failed! Please try to verify or disprove rules! In particular, we'd really like to have some of our rules backed up with measurements or better examples.

你将发现有些规则有悖于你的期望，甚至有悖于你的经验。如果我们没有以任何方式建议你改变你的代码风格，我们便已将已经失败了！请尝试验证或反驳这些规则！特别的，我们真的很乐意将我们的一些规则，在有改进措施或更好的示例的情况下回退(此句可以翻译得更好)。 

> You will find some of the rules obvious or even trivial. Please remember that one purpose of a guideline is to help someone who is less experienced or coming from a different background or language to get up to speed.  

你将发现一些规则是浅显的甚至琐碎的。请记住一份指南的目标是帮助那些并不熟练的，或来自其他的背景、使用其他的编程语言的人提高开发速度。  

> The rules are designed to be supported by an analysis tool. Violations of rules will be flagged with references (or links) to the relevant rule. We do not expect you to memorize all the rules before trying to write code.  

这些规则设计成能被分析工具所支持。规则的违规设计将被用引用（或链接）来标记，这些引用（或链接）指向与其相悖的规则。我们不指望你在尝试写代码之前记住所有的规则。  

> The rules are meant for gradual introduction into a code base. We plan to build tools for that and hope others will too.  

这些规则旨在逐步引入到一个代码库。我们计划开发一些工具来辅助做这件事，我们也希望其他人同样这么做。  

> Comments and suggestions for improvements are most welcome. We plan to modify and extend this document as our understanding improves and the language and the set of available libraries improve.

我们非常欢迎大家提出帮助改进的意见和建议。随着我们理解的深入，以及语言和可用库的完善，我们将修改和扩展这份文档。

