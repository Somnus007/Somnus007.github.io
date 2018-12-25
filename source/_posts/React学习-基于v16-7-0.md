---
title: React学习-基于v16.7.0
date: 2018-12-25 16:05:13
categories: 前端
tags: 
    - React
    - JavaScript
    - Js框架
---

![Alt React学习笔记](React学习-基于v16-7-0/react.jpeg "React学习笔记")

## 概述

React 起源于 Facebook 的内部项目，并于2013年5月开源。更多精彩见[React 官网](https://reactjs.org/ "React 官网")

<!-- more -->

**React 核心特色**

- 声明式渲染
  

先来说明一下**命令式编程**和**声明式编程**：
**命令式编程关注怎么做**，通俗点说就是我们通过一行一行代码让机器照着一步一步的去做。例如我有一个数组，然后想通过它得到每个值都是它的只两倍的数组：

    const originArr = [1,2,3]; // 原始数组
    const resultArr = []; // 定义一个空数组
    for(let i = 0;i < originArr.length;i++){ // 遍历原始数组，然后将每个值乘于2之后添加到空数组中
        resultArr.push(originArr[i] * 2)
    }

**声明式编程关注做什么**，就是我们的目的。同样的例子适用声明式编程：

    const originArr = [1,2,3]; // 原始数组
    const resultArr = originArr.map(item => item * 2); // 遍历数组由map方法代为实现，而我们只需要关注我们要做什么：即把每个值乘于2

那么react的声明式渲染体现在什么地方呢？简单点说就是react独创的**JSX**语法，一种把html和js结合起来的成果，例如：

    const title = <h3>This is a title</h3> ; 

上述代码中`<h3>This is a title</h3>` 既非html也非字符串，我们可以叫它react element，实际上它在被react渲染成真实DOM之前只是一个普通的js对象，后面会有介绍。
React使用JSX语法让我们只需要是关注我们想要做什么，输入的state或者props，输出的UI界面，而不用分心关注于原生的DOM操作。


- 组件化


在React中一切皆组件，组件是React中最基本的单元结构。大到整个页面，小到一个按钮或者弹窗都可以成为一个组件。


- 可移植性强

React不仅可以在web端使用，它还可以借助nodejs在server端渲染，还可以借助 React Native 开发移动端应用。

## 主要概念
