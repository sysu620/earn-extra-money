## 逻辑架构
逻辑架构由三层模型（表示层、业务层、持久化层）构成

1. 表示层
客户端使用微信小程序作为表示层，提供用户界面，任务界面，问卷界面，快递界面

2. 业务层
服务器充当业务层的角色，为表示层的各个子系统提供相应的服务模块

3. 持久化层
MySQL 提供了数据的持久化服务


## 客户端
```
.
├── build
│   ├── build.js
│   ├── check-versions.js             
│   ├── logo.png  
│   ├── vue-loader.conf.js
│   ├── webpack.base.conf.js
│   ├── webpack.dev.conf.js               
│   └── webpack.prod.conf.js
├── config
│   ├── dev.env.js
│   ├── index.js
│   ├── prod.env.js
├── semantic	        #semantic ui的相关配置文件   
├── src
│   ├── assert          #使用的图片资源
│   ├── components      #用于可视化的页面的组件
│   ├── config		    #localStorage的目录
│   ├── pages           #可视化的页面
│   ├── router          #可视化页面的跳转路由
│   ├── service         #联结可视化页面和服务端响应数据的交互函数
│   ├── store           #客户端状态存储
│   ├── App.vue
│   └── main.js
├── .gitignore
├── .babelrc
├── .editorconfig
├── .postcssrc.js
├── index.html
├── package.json
├── semantic.json
└── README.md
```



## 服务端
```
.
├── go
│   ├── routers.go            # 处理 http 请求，并匹配函数
│   ├── api_task.go           # 集成task相关的api匹配函数
│   ├── api_user.go           # 集成user相关的api匹配函数
│   ├── user.go				  # user结构体 
│   ├── task.go               #task结构体  
│   ├── questionare.go        #questionare结构体
│   ├── delivery.go           #delivery结构体
│   ├── user_and_task.go      #user和task的关系结构体
│   ├── log.go                #日志结构体
│   └── ...                   # 其余辅助功能结构体
├── main.go
└── ...					      #其余配置文件


```

## 与 ECB 关系
- ECB中：

**Entity**：代表系统数据，如：用户、任务、问卷等
**Boundary**：与用户的接口，如：界面、网关、代理等
**Controller**：在 Boundary 和 Entity 中衔接的媒介，编排来自 Boundary 的命令的执行

- 在本系统中，Boundary：

客户端 Web 程序用户界面

- Controller ：

GO服务端 routers.go 接受来自Boundary的命令，并调用API匹配函数
服务端 api_task.go，api_user.go执行API匹配函数，处理Entity 

- Entity 包含：

GO服务端中，对应MySQL数据存储结构的结构体文件

MySQL的数据存储结构
