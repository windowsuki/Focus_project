# Focus_project
记录一下学习过程
## 1/14
### TASK1
**auduino环境配置:**

在preference里添加

``` 
https://espressif.github.io/arduino-esp32/package_esp32_index.json
https://arduino.esp8266.com/stable/package_esp8266com_index.json
```

在boards manager中搜索并自动下载esp32驱动

自动下载跑不动就手动复制粘贴要下载的文件到下载路径XD

**阿里云物联网平台配置:** 

试着用mqtt.fx测试了

照着[使用MQTT协议模拟设备快速接入物联网平台_物联网平台(IoT)-阿里云帮助中心](https://help.aliyun.com/zh/iot/getting-started/using-mqtt-fx-to-access-iot-platform?spm=5176.28426678.J_HeJR_wZokYt378dwP-lLl.2.32585181XUcakx&scm=20140722.S_help@@文档@@140507.S_BB1@bl+BB2@bl+RQW@ag0+os0.ID_140507-RL_mqttfx-LOC_search~UND~helpdoc~UND~item-OR_ser-V_4-P0_1-P1_0)做就行了

**点灯: **我板子呢

## 1/18

**转用platformio**

### TASK2.0

![image](.\esp32\picture\helloworld.png)

platformio自带的串口监视器不知道为什么监测不到，先用之前的小工具

### TASK2.1

![image](.\esp32\picture\helloWifi.png)

[使用Arduino开发ESP32（03）：WiFi基本功能使用_arduino wifi 功率-CSDN博客](https://blog.csdn.net/Naisu_kun/article/details/86165403)

### TASK2.2

先通过mqtt.fx测试了一下

![mqttesp32](.\esp32\picture\mqttfx.png)

然后在板子上通过例程实现了和物联网平台的通信

![mqttesp32](.\esp32\picture\mqttesp32.png)

[使用MQTT协议模拟设备快速接入物联网平台_物联网平台(IoT)-阿里云帮助中心](https://help.aliyun.com/zh/iot/getting-started/using-mqtt-fx-to-access-iot-platform?spm=a2c4g.11174283.6.584.3a8b1668HMO0MX#84180893107ui)

mqtt连接所用的参数，都能在物联网平台>设备>设备信息中查看

## 1/19

### TASK2.2.1/2.2.2

1. Android Studio下载速度过慢，配置镜像源: [解决Gradle报错：Plugin [id: ‘com.android.application‘, version: ‘x.x.x‘, apply: false\] was not found_plugin [id: 'com.android.application', version: '8-CSDN博客](https://blog.csdn.net/qq_43811536/article/details/139447518)

2. 先尝试着构建他给出的代码，并作出简单改变（mqtt参数设置、ui改写）![androidtest](.\picture\androidtest.png)
3. 安装app到模拟器，通过物联网平台的日志，确认可以连接并发送消息![androidconnect](.\picture\androidconnect.png)

## 总结

本次冬令营由于本人散漫的习惯及忘记带板子回家，时间实在是不够充裕，只能粗略的完成合格要求。

在本次冬令营中，我学到了1. 基于platformio和arduino的esp32开发 2. 基于Android studio的app开发

其中，esp32我主要学习了wifi和mqtt连接；Android studio我在给出的源码的基础上修改，对其逻辑几乎是一窍不通，只是改了些皮毛
