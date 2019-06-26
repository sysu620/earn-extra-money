
# 后端代码规范

官方代码规范：https://golang.org/doc/effective_go.html
团队规范
## 工具

- 提交代码前需使用fmt工具格式化
- 提交代码前需使用vet工具进行静态检查
## 目录规范
```
|– bin

|– build

    |–build_dev/test/release.sh

|– gen-go

|– config

    |– dev/test/release.yml

|– pkg

    |–controller

    |–dao

    |–rpc

    |–service

        |–*_impl.go

        |–*_test.go

        |–*_mock.go

|– vendor

|– README.md

```
### 命名规范

- 文件：
-  - 小写+下划线
- 包命名
- - package名和目录保持一致，需避免和标准库冲突
- - 避免import相对路径
- 方法/接口
- - 采用驼峰命名法
- - 非对外方法，首字母需为小写
- 变量
- - 采用驼峰命名法
- 常量
- - 大写+下划线
### 4. 注释

- 可以通过 /* …… */ 或者 // ……增加注释， //之后应该加一个空格
- 注释内容需要在文件/方法/变量上方
### 5.异常

需要对异常做判断处理
不要将error赋值给匿名变量_
### 其他

- 不允许逻辑中调用Panic，选择日志的log.Fatal
- 不要频繁的调用defer
- 尽早return，一旦有错误发生，马上返回
- if接受初始化语句，约定如下方式建立局部变量
```
    if err := file.Chmod(0664); err != nil {
        return err
    }
 ```

- 方法 的接收器的名称 一般采用strcut的第一个字母且为小写，而不是this，me或者self
```
type rpcClient struct {
       once sync.Once
}
func (r *rpcClient) newCodec(contentType string) (codec.NewCodec, error) {
       //
}
```
- 对于bool类型的变量var b bool,直接使用它作为判断条件，而不是使用它和true/false进行比较
- byte/string slice相等性比较，使用Equal
- 当接受者是map, chan, func, 不要使用指针传递，因为它们本身就是引用类型
- 当接受者是slice，而函数内部不会对slice进行切片或者重新分配空间，不要使用指针传递
- 当函数内部需要修改接受者，必须使用指针传递
- 当接受者是一个结构体，并且包含了sync.Mutex或者类似的用于同步的成员。必须使用指针传递，避免成员拷贝
- 当接受者类型是一个结构体并且很庞大，或者是一个大数组，建议使用指针传递来提高性能，其他场景使用值传递即可



# 前端代码规范
## HTML规范
### 书写风格
#### HTML代码大小写
HTML标签名，类名，标签属性和大部分属性值统一用小写，例如

```
<div class="test"></div>
```
HTML文本，CDTA，Javescript，meta变迁某些属性等内容可大小写混合。
#### 类型属性
不需要位CSS，JS制定类型属性，HTML5中默认已包含，例如

```
<link rel="stylesheet" href="" >
<script src=""></script>
```
#### 元素属性
- 元素属性值使用双引号语法
- 元素属性值可以写上的都协商
例如：

```
<input type="text">
	
<input type="radio" name="name" checked="checked" >
```
#### 代码缩进
统一使用四个空格进行代码所继，使得各编辑器表现一致，例如

```
<div class="jdc">
    <a href="#"></a>
</div>
```

#### 代码嵌套
元素嵌套规范，每个块状元素独立一行，内联元素可选，例如

```
<div>
    <h1></h1>
    <p></p>
</div>	
<p><span></span><span></span></p>
```

## 图片规范
### 内容图
内容图多以商品图等照片类图片形式存在，颜色较为丰富，文件体积较大
- 优先考虑 JPEG 格式，条件允许的话优先考虑 WebP 格式
- 尽量不使用PNG格式，PNG8 色位太低，PNG24 压缩率低，文件体积大

### 背景图
背景图多为图标等颜色比较简单、文件体积不大、起修饰作用的图片
- PNG 与 GIF 格式，优先考虑使用 PNG 格式,PNG格式允许更多的颜色并提供更好的压缩率
- 图像颜色比较简单的，如纯色块线条图标，优先考虑使用 PNG8 格式，避免不使用 JPEG 格式
- 图像颜色丰富而且图片文件不太大的（40KB 以下）或有半透明效果的优先考虑 PNG24 格式
- 图像颜色丰富而且文件比较大的（40KB - 200KB）优先考虑 JPEG 格式
- 条件允许的，优先考虑 WebP 代替 PNG 和 JPEG 格式

### 图片大小
PC平台单张的图片的大小不应大于 200KB。

移动平台单张的图片的大小不应大于 100KB。

### 图片质量
上线的图片都应该经过压缩处理，压缩后的图片不应该出现肉眼可感知的失真区域。
60质量的JPEG格式图片与质量大于60的相比，肉眼已看不出明显的区别，因此保存 JPEG 图的时候，质量一般控制在60，若保真度要求高的图片可适量提高到 80，图片大小控制在 200KB 以内。
### 图片引入
#### CSS Sprites使用简易
- 适合使用频率高更新频率低的小图标
- 尽量不留太多的空白
- 体积较大的图片不合并
- 确保要合并的小图坐标数值和合并后的 Sprites 图尺寸均为偶数

#### Data URIs（base64编码）使用建议
- 适合更新频率高的小图片，如某些具备自定义功能的标题icon等
- 转换成 Base64 编码的图片应小于 2KB
- 移动端不使用 Base64 编码
- 要兼容 IE6/IE7 的不使用

## CSS代码风格
### 代码格式化
样式书写一般有两种：一种是紧凑格式 (Compact)

```
.jdc{ display: block;width: 50px;}
```
一种是展开格式（Expanded）

```
.jdc{
    display: block;
    width: 50px;
}
```
团队约定，统一使用展开格式书写样式

### 代码大小写
样式选择器，属性名，属性值关键字全部使用小写字母书写，属性字符串允许使用大小写。

```
.jdc{
	display:block;
}
```
### 选择器
- 尽量少用通用选择器 *
- 不使用 ID 选择器
- 不使用无具体语义定义的标签选择器
例如

```
.jdc {}
.jdc li {}
.jdc li p{}

```
### 代码缩进
统一使用四个空格进行代码缩进，使得各编辑器表现一致（各编辑器有相关配置）

```
.jdc {
    width: 100%;
    height: 100%;
}
```
### 分号
每个属性声明末尾都要加分号

```
.jdc {
    width: 100%;
    height: 100%;
}
```
### 代码易读性
左括号与类名之间一个空格，冒号与属性值之间一个空格，例如

```
.jdc { 
    width: 100%; 
}
```
### 属性书写顺序
建议遵循以下顺序：

- 布局定位属性：display / position / float / clear / visibility / overflow
- 自身属性：width / height / margin / padding / border / background
- 文本属性：color / font / text-decoration / text-align / vertical-align / white- space / break-word
- 其他属性（CSS3）：content / cursor / border-radius / box-shadow / text-shadow / background:linear-gradient …

## js规范
### 单行代码块
在单行代码中使用空格，推荐

```
function foo () { return true }
if (foo) { bar = 0 }
```
### 大括号风格
js使用One True Brace Style，例如

```
if (foo) {
  bar()
} else {
  baz()
}
```
### 变量声明
团队约定使用驼峰式命名

### 拖尾逗号
 因为拖尾逗号有好也有不好，所以团队约定允许在最后一个元素或属性与闭括号 ] 或 } 在不同行时，可以（但不要求）使用拖尾逗号。当在同一行时，禁止使用拖尾逗号。
### 逗号空格
逗号前后的空格可以提高代码的可读性，团队约定在逗号后面使用空格，逗号前面不加空格。例如

```
var foo = 1, bar = 2
```
### 逗号风格
逗号分隔列表时， 逗号放置在当前行的末尾
例如

```
var foo = 1,
    bar = 2

var foo = ['name',
            'age']
```
### 计算属性的空格
团队约定在对象的计算属性内，禁止使用空格，例如

```
obj['foo']
```

### 拖尾换行
在非空文件中，存在拖尾换行是一个常见的 UNIX 风格，它的好处是可以方便在串联和追加文件时不会打断 Shell 的提示。在日常的项目中，保留拖尾换行的好处是，可以减少版本控制时的代码冲突。

### 函数调用
为了避免语法错误，团队约定在函数调用时，禁止使用空格


### 缩进
约定使用 空格 来缩进，而且缩进使用两个空格。

### 构造函数的参数
在 JavaScript 中，通过 new 调用构造函数时，如果不带参数，可以省略后面的圆括号。但这样会造成与整体的代码风格不一致，所以团队约定使用圆括号，例如

```
var person = new Person()
```

### 链式调用
链式调用如果放在同一行，往往会造成代码的可读性差，但有些时候，短的链式调用并不会影响美观。所以本规范约定一行最多只能有四个链式调用，超过就要求换行。

### 空行
空白行对于分离代码逻辑有帮助，但过多的空行会占据屏幕的空间，影响可读性。团队约定最大连续空行数为 2

### 链式赋值
链式赋值容易造成代码的可读性差，所以团队约定禁止使用链式赋值，例如

```
var a = 1
var b = 1
var c = 1
```

### 变量声明
JavaScript 允许在一个声明中，声明多个变量。团队约定在声明变量时，一个声明只能有一个变量，例如：

```
var a
var b
var c
```

