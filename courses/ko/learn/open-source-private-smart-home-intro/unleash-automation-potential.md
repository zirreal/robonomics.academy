---
title: "자동화 잠재력을 발휘하다"
lastUpdate: Mon August 28 2023 12:46:49 GMT+0400 (Samara Standard Time)
description: 스마트 홈 스탠드를 예로 하여 일상 생활을 더 쉽게 만드는 기본 자동화에 대해 배우게 될 것입니다.
metaOptions: [배우다]
defaultName: Introduction to open source solution for private smart homes
---

<RoboAcademyText>지난 시간에는 데모 스탠드에 다양한 스마트 기기를 설치하고 연결하는 과정을 진행했습니다. 실제 아파트나 집에서는 물론 고유한 특성이 있을 것입니다. 전기 작업 시 안전 주의를 따르고, 무엇을 하는지 모르면 작업하지 마십시오.

이제 가장 흥미로운 부분으로 넘어가 보겠습니다. 이를 위해 스위치를 변경하고 공간에 센서를 설치해야 했습니다.</RoboAcademyText>

**가정 자동화는 가정에서 다양한 기능을 제어하고 자동화하는 기술과 스마트 기기의 사용을 포함합니다. 여기에는 가정 자동화의 몇 가지 예가 있습니다:**

* *스마트 조명*: 스마트 전구나 스위치를 사용하여 조명을 제어하고 자동화할 수 있습니다. 이를 통해 불을 켜고 끌 수 있고 밝기를 조절하고 색상을 변경할 수 있습니다.
* *기후 제어*: 스마트 온도 조절기를 사용하면 집 안의 온도를 원격으로 제어할 수 있습니다. 이를 통해 일정에 맞게 설정을 조정하고 에너지 소비를 최적화할 수 있습니다.
* *보안 시스템*: 가정 자동화에는 스마트 잠금장치, 비디오 인터폰, 감시 카메라 또는 간단한 모션 센서와 같은 보안 기능이 포함될 수 있습니다. 이러한 장치를 사용하면 세계 어디에서나 집의 출입을 제어할 수 있습니다.
* *가전 제어*: 스마트 플러그를 사용하면 가정용 가전제품과 전자 기기의 작동을 자동화할 수 있습니다. 예를 들어, 일어나기 전에 커피 메이커가 작동하도록 일정을 예약할 수 있습니다.
* *엔터테인먼트 시스템*: 오디오 및 비디오 시스템은 가정 자동화에 완벽하게 적합합니다. 예를 들어, 이벤트나 일정에 따라 음악 재생을 설정할 수 있습니다.

**이제 일반적인 가정 자동화의 장단점 중 일부를 논의해 보겠습니다.**

장점:

* *편의성*: 홈 자동화는 주로 매일 수행되는 루틴 활동으로부터 당신을 구해주는 것을 목적으로 설계되었습니다.
* *에너지 효율성*: 모든 것은 전기의 주요 소비자를 고려하는 것으로 시작합니다. 통계를 손에 넣으면 일정을 설정하거나 특정 장치를 사용하는 데 더 의식적일 수 있습니다.
* *개선된 보안*: 집을 모니터링하고 의심스러운 활동이 있을 경우 알림을 받을 수 있습니다.
맞춤 및 통합: 홈 자동화 시스템은 종종 유연하며 특정 요구에 맞게 맞춤 설정할 수 있습니다. 또한 다른 스마트 장치와 통합하여 다양한 시스템의 원활한 제어와 자동화를 제공할 수 있습니다.

단점:

* *비용*: 장치를 구입하고 구성하는 초기 비용은 복잡한 시스템의 경우 상대적으로 높을 수 있습니다.
* *복잡성*: 홈 자동화 시스템을 설치하고 구성하는 것은 기술적 지식과 문제 해결 능력이 필요한 복잡한 작업일 수 있습니다.
* *개인 정보 보호 및 보안 위험*: 연결된 장치는 해킹이나 무단 액세스에 취약할 수 있으며 개인 정보 보호와 보안을 침해할 수 있습니다. 보안 모 사례를 따르고 장치를 최신 상태로 유지하는 것이 중요합니다.

전반적으로, 홈 자동화는 편의성, 에너지 효율성 및 보안 측면에서 많은 혜택을 제공합니다. 그러나 장치의 기술적 기반, 어떤 프로토콜로 작동할지 및 서로 연결하는 방법에 대해 사전에 고려하는 것이 가치가 있습니다.

우리의 스마트 홈 데모 스탠드로 돌아와 몇 가지 기본 자동화를 실제로 보겠습니다.

## 커튼 제어

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmRMibK3Huppxfhvjk3Hs5NBn4ndFoxHHA2mJn22URnwf4', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-1.png" />

커튼을 집 서버에 연결하여 애플리케이션에서 커튼을 제어할 수 있습니다. 그러나 가장 중요한 것은 이제 일정을 설정하거나 알람 시계를 커튼 열림과 연결할 수 있다는 것입니다. 자연광에서 깨어나는 것은 좋은 일로 여겨집니다!

## 도어 센서와 조명

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmR1WHAAdmPxSP2neFV8VhqFShbeVaYUsNLQ7n9Exh3JUz', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-1.png" />

문이 열리는 센서에 의해 조명이 켜지는 것은 가장 간단한 자동화 중 하나입니다. 주방에서 유용할 수 있습니다. 문을 열 때 조명이 자동으로 켜지고, 일을 마치고 문을 닫으면 조명이 그냥 꺼지지 않습니다.

## 누수 센서와 스마트 밸브

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmVEdwbE1wagebNybfneGKWpAPp3fyXBNnFRt2vduyMSCP', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-1.png" />

누수가 발생했음을 알면 전투의 반은 이루어진 것입니다. 예방은 치료보다 낫다고 하죠. 그러나 센서와 밸브를 연결하면 홍수를 예방하기 위한 모든 필요한 조치가 두려워하기도 전에 취해집니다.

## 모션 센서 및 라이트

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmWMAC3dUvuUg6Zxszoe3aJDatPCaw48QVSyujWyrhKJih', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-1.png" />

모션 센서의 가장 명백한 사용은 조명을 켜는 것입니다. 이러한 자동화는 화장실이나 복도에 구성할 수 있습니다

## 데모 스탠드 통계

스탠드 작업 중에 다음 통계를 수집하는 데 성공했습니다

|Statistics|
|--------------------------|--------|
| Total transactions       | 6557   |
| Users                    | 16     |
| Logins                   | 50     |
| Pinned files in IPFS     | 58     |
| Data in IPFS             | 980 Mb |

[기본 설정](https://www.home-assistant.io/integrations/recorder/), 홈 어시스턴트는 기본적으로 10일간의 기록을 유지합니다. 로보노믹스 통합은 구독이 [활성화](https://dapp.robonomics.network/#/rws-activate)되면 매 10분마다 기록을 업로드합니다. 따라서 기록의 추가 백업에 대해 걱정할 필요가 없습니다. 예를 들어, 아래는 센서에서의 기록에서 몇 가지 그래프입니다

<LessonImages figure figureCaption="Image 1. Turn on the boiler button" src="smart-home-intro/unleash-boiler.png" alt="Image 1. Turn on the boiler button"/>

<LessonImages figure figureCaption="Image 2. Temperature sensor" src="smart-home-intro/unleash-temperature.png" alt="Image 2. Temperature sensor"/>

<LessonImages figure figureCaption="Image 3. Humidity sensor" src="smart-home-intro/unleash-humidity.png" alt="Image 3. Humidity sensor"/>

스탠드 및 자동화에 관한 일련의 기사를 마무리하면 제안된 시스템의 가능성이 여기에 제한되지 않음을 말씀드리고 싶습니다. 구체적인 자동화 시나리오는 특정 사례와 입주자에 따라 다를 것이며, 모든 것이 가정 생활의 편의를 위해 이루어지기 때문입니다.
