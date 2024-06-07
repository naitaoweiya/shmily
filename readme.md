# GitHub
---
## GitHub 关键字查询  
   awesome,去此标签中查询项目<br>
   eg：Cpp awesome 查找有cpp标签的项目<br>
   python tutorial,查询资料，书籍，文档<br>
   socket sample，查询对应技术的代码样本<br>
---
## GitHub 三要素
### Repository 仓库
    仓库是github项目管理存储基本单位,
    一个仓库中存储一个项目，
    一个用户可以拥有多个仓库，
    一般仓库分为public，private。
### Commit 提交
    程序员在整个开发周期，
    有大量的对代码资源的选代和修改，
    都可以通过commit的方式进行记录,
    便于程序员回溯代码，
    即是这些代码被删除，便于使用者观察整个工程的开发流程以及设计流程  
### Branch 分支
    在仓库中可以包含多个分支，
    分支才是代码文件的第一存储单位，
    默认的仓库主分支为master/main
    不仅可以管理代码存储， 便于多人协作开发
![](https://picture.gptkong.com/20240607/22324e0689b0db43f8810f84f4e7f1a175.jpg)
---
## 仓库内容
    Code，资源存储，代码资源，二进制，项目管理脚本，
    许可证等等issues，使用时遇到的bug或进行提交,等待反馈README，
    使用markdown语吉编写，工程自述文件，开发进度，版本更新使用介绍等等
    LICENSE 许可证
    GPL 2.0,3.0.Apahce 2.0, Mit,i这些许可证，
    给使用者最大使用权限以及最少的限制
---
## Git 软件,分布式版本控制系统
   仓库管理软件，使用git管理私人代码或企业代码
![](https://picture.gptkong.com/20240607/22479663c471b049e2a8aff9caf1327cb8.jpg)
---
## 设备认证
### 1.如何让网站的账户与设备绑定，后续完成代码的管理，上传下载

  ```c
        git init //创建本地仓库 *后续对仓库操作都在仓库位置（master）
	    git config --list //查看git的配置文件
	    git config --global user.email “邮箱”
        						SSH远程访问
        git config --global user.name”用户名”
        ssh-keygen -t rsa -C“注册邮箱”//创建本地密文
        *去对应的目录查找密文文件
        rsa.pub复制密文，粘贴settings ->SSH key and GPG->new ssh key->粘贴
        ssh -T git@github.com//测试关联是否成功

  ```
### 2.为目标仓库取别名，定位目标仓库，后续上传
```c
    	git remote add orgin “ssh地址”//为ssh仓库地址创建别名为origin
	git remote remove orgin //删除origin
```
---
##  本地设备与云端仓库的交互逻辑
![](https://picture.gptkong.com/20240607/2313c5c4a63d6d4ef0b3541b004a8f7dbb.png)
```c
        git add .//添加内容<br>
        git rm //删除本地文件并删除仓库数据<br>
        git restroe //恢复被删除(仓库存在)<br>
```
---
## 代码更新的依赖关系被破坏
   本地内容要比云端新，完成更新替换，
   但是如果直接修改云端内容，导致，本地内容无法再次提交
   做法：
1. \*先拉取git pull云端内容与本地内容合并或操作，而后再次推即可
2. ```c
           git pull --rebase origin master  
   	git rebase --skip//”忽略本地内容保留云端内容”  
   	git rebase -abort// ”忽略云端内容保留本地内容”  
   	git rebase --continue  
   ```
---
## 下载开源代码
   ```c
   	git clone "https仓库地址"//下载开源项目code资源
   ```
---
## 分支Branch
   \*关于分支的相关命令，创建分支，选择分支，合并分支
---
## Markdown 
1.  \# 标题修饰符
  有几个#就是几级标题 可以无限下去
  可以用\<br\>换行
2. \*\* 文字修饰符
   一对** 在中间输入文字 表示倾斜文字
   两对**** 中间键入文字 表示加粗
   三对****** 表示即倾斜也加粗

3. ---表示分割线
4. \>大于号表示引用
5. 列表修饰符 \*
   表示无序列表
   直接用数字加句号 再加空格表示有序列表
6. 表格
   \|表示 可以用:来进行左右对齐
   eg：不加为左对齐|::|为居中对齐|:为右对齐
名称|技能|排行
--|:--:|--:
神里绫华|雾切之回光|18
7. \`\`\`表示代码片段
![](https://picture.gptkong.com/20240607/2345a0bb9ff8ce4479a85285d04d055d2f.png)
8. \[\]\(\) 表示超链接
   前方为超链接名称 后方为超链接具体链接 可以在（）内添加“”来进行超链接的命名 光标移动到超链接会弹出具体作用
[哈尔滨理工大学](http://www.hrbust.edu.cn "全中国最好的大学")
9. \!\[\]\(\) 表示图片插入
   跟超链接一样 只不过多了一个！表示区别
![校徽](https://picture.gptkong.com/20240607/2352d1472fe4f7496fb0274e72433fe424.png)
