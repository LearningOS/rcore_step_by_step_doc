# 从零开始写 OS

## 前言

本系列文章记录了使用 Rust 编程语言编写一个小型操作系统的详细过程。每篇文章包含所需所有所需代码和相关知识点讲解。

- [源代码](https://github.com/LearningOS/rcore_step_by_step)
- [源文档](https://learningos.github.io/rcore_step_by_step_doc)
- [web 文档](https://learningos.github.io/rcore_step_by_step_webdoc)

## 前置知识

- 简单的 Rust 语法（这个语言的基础使用方式和 C 类似，文章会介绍其新奇的语法）
- RISCV 汇编（用的不多）

## 如何使用

在阅读文章以及复现的过程中了解 OS 。

为了方便起见，建议使用 [docker](http://www.runoob.com/docker/docker-tutorial.html) ，可以省去配置环境的功夫。

在工作目录下创建 **Makefile** ：

```Makefile
docker:
	sudo docker run -it --mount type=bind,source=$(shell pwd)/..,destination=/mnt panqinglin/rust_riscv
```

进入 docker 后，执行 `cd mnt` ，即可看见工作目录，然后就可以开始写代码啦！

> 每一章或小节对应的源代码可以在 [git](https://github.com/LearningOS/rcore_step_by_step) 的分支中找到

## reference

- https://github.com/rcore-os/rCore
- https://github.com/oscourse-tsinghua/rcore_plus/tree/lab8-rv32-tinyfs
- https://github.com/chyyuu/rcore_plus/tree/lab1-rv32-interrupt .. https://github.com/chyyuu/rcore_plus/tree/lab8-rv32-fs
