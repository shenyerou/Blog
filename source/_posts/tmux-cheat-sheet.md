---
title: Tmux cheat sheet
tags: [tool use]
mathjax: true
date: 2026-06-26 20:26:19
---

## 1. Tmux简单说明

tmux是一个终端复用器，最核心的作用就是解除终端窗口与会话进程的绑定，实现关闭窗口后，会话中进程会继续运行。这一特性可以帮助解决网络对ssh远程连接的影响，即使ssh连接受网络波动影响而断开，会话进程也不会终止。其具体作用包括：

1. 允许在单个窗口中，同时访问多个会话；
2. 可以让新窗口绑定（attach）已经存在的会话；
3. 每个会话有多个连接窗口，因此可以多人实时共享会话；
4. 支持窗口任意的垂直和水平拆分为多个窗格。

## 2. Tmux 基本使用

### 2.1 会话管理

tmux新建会话：

```bash
tmux new -s sesstion-name 
```

tmux分离当前聚焦的会话：

```bash
tmux detach
```

tmux接入会话：

```bash
tmux a -t session-name
tmux attach -t session-name
```

tmux查看会话列表：

```bash
tmux ls
```

tmux杀死会话：

```bash
tmux kill-session -t session-name
```

tmux切换会话：

```bash
tmux switch -t session-name
```

会话管理常用快捷键

### 2.2 窗格管理

## 3. tmux实践操作

## 参考资料

[1] [Tmux的使用教程-阮一峰的网络日志](https://www.ruanyifeng.com/blog/2019/10/tmux.html)
