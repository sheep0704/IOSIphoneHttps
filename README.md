# IOSIphoneHttps

* [英文版](https://github.com/sheep0704/IOSIphoneHttps/blob/master/README_eng.md)
* [中文版](https://github.com/sheep0704/IOSIphoneHttps/blob/master/README.md)

<br/>

 * 今日更新：最近超级签相关的封号严重，都是关联引起，建议不要绑定同一张卡。

 * 后面更新：之后会更新不掉签，也就是所谓的超级超级签的办法，无需第三方操作，只是成本贵了点。

 * 最新版：2019 苹果应用又严格，直接签名直接下载安装，无需进入appstore商城，无需第三方可以自己直接使用安装

想不经过App Store直接下载游戏吗？下载完不知道怎么安装？需要通过第三方软件来安装？下面奥特曼超人来带你进入新版的安装教程：

搭建一个HTTPS服务，可以使用HTTPD或者Tomcat构建

使用plist文件
通过A标签调起安装
扩展-（可通过js判断是否安装，如果未安装直接安装，安装了就下载）
早上在撸HTML5，有个下载页的需求，需要安卓和苹果，一般来说苹果用第三方或者AppStore的，但这次是在内部使用的App和Ipa，所以得有个方法来绕过这个，其实第三方实现的原理也是如此，来看下执行步骤。
<br/>
首先，下载plist 文件模版：点我下载
外链：https://github.com/sheep0704/IOSIphoneHttps/blob/master/x5.plist
注意细节，如果自己复制模版，不要漏下下面的声明：
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
 
 

<br/>
然后把plist文件放在https服务目录下，如果没有服务器的建议使用BaiduYun或者Github来进行测试，如果浏览器提示【无法连接到github.com】，请检查plist文件和服务器的拦截问题，有些马大哈也会把xml写错，可直接用浏览器访问plist地址看看。

然后通过A标签写入进行测试

<a href="itms-services:///?action=download-manifest&url=https://github.com/sheep0704/IOSIphoneHttps/blob/master/x5.plist" class="button button-stripe">苹果正版下载</a>
 
 


点击测试，发现并没有效果，苹果浏览器会提示连接不上github.com，我们拦截下请求看看，发现了 Provisional headers are shown！ 
奥特曼超人

原因： itms-services应该不支持自签名的SSL证书，要搞一下ssl证书来放plist文件




总结：一开始调试几次发现不行，因为用的是NGR，映射了127.0.0.1的Tomcat，所以后来替换回我们自己的服务器地址，经过测试是可行的，所以建议中间不要有转发的过程，直接用外网服务器进行测试。 


|| 版权声明：本文为博主杜锦阳原创文章，转载请注明出处。

http://dujinyang.blog.csdn.net/article/details/70267202

http://dujinyang.blog.csdn.net



- 企业签最近越来越严格，所以有的人想出了插件化，但是最终效果告诉大家，还是不要尝试的较好。


分享下效果图：

奥特曼超人 - KARL-Dujinyang

![image](https://img-blog.csdn.net/20170420161354914?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvREpZMTk5Mg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

<hr/>

有兴趣的可以关注【Python2048】 公众号<br/>
分享技术、灰色产业、职业规划、赚钱之道、逆向破解等趣事……

<img src="https://github.com/sheep0704/IOSIphoneHttps/blob/master/python2048-.jpg" width="400" height="400">

![image](https://github.com/sheep0704/IOSIphoneHttps/blob/master/python2048-.jpg)



 

