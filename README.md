# think-layer-multi-app

用于ThinkPHP6+的多应用支持

## 安装

~~~
composer require dragonlhp/think-layer-multi-app
~~~

## 使用

用法参考ThinkPHP6完全开发手册[多应用模式](https://www.kancloud.cn/manual/thinkphp6_0/1297876)章节。
思路是把入口文件的名称与控制器层（controller_layer）目录对应，然后将pathinfo的第一个路径作为应用的名称。相当于是把两个错位后达到的效果！
修改后的访问方式改为：

访问  http://serverName/index.php/index/index/index 指向的是 index应用下面controller的index控制器index方法

访问  http://serverName/admin.php/index/index/index 指向的是 index应用下面admin的index控制器index方法

访问  http://serverName/api.php/index/index/index 指向的是 index应用下面api的index控制器index方法