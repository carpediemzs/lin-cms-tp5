# 简介

## 什么是 Lin CMS？

> Lin-CMS 是林间有风团队经过大量项目实践所提炼出的一套**内容管理系统框架**。Lin-CMS 可以有效的帮助开发者提高 CMS 的开发效率。

本项目是基于ThinkPHP 5.1的 Lin CMS 后端实现。

本项目非官方团队出品，仅出于学习、研究目的丰富下官方项目的语言支持。

官方团队产品了解请访问[TaleLin](https://github.com/TaleLin)

## Lin CMS 的特点

Lin CMS 的构筑思想是有其自身特点的。下面我们阐述一些 Lin 的主要特点。

**Lin CMS 是一个前后端分离的 CMS 解决方案**

这意味着，Lin 既提供后台的支撑，也有一套对应的前端系统，当然双端分离的好处不仅仅在于此，我们会在后续提供NodeJS和PHP版本的 Lin。如果你心仪 Lin，却又因为技术栈的原因无法即可使用，没关系，我们会在后续提供更多的语言版本。为什么 Lin 要选择前后端分离的单页面架构呢？

首先，传统的网站开发更多的是采用服务端渲染的方式，需用使用一种模板语言在服务端完成页面渲染：比如 JinJa2、Jade 等。 服务端渲染的好处在于可以比较好的支持 SEO，但作为内部使用的 CMS 管理系统，SEO 并不重要。

但一个不可忽视的事实是，服务器渲染的页面到底是由前端开发者来完成，还是由服务器开发者来完成？其实都不太合适。现在已经没有多少前端开发者是了解这些服务端模板语言的，而服务器开发者本身是不太擅长开发页面的。那还是分开吧，前端用最熟悉的 Vue 写 JS 和 CSS，而服务器只关注自己的 API 即可。

其次，单页面应用程序的体验本身就要好于传统网站。

更多关于Lin CMS的介绍请访问[Lin CMS线上文档](http://doc.cms.7yue.pro/)

**框架本身已内置了 CMS 常用的功能**

Lin 已经内置了 CMS 中最为常见的需求：用户管理、权限管理、日志系统等。开发者只需要集中精力开发自己的 CMS 业务即可

## 所需基础

由于 Lin 采用的是前后端分离的架构，所以你至少需要熟悉 PHP 和 Vue。

Lin 的服务端框架是基于 ThinkPHP5.1的，所以如果你比较熟悉ThinkPHP的开发模式，那将可以更好的使用本项目。但如果你并不熟悉ThinkPHP，我们认为也没有太大的关系，因为框架本身已经提供了一套完整的开发机制，你只需要在框架下用 PHP 来编写自己的业务代码即可。照葫芦画瓢应该就是这种感觉。

但前端不同，前端还是需要开发者比较熟悉 Vue 的。但我想以 Vue 在国内的普及程度，绝大多数的开发者是没有问题的。这也正是我们选择 Vue 作为前端框架的原因。如果你喜欢 React Or Angular，那么加入我们，为 Lin 开发一个对应的版本吧。

## 快速开始

### Server 端必备环境

* 安装MySQL（version： 5.6+）

* 安装PHP环境(version： 7.1+)

### 获取工程项目

```bash
git clone https://github.com/ChenJinchuang/lin-cms-tp5.git
```

> 执行完毕后会生成lin-cms-tp5目录

### 安装依赖包

执行命令前请确保你已经安装了composer工具

```bash
cd lin-cms-tp5

composer install
```

### 数据库配置

Lin 需要你自己在 MySQL 中新建一个数据库，名字由你自己决定。例如，新建一个名为 lin-cms 的数据库。接着，我们需要在工程中进行一项简单的配置。使用编辑器打开 Lin 工程根目录下``/config/database.php``，找到如下配置项：

```php
// 服务器地址
  'hostname'        => '',
// 数据库名
  'database'        => 'lin-cms',
// 用户名
  'username'        => 'root',
// 密码
  'password'        => '',
```
