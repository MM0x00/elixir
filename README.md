# elixir 在线实验环境

## 软件简介

软件基本信息，License，所属的类别，作用，特点等。

Elixir是一种用于构建可扩展和可维护应用程序的动态功能语言。

Elixir 是一个基于Erlang VM的函数式元编程语言(类似Ruby)，通过动态语言的灵活的语法和宏能够利用Erlang建立一个并发 分布 失败冗余的高质量代码。

Elixir提供第一层次的模式匹配pattern matching, 通过协议的多态性(类似 Clojure), 别名等。 Elixir 和 Erlang 分享同样的字节码和数据类型，可以直接调用Erlang。

所属类型是编程语言

特点:

一切都是表达式



## 软件官网

https://elixir-lang.org/

## Dockerfile 使用方法

运行它作为REPL
```
➸ docker run -it --rm elixir
Erlang/OTP 18 [erts-7.2.1] [source] [64-bit] [smp:8:8] [async-threads:10] [hipe] [kernel-poll:false]

Interactive Elixir (1.2.1) - press Ctrl+C to exit (type h() ENTER for help)
iex(1)> System.version
"1.2.1"
iex(2)>
➸ docker run -it --rm -h elixir.local elixir iex --sname snode
Erlang/OTP 18 [erts-7.2.1] [source] [64-bit] [smp:8:8] [async-threads:10] [hipe] [kernel-poll:false]

Interactive Elixir (1.2.1) - press Ctrl+C to exit (type h() ENTER for help)
iex(snode@elixir)1> System.version
"1.2.1"
iex(snode@elixir)2> :c.uptime
14 seconds
:ok
```
运行一个Elixir exs脚本
```
$ docker run -it --rm --name elixir-inst1 -v "$PWD":/usr/src/myapp -w /usr/src/myapp elixir elixir your-escript.exs
```
## 资源链接

- https://elixir-lang.org/
