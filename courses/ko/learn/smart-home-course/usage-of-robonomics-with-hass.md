---
title: "레슨 #7, 홈 어시스턴트와 로보노믹스 사용법"
lastUpdate: Thu May 18 2023 10:46:29 GMT+0400 (Samara Standard Time)
description: 홈 어시스턴트 코스
lessonNumber: 8
metaOptions: [로보노믹스와 홈 어시스턴트를 활용한 주권 스마트 홈 배우기]
defaultName: Sovereign Smart Home with Robonomics and Home Assistant
---

## 이것은 무엇에 관한 것입니까

이 레슨에서는 주요 로보노믹스 IoT 서비스를 사용해보게 될 것입니다. 첫 번째로는 스마트 홈 장치의 텔레메트리를 조회할 수 있어서 홈 어시스턴트로부터 원격으로 데이터를 수신할 수 있습니다. 두 번째 서비스는 홈 어시스턴트 구성의 백업을 생성하고 필요할 때 복원합니다 (예: SD 카드 고장 시).


## 파라체인 기능에 대해

다음으로 로보노믹스 파라체인의 기능이 어떻게 홈 어시스턴트 사용자에게 필요한 서비스를 제공하는 데 사용되는지 알아볼 것입니다. 

텔레메트리 가져오기는 이미 알고 있는 <code>datalog</code> 팔렛을 기반으로 합니다. 일정 기간마다 (누적된 가중치가 허용하는 한) <code>datalog.record()</code> 트랜잭션이 <code>SUB_CONTROLLER</code> 주소에서 암호화된 파일의 IPFS 해시와 함께 파라체인으로 전송됩니다. 실제로 텔레메트리를 얻기 위해 파라체인에서 IoT 구독과 관련된 필요한 데이터로그를 요하고 그것들을 키로 복호화합니다.

백업을 생성하기 위해 다른 로보노믹스 팔렛인 <code>digitalTwin</code>이 사용됩니다. 이는 실제 장비의 디지털 버전인 디지털 트윈의 아이디어를 구현한 것으로, 기술적 특성과 기록 데이터를 복사합니다. 먼저 <code>digitalTwin.create()</code> extrinsic를 사용하여 홈 어시스턴트의 디지털 트윈을 위한 고유한 ID가 생성됩니다. 그런 다음 <code>digitalTwin.setSource()</code> extrinsic를 사용하여 이 ID가 일부 데이터 (<code>topic</code> 필드) 및 파라체인의 주소 (<code>source</code> 필드)와 결합됩니다. 홈 어시스턴트 백업을 위해 백업 파일의 해시가 <code>topic</code>에 저장되고 <code>SUB_OWNER</code> 주소가 <code>source</code>에 저장됩니다.

## 지침

<List type="numbers">

<li>

텔레메트리 가져오기

<List>


<li>

Dapp로 이동하여 [스마트홈 텔레메트리](https://dapp.robonomics.network/#/smarthome-telemetry) 서비스를 선택합니다.

<LessonVideo  :videos="[{src: 'https://crustipfs.info/ipfs/Qmao9RoWcKo2qs4PAGtm5gqHzyAHJcpDqNLgciU35FJeVm', type:'mp4'}]" />

</li>

<li>

<code>CONTROLLER</code> 필드에 <code>SUB_CONTROLLER</code> 주소를 입력합니다. 데이터를 암호화하려면 시드 구문을 삽입합니다.

</li>

<li>

<code>Get telemetry</code> 블록에서 드롭다운 목록에서 타임스탬프를 선택하고 <code>DOWNLOAD TELEMETRY</code> 버튼을 누릅니다.


텔레메트리 다로드에는 시간이 걸릴 수 있습니다. 완료되면 센서에서 정보를 볼 수 있습니다.

</li>
</List>
</li>


<li>

백업 생성

<List>

<li>

구성 파일을 포함하는 안전한 아카이브를 생성하는 서비스를 호출하여 백업을 생성합니다. 이 서비스는 그런 다음 아카이브를 IPFS에 추가하고 결과 CID를 로보노믹스 디지털 트윈에 저장합니다.

<robo-academy-note type="warning" title="WARNING">
구성을 복원하려면 Pinata (pinata.cloud) 또는 Crust Network (crust.network)와 같은 사용자 정의 IPFS 게이트웨이를 사용해야 합니다. 그렇지 않으면 백업은 로컬 IPFS 노드에만 저장되어 로컬 노드 고장 시 홈 어시스턴트 구성을 복원하는 데 어려움을 겪을 수 있습니다. 
</robo-academy-note>

<LessonVideo  :videos="[{src: 'https://crustipfs.info/ipfs/QmVo91dLaAYgFDM1vrL2PYfAffM6SGGC59ZERbfHR44tqW', type:'mp4'}]" />

</li>

<li>

홈 어시스턴트의 웹 인터페이스에서 <code>개발자 도구</code> -> <code>서비스</code>로 이동하십시오. <code>Robonomics: Robonomics에 백업 저장</code>을 검색하고 <code>서비스 호출</code>를 누르세요.

</li>

<li>

<code>백업이 Robonomics에 업데이트되었습니다</code>라는 알림이 <code>알림</code>에 표시될 때까지 기다리세요.

</li>

<li>

구성을 복원하려면 이전에 생성한 시드를 사용하여 Robonomics Home Assistant 통합이 적용된 새로운 홈 어시스턴트 인스턴스를 설치해야 합니다. 또한 동일한 사용자 이름과 암호로 MQTT 브로커를 설정해야 합니다.

<robo-academy-note type="warning" title="WARNING">
홈 어시스턴트에 Wi-Fi 또는 MQTT를 통해 연결된 일부 장치는 라즈베리 파이의 로컬 IP 주소를 명시적으로 지정해야 할 수 있으므로 백업을 복원할 때 이 IP가 변경되어 사용할 수 없을 수 있습니다. 이러한 장치의 설정에서 새 IP 주소를 다시 입력해야 합니다. 이를 피하기 위해 라우터 설정에서 라즈베리 파이에 대한 정적 로컬 IP를 설정할 수 있습니다 (이 기능을 지원하는 경우).
</robo-academy-note>

<LessonVideo  :videos="[{src: 'https://crustipfs.info/ipfs/QmWmnmkXUcPXsAnQzwN3UEuki2GMYnQDx3vhgjEypCU8aR', type:'mp4'}]" />


</li>

<li>

홈 어시스턴트의 웹 인터페이스에서 <code>개발자 도구</code> -> <code>서비스</code>로 이동하십시오. <code>Robonomics: Robonomics에서 백업 복원</code>을 검색하고 <code>서비스 호출</code>를 누릅니다. <code>개요</code> 페이지로 이동하여 백업 상태를 확인하세요.

</li>

<li>

홈 어시스턴트가 다시 시작되면 구성이 복원됩니다. 상태가 <code>복원됨</code>으로 변경되지만 홈 어시스턴트가 자동으로 다시 시작되지 않으면 <code>설정</code> > <code>시스템</code>으로 이동하여 오른쪽 상단의 <code>다시 시작</code> 버튼을 클릭하여 수동으로 다시 시작해야 합니다.

</li>

</List>
</li>

</List>

## 코스 완료

<List>

<li class="flex"> 

축하합니다! 주권을 갖는 스마트 홈의 전체 설정 및 배포를 성공적으로 완료했습니다. Discord 채널을 방문하여 우리에게 코스 완료 증명서를 요청할 수 있습니다. [robonomics-academy](https://discord.com/channels/803947358492557312/803947358492557315) 채팅에서 우리에게 쓰고 대표가 연락을 드릴 것입니다.
</li>

<li class="flex">

코스 완료의 증명은 [Polkadot explorer](https://robonomics.subscan.io/)에서 확인할 수 있는 해당 거래입니다. 이는 구독 구매, 구독에 장치 추가 및 장치에서 데이터 로그를 보내는 거래입니다.

</li>

</List>