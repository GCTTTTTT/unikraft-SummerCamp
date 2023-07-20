#  软件定义操作系统的全生命周期管理技术实践

## 文件大体结构

```
.
│--task1-use Unikraft and read the source code
	└─Session01-BabySteps
	│--Session02-BehindtheScenes
	│--Session04-ComplexApplications
	│--内存管理模块源码阅读与分析
	│--README.md
│--task2-use Libvirt to manage Unikraft
	└─libvirtTest
	│--img
	│--Session04-ComplexApplications
	│--README.md
│--task3-ELF
	└─elfloader
	│--img
	│--README.md
│--README.md
```

## task1-use Unikraft and read the source code

该文件夹中为“任务一：掌握使用 Unikraft 并阅读源码”的相关代码与文档，各个session涉及的代码保存于Session01-BabySteps，Session02-BehindtheScenes，Session04-ComplexApplications，且对每个session进行了知识整理与学习总结，各个session的文档报告保存于各个session文件夹下的markdown文件中。

此外，在本次实践中我选择了内存管理模块进行源码阅读并说明它的整体架构和原理，具体对源码的阅读与整体架构和原理等的整理与分析文档报告在 `内存管理模块源码阅读与分析/内存管理源码阅读分析.md`中。

## task2-use Libvirt to manage Unikraft

该文件夹中为“任务二：使用 Libvirt 管理 Unikraft”的相关代码与文档，libvirtTest文件夹中为实践过程中所需用到的镜像文件与对应的XML配置文件，README.md文件为该任务的文档报告。

## task3-ELF

该文件夹中为“任务三： ELF 场景扩展”的相关代码与文档，elfloader文件夹中为实践过程中代码等文件，README.md文件为该任务的文档报告。