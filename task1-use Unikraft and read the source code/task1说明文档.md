# task1说明文档

任务一：掌握使用 Unikraft 并阅读源码

主要评分点：

1. 完成Unikraft社区的Session练习，至少完成Session 1, 2,
   4。后续会提问Session里的内容进行提问；
2.  Unikraft的线程调度、内存管理、网络、存储四大模块四选一，进行源码阅读并说明它的整体架构和原理。

## 文件结构：

```
.
│--Session01-BabySteps
	└─01-echo-back
	│--02-rot13
	│--03-mount-9pfs
	│--04-store-strings
	│--img
	│--Session01-BabySteps学习总结.md
│--Session02-BehindtheScenes
	└─03-more-messages
	│--04-going-through-the-code
	│--05-important-message
	│--04-store-strings
	│--06-adding-filesystems
	│--07-give-a-choice
	│--09-a-new-source-file
	│--10-more-power
	│--img
	│--Session02-BehindtheScenes学习总结.md
│--Session04-ComplexApplications
	└─01-set-up-and-run-sqlite
	│--02-change-filesystem-sqlite
	│--03-set-up-and-run-redis
	│--04-obtain-the-ip-statically
	│--05-benchmark-redis
	│--06-set-up-and-run-nginx
	│--08-Quiz.txt
	│--Session04-ComplexApplications学习总结.md
│--内存管理模块源码阅读与分析
	│--img
	│--内存管理源码阅读分析.md
│--task1说明文档.md
```

- 完成Unikraft社区的Session练习，至少完成Session 1, 2,4。

  各个session涉及的代码保存于Session01-BabySteps，Session02-BehindtheScenes，Session04-ComplexApplications，且对每个session进行了知识整理与学习总结，保存于各个session文件夹下的markdown文件中。

- Unikraft的线程调度、内存管理、网络、存储四大模块四选一，进行源码阅读并说明它的整体架构和原理。

  选择内存管理模块进行源码阅读并说明它的整体架构和原理，具体对源码的阅读与整体架构和原理等的整理与分析在 `./内存管理模块源码阅读与分析/内存管理源码阅读分析.md`中。