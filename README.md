# 目录：

1. ADB not responding. If you'd like to retry, then please manually kill "adb.exe" and click 'Restart

2. 快捷键问题

3. 没找到Preferences

4. R文件在哪？？

5. 删除项目

6. 新建的项目没有R文件

7. Cannot set up guest memory 'android_arm': Invalid argument

8. 快捷键，代码提示

9. 给Android studio 安装Genymotion 插件

10. VirtualBox 4.2.12

11. Android项目上出现红叉，而代码和路径无误

12. 怎么用手机链接

----------


## 1. ADB not responding. If you'd like to retry, then please manually kill "adb.exe" and click 'Restart

解决：上网搜索了一下，原来这个东西是要使用端口5037的，管理员打开cmd，输入指令netstat -aon|findstr 5037看一下哪个进程在占用



## 2. 快捷键问题

解决：Preferences -> Keymap    可以自己修改，也可以改为自己熟悉的工具的快捷键

## 3. 没找到Preferences

解决：File -> Settings

## 4. R文件在哪？？

解决：

## 5. 删除项目

解决：

- 1、File -> Project Structure （工程结构）

- 2、选中想删除的project -- 单击红色的减号 -- 出现下图 -- Yes

- 3、回到项目目录，右键出现delete 选项，就可以删除了

## 6. 新建的项目没有R文件

解决：删了重新创建，目测是因为在新建项目的时候进行操作打断了创建过程，出现下图就算完成

## 7. Cannot set up guest memory 'android_arm': Invalid argument

解决：内存不足，需要修改模拟器外置存储器的大小

## 8. 快捷键，代码提示

解决：在eclipse 中代码提示叫Content Assist，快捷键是alt+/

在android studio 中代码提示叫Class Name Completion，快捷键是ctrl+alt+space

修改选中右键第一个

## 9. 给Android studio 安装Genymotion 插件

看视频发现老师用的是Genymotion的模拟器特别流畅，在看自己的模拟器卡的不行，果断换

解决：

1、file -> settings  -> plugins 如图

2、点击下图的Browse repositories...

3、输入genymotion

白色这张是没安装的点击，黑色是我安装完的，安装完会提示你重启

4、重新启动后出现下图

5、点击图标初次点开需要我们设置一下genymotion的安装目录。

E:\Android\Genymobile\Genymotion

Genymotion warning: You must specify the path to the Genymotion folder to use this feature

genymotion警告：您必须指定路径的genymotion文件夹使用此功能

## 10.VirtualBox 4.2.12

Unable to load R3 module E:\Android\Oracle\VirtualBox/VBoxDD.DLL (VBoxDD): GetLastError=1790 (VERR_UNRESOLVED_ERROR).

返回 代码:

E_FAIL (0x80004005)

组件:

ConsoleWrap

界面:

IConsole {872da645-4a9b-1727-bee2-5585105b9eed}

解决：重装VirtualBox 4.2.12

## 11.Android项目上出现红叉，而代码和路径无误

DescriptionResourcePathLocationType

Error generating final archive: Debug Certificate expired on 12-4-25 上午8:35aaUnknownAndroid Packaging Problem

解决办法：

Project->Clean

然后重启工程。

原因：

To fix this problem, simply delete the debug.keystore file. The default storage location for AVDs is in ~/.android/avd on OS X and Linux, in C:\Documents and Settings\\.android\ on Windows XP, and in C:\Users\\.android\ on Windows Vista.

The next time you build, the build tools will regenerate a new keystore and debug key

为了解决这个问题，只要删除debug.keystore文件。为AVDS的默认存储位置是在~ / Android AVD。/ C在OS X和Linux，：\文件和设置\\。在Windows XP和Android，C：\用户\。Android在Windows Vista。

下次你建立，构建工具将生成新的密钥库和调试的关键

另外：

android的key到期，也会出现上述问题，解决方法是：C:\Users\Freshen\.android（不同OS路径应该不同）这个目录下有个文件debug.keystore删掉，然后关闭工程，再打开应该就可以。

## 12. 怎么用手机链接

android studio设置：

Run→Edit Configurations...→Android Application→app→General页签→Target Device，选择USB device

中兴V5 U9180手机端设置：

设置→其他→开发者选项→勾选[不锁定屏幕 always stay awake][USB调试][允许模拟位置]

用USB线连接手机，AS中点击运行，选择自己的真机就可以
