[TOC]



# Session04-ComplexApplications学习总结



在学习Session04-Complex Applications的过程中，认识到了Unikraft在处理复杂应用程序时的能力和挑战。复杂应用程序通常需要更多的功能和资源，对操作系统和构建过程提出了更高的要求。

## 基本知识总结

### 关于Complex Applications

复杂应用程序通常是指具有大量代码、依赖项和功能的应用程序。它们可能需要与多个硬件组件和外部库进行交互，处理大量数据或运行复杂算法。Unikraft作为一种轻量级、可配置的操作系统，具有与虚拟机相当的性能，同时具备容器的小型化特性，因此在处理复杂应用程序时具备优势。

在处理复杂应用程序时，需要特别关注以下几个方面：

1. 依赖项管理：复杂应用程序通常依赖于多个外部库和组件。Unikraft通过支持添加外部库和组件的方式，实现依赖项管理。这些外部库可以通过Unikraft的配置选项添加进来，使得复杂应用程序能够正确链接和运行。
2. 系统调用支持：复杂应用程序可能需要使用更多的系统调用。Unikraft支持在Config.uk文件中进行配置，使得需要的系统调用能够正确地在Unikraft上运行。需要注意的是，Unikraft并不像传统操作系统那样支持所有的系统调用，因此在开发复杂应用程序时需要对系统调用做适当的选择和调整。
3. 外部硬件交互：复杂应用程序可能需要与多个硬件设备进行交互，例如网络接口、存储设备等。Unikraft通过平台代码和架构代码提供对硬件的交互支持，使得复杂应用程序能够直接与硬件进行通信。
4. 性能和优化：复杂应用程序对性能要求较高。Unikraft通过优化组件的构建过程和减少不必要的功能，实现了较小的内存占用和较快的启动时间，从而满足复杂应用程序对性能的需求。

### 前置应用

- [Print system](https://unikraft.org/community/hackathons/sessions/complex-applications/#print-system)

- [Assertions](https://unikraft.org/community/hackathons/sessions/complex-applications/#assertions)

- [GDB](https://unikraft.org/community/hackathons/sessions/complex-applications/#gdb)

- [Tracepoints](https://unikraft.org/community/hackathons/sessions/complex-applications/#tracepoints)



### Unikraft的优势 

Unikraft是一个特殊类型的操作系统，它具备虚拟机的直接硬件控制能力，这使得它在处理复杂应用程序时具备优势。与传统操作系统相比，Unikraft的内核和组件可根据实际需求进行配置和精简，从而减少资源消耗和不必要的功能。Unikraft的构建过程还可以通过Kconfig配置选项进行个性化定制，使其适应复杂应用程序的需求。

## Work Items

### 01. SQLite (Tutorial)

本教程目标是在 Unikraft 之上设置和运行 SQLite。

参考教程一步步进行：https://unikraft.org/community/hackathons/sessions/complex-applications/#01-sqlite-tutorial

具体实现在./01-set-up-and-run-sqlite中体现

### 02. SQLite New Filesystem (Tutorial)

在上一个工作中，选择使用 9PFS 作为文件系统。在此工作项，将文件系统更改为 InitRD 并加载 SQLlite 脚本。

参考教程一步步进行：https://unikraft.org/community/hackathons/sessions/complex-applications/#02-sqlite-new-filesystem-tutorial

具体实现在./02-change-filesystem-sqlite中体现

### 03. Redis (Tutorial)

本教程目标是在 Unikraft 之上设置和运行 Redis。

参考教程一步步进行：https://unikraft.org/community/hackathons/sessions/complex-applications/#03-redis-tutorial

具体实现在./03-set-up-and-run-redis中体现

### 04. Redis Static IP Address

修改启动脚本并使用静态IP运行应用程序。

参考教程一步步进行：https://unikraft.org/community/hackathons/sessions/complex-applications/#04-redis-static-ip-address

具体实现在./04-obtain-the-ip-statically中体现

### 05. Redis Benchmarking (Tutorial)

目标是对在 Unikraft 上运行的 Redis 应用程序和在 Linux 上运行的 Redis 进行基准测试。

参考教程一步步进行：https://unikraft.org/community/hackathons/sessions/complex-applications/#05-redis-benchmarking-tutorial

具体实现在./05-benchmark-redis中体现

### 06. Nginx

此工作项目的目的是设置和运行 Nginx。

参考教程一步步进行：https://unikraft.org/community/hackathons/sessions/complex-applications/#06-nginx

具体实现在./06-set-up-and-run-nginx中体现

### 07. Nginx Benchmarking (Tutorial)

使用名为iperf的程序来对在 Unikraft 之上运行的 Nginx 进行基准测试。

参考教程一步步进行：https://unikraft.org/community/hackathons/sessions/complex-applications/#07-nginx-benchmarking-tutorial

### 08. Quiz

Q:Why is it easier to use qemu-guest instead of the manual approach?
A:
Less arguments, focuses on the specific requirements of the app.
Easier to clean up, no need to kill the qemu instance.

Q:What is the easiest way to find the dynamically allocated IP for apps that use lwip with debug information enabled?
A:Inspecting the dnsmasq log file.

Q:What is a necessary step in manually cleaning up your work?
A:
Killing the dnsmasq process.
Deleting the bridge.

Q:What are the 2 usecases for a Redis app?
A:Key-value databases; fast writing and reading of data from memory

## 总结

总结来说， Unikraft是一个非常有潜力的操作系统，可以应用于处理复杂应用程序。通过其轻量级、可配置的特性，Unikraft能够根据不同应用程序的需求进行个性化定制。然而，在开发复杂应用程序时，也需要仔细考虑其对系统调用、依赖项和性能的需求，以充分发挥Unikraft的优势。