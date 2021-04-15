# 实习手册 2021-Spring-Tour
Join Us And Explore
## git
```shell
# clone下来一个远程仓库
git clone https://github.com/Pivot-Studio/2021-Spring-Tour.git

# 将更改记录加入缓存区
git add .
# 将更改记录提交
git commit -m "Tag:Your commit info"
# 推送到远程分支
git push
# 查看分支情况
git branch
# 切换分支
git checkout your-branch-name
```

## 任务

我们为后端提供了三个实习任务（每个任务 的具体要求详见实习群中发的pdf)

1. 对树洞的运维提供支持

2. 实现一个Github管理系统

3. 实现一个博客后端

  
这三个任务难度依次递增，第一个任务面向没有网络和数据库操作编程经验的同学，第三个任务适合有一定后端基础并且对一些框架有所了解的同学。

## 实习要求

1. 所有实习题目语言框架不限
2. 我们希望你有良好的分支管理能力，提交commit时，请简单描述一下做出的改动，增添新功能以FEA:开头，修改bug以FIX:开头，将自己的分支基于主分支开发。
3. 保证代码风格的统一和工程化，不同模块的功能拆分到不同的包里面。
4. 良好的写注释习惯，推荐为自己负责的 class 及 function 添加相关文档。
5. 每天有适量的工作日志来记录完成的新功能，遇到的问题，学到的知识等等。
6. 在每天23:30之前将你的工作日志和更新的代码push到仓库的分支上面。
7. 在善用搜索引擎的同时主动提问，在遇到问题时可以咨询对应的出题人或者组长，欢迎私戳。

## 四月八日

1. 我先基于自己的水平和团队的推荐和情况确定选择任务二完成项目使用的编程语言为go语言，虽然并不熟练，以前也几乎没有用go语言编写代码的经历，但我认为实习就是一个挑战自我，不断学习的过程，也可以为将来的发展打好基础。
2. 通过网上查找资料学习了.gitgnore文件的作用和用法，并push了一个go的gitignore模板。
3. 由于以前我没有在vscode上配置完善go语言的环境，有多个远程北宋还未下载。我趁这次机会，查找资料配环境，其间我经历了许多波折。首先我弄明白了无法下载的原因是vscode无法翻墙下载，即使我开了vpn也无济于事。后来，我根据csdn上的文章手动clone了github上的go的库到本地，结果仍然无法成功配置。我又查找资料，可以复制错误信息上的网址来下载，可是我失望地发现有些网址已经找不到网页了（404）。就在我濒临绝望之际，天无绝人之路，我又发现了一篇博客，上面分享了go的包，我用网盘下载之后解压缩在放到规定目录，再下载就成功了。在这个过程中，我也算更加熟悉了git bash的用法。
4. 我正在阅读github 的 官方 api 文档，熟悉postman功能（尚未完成）

##  四月九日

1. 我基本完成GitHub官方文档rest api部分的目前所需知识的阅读，通过网络查找各种相关知识，对项目有了更深的理解。
2. 我了解了postman 和 curl命令的用法并加以测试 完成网络请求 push了一张响应截图
3. 我通过查找资料写了实现网络请求的go语言代码，成功实现。
4. 我查找相关知识，创建了GitHub的私人token，但不会如何完成身份认证，仍在学习。
## 四月十日
1. 我在花费大量时间查阅token身份认证相关资料而发觉有些不对劲而看不懂后咨询了学长，发现自己查找到的资料并不是本次实习项目所需要的，于是我转换了学习方向和内容。
2. 我发现get请求无法进行身份认证（明文），于是转化为了post请求，但并未完善，仍在学习。
## 四月十一日
1. 尝试建立一个go项目，想要将token存在另一个文件里，使用了：=，发现编译错误，搜索后发现全局变量需要使用var定义。
2. 发现原来的.gitgnore无法起到应有的作用，搜索后得知，编码方式有问题，应该改成Linux默认的编码方式ANSI格式。
3. 在自己的摸索与学长的指引下历经一系列波折终于完成了get请求与身份认证的go语言代码，从中我也加深了对网络请求的理解，收获颇丰。
4. 为了隐藏自己的token要新建一个文件储存，涉及到go语言不同文件相互引用，我也踩了好几个坑，包括要函数名首字母大写来引用，新建包，要设置状态为off，否则报错等等，最后终于成功了。
## 四月十二日
1. 学习了go语言解析json信息相关知识，但我写的程序其实已经输出了可以看懂的字符串，后续处理我决定等到后续任务用到时再进行。
2. 我学习了go语言发送邮件（使用QQ邮件SMTP功能）但由于我的邮箱更换了密保手机号出于未知原因无法验证通过，因此尚未开启SMTP功能，但我还是完成了go代码的编写。
3. 通过与学长的交流，对任务项目的实现有了更深的理解。
## 四月十三日
1. 查找资料了解Github events,实现了返回目标用户的events
2. 查找长短轮询的资料
3. 实现了自己写的版本的轮询监控GitHub目标用户的代码
4. 在发邮件代码中添加了panic和recover（由于smtp服务仍未启动，暂时无法真正发送邮件）
5. 在一个文件中完成调用多个文件，有了项目的雏形。
## 四月十四日
1. 通过查找相关资料学习了解析json信息的相关知识
2. 实现了用get方法返回目标用户的star相关信息
3. 实现了go语言解析需要的star信息的代码
4. 通过咨询学长解决了多文件调用时出现的错误
## 四月十五日
1. 完成了对已经解析好的数据加入收藏夹，删除出收藏夹，创建收藏夹，按创建时间来排序的操作。
2. 由于我的QQ邮箱始终无法通过身份验证开启SMTP服务，于是我创建了一个163邮箱并修改了相关代码以达到测试的目的。
3. 第一次测试没有响应，我添加输出项，多次调试，最后发现是我的163邮箱名字输错了，最后成功发送了邮件，完成了任务要求。