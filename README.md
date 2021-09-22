# websocket-car-controller

这是一个基于websocket的小车控制前后端系统,服务端基于ros(可以换成其他),支持网页客户端和程序客户端控制

## 目录结构
│  Carwebsocketclient.exe//客户端程序windows下打包
│  Carwebsocketclient.py//客户端程序的源码
│  Carwebsocketserver.py//服务端源码,使用ros,用于实际有ros环境的地方部署调用httpserver.py作为web服务端
│  favicon.ico
│  httpserver.py//web服务
│  websocketservertest.py//服务端源码,不使用ros,可以用于简单验证控制程序
│      
├─controlserver//ros的一个完整的服务端的包,基于ros使用的服务端例子
│  │  package.xml
│  │  setup.cfg
│  │  setup.py
│  │  
│  ├─controlserver
│  │  │  Carwebsocketclient.py
│  │  │  Carwebsocketserver.py
│  │  │  favicon.ico
│  │  │  httpserver.py
│  │  │  __init__.py
│  │  │  
│  │  ├─html
│  │  │  │  controlpage.html
│  │  │  │  
│  │  │  └─img
│  │  │          background.png...
│  │  │          
│  │  └─img
│  │          background.png...
│  │          
│  └─launch//ros启动文件
│          launchserver.launch.py
│          
├─html//网页源码
│  │  controlpage.html
│  │  
│  └─img//网页图片资源目录
│          background.png...
│          
├─img//图片文件夹
