---
title: "수업 #1, 이론적 개요"
lastUpdate: Thu May 04 2023 12:54:41 GMT+0400 (Samara Standard Time)
description: 홈 어시스턴트 코스
lessonNumber: 1
metaOptions: [로보노믹스와 홈 어시스턴트를 활용한 주권 스마트 홈 배우기]
defaultName: Sovereign Smart Home with Robonomics and Home Assistant
---

## 주권 스마트 홈의 주요 구성 요소 

<List>

1. **[라즈베리 파이](https://www.raspberrypi.org/), 싱글 보드 컴퓨터**.

모든 필요한 소프트웨어를 설치한 후에 이 장치를 IoT 허브로 변환할 수 있습니다. 허브의 주요 목적은 스마트 홈의 프로토콜, 네트워크, 응용프로그램 및 다양한 장치를 조율하는 것입니다.

2. **[홈 어시스턴트](https://www.home-assistant.io/), 오픈 소스 제어 시스템 소프트웨어**.

스마트 장치를 위한 중앙 허브로 설계되었습니다. 네트워크에서 알려진 장치를 자동으로 스캔하고 사용자가 모든 필요한 자동화를 쉽게 구성할 수 있도록 합니다. 라즈베리 파이에 홈 어시스턴트를 설치할 것입니다.

홈 어시스턴트는 장치와 통신하고 그들의 데이터를 로컬로 저장합니다. 이로 인해 원격으로 장치를 제어할 수 없습니다. 이 문제를 해결하기 위해 우리는 Robonomics Network를 사용합니다.

3. **[로보노믹스 네트워크](https://robonomics.network/), IoT 애플리케이션의 안전하고 신뢰할 수 있는 제어를 위한 분산 클라우드**.

로보노믹스는 스마트 장치와 그들의 데이터를 보호하기 해 분산화와 블록체인 기술을 결합한 web3 기술을 사용합니다.

로보노믹스의 주요 기능은 Polkadot/Kusama 생태계의 블록체인(패러체인)을 기반으로 구현됩니다. 패러체인의 주요 기능 중 하나는 장치를 실행하는 명령을 보내고 사용자 데이터를 블록체인에 저장할 수 있는 능력입니다.

로보노믹스 패러체인에는 사용자가 한 달 동안 수수료 없이 패러체인에 거래를 보낼 수 있는 IoT 구독 기능이 있습니다. 이 과정의 실제 섹션에서는 구독 방법을 사용할 것입니다.

IoT 허브와 로보노믹스 패러체인 간의 상호 작용은 [robonomics-interface](https://github.com/Multi-Agent-io/Robonomics-interface)를 사용하여 이루어집니다 — 로보노믹스와의 편리한 프로그래밍을 위해 특화된 Python 라이브러리입니다.

4. **[간행성 파일 시스템](https://ipfs.tech/) (IPFS), 분산 파일 시스템에서 데이터를 저장하고 공유하기 위한 P2P 소프트웨어**.

IPFS는 블록체인에 대용량 파일을 저장하는 것을 피하기 위해 필요합니다 (비용이 너무 비쌉니다). 대신 파일의 IPFS 해시를 저장할 수 있으며, 이는 이러한 파일로의 링크 역할을 합니다.

## 스마트 기기용 프로토콜
스마트 기기에는 두 가지 주요 프로토콜을 사용합니다:

1. **[지그비](https://csa-iot.org/all-solutions/zigbee/), 무선 통신 프로토콜.**

스마트 기기를 연결하는 데 매우 일반적으로 사용됩니다. 저전력 소비, 구성의 용이성 및 유연성, 자가 조직화 및 자가 복구 메시 네트워크 토폴로지를 지원하도록 설계되었습니다. 지그비 지원 장치는 수천 개가 시장에 출시되어 있어 스마트 홈 솔루션 구축에 매우 유용합니다. 지그비 장치를 제어하려면 지그비 네트워크와 다른 네트워크(예: Wi-Fi) 간에 데이터를 전송하는 게이트웨이가 필요합니다.

2. **[메시지 큐잉 텔레메트리 전송](https://mqtt.org/) (MQTT), IoT 애플리케이션을 제어하기 위해 설계된 발행-구독 프로토콜.**

이 프로토콜은 가벼우며 최소한의 리소스를 필요로 하며 메시지 전달의 신뢰성을 보장합니다. 이 프로토콜은 저 대역폭, 높은 지연 시간, 신뢰할 수 없는 네트워크를 대상으로 설계되어 있어 센서 메시지의 대량 처리에 우수한 선택지입니다. MQTT는 MQTT 브로커를 실행하는 서버가 필요합니다(우리의 경우에는 라즈베리 파이와 함께 작동할 것입니다). 브로커는 MQTT 클라이언트로부터 모든 메시지를 수신하고 이를 적절한 구독 클라이언트로 라우팅합니다.

## 지그비 연결 옵션
로보노믹스와 함께 홈 어시스턴트에 장치를 연결하는 두 가지 시나리오를 탐색하게 될 것입니다.

1. 첫 번째 시나리오는 장치를 연결하기 위해 별도의 지그비 게이트웨이를 사용하지 않습니다. 대신 [지그비 어댑터](https://www.zigbee2mqtt.io/guide/adapters/)와 [Zigbee2MQTT](https://www.zigbee2mqtt.io/guide/adapters/) 소프트웨어의 조합을 사용합니다.

<LessonImages figure figureCaption="Architectural scheme of the scenario with Zigbee adapter" src="smart-house-course/lesson-1-1.png" alt="Architectural scheme of the scenario with Zigbee adapter"/>

어댑터(예: JetHome USB JetStick Z2)는 라즈베리 파이에 연결되어 컴퓨터와 지그비 무선 통신 간의 인터페이스 역할을 합니다. Zigbee2MQTT는 Zigbee를 MQTT 네트워크에 연결할 수 있게 해주는 소프트웨어입니다. 이 소프트웨어는 Zigbee 네트워크에서 메시지를 가져와 MQTT의 사용하기 쉽고 잘 구조화된 메시지로 변환합니다.

2. 두 번째 시나리오에서는 장치를 ESP32 마이크로컨트롤러를 기반으로 한 [SLS 게이트웨이](https://github.com/slsys/Gateway)를 사용하여 연결합니다. 사용 의성을 위해 로보노믹스는 게이트웨이의 [자체 수정](https://oshwlab.com/ludovich88/robonomics_sls_gateway_v01)을 개발했습니다.

<LessonImages figure figureCaption="Architectural scheme of the scenario with SLS Gateway" src="smart-house-course/lesson-1-2.png" alt="Architectural scheme of the scenario with SLS Gateway"/>

SLS 게이트웨이는 지그비 프로토콜 메시지의 코디네이터 역할을 하며 대부분의 사용 가능한 지그비 장비를 사용할 수 있게 합니다. 홈 어시스턴트와의 통합을 위해 MQTT 프로토콜을 사용합니다.

## 원격 제어

스마트 홈의 원격 제어는 [로보노믹스 탈중앙화 애플리케이션](https://dapp.robonomics.network/)(dapp)을 사용하여 수행됩니다. 이 애플리케이션은 사용자 친화적인 방식으로 파라체인 기능에 액세스를 제공합니다. 사용자 데이터의 보안성과 불변성은 암호화된 데이터를 IPFS로 보내어(사용자의 키로만 해독할 수 있음) 보장되며, 이 데이터의 IPFS 해시를 블록체인에 배치함으로써 또 다른 보안성을 제공합니다.

</List>



