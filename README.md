##  Autovisor

智慧树视频课辅助脚本，开启挂机摸鱼时代~

**新学期必备干货, 建议收藏备用 !!**

**Github项目主页：**[CXRunfree/Autovisor](https://github.com/CXRunfree/Autovisor)

------
#### 2025/4/3 stable-3.16.2 更新

**注意: ** 本次更新调整了`configs.ini` 文件的可选功能, 从旧版本迁移时请先看清楚 !

**近期更新:**

- **新增自动隐藏播放界面功能(可选)**, 当出现人机验证时会自动显示;

- **新增对 "翻转课" 视频的支持 @PencilCore**
- **通过域名拦截阻止人机验证弹窗出现(可选) @mc139790**
- 修复了播放页部分提示框未成功关闭导致程序卡住的bug;
- 其他代码层面调整优化, 提高了程序稳定性.

如若此版本存在稳定性bug，请及时提出issue  ~

一定要附上报错信息，特别是`logs/`目录下的日志文件；不论类型, 越详细越好 !

------

#### 一、程序介绍:

**项目简介：**

这是一个可无人监督的自动化程序，基于微软的Playwright框架，由Python和JavaScript编写而成；相对于常见的油猴脚本，本程序可有效防止被网页检测。核心原理是使浏览器模拟用户的点击操作。

**程序功能:**
- **支持自动登录**
- **自动通过滑块验证(可选)**
- **自动播放和切换下一集**
- **跳过弹窗和弹出的题目**
- **自动静音、调成指定的倍速**
- **检测视频是否暂停并续播**
- **支持刷习惯分**
- **支持智慧共享课**
- **支持翻转课**
- 检测当前学习进度并后台实时更新
- 根据当前时间自动设置背景颜色(白昼/暗夜)
- 完成章节时将提示已刷课时长
- 各种自定义配置

#### 二、使用须知:

1.请确保系统为windows10及以上

2.文件夹内有 **configs.ini文件** (可能没显示 **.ini**后缀名)，请用文本编辑器打开;

3.填写配置文件

- 默认启动Edge(win10及以上自带), 也可指定为Chrome
- 文件里的 **EXE_PATH项** 用于自定义浏览器路径, 但必须精确到**浏览器可执行文件的位置**;

​    若不填此项, 就会启动位于系统默认位置的浏览器。

​    不知浏览器的安装路径? 请看下方  **四、常见问题** 

4.根据文件内的说明填写好配置信息，一定要**保存后**再退出。

**注意: 所有配置项都不加"引号"**

<img src="https://i-blog.csdnimg.cn/direct/e3f06598535c4b48bc1e8a52eb2d0ef8.png"/>

4.运行 **Autovisor.exe**，会自动打开浏览器，进入网课界面后就能自动刷课了 !

(如果未设置 **enableAutoCaptcha=True**, 则需要**手动完成**登录时的滑块验证.)

------

#### 三、发行版下载:

Github: [Releases · CXRunfree/Autovisor (github.com)](https://github.com/CXRunfree/Autovisor/releases)

网盘备用: [[蓝奏云\] Autovisor-for-windows](https://wwk.lanzouj.com/b05evsxif) 密码:492l

这是已经打包好的程序, 若需要**源代码**请于Github项目主页下载.

#### 四、常见问题 :

0.为什么解压后没有Autovisor.exe / 运行报错**缺失依赖文件**?

- 可能是被杀毒软件误杀了, 考虑暂时关闭杀毒软件;

1.为什么会出现一个命令行黑框?

- 这是程序运行的后台，你可以查看当前运行的状态;

2.为什么网页一片空白/无法加载课程界面,一段时间后程序就退出了?

- 大概率你在配置文件里填入的**课程链接有误**;

3.为什么运行程序只出现后台却没出现浏览器界面？

- 只要后台未异常退出就不必担心; 如果出错可能是你的浏览器安装路径有问题

4.我想自定义要启动的浏览器, 但是找不到装在哪里? 

- 打开你的浏览器, 在地址栏中输入 Chrome://version 回车之后, 如图的"可执行文件目录" 就是浏览器安装目录了。

  
  
  <img src="https://i-blog.csdnimg.cn/blog_migrate/e8fd696257e0b4623a19d4a9e0448bfd.png" alt="img">

5.关于弹题关不掉/程序卡住的问题:

- 因为弹题是时刻有可能发生的, 而弹题检测不是时刻都进行, 所以这个问题不能完全消除;
- 3.14以上版本使用 异步+协程 进行弹题检测，目前效果非常好，建议更新使用。

6.我已经打赏过了,不希望再弹赞赏码怎么办?

- 感谢您对本项目的支持~ ~  只需要删掉`res/QRcode.jpg`文件就好了 !

------

**已知Bug:**

- 浏览器版本太新可能导致第一次启动失败, **重启程序**才能解决;
- **长时间挂机**有概率弹出人机验证, 程序检测到后会暂停操作，直到手动验证完成; 
- 浏览器窗口若**最小化**可能导致视频播放进度不增加;
- 若出现其他异常崩溃，请提交issue并附上报错信息；

**碎碎念:**

觉得体验还不错 ?  请留下你宝贵的Star ⭐, 并分享给更多有需要的人!

或者为项目发电支持一下 ~  (狠狠push才会有动力 ^-^)

<img src="https://i-blog.csdnimg.cn/blog_migrate/0d254d88c1cd0cb0a2fe6c50f8992efb.png" alt="img" style="zoom: 50%;" />

**作者的CSDN:** [欢迎关注~](https://blog.csdn.net/Runfreeone)

**注意：本程序只可用于学习和研究计算机原理**

