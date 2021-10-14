---
title: Pintos 实验规划
type: docs
---

# Pintos 实验规划

## 总体设计

实验来自[CS 140: Operating Systems (Spring 2020)](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/index.php)，包含以下若干个 Projects：

- [x] [Problem Set 0: Synchronization](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/problemSet0.php) 单人，必做，10 月 14 日 23：00 前提交（任老师班是 0 点，为防止云平台卡住，原老师班特提早一小时，下同）
- [x] [Project 1: Threads](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintosProjects.php) 组队，必做，11 月 11 日 23：00 前提交
- [x] [Project 2: User Programs](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintosProjects.php) 组队，必做，暂定 12 月 14 日 23：00 前提交
- [ ] [Project 3: Virtual Memory](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintosProjects.php) 组队，选做，暂定 12 月 14 日 23：00 前提交
- [ ] [Project 4: File Systems](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintosProjects.php) 没要求

### Problem Set 0: Synchronization

> 关于进程间同步的练习

Note: this problem set should be done individually, not in teams. The teams will apply to the four Pintos projects. For this problem set it is OK to discuss general strategy with other people, and it's OK to give and receive help tracking down problems, but you must write your own code.

### Project 1: Threads

> 进程管理

See the Pintos documentation for details on this project:

- [Assignment](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/pintos_2.html)
- [Frequently asked questions](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/pintos_2.html#Project%201%20FAQ)
- [Template for design document](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/threads.tmpl)

Additional notes and modifications for Project 1:

- A common mistake students make throughout the Pintos projects is to use `malloc` carelessly. If you call `malloc`, you must check the result to make sure the system did not run out of memory (and you must do something reasonable if memory does run out). In addition, you must be sure that any memory you allocate is eventually freed.

### Project 2: User Programs

> 处理系统调用

See the Pintos documentation for details on this project:

- [Assignment](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/pintos_3.html)
- [Frequently asked questions](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/pintos_3.html#Project%202%20FAQ)
- [Template for design document](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/userprog.tmpl)

### Project 3: Virtual Memory

> 虚拟内存

See the Pintos documentation for details on this project:

- [Assignment](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/pintos_4.html)
- [Frequently asked questions](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/pintos_4.html#Project%203%20FAQ)23
- [Template for design document](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/vm.tmpl)

## 提交方式和内容

所有实验均以小组形式提交，其中 Problem Set 0 需个人单独完成，组长收齐后提交。

每个实验需提交代码（需要提供必要的中文代码注释）和中文实验文档。

- [**必做**] 官方所给的 Design Document、过点的情况、Git 仓库地址（请设置为 Private，并邀请助教进仓库）
- [**必做**] 实验要求、需求分析、设计方案（算法描述、数据结构）、踩坑记录、Debug 的解决方案、实验心得体会、用户手册、测试报告、你认为有意义的任何内容（有模板提供）

我们会提供文档 Markdown 模板和需要提交文件的参考目录结构，请在完成实验后将所有需要提交的文件压缩成 Zip 包上传至北航软件学院云平台。命名方式和具体提交内容见各实验的详细说明。

另外，每周需要通过周例会的形式记录小组内的组织进度安排，周例会需要写一份报告，同样以小组为单位。从第五周上机课开始，每周四晚 23 时前提交至云平台上。第一次周例会的文档提交时间为 10 月 14 日，请在 14 日前及时开展周例会活动。

周例会的内容务必如实填写，我们会在上机时间检查各组的周例会的开展情况和 Git 的历史提交记录（请各组提前作好准备，验收时向助教展示），并对组内同学随机抽查提问。（小提示：如果早就把实验 AK 了，就在周例会写“已经做完了，没有进行讨论。”这不会影响当次周例会的考核分数。如果 Project 3 都提早做完并验收完了，上机课都不用来。Project 2 做完验收完并向助教表示了不做附加实验，也不用来。）

**注意：**

请务必在实验截止前 1-2 个小时便提交作业，如云平台有故障，联系助教，不接受任何形式的作业补交。

## 评分说明

实验内容占总成绩的 40 \%。实验课上机时会有签到和对周例会的过程性检查，每次实验和文档完成后，可主动联系助教来进行验收（早做完早验收）。验收方式：向助教现场展示过点的情况，对所提交的文档提问检查。

分数占比：

- 签到（含周例会的过程性检查）：10 分
- 考试：50 分
- Pintos 实验：40 分
  - Problem Set 0：5 分
  - Project 1：15 分
  - Project 2：20 分
  - Project 3：附加 5 分

关于申优答辩的说明：

在实验课上机的最后一周组织申优答辩，小组可自由报名参与申优答辩（云平台上提交答辩材料即算参与答辩，可现场放弃）。其中，若完成了 Project 3，必须参加验收，否则得不到该附加的 5 分。验收内容可为 Project 1~3 的相关内容，如做了 Project 3，答辩 Project 1~3，否则答辩 Project 1~2。着重介绍本学期团队在完成 Pintos 实验时遇到的重难点以及对应的解决方案。申优答辩的分值占平时分的 10%（5 分），如不参与申优，则平时分的上限为 45 分。

最终的总成绩 = (签到 + Pintos 实验分) \* 90 \% + 申优答辩分 + Project 3 的附加分 5 分 + 考试分。

**注意：**

本门课程不设置组内权重。组员的验收表现与全组的团队分挂钩，同时个人的过程性验收情况关系到了个人分。周例会的记录内容和 Git 提交的记录将作为组内差异分重要依据。但刷 commit 记录和编造周例会记录的行为是不被接受的，一旦发现将严肃处理。

## 实验时间安排

- 正式实验从第 4 周开始。
- 实验时间为每周四，原老师班的实验机房：（一）316，任老师班的实验机房：（一）215。
- 每周实验有签到考察，每组成员没有特殊情况请假务必到场。
- 实验课上机的最后一周组织申优答辩（考期前，约 12 月末），小组以 PPT 展示的形式总结实验，所有代码在截止日期前提交至云平台的作业中。

## 助教联系方式

- 朱英豪（微信 zhuyinghao）
- 康曦文（微信 kxw009988）
- 杨智茹（QQ 1270367357）

## 诚信说明

实验代码和报告将严格查重，如发现抄袭，以零分处理。不允许参考他人的 Pintos 实现（读开源项目如 Linux、FreeBSD 等的源码是鼓励的，但同样不允许抄袭，如它们有哪部分的实现启发了你，请在实验文档中引用注明），请务必独立完成每次实验。

附 Stanford 的 Honor Code 的说明：

As in all Stanford classes, you are expected to follow the Stanford Honor Code. For example, the following activities are prohibited and will be treated as Honor Code violations (this is not intended to be a complete list of Honor Code violations):

Submitting code that you did not write personally, with the exception of project code written by your partner(s).
Consulting pre-existing solutions for problem sets and projects (such as solutions posted on the Internet).
Posting your solutions on the Internet or making them available to other students in any form.
You are allowed to discuss general approaches and issues with other students in the class besides your team members. It's also fine to give other students help finding bugs if they are stuck, or to answer general questions, such as "what is the meaning of this bit in a page table entry?" But, any code you write must be written by you and your team members, from scratch, without consulting existing solutions. We reserve the right to use computer software such as MOSS to analyze material that you submit in order to detect duplication with other students or existing solutions.

A general way to think about this is that if a particular activity significantly short-circuits the learning process (it saves you time but reduces the amount you learn and/or figure out on your own), or if it misrepresents your capabilities or accomplishments, then it is probably an Honor Code violation.
