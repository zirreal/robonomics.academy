---
title: "수업 #3, 센서 설정 및 연결"
description: '센서 설정 및 연결'
lessonNumber: 3
metaOptions: [배우기, 센서 연결 및 분산 센서 네트워크]
defaultName: Sensors Connectivity & Decentralized Sensors Network
---

당사의 센서는 일부 센서가 추가되고 데이터 전송 방식이 변경된 sensor.community 펌웨어의 확장 버전인 Robonomics 펌웨어를 사용합니다. 소스코드는 [링크](https://github.com/LoSk-p/sensors-software/tree/master/airrohr-firmware)에서 확인하실 수 있습니다.

Robonomics 보드를 사용할 준비가 되었다면 "연결" 섹션으로 이동할 수 있습니다.

## 요구 사항

**Linux 용:**

<List type="numbers">

<li>

`dialout` 그룹에 사용자를 추가하여 USB 포트에 액세스하세요 (Ubuntu의 경우):

<LessonCodeWrapper language="bash" noLines>sudo usermod -a -G dialout $USER</LessonCodeWrapper>

</li>

<li>컴퓨터를 다시 시작하세요.</li>

<li>

[릴리스](https://github.com/airalab/sensors-connectivity/releases)에서 Robonomics `airrohr-flasher` 실행 파일을 다운로드하세요.

</li>

<li>

파일의 권한을 변경하고 실행하세요:

<LessonCodeWrapper language="bash">chmod +x airrohr-flasher-linux
./airrohr-flasher-linux</LessonCodeWrapper>


</li>

</List>


**Windows 용:**

<List type="numbers">

<li>

USB2serial 드라이버 설치 (Windows 10에서는 자동으로 시작됩니다) - NodeMCU v3 (CH340)용 드라이버: [링크](http://www.wch.cn/downloads/file/5.html), [대체 링크](https://d.inf.re/luftdaten/CH341SER.ZIP). 

</li>

<li>

[릴리스](https://github.com/airalab/sensors-connectivity/releases)에서 Robonomics `airrohr-flasher` 실행 파일을 다운로드하고 실행하세요.

</li>

</List>

**MacOS 용:**

<List type="numbers">

<li>

USB2serial 드라이버를 설치하세요 — NodeMCU v3 (CH340)용 드라이버: [링크](http://www.wch.cn/downloads/file/178.html), [대체 링크](https://d.inf.re/luftdaten/CH341SER_MAC.ZIP).

</li>

<li>

[릴리스](https://github.com/airalab/sensors-connectivity/releases)에서 Robonomics `airrohr-flasher` 실행 파일을 다운로드하고 실행하세요.

</li>

</List>


## 설정

<List type="numbers">

<li>

PC에 센서를 연결하고 `airrohr-flasher` 프로그램을 실행합니다. 프로그램을 열면 다음을 볼 수 있습니다 (OS에 따라 다름):

<LessonImages imageClasses="mb" src="sensors-connectivity-course/lesson-3-0.png" alt="tutorial image"/>

</li>

<li>

`Board` 필드는 자동으로 채워집니다. 그렇지 않은 경우 드롭다운 목록에서 필요한 포트를 선택하십시오.

<RoboAcademyNote type="okay" title="INFO">
<code>airrohr-flasher</code>가 보드를 찾을 수 없는 경우, <b>요구 사항</b> 부분을 제대로 수행했는지 확인하십시오.
</RoboAcademyNote>

</li>

<li>

선호하는 언어로 펌웨어를 선택하고 `Upload`를 클릭합니다. 펌웨어 업로드에는 시간이 소요됩니다. 나중에 언어를 변경하거나 구성을 재설정하려는 경우 `플래시 지우기` 페이지로 이동하여 센서의 플래시 메모리를 지우는 버튼을 누릅니다.

</li>

<li>

펌웨어를 다운로드 한 후 ESP를 다시 부팅합니다 (USB를 연결 해제하고 다시 연결).

</li>

<li>

체크 박스 메뉴에서 센서를 선택합니다. SDS011 및 추가 센서를 선택합니다. `구성 저장`을 누릅니다.

</li>

<li>

구성을 다운로드 한 후 ESP를 다시 부팅합니다 (USB를 연결 해제하고 다시 연결).

</li>

</List>

## 연결

<List type="numbers">

<li>

재부팅 후 보드는 `RobonomicsSensor-xxxxxxxxx`라는 Wi-Fi 네트워크를 생성합니다. 휴대폰이나 컴퓨터에서 연결하면 인증 창이 나타납니다(그렇지 않은 경우 브라우저를 열고 `192.168.4.1`으로 이동).

</li>

<li>

목록에서 Wi-Fi 네트워크를 선택하고 (목록에 없는 경우 직접 작성) 암호 필드를 작성합니다.

</li>

<li>

센서를 설치할 위치의 좌표를 작성합니다.

<RoboAcademyNote type="warning" title="WARNING">
센서 좌표는 공개적으로 사용 가능한 지도에 표시됩니다. 개인 정보를 표시하고 싶지 않은 경우, 정확하지 않지만 가까운 좌표를 작성하십시오.
</RoboAcademyNote>

<LessonImages src="sensors-connectivity-course/lesson-3-1.png" alt="tutorial image"/>

</li>

<li>

`Save configuration and restart`을 클릭하세요. 보드가 재부팅되고 지정된 Wi-Fi 네트워크에 연결됩니다.

</li>

<li>

[로보노믹스 센서 맵](https://sensors.robonomics.network/#/)을 열고 센서를 설치한 장소를 찾아보세요. 몇 분 안에 지도에서 데이터가 포함된 센서를 볼 수 있습니다.


<LessonImages src="sensors-connectivity-course/lesson-3-2.jpg" alt="tutorial image"/>

</li>

</List>

기본 설치로 끝났습니다. 더 고급 설정(데이터를 자체 서버로 보내기)을 위해서는 다음 섹션을 읽으세요.

## Additional 구성

구성하기 전에 Wi-Fi 네트워크에서 센서의 주소를 찾아야 합니다. 이를 위해 `airrohr-flasher`를 사용할 수 있습니다(컴퓨터가 센서와 동일한 네트워크에 있어야 함). 시작하고 `Discovery` 탭으로 이동한 다음 `Refresh`를 누르고 잠시 기다리면 센서 주소가 나타납니다.

<LessonImages imageClasses="mb" src="sensors-connectivity-course/lesson-3-3.png" alt="tutorial image"/>

이 주소를 더블 클릭하거나 브라우저에 입력하면 센서 메뉴로 이동합니다.

<LessonImages imageClasses="mb" src="sensors-connectivity-course/lesson-3-4.png" alt="tutorial image"/>

이제 구성을 사용자 정의할 수 있습니다.


## 사용자 정의 API

자체 서버로 데이터를 보내도록 설정할 수도 있습니다. 이를 위해 `APIs` 탭에서 `Send to own API`를 클릭하고 서버 주소와 포트(`65`는 센서 연결성을 위한 것)를 지정하세요.

<LessonImages imageClasses="mb" src="sensors-connectivity-course/lesson-3-6.png" alt="tutorial image"/>

`Save and restart`을 클릭하여 설정을 저장하세요.