## 架构问题

内存问题

## 解决方案说明
#### 缓存技术
分别采用了vuex和localstorage进行页面的管理

#### 技术选型理由及对应代码
vuex用于状态管理，管理一个页面不同component的通信。实现：

组件之间的数据tongxin
使用单向数据流的方式进行数据的中心化管理
对应模块：src/store
localstorage用于存储部分用户数据。

vuex 属于js，因此vuex使用的数据自然会放在内存。而浏览器在每次刷新页面之后都会清空一次内存，因此vuex存储的消息自然就会消失
而localstorage以文件的形式存储在本地，因此localstorage不会随页面更新而消失。
对应模块：目录：src/config/mutils


## 逻辑视图
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190627010355795.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)
## 物理视图
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190627122500358.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NhdF94aW5n,size_16,color_FFFFFF,t_70)
