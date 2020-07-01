# idea
记录日常我的一些想法
## 嵌入式平板电脑的一些进展
**软件方面** <br> 
* 我想直接移植一个开源的电子书阅读器软件[bookworm](https://github.com/babluboy/bookworm).<br>
	* 它是基于[vala](https://github.com/GNOME/vala)这门语言开发的。<br>
	* 就是面向对象的编程方式，把代码全部转换成C语言，然后编译成二进制文件，用的是GTK+图形界面,我做嵌入式软件开发，对这个图形界面熟悉 
	* 很适合嵌入式平台用的轻量级图形界面，编译后打开一个PDF文件，发现里面的图片是看不到的
* 于是我在找kindle的资料的时候发现有个[koreader](https://github.com/koreader/koreader)软件
	* 很满足我的胃口
**koreader**<br>
	*软件的话用koreader.<br>
	*现在就差把屏幕坐标对应起来<br>
	*看了一晚上的代码还是没有进展，还是SDL的问题。<br>
	*把SDL好好整理一下<br>
	*[SDL资料](https://tieba.baidu.com/p/2682080782?red_tag=2799053608#)<br>
	*修改完成后，想办法导入lua程序种。<br>
        *修改SDL中的坐标值是正确的。<br>
	*还是有一点小问题没有解决。<br>
	*最近在忙南向接口的事情。<br>
	*先把模拟的做出来<br>
	*******************************************************
	*CMakeLists.txt这个文件还是没有写好，得好好学一下它得语法知识。<br>
        *现在移植库的时候遇到交叉编译器版本过低的问题，主要是sysrepo这个库。<br>
	*cmake的一些知识点<br>
	*借助开源的力量来做事好一些。<br>
	*第一次遇到"/home/mo/share/gcc-4.4.4-glibc-2.11.1-multilib-1.0/arm-fsl-linux-gnueabi/bin/../lib/gcc/arm-fsl-linux-gnueabi/4.4.4/../../../../arm-fsl-linux-gnueabi/bin/ld: warning: libcrypto.so.1.1, needed by /home/mo/share/netconf2/lib/libssh/_install/lib/libssh.so.4.8.1, not found (try using -rpath or -rpath-link)
/home/mo/share/gcc-4.4.4-glibc-2.11.1-multilib-1.0/arm-fsl-linux-gnueabi/bin/../lib/gcc/arm-fsl-linux-gnueabi/4.4.4/../../../../arm-fsl-linux-gnueabi/bin/ld: warning: libssl.so.1.1, needed by /home/mo/share/netconf2/lib/libnetconf2/_install/lib/libnetconf2.so.1.3.5, not found (try using -rpath or -rpath-link)"<br>
