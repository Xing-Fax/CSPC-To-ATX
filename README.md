# CSPC转ATX 电源转接板

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

待完善...
