---
title: Pintos 实验规划
type: docs
---

# Pintos 实验规划

## 总体设计

实验来自[CS 140: Operating Systems (Spring 2020)](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/index.php)，包含以下若干个 Projects：

- [x] [Problem Set 0: Synchronization](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/problemSet0.php) 单人，必做，10 月 14 日 22：00 前提交
- [x] [Project 1: Threads](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintosProjects.php) 组队，必做，暂定 11 月 7 日 22：00 前提交
- [x] [Project 2: User Programs](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintosProjects.php) 组队，必做，暂定 11 月 28 日 22：00 前提交
- [ ] [Project 3: Virtual Memory](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintosProjects.php) 组队，选做，暂定 12 月 5 日 22：00 前提交
- [ ] [Project 4: File Systems](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintosProjects.php) 没要求

### Problem Set 0: Synchronization

Note: this problem set should be done individually, not in teams. The teams will apply to the four Pintos projects. For this problem set it is OK to discuss general strategy with other people, and it's OK to give and receive help tracking down problems, but you must write your own code.

### Project 1: Threads

See the Pintos documentation for details on this project:

- [Assignment](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/pintos_2.html)
- [Frequently asked questions](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/pintos_2.html#Project%201%20FAQ)
- [Template for design document](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/threads.tmpl)

Additional notes and modifications for Project 1:

- A common mistake students make throughout the Pintos projects is to use `malloc` carelessly. If you call `malloc`, you must check the result to make sure the system did not run out of memory (and you must do something reasonable if memory does run out). In addition, you must be sure that any memory you allocate is eventually freed.

### Projects 2: User Programs

See the Pintos documentation for details on this project:

- [Assignment](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/pintos_3.html)
- [Frequently asked questions](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/pintos_3.html#Project%202%20FAQ)
- [Template for design document](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/userprog.tmpl)

### Project 3: Virtual Memory

See the Pintos documentation for details on this project:

- [Assignment](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/pintos_4.html)
- [Frequently asked questions](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/pintos_4.html#Project%203%20FAQ)
- [Template for design document](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/vm.tmpl)

## 提交方式和内容

我们会提供 Markdown 模板和需要提交文件的参考目录结构，请在完成实验后将所有需要提交的文件压缩成 Zip 包上传至北航软件学院云平台。命名方式和具体提交内容见各实验的详细说明。

每周需要通过周例会的形式记录小组内的组织进度安排，周例会需要写一份报告，以小组为单位，每周提交至云平台上。

## 评分说明

实验内容占总成绩的 40%，实验课上机时会有签到，每次实验后会有验收答辩。

分数占比：

- 签到：10 分
- 考试：50 分
- Pintos 实验：40 分
  - Problem Set 0：5 分
  - Project 1：15 分
  - Project 2：20 分
  - Project 3：附加 5 分

## 助教联系方式

- 朱英豪（微信 zhuyinghao）
- 康曦文（微信 kxw009988）
- 杨智茹（QQ 1270367357）
