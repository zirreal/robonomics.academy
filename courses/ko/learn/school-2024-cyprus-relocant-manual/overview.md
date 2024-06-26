---
title: "로보노스 스쿨 2024 / 사이프러스 이주자 매뉴얼: 스마트 홈"
lastUpdate: 
description: "사이프러스 이주자 매뉴얼: 스마트 홈"
metaOptions: [배우기, "로보노믹스 스쿨 2024 / 사이프러스 이주자 매뉴얼: 스마트 홈"]
defaultName: "Robonomics School 2024 / Cyprus Relocant Manual: Smart Home"
---

<LessonImages imageClasses="mb"  src='school-2024-cyprus-relocant-manual/Setup_SmartHome-Academy.jpg' alt="Cyprus Relocant Manual Cover" />

거주 국가를 변경하는 것은 항상 새로운 기회뿐만 아니라 도전을 가져옵니다. 내 경우에는 새로운 나라가 사이프러스였는데, 거기서 회사를 설립하기 위해 왔습니다. 이사하기 전 10년 동안 큰 도시에서 살았는데, 그곳에서 도시로부터의 중앙 난방, 온수 공급, 저렴한 전기와 같은 특정 혜택에 익숙해졌습니다. 사이프러스에서는 각 집과 각 아파트가 생활 지원 측면에서 훨씬 더 자율적이지만 편안한 삶을 유지하는 것에 대한 걱정은 소유자에게 달려 있습니다. 예를 들어 온수를 들어보겠습니다. 추운 달에는 보일러를 직접 켜서 데워야 합니다. 아파트도 직접 난방해야 합니다. 겨울에는 열담요와 보일러를 켜고 끄고, 여름에는 에어컨과 모기 퇴치제를 사용합니다. 이것은 시간과 에너지뿐만 아니라 돈도 필요로 합니다.

사이프러스에서의 첫 겨울은 천문학적인 전기 요금으로 이어졌습니다. 이것은 내 예산에 심각한 타격을 입혔습니다. 한 가지 가능한 해결책: 습관을 바꾸고 새로운 환경에 적응하는 것입니다. 그러나 이사한 후에는 이미 충분한 걱정이 있을 것입니다. 엔지니어로서, 비용을 통제하고 내 삶을 더 편안하게 만들어줄 솔루션을 찾기 시작했고, 그 경험을 여러분과 공유하고 싶습니다.

## 하드웨어 선택

처음으로 시작하고 싶은 것은 생태계를 선택하는 것입니다. 유선 시스템은 큰 예산과 아파트/집의 인프라에 심각한 개입을 필요로 하기 때문에 즉시 제외됩니다. 무선 장치 중에는 Sonoff와 Tyua 브랜드 아래에 수많은 장치가 있지만, 모두 인터넷을 통해 작동하기 때문에 섬에서 항상 신뢰할 수 없습니다. 이는 다른 회사의 서버에서 개인 데이터의 개인 정보 보호와 안전 문제를 언급하지 않은 것입니다. 주요 홈 서버로 [Home Assistant](https://www.home-assistant.io)를 사용하여 스마트 홈을 구축하는 것을 권장합니다. 장점: 외부 인터넷에 액세스하지 않고 작동할 수 있음; 이사할 때 가져갈 수 있으며 설정을 잃지 않고 새로운 장소에 배치할 수 있음; 스마트 TV, 청소기 등을 포함한 수많은 장치를 지원함.

장치의 무선 연결을 위한 가장 인기 있는 프로토콜�� Wi-Fi, Zigbee, Bluetooth입니다. 한 아파트에서 세 가지 유형의 연결을 동시에 찾을 수 있지만, 일반적인 것들을 스마트하게 만드는 장치에 대해선 Zigbee 프로토콜로 작업하는 것이 더 편리합니다. 이 경우, 주소와 커버리지 영역에 대해 걱정할 필요가 없으며 배터리로 작동할 수 있습니다. Wi-Fi 장치는 전원에 지속적으로 연결되어 있어야 하며 Wi-Fi 신호의 강도에 의존합니다. 라우터와 침실 사이에 벽이 두 개 있는 작은 아파트에서도 때로는 Wi-Fi 익스텐더를 설치해야 할 수도 있습니다. Zigbee의 경우, 장치 자체가 중계기 역할을 합니다.

사이프러스로 돌아와서, 필요한 최소한의 장치는 다음과 같았습니다:

## 컴퓨터 - ��� 서버

서버의 궁극적인 역할은 Home Assistant로 제어되는 스마트 홈을 제공하는 것입니다. 가장 쉬운 방법은 이미 사전 구성된 [Home Assistant Green](https://www.home-assistant.io/green/)를 사용하는 것입니다. 비용은 [세금 제외 €70](https://thepihut.com/products/home-assistant-green)입니다.

<LessonImages src="school-2024-cyprus-relocant-manual/home-assistant-green.png" alt="Home Assistant green"/>

옵션은 조금 더 고급스러울 수 있지만, 운영 체제에 대한 제어도 가능합니다. 이를 위해 [Raspberry Pi](https://www.raspberrypi.com)를 찾거나 구입할 수 있습니다. 비용은 [세금 제외 €90](https://https://thepihut.com/products/raspberry-pi-5-starter-kit)입니다. [Installation](https://www.home-assistant.io/installation/) 페이지에는 모든 취향에 맞는 많은 옵션이 있습니다.

<LessonImages imageClasses="small" src="school-2024-cyprus-relocant-manual/raspberry-pi.png" alt="Raspberry Pi"/>

Zigbee Coordinator로는 [Sonoff Zigbee Dongle P 또는 E](https://sonoff.tech/product/gateway-and-sensors/sonoff-zigbee-3-0-usb-dongle-plus-p/)를 사용합니다. 이 제품들은 거의 항상 구입 가능합니다. 비용은 약 [€35](https://www.amazon.de/-/en/dp/B09KXTCMSC/)입니다. [이 목록](https://www.zigbee2mqtt.io/guide/adapters/)에서 스틱을 선택할 수도 있습니다.

<LessonImages imageClasses="small" src="school-2024-cyprus-relocant-manual/sonoff-zigbee-stick.png" alt="Sonoff Zigbee USB Stick"/>

가정용 서버에는 정적 로컬 IP 주소를 할당하는 것을 강력히 권장합니다. 라우터 설정에 들어갈 수 없는 경우, 추가로 �� 번째 라우터를 설치하고 인터넷을 구성할 수 있습니다. (저는 [MikroTik](https://mikrotik.com/product/hap_ax2)을 사용하고 있습니다. 약 [€80](https://www.mstronics.com/c/337_1345_485/networking-devices-routers.html?filter_id=154)입니다.) 그리고 일반적으로 모든 스마트 Wi-Fi 장치에는 정적 IP를 할당하는 것이 좋습니다. 이것은 Home Assistant 통합이 올바르게 작동하는 데 종종 중요합니다.

## 보일러 ��위치

보일러는 3-3.5 kWh를 소비하며 일반적인 스마트 스위치는 작동하지 않을 것입니다. 선택할 때 허용 전류에 주의해야 합니다. 최소 16A, 가능하면 20A여야 합니다. 섬 자체에서 빠르게 Zigbee 스위치를 찾기 어렵습니다. [중국](https://vi.aliexpress.com/item/1005006833309900.html)에서 주문했고 약 €20 정도 들었습니다.

<robo-academy-grid :columns="2" textAlign="center">
    <robo-academy-grid-element>
      <LessonImages src="school-2024-cyprus-relocant-manual/boiler-switch-dimension.png" alt="Boiler Switch"/>
    </robo-academy-grid-element>
    <robo-academy-grid-element>
      <LessonImages src="school-2024-cyprus-relocant-manual/boiler-switch-wiring.png" alt="Boiler Switch Wiring"/>
    </robo-academy-grid-element/>
</robo-academy-grid>

가장 중요한 첫 번째 자동화는 모든 활성화 후 N분 후에 버튼을 끄는 것입니다. 설정하고 나면 버튼을 까먹었는지 또는 세 번째 날부터 작동했는지 생각할 필요가 없습니다. Home Assistant용 자동화 예제입니다. `device_id`와 `entity_id`로 교체해야 합니다.

<LessonCodeWrapper language="yaml" noCopyIcon>
    alias: Boiler turn off after 30 min
    description: ""
    trigger:
    - platform: device
        type: turned_on
        device_id: a7ee4b26ec5b9e36d959f7b4b8490c42
        entity_id: 61230c7b5528330e3b60ee38c5fe1f12
        domain: switch
        for:
        hours: 0
        minutes: 30
        seconds: 0
    condition: []
    action:
    - type: turn_off
        device_id: a7ee4b26ec5b9e36d959f7b4b8490c42
        entity_id: 61230c7b5528330e3b60ee38c5fe1f12
        domain: switch
    mode: single
</LessonCodeWrapper>

해당 연도 내내 시간을 변경할 수 있습니다. 예를 들어, 2월에는 물을 1시간 동안 가열해야 하고, 4월에는 30분이면 충분합니다. 물이 가열될 때 핸드폰으로 알림을 보내는 것이 유용합니다.

<robo-academy-note type="note" title="Homework">
  지정된 X분 후에 보일러를 끄는 자동화를 만드세요. 시간을 변수로 설정하려면 <a href="https://www.home-assistant.io/integrations/input_number/">이 통합</a>을 살펴보세요.
</robo-academy-note>

## 에어컨 및 TV용 IR 리모컨

리모컨은 Wi-Fi 연결(상시 전원 필요) 및 Zigbee 연결(배터리 작동)이 함께 제공됩니다.

저는 시도한 Wi-Fi 옵션은 제조사 [Broadlink](https://www.ibroadlink.com/productinfo/762674.html)에서 구입한 것이었으며 [Amazon](https://www.amazon.de/-/en/dp/B07ZSG9Y67/)에서 약 €30에 구입했습니다. 초기 설정을 위해 핸드폰에 애플리케이션을 설치하고 계정을 생성해야 하지만 그 후에 IR 리모컨은 로컬 네트워크에서 작동하며 HA에 연결하는 것은 [통합](https://www.home-assistant.io/integrations/broadlink/)을 사용하여 수행됩니다. 리모컨을 사용자의 요구에 맞게 더 맞추려면 [SmartIR](https://github.com/smartHomeHub/SmartIR) 저장소를 살펴보는 것을 추천합니다 - 이것은 다양한 에어컨 및 TV용 미리 만들어진 명령어의 대규모 라이브러리입니다.

<robo-academy-note type="note" title="팁">
  특정 A/C 모델을 찾을 수 없다면 동일 제조사의 다른 모델을 시도해보세요. 명령어는 아마도 동일할 것이며 A/C를 연결할 수 있을 것입니다.
</robo-academy-note>

<LessonImages src="school-2024-cyprus-relocant-manual/broadlink-ir.png" alt="Broadlink IR Remote Control"/>

Broadlink IR Remote의 구성 예:

<LessonCodeWrapper language="yaml" noCopyIcon>
    climate:
    - platform: smartir
        name: Living Room AC
        unique_id: living_room_ac
        device_code: 1390
        controller_data: remote.living_room_ir_remote_control
        temperature_sensor: sensor.0xa4c138b6ad623598_temperature
        humidity_sensor: sensor.0xa4c138b6ad623598_humidity 
</LessonCodeWrapper>

Zigbee에서 작동하는 원격 제어기는 전원에 대한 지속적인 연결이 필요하지 않지만 배터리로 작동합니다. 한편, 이것은 장점입니다. 왜냐하면 장치를 방 안의 어느 편리한 곳에 놓을 수 있기 때문입니다. 반면에, 배터리는 필요에 따라 교체해야 합니다. 이러한 원격 제어기의 설정 과정은 Broadlink와도 다를 수 있습니다. SmartIR 라이브러리를 사용할 수 없는 경우, 각 명령에 대해 원격 제어기를 별도로 훈련시키고 Home Assistant 구성에 저장해야 합니다.

프로그래밍 가능한 원격 제어기는 매우 쉽게 설치하고 구성할 수 있습니다. 벽에 부착하거나 에어컨 버스에 연결할 필요가 없습니다. 그러나 장치 간 피드백이 없어 약간의 제한이 있습니다. 우리는 A/C가 켜졌고 우리가 보낸 명령을 정확히 실행하는지 확인할 수 없습니다. 그러나 우리는 빠르게 그리고 아파트에 손상을 주지 않고 그렇게 합니다. 원격 제어기에 조금 더 정보를 제공하기 위해 Zigbee 온도 및 습도 센서를 설치할 수 있습니다. 예를 들어 [이 제품](https://vi.aliexpress.com/item/1005005595631552.html)을 10유로에 구입하여 읽기를 원격 제어기에 연결할 수 있습니다. 이렇게 하면 간단한 피드백이 생기고 흥미로운 시나리오의 수가 증가합니다.

## 에너지 미터

아래 이미지에 있는 전기 소비를 위한 준침입형 미터가 있습니다:

<LessonImages imageClasses="small" src="school-2024-cyprus-relocant-manual/energy-meter.png" alt="Energy Meter"/>

입력에 L과 N을 적용하여 전원을 공급해야합니다. 반대편에는 미터에 연결된 유도 링이 있으며, 이를 측정을 위해 상 또는 소비 라인에 걸어둡니다. 대부분의 집과 아파트에는 3상이 있으므로 3개의 모듈을 설치해야합니다. 저는 [Amazon](https://www.amazon.de/gp/product/B0C37DJXVD/)에서 각 상당 €60에 구입했습니다. 오래된 집은 한 상만 가지고 있을 수도 있습니다.

## 결론

나에게 스마트 홈은 사치가 아닌 필수품입니다. 이곳은 나와 가족과 함께 편안히 쉬고 시간을 보내고 싶은 곳이며, 일상적인 문제 해결에 에너지를 낭비하고 싶지 않습니다. 나의 경우 위의 키트 비용은 약 €500이 소요되었으며 몇 개의 저녁이 걸렸습니다. 결과는 값진 것입니다!