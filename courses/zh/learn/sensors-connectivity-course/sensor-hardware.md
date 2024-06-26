---
title: "第2课，传感器硬件"
description: '传感器硬件'
lessonNumber: 2
metaOptions: [学习, 传感器连接性和分散式传感器网络]
defaultName: Sensors Connectivity & Decentralized Sensors Network
---

如果您希望参与分散式传感器网络的空气监测，您需要获取一个带有传感器的空气污染板。有两种方法可以做到这一点:

<List>

<li>订购所有必要的零件并自己组装定制板。</li>
<li>从Robonomics团队订购一个现成的板。</li>

</List>

## 手动板组装

要构建您自己的板，您需要找到以下组件:

- 激光PM2.5和PM10传感器[SDS011](https://www.amazon.com/SDS011-Quality-Detection-Conditioning-Monitor/dp/B07FSDMRR5)

- 基于ESP8266的串行无线模块[NodeMcu V3 CH340](https://www.amazon.com/ACEIRMC-Wireless-Development-Compatible-MicroPython/dp/B092ZCG2X2)

- 5A DC-DC mini560转换器[(示例)](https://www.amazon.com/Alinan-Efficiency-Converter-Regulator-Stabilized/dp/B09W8P1QNM)

- DC连接器[(示例)](https://www.amazon.com/CenryKay-DC-099-Threaded-连接or-Adapter/dp/B08CMMQMP6?th=1)

- 12V/2А电源适配器[(示例)](https://www.amazon.com/TMEZON-Power-Adapter-Supply-2-1mm/dp/B00Q2E5IXW)

- 安装盒[(示例)](https://www.amazon.com/LeMotech-Dustproof-Waterproof-Electrical-300mmx250mmx120mm/dp/B075DHT7X2/ref=sxin_18_ac_d_mf_brs?ac_md=7-4-TGVNb3RlY2g%3D-ac_d_mf_brs_brs&content-id=amzn1.sym.1ad31f34-ba12-4dca-be4b-f62f7f5bb10d%3Aamzn1.sym.1ad31f34-ba12-4dca-be4b-f62f7f5bb10d&crid=2ZDX87O7MINYG&cv_ct_cx=junction+box+plastic&keywords=junction+box+plastic&pd_rd_i=B075DHT7X2&pd_rd_r=2bbd50d4-9ef9-4fa1-a1a2-e55c482bce49&pd_rd_w=EcHLy&pd_rd_wg=z42mC&pf_rd_p=1ad31f34-ba12-4dca-be4b-f62f7f5bb10d&pf_rd_r=WDAX58YZKG6YKZ70X5QE&qid=1676642125&sprefix=Junction+Box%2Caps%2C451&sr=1-4-8b2f235a-dddf-4202-bbb9-592393927392)

此外，您还可以安装其他传感器:

<List  type="numbers">

<li>

使用I2C接口：

<List>

<li>

[BMP180](https://cdn-shop.adafruit.com/datasheets/BST-BMP180-DS000-09.pdf) — 温度和湿度

</li>

<li>

[BME/P280](https://www.mouser.com/datasheet/2/783/BST-BME280-DS002-1509607.pdf) — 温度、湿度、大气压力

</li>

<li>

[HTU21D](https://eu.mouser.com/ProductDetail/Measurement-Specialties/HTU21D?qs=tx5doIiTu8oixw1WN5Uy8A%3D%3D) — 温度和湿度

</li>

<li>

[CCS811 VOC传感器](https://www.sciosense.com/wp-content/uploads/documents/Application-Note-Baseline-Save-and-Restore-on-CCS811.pdf) — 挥发性有机化合物、CO2等效

</li>

</List>

</li>

<li>

使用1-Wire接口：

<List>

<li>

[DHT22(AM2302)](https://files.seeedstudio.com/wiki/Grove-Temperature_and_Humidity_Sensor_Pro/res/AM2302-EN.pdf) — 温度和湿度

</li>

<li>

[DS18B20](https://cdn.sparkfun.com/datasheets/Sensors/Temp/DS18B20.pdf) — 温度

</li>

</List>

</li>

</List>

您可以在下面的视频中找到组装过程。视频还展示了闪存过程，但我们稍后会讨论它。

<RoboAcademyYoutube link="https://www.youtube.com/watch?v=OdTd1sacCso" />

## 请求Robonomics板

或者，您可以请求Robonomics板。要这样做，请发送电子邮件至以下地址之一：

- vm@multi-agent.io
- ping@airalab.org

Robonomics板基于ESP8266，设计用于6-24V电源供应，使用DC-DC转换器DC MINI560。该板允许您连接SDS011颗粒传感器和几个附加传感器（请查看上面的列表）。还有一个较小的MINI型号，可接的设备列表较短。

<LessonImages figure figureCaption="Full model of Robonomics board" src="sensors-connectivity-course/lesson-2-1.png" alt="Full model of Robonomics board"/>

<LessonImages  figure figureCaption="Mini model of Robonomics board" src="sensors-connectivity-course/lesson-2-2.png" alt="Mini model of Robonomics board"/>

这两种型号的蓝图可以在这里找到：[完整型号](https://oshwlab.com/ludovich88/aira_sensor_rev0-1) 和 [迷你型号](https://oshwlab.com/ludovich88/aira_sensor_d1_mini)。

让我们更仔细地看看这块板。它有几个连接端口（用蓝色和绿色标出）。

<LessonImages imageClasses="mb" src="sensors-connectivity-course/lesson-2-3.png" alt="Full model of Robonomics board"/>

蓝色端子块，从左到右（所有端子都有标记）：

<List>
  <li class="flex">

  <code>12V</code> — 连接电源供应到板的端子；推荐电压为12伏特。

  </li>

  <li class="flex">

  <code>GND</code> 地线（零电位点） — 用于连接电源的零电位，也用于连接传感器。

  </li>

  <li class="flex">

  <code>POWER SENSOR</code> — 可配置的电源输出，连接传感器；输出可以设置为3.3或5伏特。

  </li>

  <li class="flex">

  <code>SDA</code> — 串行数据线，用于通过I2C接口连接传感器。

  </li>

  <li class="flex">

  <code>SCL/1WIRE</code> — 可配置的端子，连接串行时钟线；用于通过I2C或1-Wire接口连接传感器。

  </li>
</List>

通过设置标记为黄色的跳线（`5V`，`3V`，`I2C`，`1WIRE`）来设置传感器的电源输出和选择接口。跳线水平安装，安装位置有标记。


<RoboAcademyNote type="warning" title="WARNING">
您可以通过设置一个跳线选择电源供应的电压为3.3伏特或5伏特。设置两个跳线为3.3和5伏特将损坏设备。选择传感器接口时也适用相同规则，只需在I2C或1-Wire的位置安装一个跳线。安装两个跳线可能会损坏设备。
</RoboAcademyNote>

该板还有一个额外的输入块，标记为绿色（`GND`，`5V`，`SDA`，`SCL`）。

在蓝色框的左侧有一个电源开关，用于强制板重新启动。默认情况下处于`ON`位置。

设置传感器后，只需闪存和配置它。
