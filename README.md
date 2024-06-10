# 第一课
## Github
### 关键字查询
* awesome，去此标签类别中查询项目<br>
* python tutorial，查询资料，书籍，文档<br>
* socket sample，查询对应技术的代码样本<br>

## github三要素
### Repository 仓库
仓库是github项目管理储存基本单位
一个仓库中储存一个项目，一个用户可以拥有多个仓库，一般仓库分为public ， private
### Commit 提交
程序员在整个开发周期，有大量的对代码资源的迭代和修改，都可以通过commit的方式进行记录，便于程序员回溯代码，即是这些代码被酬除提交便于使用者观察整个工程的开发流程以及设计流程
### Branch 分支
在仓库中可以包含多个分支，分支才是代码文件的第一存储单位，默认的仓库主分支为master/main
![仓库分支](https://i.postimg.cc/rpR1YL8F/image.jpg"仓库分支")

## 仓库内容
* Code，资源存储，代码资源，二进制，项目管理脚本，许可证等等<br>
* issues， 使用时遇到的bug或进行提交， 等待反馈<br>
* README， 使用markdown语言编写， 工程自述文件， 开发进度， 版本更新， 使用介绍等等<br>
* LICENSE：许可证GPL 2.0,3.0. Apahce 2.0, Mit, 这些许可证, 给使用者最大使用权限以及最少的限制

## Git 软件，分布式版本控制系统
仓库管理软件，使用git管理私人代码或企业代码
https://i.postimg.cc/mZKt8FPM/image.png
![发布版本](https://i.postimg.cc/mZKt8FPM/image.png"发布版本")
仓库管理软件，使用git管理私人代码或企业代码

# 第二课
## 设备认证
***如何让网站的账户与设备绑定，后续完成代码的管理，上传下载***
1. 创建本地仓库（后续对仓库的操作， 都要在仓库位置(master)）
```bash
	git init
```
2. 查看git的配置文件
```bash
        git config --list
```
3. 绑定账号（SSH远程访问）
```bash
	git config --global user.email "邮箱"
	git config --global user.name "用户名"
```
4. 创建本地密文
```bash
	ssh_keygen -t rsa -C "邮箱"
```
5. 去对应的目录查找密文文件
6. 在.pub文件中复制密文
7. 在settings-SSH key and GPG-new ssh key中粘贴
8. 测试关联是否成功
```bash
	ssh -T@github.com
```
***为目标仓库起别名，定位目标仓库，后续上传***
* 为ssh仓库地址创建别名为prigin
```bash 
	git remote add origin "ssh地址"
```
* 删除origin别名
```
	git remote remove origin
```

## 本地设备与云端仓库的交互逻辑
![本地与云端的交互](https://i.postimg.cc/G3Z7xqdC/image.png"本地与云端的交互")
* 添加内容
```bash
	git add
```
* 删除本地文件并删除仓库数据
```bash
	git rm
```
* 恢复被删除文件（仓库存在）
```bash
	git restroe
```

## 代码更新的依赖关系被破坏
本地内容要比云端新，完成更新替换，但是如果直接修改云端内容，导致，本地内容无法再次提交
先拉取ght pull 云端内容 与本地内容合并或操作，而后再次推即可
拉取云端内容
```bash
	git pull --rebase origin master
```
* 忽略云端，保存本地
```bash
	git rebase --skip
```
* 忽略本地，保存云端
```bash
	git rebash --abort
```
* 本地云端合并 
```bash
	git rebase --continue
```

## 下载开源代码
```bash
	git clone "仓库地址"
```

## 分支Branch
关于分支的相关命令，创建分支，选择分支。合并分支等等

## Markdown 语言
github可以编写readme，文本修饰语言

# 第三课
Markdown，文本修饰语言，用特殊符号修饰正文效果<br>

## 标题修饰符\#

# 标题修饰符（一级标题）
## （二级标题）
### （三级标题）
#### （四级标题）
##### （五级标题）


## 正文内容

	输入正文内容，但是如果需要换行，用\<br\>标签

## 修饰正文

  *一段测试文本*<br>
  **一段测试文本**<br>
  ***一段测试文本***<br>
  ~~一段测试文本~~<br>
  突出`关键字`<br>
  使用空行和\<br\>都可以达到换行效果

## 分割线
  用\-\-\-表示分割线
---

## 应用效果用\>表示
> 世间万般兵刃，唯有过往伤人最深
>> 亚索
>>> 三级引用
>>>> 四级引用

## 列表修饰符
### 无须列表 \*
* 二次元
  * 原神
    * 钟离
* MOBA
  * 英雄联盟
  * DOTA2

### 有序列表 n.
1. 火影忍者
   1. 宇智波
      1. 鼬
      2. 斑
   2. 千手
      1. 柱间
      2. 扉间
2. 鬼灭之刃
   1. 碳治郎
   2. 祢豆子

### 混合列表
1. 测试
   * 测试
     1. 测试

### 表格
英雄|技能|排名
--|:--:|--:
镜|一二|1
妲己|一二三|23
姜子牙|一二三四|456

### 代码
```c
	#include<stdio.h>
```
```c++
	#include<iostream>
	using namespace std
```
```python
	improt <os>
```
```bash
	echo "测试"
	pwd
	ps aux
```

### 超链接技术

[https://github.com/2921333894/new](https://www.github.com"点击访问")

### 插入图片
![壁纸截图](https://i.postimg.cc/Jz20gDnj/image.png"壁纸截图")
