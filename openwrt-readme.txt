首先要说http://code.google.com/p/goagent/上有详细的说明。
之所以修改代码，主要是将goagent使用到openwrt的过程中，发现一些不稳定情况，查看了一下代码，注释掉部分文字输出，以及添加了异常处理，以此保证proxy在openwrt上工作正常。

简要描述一下openwrt上的部署过程。
1.通过LuCI关键界面安装python、python-openssl、openssh-sftp-server；
2.使用SSH Secure File Transfer Client将配置后的openwrt-port上传至/usr/lib/goagent,并将proxy.py置为可执行；
3.使用SSH Secure Shell Client执行/usr/lib/goagent/proxy.py &；
4.退出工具。