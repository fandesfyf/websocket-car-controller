# websocket-car-controller

这是一个基于websocket的小车控制前后端系统,服务端作为一个ros包(也可以不用ros)部署后,可以通过网页客户端和程序客户端控制

```
## 目录结构
│  Carwebsocketclient.exe//客户端程序windows下打包
│  Carwebsocketclient.py//客户端程序的源码
│  Carwebsocketserver.py//服务端源码,使用ros,用于实际有ros环境的地方部署调用httpserver.py作为web服务端
│  favicon.ico
│  httpserver.py//单独的web服务端,最新版的源码web服务端已经整合到Carwebsocketserver里面去了
│  websocketservertest.py//服务端源码,不使用ros,可以用于简单验证控制程序,要是也可以基于此增加自己的控制服务端程序
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
```
## 界面演示
![image](https://github.com/fandesfyf/websocket-car-controller/blob/main/demo/1.jpg)
![image](https://github.com/fandesfyf/websocket-car-controller/blob/main/demo/2.jpg)

## 使用方法
#### 网页端控制：
浏览器通过 http://[ip]:10590 即可访问控制界面

摇杆控制:点击屏幕即可

键盘控制:键盘上的WS键改变前进后退速度,AD键改变转弯速度;双击WSAD键可在对应方向加速,多次按下箭头键连续加速;ESC/q键断开,其他键急停,运动时按反向键急停

虚拟按键:点击屏幕上的虚拟按键即可，规则与键盘控制规则一样，虚拟按键模式下摇杆不可用

虚拟摇杆/虚拟按键模式下外接键盘均可用


#### 客户端控制：
打开客户端程序后输入服务端所在的ip(客户端控制的端口默认为8787),点击连接后连接成功即可控制.

WS键改变前进后退速度,AD键改变转弯速度;双击WSAD键可在对应方向加速,箭头键连续加速;ESC/q键断开,其他键急停,运动时按反向键急停;



