# CSPC转ATX 电源转接板

## 工程概述

将CSPS接口的电源转接为标准ATX电源转接器，具有额定750W功率(5V 30A、3.3V 30A、5Vsb 10A、12V视电源决定)，具备基本过欠压保护、软起动、电压补偿、PMBus监控(待完善)，主板预留I2C通信接口、线损补偿输入接口、12V常电及调试拨码开关(强制启动、POSN信号工作状态切换、DC-DC模块使能)

![image (3)](CSPS%20To%20AXT%20Power/image/image(3).jpg)

转接板使用TSP3511芯片作为电源管理芯片，并提供PSON启动时序

![image (3)](CSPS%20To%20AXT%20Power/image/Seq.png)

使用 VRP1-30E1A0 作为DC-DC模块，提供3.3V、5V、5Vsb电压，具备30A供电能力

![image (3)](CSPS%20To%20AXT%20Power/image/30E.png)

## 电路原理图预览

![image (3)](CSPS%20To%20AXT%20Power/image/Main.png)

![image (3)](CSPS%20To%20AXT%20Power/image/Mode.png)

![image (3)](CSPS%20To%20AXT%20Power/image/TPS3511.png)

## 已知问题

VRP1-30E1A0模块在低负载时温度会很高，所以5Vsb那一路DC-DC模块设计有缺陷，应考虑替换为其他DC-DC

PMBus程序尚未完善，参考[Client for KCORES CSPS to ATX Converter](https://github.com/KCORES/kcores-link) 未来会通过单片机+屏幕+上位机实现此功能

需要自己定制模组线，ATX24Pin需要带线损补偿接口，8Pin接口并没有对CPU供电或者显卡供电做极性调换，请注意正负极

总之问题一大堆，开发费资金，所以项目也就暂时咕咕咕了...未来如果有机会将会构它

目前此方案已经到验证，负载450W，连续8小时，室温约26°C，表面温度不超过60°C(DC-DC模块有风扇进行散热)

上测试平台，正常运行约5个月，目前未出现任何问题

## 工程文件

## 参考文档
待完善...
