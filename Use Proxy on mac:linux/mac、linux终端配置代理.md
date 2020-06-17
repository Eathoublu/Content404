在使用brew、git、pip等命令时，直接使用速度会比较慢，配置代理可以显著提高速度。
1. 配置代理：
使用【little plane】的用户打开菜单，有一个这个选项：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200617172538736.png)
开启http代理，跟随全局模式，设置HTTP监听地址：127.0.0.1，监听端口：1087
然后打开终端，输入
```bash
export http_proxy=http://127.0.0.1:1087;export https_proxy=http://127.0.0.1:1087;
```
回车即可让终端走代理。

2. 取消代理：
```bash
unset http_proxy; unset https_proxy;
```
3. 如果要默认使用代理，将1中两个export加入~/.bash_profile然后
```bash
source ~/.bash_profile
```
就可以了。
