## 一、Introduction

### 1.Why？

（1）自己感兴趣也有用

（2）ME传承传统

（3）在教中互相学习

### 2.学习注意事项

（1）基础不重要，但是**态度**很重要

（2）找到属于自己的学习方法

（3）课上听学，课下多实践

（4）养成**做笔记**和**写博客**的习惯，也可以在**B站**上发布学习视频

（5）多交流

---

## 二、Markdown

### 1.What is markdown

Markdown 是一种轻量级标记语言，它允许人们使用易读易写的纯文本格式编写文档。

### 2.The purpose of markdown

- [Python 教程 - Sipeed Wiki](https://wiki.sipeed.com/soft/maixpy3/zh/origin/video.html)
- [简书 (jianshu.com)](https://www.jianshu.com/p/b505a6ea7e58)
- [次世代BUG池 ](https://neucrack.com/p/179)

###  3. Some basic grammar

1. use `##` to make a title

2. join `**` on both sides of the words change to `Bold`, what's more, `#` -- `Italics`, `###` -- `Bold italics`

3. use `-` to make a list, `>` to make a block

4. when you write a function -- `print("hello world")`

5. Write a piece of code :

   ```python
   import os 
   print(os.listdir())
   ```

### 4.Independent exploration

​	Studying `markdown` according to [Markdown 教程 | 菜鸟教程 (runoob.com)](https://www.runoob.com/markdown/md-tutorial.html) 

---

## 三、Git Learning

### 1.What is git？

Git 是一个开源的分布式版本控制系统，用于敏捷高效地处理任何或小或大的项目。

Git 是 Linus Torvalds 为了帮助管理 Linux 内核开发而开发的一个开放源码的版本控制软件。

### 2.Concepts

![概念图](D:\ME\概念图.png)

![150046-20181219085715030-2070609804](D:\ME\150046-20181219085715030-2070609804.png)

文件的三种状态：已提交（committed），已修改（modified）和已暂存（staged）

P：为什么会有缓存区？

- 为了能够实现部分提交
- 为了不再工作区创建状态文件、会污染工作区。
- 暂存区记录文件的修改时间等信息，提高文件比较的效率。

```git
$ ssh-keygen -t rsa -C "你自己注册GitHub的邮箱"

add ssh keys	//id_rsa.pub 默认在C:\Users\Administrator.ssh

$ ssh -T git@github.com		//hi + balabal表示成功

$ git config --global user.name "你的GitHub登陆名"

$ git config --global user.email "你的GitHub注册邮箱"

```

```git
git init	//初始化

git add .	//添加文件夹

git commit -m "注释说明"	//注释的作用是告诉下载和浏览的用户你这次提交代码所改变的地方

!: fatal:remote origin already exists
git remote rm origin
git remote add origin 仓库地址

git pull --rebase origin master		//进行代码合并

git push -u origin master	//把当前分支 master 推送到远程


```

```git
git clone+创库地址
cd+文件名	//将你更新的文件复制到该本地目录下
git add .	//提交更新的项目到缓存区
git commit - m “更新信息”	//更新说明
git remote rm origin 	//将原来的项目抹去
git remote add origin HTTPS地址
git push -u origin master
```

```git
  1 查看、添加、提交、删除、找回，重置修改文件
  2 
  3 
  4 git help <command> # 显示command的help
  5 
  6 git show # 显示某次提交的内容 git show $id
  7 
  8 git co -- <file> # 抛弃工作区修改
  9 
 10 git co . # 抛弃工作区修改
 11 
 12 git add <file> # 将工作文件修改提交到本地暂存区
 13 
 14 git add . # 将所有修改过的工作文件提交暂存区
 15 
 16 git rm <file> # 从版本库中删除文件
 17 
 18 git rm <file> --cached # 从版本库中删除文件，但不删除文件
 19 
 20 git reset <file> # 从暂存区恢复到工作文件
 21 
 22 git reset -- . # 从暂存区恢复到工作文件
 23 
 24 git reset --hard # 恢复最近一次提交过的状态，即放弃上次提交后的所有本次修改
 25 
 26 git ci <file> git ci . git ci -a # 将git add, git rm和git ci等操作都合并在一起做　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　git ci -am "some comments"
 27 
 28 git ci --amend # 修改最后一次提交记录
 29 
 30 git revert <$id> # 恢复某次提交的状态，恢复动作本身也创建次提交对象
 31 
 32 git revert HEAD # 恢复最后一次提交的状态
 33 
 34 查看文件diff
 35 
 36 
 37 git help <command> # 显示command的help
 38 
 39 git show # 显示某次提交的内容 git show $id
 40 
 41 git co -- <file> # 抛弃工作区修改
 42 
 43 git co . # 抛弃工作区修改
 44 
 45 git add <file> # 将工作文件修改提交到本地暂存区
 46 
 47 git add . # 将所有修改过的工作文件提交暂存区
 48 
 49 git rm <file> # 从版本库中删除文件
 50 
 51 git rm <file> --cached # 从版本库中删除文件，但不删除文件
 52 
 53 git reset <file> # 从暂存区恢复到工作文件
 54 
 55 git reset -- . # 从暂存区恢复到工作文件
 56 
 57 git reset --hard # 恢复最近一次提交过的状态，即放弃上次提交后的所有本次修改
 58 
 59 git ci <file> git ci . git ci -a # 将git add, git rm和git ci等操作都合并在一起做　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　git ci -am "some comments"
 60 
 61 git ci --amend # 修改最后一次提交记录
 62 
 63 git revert <$id> # 恢复某次提交的状态，恢复动作本身也创建次提交对象
 64 
 65 git revert HEAD # 恢复最后一次提交的状态
 66 
 67 查看提交记录
 68 
 69 git log git log <file> # 查看该文件每次提交记录
 70 
 71 git log -p <file> # 查看每次详细修改内容的diff
 72 
 73 git log -p -2 # 查看最近两次详细修改内容的diff
 74 
 75 git log --stat #查看提交统计信息
 76 tig
 77 
 78 Mac上可以使用tig代替diff和log，brew install tig
 79 
 80 
 81 Git 本地分支管理
 82 查看、切换、创建和删除分支
 83 
 84 
 85 git br -r # 查看远程分支
 86 
 87 git br <new_branch> # 创建新的分支
 88 
 89 git br -v # 查看各个分支最后提交信息
 90 
 91 git br --merged # 查看已经被合并到当前分支的分支
 92 
 93 git br --no-merged # 查看尚未被合并到当前分支的分支
 94 
 95 git co <branch> # 切换到某个分支
 96 
 97 git co -b <new_branch> # 创建新的分支，并且切换过去
 98 
 99 git co -b <new_branch> <branch> # 基于branch创建新的new_branch
100 
101 git co $id # 把某次历史提交记录checkout出来，但无分支信息，切换到其他分支会自动删除
102 
103 git co $id -b <new_branch> # 把某次历史提交记录checkout出来，创建成一个分支
104 
105 git br -d <branch> # 删除某个分支
106 
107 git br -D <branch> # 强制删除某个分支 (未被合并的分支被删除的时候需要强制)
108  分支合并和reba
109 git merge <branch> # 将branch分支合并到当前分支
110 
111 git merge origin/master --no-ff # 不要Fast-Foward合并，这样可以生成merge提交
112 
113 git rebase master <branch> # 将master rebase到branch，相当于： git co <branch> && git rebase master && git co master && git merge <branch>
114  Git补丁管理(方便在多台机器上开发同步时用)
115 
116 
117 git merge <branch> # 将branch分支合并到当前分支
118 
119 git merge origin/master --no-ff # 不要Fast-Foward合并，这样可以生成merge提交
120 
121 git rebase master <branch> # 将master rebase到branch，相当于： git co <branch> && git rebase master && git co master && git merge <branch>
122 
123  Git暂存管
124 git stash # 暂存
125 
126 git stash list # 列所有stash
127 
128 git stash apply # 恢复暂存的内容
129 
130 git stash drop # 删除暂存区
131 
132 Git远程分支管理
133 
134 git pull # 抓取远程仓库所有分支更新并合并到本地
135 
136 git pull --no-ff # 抓取远程仓库所有分支更新并合并到本地，不要快进合并
137 
138 git fetch origin # 抓取远程仓库更新
139 
140 git merge origin/master # 将远程主分支合并到本地当前分支
141 
142 git co --track origin/branch # 跟踪某个远程分支创建相应的本地分支
143 
144 git co -b <local_branch> origin/<remote_branch> # 基于远程分支创建本地分支，功能同上
145 
146 git push # push所有分支
147 
148 git push origin master # 将本地主分支推到远程主分支
149 
150 git push -u origin master # 将本地主分支推到远程(如无远程主分支则创建，用于初始化远程仓库)
151 
152 git push origin <local_branch> # 创建远程分支， origin是远程仓库名
153 
154 git push origin <local_branch>:<remote_branch> # 创建远程分支
155 
156 git push origin :<remote_branch> #先删除本地分支(git br -d <branch>)，然后再push删除远程分支
157 
158 Git远程仓库管
159 git remote -v # 查看远程服务器地址和仓库名称
160 
161 git remote show origin # 查看远程服务器仓库状态
162 
163 git remote add origin git@ github:robbin/robbin_site.git # 添加远程仓库地址
164 
165 git remote set-url origin git@ github.com:robbin/robbin_site.git # 设置远程仓库地址(用于修改远程仓库地址) git remote rm <repository> # 删除远程仓库
166 
167 创建远程仓库
168 
169 git clone --bare robbin_site robbin_site.git # 用带版本的项目创建纯版本仓库
170 
171 scp -r my_project.git git@ git.csdn.net:~ # 将纯仓库上传到服务器上
172 
173 mkdir robbin_site.git && cd robbin_site.git && git --bare init # 在服务器创建纯仓库
174 
175 git remote add origin git@ github.com:robbin/robbin_site.git # 设置远程仓库地址
176 
177 git push -u origin master # 客户端首次提交
178 
179 git push -u origin develop # 首次将本地develop分支提交到远程develop分支，并且track
180 
181 git remote set-head origin master # 设置远程仓库的HEAD指向master分支
182 
183 也可以命令设置跟踪远程库和本地库
184 
185 git branch --set-upstream master origin/master
186 
187 git branch --set-upstream develop origin/develop
```



## 四、 Python!

## 1. Python 语言

> 只提及一些重点，更详细的就请到一些 Python 教程网站学习吧。

为了让从程序员从~~秃头~~事业中解脱，在开源世界里诞生了名为大蟒蛇（Python）的编程语言。

它带来了什么？

- 提供了完整的软件开发标准库。
- 适应多种编程方式。
- 用尽量少的代码完成更多工作。
- 适应时间短、变化快的需求。
- 让编程工作看起来更像是在“搭积木”。
- 开源社区长期贡献了大量的第三方库。
- 可拓展 C 、 C++ 等其他语言编写的模块。
- 满足了想偷懒的愿望。

它是一门易用的动态编程语言，可以看作现代入门编程语言的起点，程序员平时或多或少都需要使用 Python 代码帮助完成一些日常、简单、重复的脚本操作。

相比其他编程语言，它看起来会很容易理解和使用，对于非专业人士也可以轻松使用起来，以 “Hello, World” 为例。

- C 

```c
#include <stdio.h>

int main(void) {
  printf("Hello, World!\n");
  return 0;
}
```

- C++

```c++
#include <iostream>
using namespace std;

int main() {
  cout << "Hello, World!" << endl;
  return 0;
}
```

- Java

```java
class HelloWorld {
  public static void main(String[] args) {
    System.out.println("Hello, World!");
  }
}
```

- JavaScript

```javascript
alert("Hello World")
```

```javascript
document.write("Hello World")
```

```javascript
console.log("Hello World")
```

- Python

```python
print("Hello, World!")
```

不难看出，从人类自然语言的角度来看 Python 语法简单直接，减少了不必要的讯息。

## 2. 它是怎样工作的呢？

在编辑框上编写的 Python 代码，实际上是依次输入到实时运行的解释器程序当中的。

例如下述代码：

```python
tmp = 1 + 1
print(tmp)
```

运行它后就会输出 2 ，其中 tmp （变量）等于 2 ，如果这时候再运行下述代码。

```python
tmp = tmp + 1
print(tmp)
```

这时候就会输出 3 ，表示 tmp （变量）等于 3 了。

这是因为每一次运行的 Python 程序都并非是一个全新的开始，它是一直存在于一段程序当中的，只有当解释器程序退出后，才是真的结束程序，所以上一次运行的结果并没有清除，这也是程序不需要编译的原因。

这是与 C / C++ / JAVA 一类编程语言相冲突的地方，我们基于这个差异将 Python 称为动态语言，与此关联的还有 JavaScript 和 Lua 等编程语言。

实时上还有各种各样支持 Python 语言的解释器，虽然写的都是 Python 代码，但并非同一个事物。

我们常用的 Python 编程环境通常指 C 语言实现的 Python 解释器，涵盖 Python2.7 ~ Python3.10 的语法。

而在其他领域来说，有各式各样的 Python 语言的实现，如下：

- MicroPython 使用 Python3.5 语法

- Jython 使用 Java 实现的 Python 语言

- PyPy 通过 JIT 优化的 Python 语言

- IPython 基于 Python 语言的交互接口

也就是说 Python 这个名词，不一定是说 Python 编程语言，还可能是解释器，也可能是程序，这可能会有利于你理解 Python 这个事物背后可能存在的事物。

> 2020 年后不再提及 Python2.7 的任何内容，今后描述的 Python 以 Python3 的语法为准。

## 3. 这一切都这么美好？

并不是。

在这么多编程语言中，Python 对于初学者来说是很上手且简单的，对于一些调用各种库的代码、不在意运行效率，甚至是代码的可维护性也可以忽略的场合，随手一写就可以完成任务。

但代价就是想提升你瞎写程序的性能，你要付出更多的时间去做优化。

> 写出文章不难，写好文章才难。

因为最初不了解 Python 所写出的代码，就像小孩子的涂鸦，到处复制粘贴，以至于写出来的代码东拼西凑整合起来的。

到了这时候，你会发现，一旦你想要改进它是很难做到的，从一开始就不了解它，又谈何改进。

所以这里提及一下，传统的编程语言入门要经历的过程：

- 学习计算机历史
- 学习计算机语法
- 学习编程范式
- 学习使用开发工具
- 学习使用调试代码
- 学习程序设计

而使用 Python 语言速成入门培养兴趣和获得成就感的代价就是以后从事这份职业会花费额外的时间补计算机的基础。

> 至少 Python 能让你点火先把火箭飞起来，而不用把火箭制造原理研究透彻了再起飞。

## 4. 学哪个语言更好？

至于哪个更好，这里无法做出评价，建议顺应时代潮流，先解决问题，其他的再说。

- 黑猫白猫抓住老鼠就是好猫。
- 实践是检验事实的唯一标准。

最终怎么选择，就取决于你自己了。

## 5. 在哪学？

[Python教程 - 廖雪峰的官方网站 (liaoxuefeng.com)](https://www.liaoxuefeng.com/wiki/1016959663602400)

[Python 基础教程 | 菜鸟教程 (runoob.com)](https://www.runoob.com/python/python-tutorial.html)