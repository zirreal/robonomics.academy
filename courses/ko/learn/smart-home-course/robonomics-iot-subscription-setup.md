---
title: "레슨 #5, Robonomics IoT 구독 설정"
lastUpdate: Thu May 18 2023 10:46:29 GMT+0400 (Samara Standard Time)
description: 홈 어시스턴트 코스
lessonNumber: 6
metaOptions: [로보노믹스와 홈 어시스턴트를 활용한 주권 스마트 홈 배우기]
defaultName: Sovereign Smart Home with Robonomics and Home Assistant
---


## 이것은 무엇에 관한 것입니까

Robonomics IoT 구독을 통해 사용자는 일정 기간 동안 표준 거래 수수료를 지불하지 않고 파라체인의 모든 기능을 사용할 수 있습니다. 구독을 활성화하면 장치가 우선적으로 거래를 보낼 수 있습니다.

이 레슨에서는 필요한 스마트 홈 보안 계정을 생성하고 IoT 구독을 구매할 것입니다.

## 이론

IoT 구독 및 구매 및 관리 방법은 모두 필요한 기능을 포함하는 <code>rws</code> 팔렛을 사용하여 구현됩니다. 일반적으로 Robonomics에서 구독은 경매 모델을 사용하여 판매되며, 이는 특정 구독 ID에 대한 경매를 생성하기 위해 <code>rws.startAuction()</code> extrinsic을 사용합니다. 사용자는 ID로 경매에 액세스하고 <code>rws.bid()</code> extrinsic을 사용하여 입찰할 수 있습니다.

경매 종료 후, 최고 입찰 주소가 구독에 할당됩니다. 이제 이 주소는 수수료 없이 <code>rws.call()</code> extrinsic을 통해 거래를 보낼 수 있습니다. 그러나 이는 주소가 언제든지 이를 무제한으로 수행할 수 있다는 것을 의미하지는 않습니다: 각 구독에는 무료 거래를 수행하기 전에 축적해야 하는 <code>weight</code> 값이 있습니다. 파라체인에서 생성된 각 블록마다 일정량의 <code>weight</code> 값이 구독에 추가되므로 Robonomics는 이를 통해 파라체인의 대역폭을 조절합니다.

또한, 구독 소유자는 <code>rws.setDevices()</code> extrinsic을 사용하여 구독을 지정된 주소에 공유할 수 있습니다. 동시에 <code>weight</code>는 동일하게 유지되므로 구독에 더 많은 주소가 포함될수록 각 주소가 무료 거래를 보내기 전에 기다려야 하는 시간이 더 길어집니다.

Robonomics를 사용하여 Home Assistant를 제어하려면 Robonomics 파라체인에 두 개의 계정이 필요합니다. 이러한 계정은 Home Assistant의 보안을 제공할 것입니다.

계정 중 하나(<code>SUB_OWNER</code>)로 Robonomics 구독을 구매할 것입니다. 이 계정은 IoT 구독의 주요 관리자로 작용하며 다른 사용자에게 Home Assistant에 대한 액세스를 제공합니다(<code>rws.setDevices()</code>를 사용). 이 계정은 구독 구매 거래를 완료하기 위해 일정량의 XRT 토큰을 보유해야 합니다.

두 번째 계정(<code>SUB_CONTROLLER</code>)은 장치의 모든 Home Assistant 프로세스(예: 텔레메트리)를 제어할 것입니다. 장치의 거래는 <code>SUB_CONTROLLER</code> 계정을 대표하여 보내질 것입니다. 당신(누구든지)은 [Subscan](https://robonomics.subscan.io/)과 같은 파라체인 익스플로러에서 이러한 거래를 볼 수 있을 것입니다. 그러나 당신만이 필요한 시드 문구를 안전하게 소유하는 한 이러한 거래의 내용을 해독할 수 있을 것입니다.

## 지침

<List type="numbers">

<li>

소유자 및 컨트롤러 파라체인 계정 생성

<List>

<li>

<robo-academy-note type="warning" title="WARNING">
두 계정 모두 ed25519 암호화로 생성되어야 합니다.
</robo-academy-note>

</li>

<li>

Polkadot / Substrate 포털의 [Robonomics 파라체인 앱](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Fkusama.rpc.robonomics.network%2F#/)로 이동하십시오. 왼쪽 상단을 확인하여 Robonomics 파라체인에 연결되어 있는지 확인하십시오.

</li>

<li>

*ed25519* 형식을 사용하기 때문에 Polkadot-JS UI를 사용하여 계정을 만들고 필요한 암호화를 선택해야 합니다. 

이 기능은 Polkadot-JS UI에서 기본적으로 비활성화되어 있습니다. 활성화하려면 <code>Settings</code> -> <code>General</code> -> <code>account options</code>로 이동하고 드롭다운 메뉴 <code>in-browser account creation</code>에서 <code>Allow local in-browser account storage</code>를 선택하십시오.
 
</li>

<li>

<code>Accounts</code> -> <code>Accounts</code>로 이동하고 <code>Add account</code> 버튼을 누르십시오. 계정 시드가 포함된 팝업 메뉴가 표시됩니다. 두 가지 형식이 있습니다: *Mnemonic* (인간이 읽을 수 있는 형식) 및 *Raw* (숫자와 문자의 연속).

<LessonVideo  :videos="[{src: 'https://crustipfs.info/ipfs/QmQiJYPYajUJXENX2PzSJMSKGSshyWyPNqugSYxP5eCNvm', type:'mp4'}]" />

</li>

<li>

<code>Advanced creation options</code>을 열고 계정 생성의 암호화 유형을 <code>Edwards - ed25519</code>로 변경하십시오. 니모닉 시드 구절을 안전하게 보관하고 <code>Next</code>를 누르십시오.

</li>

<li>

다음 메뉴에서 계정 이름과 암호를 설정해야 합니다. 편의를 위해 이름을 <code>SUB_OWNER</code>로 지정하고 <code>Next</code>를 누르십시오.

</li>

<li>

마지막 창에서 <code>Save</code>를 클릭하여 계정 생성을 완료하십시오. 또한 안전하게 보관해야 할 백업 JSON 파일이 생성됩니다. 나중에 비밀번호를 기억한다면 이 파일을 사용하여 계정을 복구할 수 있습니다.

</li>

<li>

<code>SUB_CONTROLLER</code> 계정에 대해 이러한 단계를 반복하십시오.

</li>
</List>
</li>

<li>

Polkadot.js Extension에 계정 추가

<List type="numbers">

<li>

편의를 위해 Polkadot.js 확장 프로그램을 사용하고 새로 생성된 계정을 추가해야합니다. ed25519 계정의 경우 백업 JSON 파일로만 그 작업을 수행할 수 있습니다. 계정을 생성할 때 저장된 파일을 사용할 수 있습니다.

계정의 백업 파일을 생성하여 이러한 파일을 다시 얻을 수 있습니다. 계정에서 세 개의 점을 누르고 <code>이 계정을 위한 백업 파일 생성</code>을 선택하고 비밀번호를 입력하십시오.

<LessonVideo  :videos="[{src: 'https://crustipfs.info/ipfs/QmRd7gztUjWkLF4W2XuJwy5aXBwzNV2aPCU6CQQLvUpSNj', type:'mp4'}]" />

</li>

<li>

확장 프로그램을 열고 오른쪽 상단에 있는 <code>+</code> 버튼을 누르고 <code>백업 JSON 파일에서 계정 복원</code>을 선택하십시오.

</li>

<li>

열린 창에서 JSON 파일을 업로드하고 비밀번호를 입력하고 <code>복원</code>을 누르십시오

</li>

<li>

Polkadot.js 확장 프로그램의 계정에 대해 Robonomics 네트워크가 선택되었는지 확인하십시오. Polkadot / Substrate Portal에서 <code>설정</code> -> <code>메타데이터</code>로 이동하고 <code>메타데이터 업데이트</code> 버튼을 클릭하십시오. 

<LessonVideo  :videos="[{src: 'https://crustipfs.info/ipfs/QmT5sTNP9t8gpbD4RJJw6ETwG4wiziiChAh2uHHBk9Zsyd', type:'mp4'}]" />

</li>

<li>

팝업에서 메타데이터 업데이트를 확인하십시오. 이제 확장 프로그램에서 주소가 사용되는 네트워크의 레이블이 표시됩니.

</li>

</List>
</li>

<li>

Robonomics 구독 활성화

<List >

<li>

<robo-academy-note type="okay">
이 단계에서는 <code>SUB_OWNER</code> 계정에 충분한 양의 XRT 토큰(최소 2-3 XRT)이 있어야합니다.
</robo-academy-note>

Robonomics dapp로 이동하여 [구독 페이지](https://dapp.robonomics.network/#/subscription)로 이동하고 오른쪽 사이드바에서 <code>계정 연결</code>을 누르십시오.

<LessonVideo  :videos="[{src: 'https://crustipfs.info/ipfs/QmXrFCajmJgkRDSbshGD3QehjnoyS6jafEPSjHdYkoBHum', type:'mp4'}]" />

</li>

<li>

다음 팝업 메뉴에서 Polkadot.js 확장 프로그램을 연결하십시오. 잔고와 함께 계정 주소가 표시됩니다.

</li>

<li>

구매 전에 <code>SUB_OWNER</code> 계정을 선택했는지 확인하십시오. 주소 프로필 아이콘을 누르고 <code>Check owner account</code> 필드 아래에 <code>SUB_OWNER</code> 계정이 표시되어야합니다.

</li>

<li>

마지막으로 <code>제출</code> 버튼을 누르고 계정의 비밀번호를 입력하십시오. 그 후 활성화 프로세스가 완료될 때까지 기다리십시오. 잠시 후 구독 상태가 표시됩니다.

사용 가능한 구독이 없는 경우 **Robonomics 팀에 문의**하십시오.

</li>
</List>
</li>

<li>

구독에 계정 추가

<List type="numbers">

<li>

이제 <code>SUB_CONTROLLER</code> 계정을 **액세스 목록**에 추가해야합니다. 확장 프로그램을 열고 계정 이름 옆에 있는 아이콘을 클릭하십시오. 이렇게 하면 계정 주소가 복사됩니다.

<LessonVideo  :videos="[{src: 'https://crustipfs.info/ipfs/QmV1gkwtcXsWv54ov9tuXfcHg7nqs1foM8cRwts4sqnqtX', type:'mp4'}]" />

</li>

<li>

이 주소를 **액세스 관리** 부분의 <code>Robonomics 파라체인 주소</code> 필드에 붙여 넣으십시오.

이름을 지정하고 <code>+</code> 버튼을 누르십시오. 팝업 창에서 <code>SUB_OWNER</code> 비밀번호를 입력하고 활성화 프로세스가 완료될 때까지 기다리십시오.

</li>

<li>

<code>SUB_OWNER</code> 계정에 대해 단계를 반복하십시오.
</li>
</List>
</li>
</List>