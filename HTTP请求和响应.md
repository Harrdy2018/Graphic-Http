# HTTP请求和响应


# HTTP请求报文格式
* HTTP请求报文主要由请求行、请求头部、请求正文3部分组成
***
![HTTP请求报文格式](https://github.com/Harrdy2018/Graphic-Http/blob/master/HTTP%E8%AF%B7%E6%B1%82%E6%8A%A5%E6%96%87%E6%A0%BC%E5%BC%8F.png)
***
* 请求行
```
由3部分组成，分别为：请求方法、URL（见备注1）以及协议版本，之间由空格分隔
请求方法包括GET、HEAD、PUT、POST、TRACE、OPTIONS、DELETE以及扩展方法，当然并不是所有的服务器都实现了所有的方法，部分方法即便支持，处于安全性的考虑也是不可用的
协议版本的格式为：HTTP/主版本号.次版本号，常用的有HTTP/1.0和HTTP/1.1
```

* 请求头部
***
```
请求头部为请求报文添加了一些附加信息，键值对构成,下面解释比较容易混淆的几个点：
Content-Type：When sending data to the server, use this content type. Default is “application/x-www-form-urlencoded;

Data-Type:The type of data that you’re expecting back from the server. If none is specified, jQuery will try to infer it based on the MIME type of the response (an XML MIME type will yield XML, in 1.4 JSON will yield a JavaScript object, in 1.4 script will execute the script, and anything else will be returned as a string).

Accept:accepts (default: depends on DataType) Type: PlainObject The content type sent in the request header that*** tells the server what kind of response it will accept in return.*

Connection:Keep-Alive,保持连接，在HTTP 1.0中默认是关闭的，需要自己设置；在HTTP1.1中是默认启用的，如果加入Connection:close,才关闭
```
***
|请求头|说明|
|:-----|:-----|
|Host|接受请求的服务器地址，可以是IP:端口号，也可以是域名|
|Connection|指定与连接相关的属性，如|
|Content-Length|请求内容的长度|
|User-Agent|发送请求的应用程序名称|
|Content-Type|告诉服务器，我要发什么类型的数据|
|Data-Type|告诉服务器，我要想什么类型的数据，如果没有指定，那么会自动推断是返回 XML，还是JSON，还是script，还是String|
|Accept|告诉服务器，能接受什么类型|
|Accept-Charset|通知服务端可以发送的编码格式|
|Accept-Encoding|通知服务端可以发送的数据压缩格式|
|Accept-Language|通知服务端可以发送的语言|

***
* 请求正文
可选部分，比如GET请求就没有请求正文

***
#HTTP响应报文格式
***
![HTTP响应报文格式](https://github.com/Harrdy2018/Graphic-Http/blob/master/HTTP%E5%93%8D%E5%BA%94%E6%8A%A5%E6%96%87%E6%A0%BC%E5%BC%8F.png)
***
