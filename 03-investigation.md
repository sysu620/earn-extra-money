## 背景

目前市面上出现了越来越多的兼职赚钱软件和网站，用户只需要在空余时间做一些简单的任务，就可以赚到零花钱。但是，各种各样的产品良莠不齐，用户不仅可能面临信息泄露、诈骗的风险，而且由于信息获取的困难，目前也没有专门针对中山大学在校学生的挣闲钱软件。因此我们调研了一些市面上具有代表性的软件和网站，并进行竞品分析，力求探索一种适用于在校学生的程序，确定必要的服务以及优化用户体验的服务。

## 交互设计与技术分析
针对挣闲钱的核心业务，我们挑选了众人帮、问卷星、蛋壳互助三款竞品做了详细的交互过程与功能架构设计做了分析。

### 功能框架

#### 众人帮
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526204412857.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)


分析：

- 功能繁多，稍显臃肿
- 多数任务需要填写个人手机号、身份证号、绑定银行卡，存在安全隐患
- 获得赏金以及提现过程比较顺畅

#### 问卷星
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526215756455.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)

分析：

- 界面简洁，支持的问卷类型丰富，操作也比较容易上手
- 用户反馈说有打不开、不能保存的情况，影响了部分人作业、报告的提交

#### 蛋壳互助
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526224200500.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)


分析：


- 界面、功能与众人帮有类似的地方，但是比众人帮要清爽很多，架构更加清晰合理
- 调查问卷参与要填写验证码，我一直都没法通过验证


### 交互体验
核心流程的界面截图在附录给出
#### 众人帮
- 界面多且杂，功能上有些重复的地方
- 有时候会莫名其妙转发一些东西到绑定的账号里（QQ空间之类的），新手需要注意

#### 问卷星
- 界面简洁大方，中规中矩
- 架构清晰合理，交互上也比较符合用户习惯

#### 蛋壳互助
- 界面相比众人帮更简洁，值得借鉴

### 亮点特点借鉴
#### 众人帮
- 有“Bang一下”功能，不知道做啥的时候可以推荐悬赏
- 查看悬赏详情、报名、提交、审核、提现，整个过程比较流畅，可以借鉴。审核过程众人帮似乎采用人工审核，对于有发问卷需求的学生不太合适，这点我们另想办法。
#### 问卷星
- 专业的问卷调查、考试、投票平台，为我们自己开发问卷系统提供借鉴
#### 蛋壳互助
- 界面相比众人帮更简洁，值得借鉴
- 配色相比众人帮给人感觉更加舒服


### 总结
综合前面调研的各个产品的优势和特点，我们需要完成的产品需要更为细致的考虑到用户的需要。

我们的主要业务是调查问卷，其中，调查问卷的交互设计可以借鉴蛋壳互助，具体的问卷内容可以借鉴问卷星。

功能不是越多越好，虽然众人帮用户多，但是界面及配色还是不如蛋壳互助，我们在设计UI的时候应该尽量做到简洁大方。

众人帮的某些功能可以作为我们的创新项。


-----

## 附录
#### 众人帮
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526221516295.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526221547463.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526221611367.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526221620995.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526221653402.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526221717138.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)


#### 问卷星
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526221213203.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526221225691.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526221238608.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526221256734.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526221313426.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2019052622133411.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526221343225.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)
#### 蛋壳互助
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526223146398.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526223156905.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526223207878.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526223219913.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526223229831.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526223238869.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190526223247888.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)
