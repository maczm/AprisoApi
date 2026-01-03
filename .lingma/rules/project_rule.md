# 通义灵码规则配置

## 开发环境

- 操作系统：Windows 11 ARM
- 开发工具：Visual Studio 2026
- Dotnet：.NET 10.0

## 生产环境

- 操作系统：Windows Server 2022
- Dotnet：NetFramework 3.5，4.7.2，4.8，4.8.1
- Delmia Apriso 2024

### Apriso2024

Apriso通过user formula editer进行C#脚本编写，有如下限制：
- 不支持using指令，但是支持using语句；
- 类名必须使用全限定类名，但是有如下例外
	- System.Collections.Generics
	- System.Linq
	- System.Text.RegularExpressions
	- System.XML
	- Newtonsoft.Json
- 字符串拼接优先使用string.Format()方法,不支持$@字符串拼接
- 不支持定义类和方法
- 局部变量使用var和小驼峰命名
- 部分?运算符支持情况：
	- 不支持可空类型 (Nullable Types)
	- 不支持空条件运算符 (?. 和 ?[])
	- 支持空合并运算符 (??)
	- 不支持空合并赋值运算符 (??=)
	- 支持三元条件运算符 (? :)
- 不支持锁和多线程
- 不支持C#自带的内联声明写法(eg:out Newtonsoft.Json.Linq.JToken fileIdToken)
- 不支持goto语句
- 处理Json数据时，使用Newtonsoft.Json
- 所有的消息提示都要是中文
- 获取可能的异常复制给msg
- 每次回答问题时，都要确保查看的代码是最新的