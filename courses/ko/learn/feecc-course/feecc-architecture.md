---
title: "아키텍처"
description: 이 강좌는 Feecc 시스템 및 그 구성 요소를 알아보는 데 관한 것입니다.
metaOptions: [배우기, Feecc에 익숙해지기]
defaultName: Getting Used to Feecc
---

<RoboAcademyText fWeight="500">
이 레슨에서는 Feecc 아키텍처를 더 자세히 살펴보고 소프트웨어의 모든 구성 요소를 살펴볼 것입니다.
</RoboAcademyText>

Feecc 플랫폼은 엔지니어 작업대의 제어부터 분석 제공까지 여러 서비스로 구성되어 있습니다. 각 서비스는 기업 환경에서 배포에 필요한 일종의 기능성을 담당합니다.

## Feecc 엔지니어 작업대

엔지니어 작업대의 주요 업무는 조립 엔지니어의 작업 공간을 조직하는 것입니다. 엔지니어가 필요한 장치는 작업에 따라 다음과 같을 수 있습니다:

- 생산 과정의 비디오 녹화를 위한 IP 카메라;
- 개인 RFID 카드로 시스템에서 식별을 위한 RFID 리더;
- 제품 라벨을 스캔하기 위한 바코드 리더;
- 제조 제품에 라벨을 붙이기 위한 라벨 프린터;
- 다양한 장치 / 스테이션으로부터 데이터를 수집하는 디지털 센서.

엔지니어 작업대 소프트웨어는 일반적으로 다음 컨테이너로 구성됩니다. 먼저, 제품 조립 중 직원이 작업하는 컴퓨터에 설치가 필요한 소프트웨어:

1. [feecc-workbench-daemon](https://github.com/Multi-Agent-io/feecc-workbench-daemon) — 모든 Feecc 기능과 구성에 대한 액세스를 제공하는 Feecc 플랫폼의 핵심으로, 라벨 프린터를 사용하여 라벨을 인쇄하고 RTSP 스트림에서 비디오를 녹화하는 경량 서비스도 포함되어 있습니다;
2. [feecc-workbench-frontend](https://github.com/Multi-Agent-io/feecc-workbench-frontend) — 직원이 Feecc 플랫폼과 상호 작용하는 웹 인터페이스;
3. [feecc-hid-reader-daemon](https://github.com/Multi-Agent-io/feecc-hid-reader-daemon) — USB 주변 장치 이벤트를 전송하기 위한 Python 데몬;

둘째, 직원의 컴퓨터와 로컬 네트워크의 서버에 모두 설치할 수 있는 소프트웨어:

1. [feecc-ipfs-gateway](https://github.com/Multi-Agent-io/feecc-ipfs-gateway) — IPFS로 파일을 게시하는 데 사용되는 마이크로서비스이며, 더 구체적으로는 파일 CID를 Robonomics Network로 전송하는 데 사용됩니다.

아래 그림은 기업 환경에서의 Feecc 엔지니어 작업 공간 아키텍처를 보여줍니다. IPFS 게이트웨이(뿐만 아니라 IPFS 노드 및 클러스터 피어 형태의 MongoDB)는 각 직원의 컴퓨터에 호스팅될 수 있으며, 이는 시스템의 분산화를 향상시키지만 계산 리소스 비용이 발생합니다.

<LessonImages src="feecc-course/feecc_global_hardware.png" alt="an architecture of Feecc"/>

### 한 작업 공간을 위한 지원되는 하드웨어:

#### RFID 스캐너

내부 배지를 사용하여 현장의 엔지니어를 승인하는 데 필요한 USB RFID 스캐너입니다. 수신된 정보는 `feecc-hid-reader-daemon`을 사용하여 처리됩니다.

#### 바코드 스캐너

제품을 바코드로 식별하고 서비스에 명령을 보내고 인증서를 올바르게 할당하는 데 필요한 USB 바코드 스캐너입니다. 수신된 정보는 또한 `feecc-hid-reader-daemon`을 사용하여 처리됩니다. 2차원으로 읽는 것이 바람직하지만 필수는 아닙니다.

#### 직원의 컴퓨터

외부 장치(코드 스캐너, RFID 스캐너)에서 신호를 처리하고 프린터에 이미지를 인쇄하고 비디오 녹화를 시작하고 중지하며 IPFS 게이트웨이로 데이터를 보내는 작은 싱글 보드 컴퓨터입니다. 다음 서비스를 실행합니다: `feecc-workbench-frontend`, 레이블 프린터 및 카메라 지원을 갖춘 `feecc-workbench-daemon`, `feecc-hid-reader-daemon`. Wi-Fi 또는 LAN을 통한 인터넷 연결이 필요합니다.
    
모니터가 있는 단일 지불 컴퓨터 대신 어떤 컴퓨터든 사용할 수 있음을 명시하는 것이 좋습니다. GNU/LINUX 운영 체제가 네이티브로 또는 가상 머신을 통해 설치되어야 합니다.
    
최소 기술 사양:
    
- CPU: Broadcom BCM2711, Quad core Cortex-A72 (ARM v8) 64-bit SoC @ 1.8GHz 또는 유사한 것;
- RAM: 4GB LPDDR4-3200 또는 유사한 것.

#### 화면

직원이 현재 생산 단계에 대한 정보를 입력하고 확인하는 데 사용하는 모니터입니다. 또한 엔지니어에게 현재 단계에 대한 힌트를 표시합니다. 다른 입력 장치도 사용할 수 있습니다.

#### 라벨 프린터

라벨 프린터는 제품 식별 및 확인을 위해 제품에 라벨을 부착하기 위해 QR 코드 및 바코드를 인쇄하는 데 사용됩니다. 프린터와의 상호 작용은 `feecc-workbench-daemon`의 해당 서비스를 사용하여 수행됩니다. 우리의 경우 XPrinter 236B 프린터를 사용합니다.

#### IP 카메라

제품 인증서에 포함하기 위해 제품 조립 영역 위에 배치된 제품 생산 과정을 촬영하기 위한 IP 카메라입니다. 카메라와의 상호 작용은 `feecc-workbench-daemon`의 해당 서비스를 사용하여 수행됩니다.

필수 기술 사양: PoE 전원 공급, RTSP 데이터 전송 프로토콜. 우리의 경우 Hikvision HiWatch DS-i200d를 사용합니다.

### 여러 작업 공간에 대한 지원되는 하드웨어:

#### 라우터 또는 스위치

IP 카메라에 전원을 공급하고 `feecc-workbench-daemon` 서비스에 연결하기 위해 PoE 802.3af 지원 및 출력 포트에서 PoE 전원 공급이 필요한 라우터 또는 스위치입니다. 우리의 경우 MikroTik hEX PoE (3-4 개의 작업 공간에 대해 하나) 및 전원 공급을 사용합니다.

#### 서버 (옵션)

`feecc-ipfs-gateway`를 실행할 수 있는 대형 서버도 설치할 수 있습니다. 직원 작업 공간 중 하나의 컴퓨터 자리에 위치할 수 있습니다. 

최소 기술 사양:

- CPU: Intel Xeon E-2200 프로세서 또는 유사한 것;
- RAM: 8GB;
- 저장 공간: 1TB HDD;
- LAN 인터페이스: 1 Gbit/s.

## Feecc Analytics

Feecc Analytics의 주요 업무는 완제품의 추적 가능성 및 제품 관리 부서에서의 사전 판매 검사 프로세스를 조직화하는 것입니다.

Feecc Analytics는 다음 컨테이너에 의존합니다:

1. [feecc-analytics-backend](https://github.com/Multi-Agent-io/feecc-analytics-backend) — 분석 서비스를 배포하는 데 사용되는 주요 소프트웨어;
2. [feecc-analytics-frontend](https://github.com/Multi-Agent-io/feecc-analytics-frontend) — 분석 서비스를 위한 프론트엔드 소프트웨어;

일반적으로 조직 내에서 데이터 보안 목적으로 로컬 서버에 배포됩니다.

Feecc Analytics가 작동하기 위해 필요한 하드웨어는 웹 응용 프로그램이 실행되고 바코드 스캐너가 있는 로컬 또는 원격 서버(가상 머신)입니다. 각 권한이 있는 직원은 사용자 이름과 암호로 자신의 컴퓨터에서 웹 응용 프로그램에 액세스할 수 있습니다.

## Feecc Validator

Feecc Validator의 주요 업무는 디지털 제품 인증서의 무결성을 검증하기 위해 다른 데이터 저장소에서 데이터를 비교하는 것입니다.

Feecc Validator는 다음 컨테이너에 의존합니다:

1. [feecc-validator-backend](https://github.com/Multi-Agent-io/feecc-validator-backend) — 인증서를 확인하고 사용자가 데이터 조각 중 하나만 가지고 있는 경우에 연결된 데이터를 처리하기 위해 설계된 마이크로서비스;
2. [feecc-validator-frontend](https://github.com/Multi-Agent-io/feecc-validator-frontend) — 인증 마이크로서비스와 상호 작용하기 위한 웹 인터페이스.

Feecc Analytics와 마찬가지로 로컬 서버에 배포되어야 하며 바코드 스캐너가 필요합니다.

<RoboAcademyText fWeight="500">
다음 수업에서는 컴퓨터에서 로컬로 실행되는 작은 데모를 통해 Feecc 시스템을 더 자세히 살펴볼 것입니다.
</RoboAcademyText>