# IDE
## 1.下载idea 社区版
[下载地址](https://www.jetbrains.com/idea/download/#section=windows)
##  2.配置主题
### 2.1 下载主题插件monokai pro
![主题插件](_v_images/20200903115303654_28998.png)

### 2.2选择主题
![](_v_images/20200903115407137_7336.png)


### 2.3设置编辑器字体

![](_v_images/20200903115629214_29970.png)

### 2.4设置color theme-java
![](_v_images/20200903120100925_6044.png)
### 2.5 设置color-theme  console
![](_v_images/20200903120423928_5604.png)





### 2.6 设置code style
![](_v_images/20200903120140460_19858.png)





## 3.配置代理
![设置代理](_v_images/20200903115523999_14368.png)

##  4.必备插件
* monokai主体
*  p3c  alibaba编程规范
*  lombok
*  plant uml
*  translation
* jclasslibbyteCode viewer (查看java byte code)
## 5.安装 consolas 字体
```
https://gist.github.com/sigoden/d01ad118da677f796bab01781b7eae23
```
```
wget -O /tmp/YaHei.Consolas.1.12.zip https://storage.googleapis.com/google-code-archive-downloads/v2/code.google.com/uigroupcode/YaHei.Consolas.1.12.zip
unzip /tmp/YaHei.Consolas.1.12.zip
sudo mkdir -p /usr/share/fonts/consolas
sudo mv YaHei.Consolas.1.12.ttf /usr/share/fonts/consolas/
sudo chmod 644 /usr/share/fonts/consolas/YaHei.Consolas.1.12.ttf
cd /usr/share/fonts/consolas
sudo mkfontscale && sudo mkfontdir && sudo fc-cache -fv
```
![](vx_images/38631696495.png =1216x)