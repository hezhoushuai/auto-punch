# auto-punch
autojs+tasker的自动打卡**晓黑板**的脚本，扔个手机在公司就能一直打一直打

安卓环境，用autojs+tasker实现。

## 使用

这个脚本需要你在公司放一个安卓手机，不用root。

<details>

#### 在设置的开发者模式中，选中直接进入系统

最新更新的版本，已经可以解锁屏幕了，只是需要不设密码。上滑动进入系统的那种。

![set](https://tva1.sinaimg.cn/large/006y8mN6gy1g7f1axqn8kj30u01hc0x1.jpg)

</details>

### 安装autojs和tasker

在仓库里面有autojs和tasker的包，安装一下

### 设置autojs

主要打开无障碍服务

![auto3](https://tva1.sinaimg.cn/large/006y8mN6gy1g7ezim97psj30u01hc446.jpg)

### 导入脚本

脚本就是`script.js`，可以在autojs里面新建一个文件，命名为script.js，然后把仓库里的代码复制进来。

这个文件存的路径是`/storage/emulated/0/脚本/<文件名>`

可以保存运行一下，看能不能打卡😉

![auto](https://tva1.sinaimg.cn/large/006y8mN6gy1g7ezjnnko2j30u01hcwjn.jpg)

### 用tasker设置定时

我查到的资料都说，autojs自带的定时不咋地，一般的操作是用tasker负责定时。

主要的设置参考[这个readme](https://github.com/e1399579/autojs/blob/master/README.md)的tasker定时方法



先设置**任务**，再设置**配置文件**

![tasker](https://tva1.sinaimg.cn/large/006y8mN6gy1g7f1b8ykynj30u01hcq4x.jpg)

#### 设置任务

1. 右下角点击新建，起个名字。
2. 再点击右下角，点击系统、操作意图
3. 依次填写

- 类别(Category)：`Default`
- Mime类型(MimeType)：`text/javascript`
- 数据(Data)：`file:///storage/emulated/0/脚本/script.js`
  如果起了其他名字，那么文件名也要相应改变
- 包名(PackageName)：`org.autojs.autojs`
- 类名(ClassName)：`org.autojs.autojs.external.open.RunIntentActivity`
- 目标(Target)：`Activity`

4. 这就已经设置好了，可以长按这个任务，点击右上角`▶播放`按钮，可以跑跑看脚本，有没有什么问题

#### 设置配置文件

开始定时

1. 点击右下角新增，也是起个名字
2. 选择时间，挑一个想要打卡的时间，结束时间和开始时间相同，“每”那里不用写
3. 确定后选择刚才创建的打卡任务即可，记得点右上角的✅来保存设置

### 现在就可以开始大摇大摆地不用打卡了😎！

## todo

- [ ] 如果不是消息栏，需要点击到消息栏

## 参考

- [tasker教程](http://tieba.baidu.com/p/5288908002?share=9105&fr=share&see_lz=0)

- [autojs b站文字教程](https://www.bilibili.com/read/cv1328014)

- [autojs教程](https://blog.csdn.net/QiHsMing/article/details/86762007)

- [参考的git仓库](https://github.com/e1399579/autojs/blob/master/README.md)

- [文档是最有用的，就是搜索很烂😂](https://hyb1996.github.io/AutoJs-Docs/#/widgetsBasedAutomation)

- [autojs的git地址](https://github.com/hyb1996/Auto.js?files=1)