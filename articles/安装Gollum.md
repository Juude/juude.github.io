gollum是一款开源的wiki系统，利用git作为版本管理。
![](http://bdunagan.com/files/Wiki.Gollum.png)
下面是安装方法。
首先安装ruby 包管理国内工具rubygems:
`sudo apt-get install rubygems`
然后安装gollum：
`gem install gollum`
但是发现了错误：
```
Building native extensions.  This could take a while...
ERROR:  Error installing gollum:
    ERROR: Failed to build gem native extension.

        /usr/bin/ruby1.8 extconf.rb
checking for main() in -licui18n... no
checking for main() in -licui18n... no


***************************************************************************************
*********** icu required (brew install icu4c or apt-get install libicu-dev) ***********
***************************************************************************************
*** extconf.rb failed ***
```
是缺少`icu`即 `International Components for Unicode`
接下来执行
`apt-get install libicu-dev`
即可。

