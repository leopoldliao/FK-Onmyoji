# FK-Onmyoji
**阴阳师抗检测多功能护肝辅助脚本**

 - 游戏多开，多种模式并发
 - 鼠标键盘模拟输入，指针变速移动，非固定点点击，随机间隔连点
 - 掉线、失败、占用警报提示
 - 抗失效随机点击复位
 - 自动接受悬赏封印邀请
 - QQ消息反馈

 
----------


# 开始

## 方案1：直接下载可执行程序 ##
 [Beta 1.0.0下载地址][1]

## 方案2：手动部署Python脚本运行环境 ##

 1. 安装Python3.7（>=3.7）。

 2. 安装拓展库：
    **PyAutoGUI**
    **OpenCV-Python**
    **PyWin32**

 3. 调整阴阳师窗口分辨率至固定合适大小（可选）：
    -打开阴阳师安装目录下的**neox.xml文件**，修改**WindowClientHeight**（窗口高度），**WindowClientWidth**（窗口宽度）。推荐宽度为683，高度为384。

 4. 根据**screenshots文件夹**下的截图样例截取图片（推荐宽高下可跳过）。

 5. 运行**screenshots文件夹**下的**convert.py**：（可选，截取新截图后推荐，可防止libpng相关警告，需要安装**ImageMagick**，下附下载地址）
    -打开**convert.py**文件修改**imageMagickPath**变量的值为**ImageMagick安装路径**后运行该脚本。
 [ImageMagick-6.2.7-Q16下载地址][2]

 
----------


## 使用 ##
 1. 手动完成一局**已选模式**以锁定阵容（**结界突破**、**章节探索**除外）。
 2. 以**管理员身份**运行（必须，以防止鼠标键盘模拟输入失效）。
 3. 根据提示输入相关信息（因为设置的窗口宽高不包括边框宽高，故需将**高度**适当增大，比如30）
	-样例：
![样例][3]
 4. 挂机（按P**暂停/继续**）。

## 相关问题 & 注意事项 ##
 1. **注意**：以下情况**蜂鸣器**会发出**警报声**（加*的建议进行人工操作）：
    -已选模式全部结束
    -检测到悬赏封印邀请
    *-失败（警报声结束后关闭所有游戏，结界突破除外）
    *-失去连接
    *-脚本可能失效，超过5分钟未进行任何操作
    *-检测到账户在其他设备登录（警报声结束后关闭所有游戏）
 2. **问题**：窗口起始位置是什么？
    -窗口边框左上角相对于屏幕左上角的位置
 3. **问题**："QQ反馈者"必填吗？填什么？
    -可选，请填入聊天窗口的标题，不需要请填写任意字符。聊天窗口位置没有要求，不能最小化。
 4. **问题**：怎样去除"**警报声结束后关闭所有游戏**"的功能？
    -删除代码`os.system("taskkill /IM onmyoji.exe /F")`
## 关于 ##
学了一天Python来**练手**的。


  [1]: https://t00y.com/file/15016760-403156759
  [2]: https://t00y.com/file/15016760-403129810
  [3]: https://github.com/BluePlumStudio/FK-Onmyoji/blob/master/sample.png