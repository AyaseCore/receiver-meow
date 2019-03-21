# receiver-meow

[![Build Status](https://travis-ci.com/chenxuuu/receiver-meow.svg?branch=master)](https://travis-ci.com/chenxuuu/receiver-meow)

能运行`lua`脚本的接待喵qq机器人

## 功能特点

- 消息处理逻辑，完全由lua实现
- lua代码动态加载，更改完后即时生效
- 酷Q接口基本全部提供给了lua层，接口丰富
- 自带了http(s) post/get、2D图片处理、数据存储(xml)等接口
- 底层使用C#开发，.net framework 4.5版本

## 说明

lua代码全部在`appdata`文件夹中

所有lua接口可以参考`com.papapoi.ReceiverMeow\Native.Csharp\App\LuaEnv\LuaEnv.cs`文件中的函数定义

如想自己编译，请注意需要将release中的package压缩包，解压到vs项目的文件夹处

## 食用

实际使用时，只需要将cpk文件放入酷q的app文件夹，cpk文件可以去[这里下载](https://cqp.cc/t/41943)，或者自行编译（自行编译注意打开开发者模式，删掉生成后的lua53.dll）

然后，请**务必**将`appdata`文件夹内的所有文件夹与文件(目前只有`lua`与`xml`两个文件夹)，复制到酷q的`酷Q Air\data\app\com.papapoi.ReceiverMeow\`文件夹下

> 注意，如果提示找不到xxx.lua，请先检查文件夹是否正确，如果正确，请尝试保证所有路径都不包含中文和空格。

## 结尾

插件基于[Native.SDK](https://github.com/Jie2GG/Native.Csharp.Frame)

MIT协议
