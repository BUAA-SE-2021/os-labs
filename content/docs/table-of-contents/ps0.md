---
title: Problem Set 0
weight: 1
---

# Problem Set 0

## 实验说明

- 单人完成，代码要求每人一份（只需提交两个 `*.c`文件）。除代码外，还需要提交文档。内容可为设计和需求说明、解决思路等，无文档模板，自由发挥。
- 对于每个人而言，请仅提交一个 PDF 文件（如果有多个文档，请合并成一个。推荐把所有内容写在一个 Markdown/LaTex 项目里）。由组长将每个人的代码文件和 PDF 文档收齐后，将每个人的提交内容放在各自的文件夹后打包为 Zip 包提交。
- 本次实验因为不涉及多人合作，故对 Git 的使用没有要求。此后的 Project 1 开始，会对小组使用 Git 的情况进行考察。
- 本实验需要利用操作系统的同步机制，实现问题中要求的逻辑功能。
- 实验代码可在官网中自行下载，无需 Pintos 环境即可直接运行。

## 实验内容

- Problem 1：自动化车站
  - 乘客行为：到站台等车、车来则上车
  - 火车行为：到站装载乘客，无人等待或车已满就开走
  - 让乘客和火车的行为流畅运行，以实现车站的自动化管理
- Problem 2：氢原子与氧原子结合，生成 H2O
  - 2 个 H 和 1 个 O 生成水分子
  - 如何保证 H2O 结构正常生成，不会遗漏或多加原子

## Problem 1

### 需求

CalTrain 程序想让你通过自动化列车和乘客管理来提高效率。每名乘客和每列火车都由一个线程控制。 要求编写同步函数，以确保列车的有序装载。避免出现多人上车座位不够的情况。

### 步骤

- 定义 `station` 结构体
  - 包含程序所用的信号量、锁、条件变量
- 编写以下处理函数：
  - 初始化函数：`station_init(struct station *station)`
  - 初始化结构体中的数据
- 列车行为：
  - 火车到站打开车门：`station_load_train(struct station *station, int count)`
  - 当且仅当列车已满或无乘客等待时，该函数返回
- 乘客行为：
  - 到站等车，添加一名位于等待状态的乘客：`station_wait_for_train(struct station *station)`
  - 乘客就坐，“通知”列车当前乘客已经就坐：`station_on_board(struct station *station)`
- 外层调用无需考虑，只需定义结构体和同步机制所需的函数

### 要求

- 允许多名乘客等车
- 只需改动 `caltrain.c`
- 不能造成忙等待
- 只能使用以下函数
  - `lock_init (struct lock *lock)`
  - `lock_acquire(struct lock *lock)`
  - `lock_release(struct lock *lock)`
  - `cond_init(struct condition *cond)`
  - `cond_wait(struct condition *cond, struct lock *lock)`
  - `cond_signal(struct condition *cond, struct lock *lock)`
  - `cond_broadcast(struct condition *cond, struct lock *lock)`

## Problem 2

### 需求

大自然母亲聘请你帮助她解决形成水的化学反应，但是她似乎无法正确处理反应中的同步问题。 将两个 H 原子和一个 O 原子同时放在一起即可生成水分子， 每个原子由一个线程表示。

### 步骤

- 定义 `reaction` 结构体
- 包含程序所用的信号量、锁、条件变量
- 编写以下处理函数：
  - 初始化函数：`reaction_init(struct reaction *r)`
  - 氢氧原子准备结合：`void reaction_h(struct reaction *r)`、`void reaction_o(struct reaction *r)`
  - 每有一个 H 或 O 原子进入等待，调用该函数，结合成功后返回
- 在代码中包含结合水的函数：`make_water()`
  - 无需实现，已经给出，需要在逻辑中加入

### 要求

- 允许多个原子等待反应
- 不能造成忙等待
- 只需改动 `reation.c`
- 只能使用以下函数
  - `lock_init (struct lock *lock)`
  - `lock_acquire(struct lock *lock)`
  - `lock_release(struct lock *lock)`
  - `cond_init(struct condition *cond)`
  - `cond_wait(struct condition *cond, struct lock *lock)`
  - `cond_signal(struct condition *cond, struct lock *lock)`
  - `cond_broadcast(struct condition *cond, struct lock *lock)`

## 测试方法

- 在代码根目录下命令行运行 `make run`
- 重新编译记得 `make clean`

正常运行时命令行输出：

```sh
...Train departed station with 17 new passenger(s) (expected 17)
Looks good!
./reaction 0
Created 0 H and 200 O atoms (0.0% H), expecting 0 H2O molecules
Looks good!
```
