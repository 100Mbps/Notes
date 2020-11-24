# day01
## 1. rec

remote command/code execute

```
python httpscan.py 192.168.1.0/24 -t 5

```


sudo docker pull zhl2008/web_14.04

docker tag zhl2008/web_14.04 web_14.04



## 2.awd-platform启动过程
**python 运行环境python2**
```
1） python batch.py web_server 2
2） python start.py ./ 2
3） docker attach check_server   python check.py
4） python stop_clean.py
```

今天root 分区容量告急主要是docker占了好多空间，遂将24g的小盘格式化后挂载到/var/lib/docker 下，第一次挂载不注意不知为何docker文件夹的owner为
hanrongjie，导致image 运行后，无法正常工作，遂将docker.io卸载，重新安装 此时docker文件夹的owner为root，此时恢复了正常，upload-labs 中
docker exec ls 中的文件夹也从root 变成了 www-data ，过程曲折去不知为何，稀里糊涂的整完了。

```
sudo docker run -d -p 80:80 c0ny1/upload-labs:latest
sudo docker exec `sudo docker ps|grep c0ny1|awk '{print $1}'` mkdir upload
sudo docker exec `sudo docker ps|grep c0ny1|awk '{print $1}'` chmod 777 upload
```



```
前提是apache的httpd.conf中有如下配置代码

AddType application/x-httpd-php .php .phtml .phps .php5 .pht

合法后缀 php,phps,php3,php5,pht
```

```php
在PHP中用作错误控制操作符。当表达式附加@符号时，将忽略该表达式可能生成的错误消息。如果启用了track_errors功能，则表达式生成的错误消息将保存在变量$ php_errormsg中。每个错误都会覆盖此变量。
```

```
base64 把不死马编码以后，发现回车换行没了，源文件中又有#注释，导致fuck.php 不可用。
```