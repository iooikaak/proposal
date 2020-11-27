# cli - 命令行工具

## 简介

kratos的配套命令行工具，提供一键式的项目骨架初始化，代码生成等功能。

## 命令行界面定义

```
Kratos:An elegant toolkit for Go microservices.

Usage:
  kratos [command]

Available Commands:
  build       编译项目
  create      创建组件
  gen         生成代码
  init        使用项目模板初始化kratos项目骨架
  help        帮助
  run         运行项目
  
Flags:
  -h, --help   help for kratos

Use "kratos [command] --help" for more information about a command. 
```

## 子命令

### build

封装go build命令

### create

[待定]

一键创建某种结构的模块，可扩展，我们也在项目模板里提供一些默认的“子模板”用于创建项目的子结构和相应的配置文件（路径等）。用户可以直接修改这个子模板目录里的模板用于自己的项目，也可以设计为项目根目录放一个用户自定义的“子模板”。

期望可以一键生成比如某个接口的所有外部代码框架，以便直接填写业务逻辑进行开发，具体细节待讨论。

```
kratos create [service/job/some_kind_of_module] foo
```



### gen

读取proto文件生成项目代码

```
kratos gen proto api/*.proto
```

### init

从仓库clone一个模板下来用于项目初始化，go-kratos组织下名称为`template-`开头的仓库为项目模板，默认使用`template-standard`，可以设置flag改变要clone的模板仓库



### Flags

* --template -T <standard/simple/blahblah>  或一个合法的git仓库地址，用于设置模板使用什么模板

### help

展示帮助信息

### run

封装go run命令


