---
title: "스마트 홈 보드 조립"
lastUpdate: Thu May 18 2023 10:46:29 GMT+0400 (Samara Standard Time)
description: 스마트 홈 보드를 어떻게 조립하는지 배우게 될 것입니다!
metaOptions: [배우다]
defaultName: Introduction to open source solution for private smart homes
---

<LessonImages imageClasses="mb" src="smart-home-intro/spring-school-2023-smart-stand-intro.gif" />

## 스마트 홈 패널 

이 패널은 가장 많이 사용되는 스위치와 데이터가 표시되는 중앙 제어 장치로 사용되도록 설계되었습니다. 또한 인터콤을 연결하여 실내 모니터로 사용할 수 있습니다. 기본적으로 우리의 경우 안드로이드 OS가 실행되는 태블릿일 뿐입니다. 전원만 제공하면 됩니다. 이 패널은 실내 모니터를 설치해야 할 곳에 설치되어야 한다고 생각합니다

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmcbdAJqbwHAQ3NeyWQUwSoS4drDexa3AEs7HXuM1BrUT1', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-1.png" />


## 빛 스위치

스마트 라이트 스위치는 일반적인 것과 거의 비슷하지만, 스위치 대신 푸시 버튼이 사용됩니다. 푸시 버튼은 누른 후에 자리로 돌아옵니다. 일반 스위치와 스마트 스위치 사이의 연결에는 차이가 없습니다: 중성선을 N에 연결하고 전원선을 L에 연결하고 번개 선을 L1에 연결하십시오. 스위치를 조립한 후 ZigBee를 통해 페어링하려면 버튼을 최소 5초 동안 누르십시오.

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/Qmb138DiQWWBgowMj2fC9kmiGYh9WEeytteSkqumWCv2LB', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-2.png" />

두 개 버튼 스위치 (또는 그 이상)의 경우, 유일한 차이점은 두 번째 (세 번째, ...) 라인의 조명입니다. 

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmZiStYZG4rmyNPXXmCXsVPm7witPpnNJMBzD8GtxedgPo', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-3.png" />

## 스마트 전구 

스마트 전구는 아마도 스마트한 것을 시도해 볼 수 있는 가장 쉬운 방법일 것입니다. 전기 기사가 되지 않아도 됩니다. 원격으로 제어할 수 있으며 밝기나 색상을 변경할 수 있습니다. 스마트 스위치와 함께 또는 별도로 설치할 수 있습니다. 이러한 장치를 사용하면 기분이나 실외 조건에 따라 자동화 페이지를 열 수 있습니다! 새로운 전구는 ZigBee를 통해 연결할 준비가 되어 있습니다. 찾을 수 없는 경우에는 5번 켜고 끌 수 있습니다


<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmbiMHLJqnDpr1Whzvo6Y7zE33cQPuTs7furbt3JW2uiek', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-4.png" />

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmTzK4dY168HVgLvVBsRxR4M4vda55XC7pFhpW5kRexujQ', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-5.png" />

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmNZFpvVUavKc1Za9SeXqikrfySsfFHuVrkdzgbVB8um7T', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-6.png" />

## 스마트 소켓 

일반적으로 가끔 켜고 끌 필요가 있는 '똑똑하지 않은' 장치들이 몇 개 있습니다. 스마트 소켓을 통해 이러한 장치를 전원을 공급하면 필요에 따라 켜고 끌 수 있습니다. 또한 이러한 소켓은 에너지 소비를 모니터링할 수 있어 이 장치가 얼마나 많은 전력을 소비하는지에 대한 데이터를 가지고 있습니다. 연결은 매우 쉽습니다. 스마트 소켓을 페어링하려면 5초 동안 버튼을 누르면 됩니다.

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmRtmKXSv7csHLbKVuZkoA5Eb2zyTkEAbUxLYT6Qt1yxZH', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-7.png" />

## 보일러 스위치 

보일러 스위치가 전용 장치로 존재하는 이유는 더 많은 부하를 견딜 수 있기 때문입니다. 보통 보일러는 3kWh 이상을 소비하므로 일반적인 (심지어 스마트한) 스위치는 이 상황에 적합하지 않습니다. 보일러 스위치는 이러한 조건 하에서 작동하도록 설계되었습니다. 연결 및 페어링은 라이트 스위치와 거의 동일합니다.

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmNZyRtXXRYCrAQe6s6ZFJLXtUrH7SZHJC1Bt61kTrRX54', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-8.png" />

## Wifi/Zigbee Thermostat

보통의 온도 조절기처럼 보이지만 무선으로 제어할 수 있는 능력이 있습니다. 옵션은 다음과 같습니다: 난방 시스템을 조절기에 직접 연결하거나 분리합니다. 후자의 경우 조절기는 우리에게 모드(난방, 냉방, 팬 등)와 온도를 알려줍니다

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmRjxo9EGUvQiMm84xvXCL6LfrQJYza71vmFsa9Zpy7qmz', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-9.png" />

## 커튼 스위치

또 다른 전용 스위치, 이번에는 커튼용입니다. 기술적인 측면에서는 이 스위치만 사용할 필요는 없습니다. 어떤 세 개의 버튼 스위치든 사용하고 커튼 모터에 연결할 수 있지만, 이 스위치는 특별한 아이콘과 함께 제공됩니다. 스위치를 페어링하려면 중간 버튼을 길게 누르세요

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmRpEpZbyNkzby8Sk22Ymz59DbAcnty1B1osWc2kZr5FZ7', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-10.png" />

## 스마트 밸브 컨트롤러

보유한 밸브에 따라 컨트롤러를 선택하세요. 가장 명백한 시나리오는 이 컨트롤러를 물 누출 센서와 결합하는 것입니다. 장치를 페어링하려면 버튼을 5초 동안 누르세요

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmcjZcJ6P8Q5yUfSRx8R2mR4A7r2fi5bLs5uoUr3EAXLZs', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-11.png" />

## 물 누출 센서

두 개의 접촉이 연결되면 신호를 보내는 매우 간단한 장치입니다. 물은 전기를 전도하며 센서 아래에 물이 있을 때 접촉이 단락됩니다. 센서는 배터리로 작동하며 일반적으로 1-2년 지속됩니다. ZigBee를 통해 센서를 페어링하려면 버튼을 길게 누르세요 

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmbgetJK1E8qQMcnBVREutpy8tKfbesqaxXiebjzpoyrdV', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-12.png" />

## IR 컨트롤러

리모컨 TV 컨트롤러로 생각해보세요...하지만 스마트한 것! 그리고 TV만 사용하는 것에 제한이 없습니다. 에어컨에 리모컨 컨트롤러가 있는 경우 이 스마트한 것으로 대체할 수 있습니다. 페어링하려면 컨트롤러 뒷면의 리셋 버튼을 한동안 누르세요. 사용할 수 있는 명령이 준비된 라이브러리가 많이 있습니다. 예를 들어 [https://github.com/smartHomeHub/SmartIR](https://github.com/smartHomeHub/SmartIR)입니다. TV나 에어컨의 모델을 찾는 것이 전부입니다

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmVjj92fMLbA6QJ5QhnmiqBT1huD5b7xyfi3VadHFDYwtm', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-13.png" />

## 도어/윈도우 센서

배터리로 작동하는 또 다른 센서이지만 간단한 보안 시스템을 구축하거나 조명 및 기타 장치에 연결하는 데 도움이 됩니다. ZigBee를 통해 페어링하려면 구멍에 바늘을 넣고 한동안 누르세요

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmZyb66dKEqk9iCVKhaBk5ZKASi7dXdFSg2CBXY1fwuu5J', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-14.png" />

## 모션 센서
도어/윈도우 센서와 마찬가지로 다양한 시나리오에서 사용할 수 있습니다. 가장 명백한 것은 조명을 제어하거나 당신이 없을 때 움직임을 감지하는 것입니다

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmUA7TLg12pkhkbdGH6fwNDasU1kiyLHBJSutA2YG71Mka', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-15.png" />


## 온도 및 습도 센서

당신이 사는 환경을 알아야 좋을 것입니다, 맞죠? 이 센서는 온도와 습도 측정값을 제공합니다. 그런 다음 이 이터를 사용하여 에어컨을 켜거나 끄거나 다른 난방/냉방 시스템을 사용할 수 있습니다. 센서를 페어링하려면 뒷면에 버튼이 있습니다 

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmayYFowfJVwQBVxPUSvi5inedqKzhyRZXp8fBUUayJnqH', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-16.png" />

## 보안 카메라

마지막으로 집에서 무슨 일이 일어나는지 살펴보는 것이 좋습니다. 좋은 자동화는 모션 센서를 카메라와 연결하여 모션을 감지할 때 10초 길이의 비디오를 얻을 수 있습니다 

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmX8nnDCgTx2kuwfAGv6B4orkEg4w6phtJtxSp44HfdD9T', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-17.png"  />


## 스마트 보드 
결과를 확인하세요 [https://www.youtube.com/watch?v=B3er7bwtvkw](https://www.youtube.com/watch?v=B3er7bwtvkw)
그리고 직접 사용해보세요 [https://twitter.com/vadim_manaenko/status/1653777703718334469?s=20](https://twitter.com/vadim_manaenko/status/1653777703718334469?s=20)

