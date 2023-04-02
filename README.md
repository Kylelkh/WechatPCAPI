# WechatPCAPI
微信PC版的API接口，可通过Python调用微信获取好友、群、公众号列表，并收发消息等功能。可用于二次开发在线微信机器人、微信消息监控、群控软件、开发界面作多个微信控制软件等用途。

**当前版本:**

当前版本是免费版本

另有更稳定、更可靠、更强大的付费版本，点这里了解。[付费版本README](https://github.com/Mocha-L/WechatPCAPI/blob/master/README-BO.md)

**如果帮到你，帮我点个star。**
遇到问题可以提Issues，或关注公众号“刘大辉在路上”联系我。


## 延伸项目

有一些小伙伴在这个项目基础上做了其他功能，我列在下面供大家参考借鉴：

https://github.com/elliot-bia/msg_reply

https://github.com/mortimer-cra/AlarmRobot （微信提醒喵）



## 怎么用？

1. clone/下载源码到本地
2. 安装源码包里的微信客户端（你以前的版本和这个不一致的都需要安装这个）
3. 执行源码中的test.py

目前提供pyd和依赖的相关文件，通过python直接import即可使用，目录里的test.py即是调用示例。

## 环境支持情况

windows 7/10 测试通过

python 3.7.4 不是该版本可能会报错dll load 错误

**微信版本 目前仅支持V2.7.1.82版本，后续会考虑兼容其他版本，目录包里有该微信版本，直接下载安装即可。**

## 国内下载慢？

现在不支持百度网盘更新了，请进群获取最新版本代码和相关文件，有问题也可以在群里咨询讨论。



## 遇到问题？

1. 请保证微信版本是从我的包里装的。
2. 出现“找不到指定模块”，请安装python3.7运行，还不行的话，大致是因为windows相关运行库的缺失，请自行打开windows更新，或安装各个版本的运行时库。
3. 其他问题和接口问题请在Issues中提问。

## 函数文档注释

不知道怎么调用的话，可以使用``help(类名)``查看函数文档，如下：

    Help on class WechatPCAPI in module WechatPCAPI:

    class WechatPCAPI(builtins.object)
     |  WechatPCAPI(on_message=None, on_wx_exit_handle=None, log=None)
     |
     |  微信PC版的API接口--当前版本:@钊@
     |
     |  Methods defined here:
     |
     |  __init__(self, on_message=None, on_wx_exit_handle=None, log=None)
     |      类初始化函数
     |      :param on_message: 收到微信消息时的回调函数
     |      :param on_wx_exit_handle: 微信退出的回调函数，可空
     |      :param log: 日志句柄
     |
     |  get_myself(self)
     |      获取我的信息，即所登录账号的信息
     |      :return: 尚未登陆成功时为None, 登陆成功后为dict格式返回
     |
     |  send_card(self, to_user, wx_id)
     |      发送名片
     |      :param to_user: 发给谁（wx_id）
     |      :param wx_id: 要发送谁的名片（wx_id）
     |      :return: 无
     |
     |  send_file(self, to_user, file_abspath)
     |      发送文件
     |      :param to_user: 发给谁（wx_id）
     |      :param file_abspath: 文件在本地的绝对路径
     |      :return: 无
     |
     |  send_gif(self, to_user, gif_abspath)
     |      发送gif表情
     |      :param to_user: 发给谁（wx_id）
     |      :param gif_abspath: gif在本地的绝对路径
     |      :return: 无
     |
     |  send_img(self, to_user, img_abspath)
     |      发送图片
     |      :param to_user: 发给谁（wx_id）
     |      :param img_abspath: 图片在本地的绝对路径
     |      :return: 无
     |
     |  send_link_card(self, to_user, title, desc, target_url, img_url='')
     |      发送链接分享
     |      :param to_user: 发给谁（wx_id）
     |      :param title: 链接标题
     |      :param desc: 链接描述
     |      :param target_url: 链接URL
     |      :param img_url: 显示图片的URL
     |      :return: 无
     |
     |  send_text(self, to_user, msg)
     |      发送文本消息
     |      :param to_user: 发给谁（wx_id）
     |      :param msg: 文本消息内容
     |      :return: 无
     |
     |  start_wechat(self, block=True)
     |      启动微信，目前仅支持微信版本v2.7.1.82
     |      :param block: 是否阻塞，默认阻塞
     |      :return: 无
     |
     |  update_frinds(self)
     |      :return: 无
     |
     |  ----------------------------------------------------------------------


## 联系我

关注微信公众号“刘大辉在路上”，即可获取我的联系方式。

## 赞赏我

支持作者继续更新，请我喝杯咖啡


## 声明

**本项目仅供技术研究，请勿用于非法用途，如有任何人凭此做何非法事情，均于作者无关，特此声明。**
