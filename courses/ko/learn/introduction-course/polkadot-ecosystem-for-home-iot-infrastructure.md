---
title: "레슨 #3, 홈 IoT 인프라를 위한 폴카닷 생태계"
lastUpdate: Thu May 04 2023 12:53:58 GMT+0400 (Samara Standard Time)
description: 이 레슨에서는 Robonomics 파라체인을 사용하여 스마트 전구를 제어해 보게 될 것입니다.
lessonNumber: 3
metaOptions: [배우다, 로보노믹스 아이디어 소개]
defaultName:  Introduction to the ideas of Robonomics
---

레슨 2에서는 Robonomics의 주요 원칙을 설명하고 폴카닷 / 쿠사마를 유망한 블록체인 생태계 플랫폼으로 언급했습니다. 이제 쿠사마 네트워크의 폴카닷 생태계의 일부인 Robonomics 파라체인의 기능을 자세히 살펴보는 시간입니다. 특히, Robonomics 파라체인의 IoT 구독이 어떻게 작동하는지 보여드리고 싶습니다. 첫 번째 레슨에서 귀하의 주소가 강의 IoT 구독에 추가되었으며 이미 두 번 사용했습니다: 검은 거울에서 자신의 반사를 찾을 때와 시험 결과를 제출할 때.

## 소개

이 레슨에서는 스마트 전구를 제어해 보게 될 것입니다. 귀하의 목표는 Robonomics 파라체인의 표준 폴카닷 / 서브스트레이트 인터페이스를 사용하여 전구를 켜거나 끄는 것입니다. 전구는 [YouTube](https://www.youtube.com/channel/UCkemsNJWaCmvF1Oi50C-hAg/live)에서 방송되므로 실시간으로 결과를 확인할 수 있습니다. 또한 IoT 구독 사용에 대한 더 자세한 지침은 [우리의 위키](https://wiki.robonomics.netw또는k/docs/subscription-launch/)에서 확인할 수 있습니다.


## 지침

<List type="numbers">

<li>

Robonomics [폴카닷 / 서브스트레이트 포털](https://polkadot.js.또는g/apps/?rpc=wss%3A%2F%2Fkusama.rpc.robonomics.netw또는k%2F#/extrinsics)을 엽니다.

Extrinsics(폴카닷 생태계의 함수) 메뉴가 표시됩니다. Extrinsics가 열리지 않으면 페이지 상단의 메뉴를 사용하여 <code> Kusama & Parachains -> Robonomics</code>로 이동한 다음 <code>Switch</code>를 누릅니다. 그런 다음 상단 헤더에서 <code>Developer</code>로 이동한 다음 <code>Extrinsics</code>로 이동합니다.

</li>

<li>
'선택된 계정 사용'이라고 표시된 첫 번째 필드에서 이전 레슨에서 사용한 동일한 Polkadot.js 계정을 선택합니다.
</li>

<li>
두 번째 필드 '다음 extrinsic 제출'에서 <code>rws</code> extrinsics를 선택하고 <code>call(subscriptionId, call)</code>을 선택합니다. 이렇게 하면 IoT 구독을 사용하여 함수 호출을 디스패치할 수 있습니다.
</li>

<li>
<code>subscriptionId: AccountId32</code> 필드에이 구독의 소유자 주소를 붙여넣기하십시오: <code>4GgRRojuoQwKCZP9wkB69ZxJY4JprmHtpzEzqJLjnqu4jk1r</code>
</li>

<li>

<code>call: Call</code> 필드에서 <code>launch(robot, param)</code> 명령을 선택합니다.

이렇게 하면 <code>robot</code> 및 <code>param</code> 두 개의 추가 필드가 표시됩니다.

</li>

<li>
<code>robot: AccountId32</code> 필드에 스마트 전구의 주소를 붙여넣으십시오: <code>4DUAnmLeEto197jDDSgvfjfS65MGvReMXibqp9ADg7ZgCDp9</code>
</li>

<li>

<code>param: H256</code> 필드에 전구를 켜려면 1을, 끄려면 0을 지정해야 합니다.

이 작업은 다음과 같이 수행할 수 있습니다:

<code>0x0000000000000000000000000000000000000000000000000000000000000001</code>

또는

<code>0x0000000000000000000000000000000000000000000000000000000000000000</code>

</li>

<li>

"트랜잭션 제출" 버튼을 누릅니다.

트랜잭션에 서명하기 전에 [YouTube에서 방송](https://www.youtube.com/channel/UCkemsNJWaCmvF1Oi50C-hAg/live)을 열지 않도록 잊지 마십시오.

</li>


</List>

<Result>

Polkadot.js 계정에 대한 성공적인 트랜잭션 전송 및 Polkadot 탐색기에 나타난 후 레슨이 완료된 것으로 간주됩니다.

[특별 확인 댑](https://lk.robonomics.academy/)에서 결과를 확인할 수 있습니다. 확인 댑에 로그인하려면 수강 중에 사용한 Polkadot.js 계정을 사용하세요.

</Result>