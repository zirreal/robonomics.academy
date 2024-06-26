---
title: "수업 #2, 센서 하드웨어"
description: '센서 하드웨어'
lessonNumber: 2
metaOptions: [배우기, 센서 연결 및 분산 센서 네트워크]
defaultName: Sensors Connectivity & Decentralized Sensors Network
---

분산 센서 네트워크를 통한 대기 모니터링에 참여하려면 센서가 장착된 대기 오염 보드를 구해야 합니다. 이를 하는 두 가지 방법이 있습니다:

<List>

<li>필요한 모든 부품을 주문하여 사용자 정의 보드를 직접 조립합니다.</li>
<li>로보노믹스 팀에서 준비된 보드를 주문합니다.</li>

</List>

## 수동 보드 조립

자체 보드를 만들려면 다음 구성 요소를 찾아야 합니다:

- 레이저 PM2.5 및 PM10 센서 [SDS011](https://www.amazon.com/SDS011-Quality-Detection-Conditioning-Monitor/dp/B07FSDMRR5)

- ESP8266 기반의 시리얼 무선 모듈 [NodeMcu V3 CH340](https://www.amazon.com/ACEIRMC-Wireless-Development-Compatible-MicroPython/dp/B092ZCG2X2)

- 5A DC-DC 미니560 컨버터 [(예시)](https://www.amazon.com/Alinan-Efficiency-Converter-Regulator-Stabilized/dp/B09W8P1QNM)

- DC 커넥터 [(예시)](https://www.amazon.com/CenryKay-DC-099-Threaded-연결or-Adapter/dp/B08CMMQMP6?th=1)

- 12V/2А 전원 어댑터 [(예시)](https://www.amazon.com/TMEZON-Power-Adapter-Supply-2-1mm/dp/B00Q2E5IXW)

- 마운팅 박스 [(예시)](https://www.amazon.com/LeMotech-Dustproof-Waterproof-Electrical-300mmx250mmx120mm/dp/B075DHT7X2/ref=sxin_18_ac_d_mf_brs?ac_md=7-4-TGVNb3RlY2g%3D-ac_d_mf_brs_brs&content-id=amzn1.sym.1ad31f34-ba12-4dca-be4b-f62f7f5bb10d%3Aamzn1.sym.1ad31f34-ba12-4dca-be4b-f62f7f5bb10d&crid=2ZDX87O7MINYG&cv_ct_cx=junction+box+plastic&keywords=junction+box+plastic&pd_rd_i=B075DHT7X2&pd_rd_r=2bbd50d4-9ef9-4fa1-a1a2-e55c482bce49&pd_rd_w=EcHLy&pd_rd_wg=z42mC&pf_rd_p=1ad31f34-ba12-4dca-be4b-f62f7f5bb10d&pf_rd_r=WDAX58YZKG6YKZ70X5QE&qid=1676642125&sprefix=Junction+Box%2Caps%2C451&sr=1-4-8b2f235a-dddf-4202-bbb9-592393927392)

또한 추가 센서를 설치할 수 있습니다:

<List  type="numbers">

<li>

I2C 인터페이스로:

<List>

<li>

[BMP180](https://cdn-shop.adafruit.com/datasheets/BST-BMP180-DS000-09.pdf) — 온도 및 습도

</li>

<li>

[BME/P280](https://www.mouser.com/datasheet/2/783/BST-BME280-DS002-1509607.pdf) — 온도, 습도, 대기압

</li>

<li>

[HTU21D](https://eu.mouser.com/ProductDetail/Measurement-Specialties/HTU21D?qs=tx5doIiTu8oixw1WN5Uy8A%3D%3D) — 온도 및 습도

</li>

<li>

[CCS811 VOC SENSOR](https://www.sciosense.com/wp-content/uploads/documents/Application-Note-Baseline-Save-and-Restore-on-CCS811.pdf) — 휘발성 유기 화합물, CO2 동등체

</li>

</List>

</li>

<li>

1-Wire 인터페이스로:

<List>

<li>

[DHT22(AM2302)](https://files.seeedstudio.com/wiki/Grove-Temperature_and_Humidity_Sensor_Pro/res/AM2302-EN.pdf) — 온도 및 습도

</li>

<li>

[DS18B20](https://cdn.sparkfun.com/datasheets/Sensors/Temp/DS18B20.pdf) — 온도

</li>

</List>

</li>

</List>

어셈블리 프로세스는 아래 비디오에서 찾을 수 있습니다. 플래싱 프로세스도 보여주지만, 나중에 이에 대해 이야기하겠습니다.

<RoboAcademyYoutube link="https://www.youtube.com/watch?v=OdTd1sacCso" />

## 로보노믹스 보드 요청

대안으로, 로보노믹스 보드를 요청할 수 있습니다. 이를 위해 다음 주소 중 하나로 이메일을 보내주십시오:

- vm@multi-agent.io
- ping@airalab.org

로보노믹스 보드는 ESP8266을 기반으로 하며 6-24V 전원 공급을 위해 설계되었으며 DC-DC 컨버터 DC MINI560을 사용합니다. 이 보드를 사용하면 SDS011 입자 센서 및 여러 추가 센서(위의 목록 확인)를 연결할 수 있습니다. 또한 연결 가능한 장치 목록이 줄어든 작은 MINI 모델도 있습니다.

<LessonImages figure figureCaption="Full model of Robonomics board" src="sensors-connectivity-course/lesson-2-1.png" alt="Full model of Robonomics board"/>

<LessonImages  figure figureCaption="Mini model of Robonomics board" src="sensors-connectivity-course/lesson-2-2.png" alt="Mini model of Robonomics board"/>

두 모델의 설계도는 여기에서 찾을 수 있습니다: [풀 모델](https://oshwlab.com/ludovich88/aira_sensor_rev0-1) 및 [미니 모델](https://oshwlab.com/ludovich88/aira_sensor_d1_mini).

보드를 자세히 살펴보겠습니다. 연결을 위한 여러 커넥터 포트가 있습니다(파란색과 녹색으로 강조되어 있습니다).

<LessonImages imageClasses="mb" src="sensors-connectivity-course/lesson-2-3.png" alt="Full model of Robonomics board"/>

왼쪽부터 파란색 단자 블록(모든 단자에는 표시가 있음):

<List>
  <li class="flex">

  <code>12V</code> — 보드에 전원 공급을 연결하는 단자; 권장 전압은 12볼트입니다.

  </li>

  <li class="flex">

  <code>GND</code> 그라운드(제로 포텐셜 지점) — 전원 공급의 제로 포텐셜 연결 및 센서 연결을 위해 사용됩니다.

  </li>

  <li class="flex">

  <code>POWER SENSOR</code> — 센서가 연결되는 구성 가능한 전원 출력; 출력은 3.3V 또는 5V로 설정할 수 있습니다.

  </li>

  <li class="flex">

  <code>SDA</code> — 시리얼 데이터 라인, I2C 인터페이스를 통해 센서를 연결하는 데 사용됩니다.

  </li>

  <li class="flex">

  <code>SCL/1WIRE</code> — 시리얼 클럭 라인이 연결되는 구성 가능한 단자; I2C 또는 1-Wire 인터페이스를 통해 센서를 연결하는 데 사용됩니다.

  </li>
</List>

센서를 위한 전원 출력 설정 및 인터페이스 선택은 이미지에서 노란색으로 표시된 점퍼를 설정하여 수행됩니다(`5V`, `3V`, `I2C`, `1WIRE`). 점퍼는 수평으로 설치되며, 점퍼를 설치할 위치에는 표시가 있습니다.


<RoboAcademyNote type="warning" title="WARNING">
전원 공급 전압을 선택하려면 3.3볼트 또는 5볼트로만 하나의 점퍼를 설정하면 됩니다. 3.3V 및 5V로 두 개의 점퍼를 설정하면 장치가 손상됩니다. 센서 인터페이스를 선택할 때도 I2C 또는 1-Wire의 위치에 하나의 점퍼만 설치하십시오. 두 개의 점퍼를 설치하면 장치가 손상될 수 있습니다.
</RoboAcademyNote>

보드에는 입력용 추가 블록이 있으며, 이미지에서 녹색으로 표시됩니다(`GND`, `5V`, `SDA`, `SCL`).

파란 상자의 왼쪽에는 보드를 다시 부팅하기 위한 전원 스위치가 있습니다. 기본적으로 `ON` 위치에 있습니다.

센서를 설정한 후에는 플래시 및 구성만 남아 있습니다.
