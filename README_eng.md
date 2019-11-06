# IOSIphoneHttps

* [英文版](https://github.com/sheep0704/IOSIphoneHttps/blob/master/README_eng.md)
* [中文版](https://github.com/sheep0704/IOSIphoneHttps/blob/master/README.md)

<br/>

  * Update today: Recently, super sign related seals are serious, which are caused by association. It is recommended not to bind the same card.
  * Later update: the signature will not be removed after the update, that is, the so-called super sign method. No third-party operation is required, but the cost is a little expensive.
  * Latest version: 2019 Apple's application is strict. It can be downloaded and installed directly by signing. It does not need to enter the Appstore mall, and it does not need a third party to directly use and install by itself
  
Would you like to download the game directly without going through the app store? Don't know how to install after downloading? Need to install through third-party software? Here's Ultraman to take you to the new installation tutorial:<br/>
To build an HTTPS service, you can use httpd or Tomcat to build<br/>
Use plist file to adjust the installation extension through a tag - (you can judge whether to install through JS. If it is not installed directly, download it when it is installed.) in the morning, there is a demand for download page in HTML 5. Android and apple are needed. Generally speaking, apple uses a third party or app store, but this time it is an internal app and IPA, so there must be a way to bypass this. In fact, the third party So is the principle of tripartite implementation. Let's take a look at the following steps.<br/>
First, download the plist file template: click here to download the external link: https://github.com/sheep0704/iosiphonehttps/blob/master/x5.plist pay attention to the details. If you copy the template yourself, don't leave out the following statement:<br/>
Then put the plist file in the HTTPS service directory. If there is no suggestion from the server to use baiduyun or GitHub for testing. If the browser prompts [can't connect to GitHub. Com], please check the interception of the plist file and the server. Some mahas will also write the XML incorrectly. You can directly access the plist address with a browser.<br/>
Then test by a tag write<br/><br/>

Apple genuine Download<br/><br/>

Click the test, and it is found that it has no effect. Apple's browser will prompt you that you can't connect to github.com. Let's intercept the request and check it out. We found that the provision headers are shown Ultraman<br/>
Reason: ITMS services should not support self signed SSL certificates. To put plist files, you need to use SSL certificates<br/>
Summary: it was found that it was not possible to debug several times at the beginning, because NgR was used and Tomcat of 127.0.0.1 was mapped, so it was later replaced with our own server address, which was feasible after testing, so it is suggested that there should be no forwarding process in the middle, and the test should be conducted directly with the external network server.<br/>
||Copyright notice: This is the original article of blogger Du Jinyang. Please indicate the source for reprint.<br/>

http://dujinyang.blog.csdn.net/article/details/70267202

<br/>

http://dujinyang.blog.csdn.net]{http://dujinyang.blog.csdn.net

Recently, enterprise signing has become more and more strict, so some people have come up with plug-ins, but the final effect tells you that it's better not to try.<br/>
Share the following renderings:<br/>
 
 
 
 
奥特曼超人 - KARL-Dujinyang

![image](https://img-blog.csdn.net/20170420161354914?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvREpZMTk5Mg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

<hr/>

有兴趣的可以关注【Python2048】 公众号Wechat<br/>
分享技术、灰色产业、职业规划、赚钱之道、逆向破解等趣事……

<img src="https://github.com/sheep0704/IOSIphoneHttps/blob/master/python2048.jpg" width="300" height="300">



 

