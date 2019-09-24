---
layout:	post
title: 	"Review: A Tour of Go"
date:   2019-09-24 00:00:00 +0000
categories: default
---
很高兴用了周末的一点时间看完了“A Tour of Go”。回顾了一下，自己之前尝试写过的语言类型林林总——C/C++/C#，C family应该是学习和工作使用时间最长的语言。大一入学编程课程的第一门课就是C++，第一份在亚马逊的工作是C，现在在微软的工作则是C++。可是用的时间虽然很长，但是期间并没有认真研究过语言本身的很多特性，以及更新后的每一代C++的新的特点和功能，至于编译器背后的逻辑，内存的如何分配，线程的调度很多知识都还给书本和老师了。JAVA短暂的用过一些，用的最多的就是在Leetcode刷题的时候，当时才研究生刚毕业，觉得Java的容器比C++的方便，又不用担心指针的问题，所以刚开始刷题和面试的时候常用Java。写过一些Android的小程序，还有好些课程作业，用Android Studio，Eclipse等，也都是Java。Python应该也是从研究生起才开始用，当时用来做NLP的作业。发现脚本语言用Python写十分方便，后来的两份工作中Python也用作同样的目的。当然也有用Python写的相对更大的程序，我就主要是user而不是developer了。其余的语言大抵都是为了写简单网站而学习的HTML，CSS，PHP和JAVASCRIPT了。

这次学习Go，感受到了很多知识融会贯通的乐趣。比如开头的package main，让我想到Java；import又会想到Python。在一步一步的学习过程中，又会发现很多与C和C++相似的点。这些都是很有意思的体验。函数和变量的定义让我感受到语言发明者想distinguish这种语言和其它语言外观区别的努力，而在pointer和reference的使用上又让我看到C语言在几十年前的智慧。defer的出现也会让我觉得像是类似finally的定义。slice和map是这个tour中介绍的两种常用数据结构。slice的cap和len很耐人寻味，我觉得会是一个容易产生bug的地方。在function closure这一节，我又回过头去研究同样的功能是如何在C++中实现的。花费了不少的时间，写出了一个C++ function closure版本的Fibonacci求和代码。与Golang相比，C++如果没有了Lambda Function，写出这样的功能一定要大费周章了。Function closure让这个function本身有了状态，可以存储只有自己可见的变量，应用场景还是很独特的。

Go里面的method，struct和interface让我想到了当时看到过的C的代码，C用各种struct和function pointer来实现一个类似C++一样的面向对象编程的架构。这里Go把这些都统一起来了。看完了Goroutines，我猛然有种想用Go重写一遍现在project的C++代码的冲动。许多当时用C++繁复的实现，Go都可以有更直接和简洁的替代方式。channels和select是现在这个project的核心关键——我们用redis的subscribe和publish的功能以及Linux的select()来实现一系列的channel给进程间通信，channel的性能很大的影响了整个程序的运行。我很好奇Go的实现是否能不单单简化代码，还可以提升整体性能。

很期待能在接下来的时间里《从入门到精通Go》。
