---
title: IntelliJ Idea 简明笔记
categories: Tool
tags:
  - IntelliJ Idea
image: 'http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_1.jpg'
updated: 2019-03-03 00:11:00
date: 2019-03-01 10:21:17
abbrlink:
---
IntelliJ Idea Note
<!-- more -->
操作系统: windows 64位
Idea版本: 2018.3.5 (2019.1在beta中)
## 安装
![20190301_2](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_2.jpg)
![20190301_3](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_3.jpg)
![20190301_4](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_4.jpg)
![20190301_5](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_5.jpg)
![20190301_6](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_6.jpg)
注册激活码，如果失效去这个网站获取[http://idea.lanyus.com/](http://idea.lanyus.com/)
![20190301_7](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_7.jpg)
## 导入项目
1. 新建一个文件夹，可以命名为ideaWorkspace(已经有父子模块项目关系的可以直接open即可)
2. 将需要导入的项目文件夹拷贝到里面
3. open该工作空间文件夹
4. 设置成maven项目
![20190301_9](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_9.jpg)
![20190301_10](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_10.jpg)
到此项目就算导入完成了。

Idea中没有workspace的概念，它顶级目录叫Project,次级目录是Module,每个project都有自己的
.idea文件夹。

## 设置
1. 设置jdk
![20190301_11](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_11.jpg)
![20190301_12](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_12.jpg)
到这里就可以直接运行项目了。
![20190301_13](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_13.jpg)

2. 修改字体大小
![20190301_14](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_14.jpg)

3. 修改文件编码
![20190301_15](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_15.jpg)
注：如果Tomcat 控制台输出乱码，并且控制台字体设置的字体包含中文，可以在 Tomcat 的 VM 
参数上加上：-Dfile.encoding=UTF-8
![20190301_16](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_16.jpg)

4. 清楚缓存和索引
Idea利用缓存和索引来加快搜索查询的速度，但有时也会出现问题，这时可以清除缓存来解决问题：
![20190301_17](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_17.jpg)
一般选择第一个就可以，清除并重启，这里实际上就是删除了system文件夹，可以手动删除，重启
Idea它会自动创建新的system文件夹，system路径位于自己的用户目录下：
> /c/Users/LYPC/.IntelliJIdea2018.3/system

5. 自动编译
因为自动编译比较耗费资源，所以idea默认没有开启自动编译，可以手动设置：
![20190301_18](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_18.jpg)
注意：这里的自动编译不是保存后自动编译，而是在编辑器里输入代码的时候自动编译，
所以比较耗费资源，可以用快捷键`ctrl + F9`来进行项目编译。

## 常用快捷键
idea默认快捷键查看及修改地址：
![20190301_8](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_8.jpg)
在设置前，应注意快捷键冲突，关掉搜狗输入法等的快捷键。
```txt
windows版：

搜索：
ctrl + e  最近打开的文件列表->列表大小可调->在settings->editor->general->limits->recent files limit
ctrl + n  搜索java类文件
ctrl + f  当前文件搜索
ctrl + shift + f   查找整个项目或指定目录内文件
ctrl + shift + v   拷贝历史记录板
ctrl + shift + e   最近修改文件列表

窗口处理：
ctrl + alt + s     打开idea setting 设置
alt + 1            显示project视图
ctrl + F4          关闭当前编辑文件
ctrl + shift + F12 最大化编辑器

tab可以多行显示或只显示一个tab,在settings->editor->General->Editor tabs->placement

光标选择：
ctrl + w  智能选择代码块
ctrl + shift + w   与ctrl+w配合使用，是递进取消选择单词
ctrl + alt + 左   退回上一个操作地方  可以改成alt + [
ctrl + alt + 右   前进到上一个操作地方  可以改成alt + ]
ctrl + shift + backspace   退回上次修改的地方
F2  跳转到下一个错误或警告位置

编辑：
ctrl + z,c,x,/  功能不变: 搜索，撤销，复制，剪切,粘贴, 注释
ctrl + shift + z  恢复撤销，相当于前进
ctrl + r  替换
ctrl + y  删除光标所在行 或 选中的行
ctrl + d  复制当前行并粘贴到下一行 或 复制选中内容并粘贴到光标后,可以改成粘贴到下一行而不是
            光标后，修改为duplicate entire lines
alt + shift + 上   当前行向上移动一行
alt + shift + 下   当前行向下移动一行
ctrl + alt + o  优化import的包
ctrl + alt + l  格式化代码，可以对当前文件或整个包目录使用
ctrl + alt + t  对选中代码弹出环绕层，有if/else, try/catch等
ctrl + shift + /   代码块注释

代码提示：
ctrl + space  这个windows系统上时切换输入法，可修改为ctrl + ; 表示基本代码补全
ctrl + shift + space   智能代码补全 可改为ctrl + shift + ;
postfix code completion:  for,nn,null,var
自定义：settings->editor->general->postfix completion
alt + enter   智能辅助，跟据位置不同提示结果不同，可用于生成get/set方法，生成接口或实现类，
              还可以进行重构
alt + insert  同eclipse,生成set/get,constructor,toString()等

编译：
ctrl + F9       make project编译项目

重构：
ctrl + shift + r   替换内容 整个项目或指定目录
alt + shift + f    加入到收藏夹中
shift + F6       重构: 重新命名
ctrl + alt + m   重构: 提取方法


mac 版：

搜索：
command + e          #   recent files
command + o          #   navigate class
command + F12        #   file structure
command + f          #   edit: Find find
command + shift + f   # find in path
command + shift + v   # paste from history
command + shift + e   # recently changed files

窗口处理：
command + ,      # file setting
command + 1      # tool windows Project
command + w      # editor tabs close
command + shift + F12 # hide all tool windows

光标选择：
option + up          #   extend selection
option + down   # shrink selection
command + [     # navigation back
command + ]     # navigation forward
command + shift + backspace # last edit location
F2  # next highlighted error

编辑：
command + z,c,x,/    #   find,undo,copy,cut,comment
command + shift + z  #   redo
command + r          #   replace
command + backspace  #   delete line
command + d          #   duplicate lines
option + shift + up  # code move line up
option + shift + down  # code move line down
command + option + l  # reformat code
command + option + t  # code surround with
ctrl + shift + /     # comment with block comment
ctrl + option + o     # optimize imports

代码提示：
ctrl + ;     # basic code complete
ctrl + shift + ;  # smart code complete
command + shift + enter  # complete current statement
option + enter     # show intention actions
ctrl + enter     # code generate

重构：
command + shift + r   # replace in path
option + shift + f    # other add to favourites
shift + F6           # refactor rename
command + option + m  # refactor extract method

编译：
command + F9         #   build project
```

注：如习惯vim操作，可以下载插件IdeaVim
![20190301_19](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_19.jpg)
安装后重启，设置开关vim模式快捷键,默认ctrl+alt+v,改成F1,同时把context help的remove掉。
![20190301_20](http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_20.jpg)
vim默认寄存器和系统剪贴板共享:
在c:\Users\用户名\下新建文件_ideavimrc文件(mac是~目录.ideavimrc):
> set clipboard+=unnamed

热部署插件JRebel

## 小设置
scroll from source
inject language
设置自动导包: settings->editor->general->auto import->check 2
代码提示忽略大小写：settings->editor->general->code completion->match case uncheck



<hr />
<img src="http://wutaotaospace.oss-cn-beijing.aliyuncs.com/image/20190301_1.jpg" class="full-image" />