# 微博用户信息爬虫

项目链接：https://github.com/RealIvyWong/WeiboCrawler/tree/master/WeiboUserInfoCrawler

## 1 实现功能

这个项目是用来根据用户id爬取微博用户信息的数据，并写入 sqlite 数据库。

而这个用户id是在[微博签到页爬虫](https://github.com/RealIvyWong/WeiboCrawler/tree/master/WeiboLocationCrawler)这个爬虫项目生成的`weibo.sqlite`数据库中读取的。所以想要爬自己有的一串用户id的数据的朋友，可能还需要在这个小爬虫上面再改改。

以及这个爬虫是需要自己微博登录的 **cookie** 的。

# 2 依赖环境

使用的是Python 3.7（在云上用过 3.5 也完全ok）。

需要额外的第三方库有 yagmail（用来发送邮件）,pandas，bs4, numpy。均可使用 pip 来安装。

```
pip install yagmail pandas bs4 numpy
```

## 3 使用方法

**step1.** 修改 cookie.txt 中的 cookie 改为自己微博登录的 cookie。（如何获取还请额外百度，非常多教程！）

**step2.** 修改代码中的邮箱账号密码以及数据库路径。

**step3.** Run！

## 4 文件说明

包含两个文件。

### cookie.txt

就是用来存放 cookie 的。

### WeiboUserInfo.py

爬虫本体。

## 5 爬取示例

如果开始成功运行之后，控制台输出大概是这样的。

![1545039042299](assets/1545039042299.png)

得到的`user.sqlite`结构就只有user一个表。

![1545039128211](assets/1545039128211.png)

## 6 Contact Me

如果有什么建议或意见，欢迎联系我（huangyingjing@whu.edu.cn)或者提 issue！
