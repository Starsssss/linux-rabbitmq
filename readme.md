centos7 安装rabbitmq
参考链接: https://blog.csdn.net/weixin_38504656/article/details/117187803?utm_medium=distribute.pc_relevant_download.none-task-blog-baidujs-2.nonecase&depth_1-utm_source=distribute.pc_relevant_download.none-task-blog-baidujs-2.nonecase

 警告：erlang-21.3.8.6-1.el7.x86_64.rpm: 头V4 RSA/SHA1 Signature, 密钥 ID 6026dfca: NOKEY 错误：依赖检测失败： libcrypto.so.10(OPENSSL_1.0.2)(64bit) 被 erlang-21.3.8.6-1.el7.x86_64 需要

解决的方法就是在rpm 语句后面加上 --force --nodeps
即 原本为 rpm -ivh ****.rpm 现在改成 rpm -ivh ****.rpm --force --nodeps就可以了，nodeps的意思是忽视依赖关系。