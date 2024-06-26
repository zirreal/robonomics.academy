---
title: 스마트 공간용 ROS 기반 프로젝트
lastUpdate: Thu May 04 2023 12:53:19 GMT+0400 (Samara Standard Time)
description: 스마트 공간용 ROS 기반 프로젝트
metaOptions: [배우다]
defaultName: ROS-based projects for smart spaces
---

로봇 운영 시스템 프레임워크는 15년의 개발 과정을 통해 수십 개의 [다양한 로봇 장치](https://robots.ros.org/)와 툴을 개발한 커뮤니티가 더 많은 알고리즘과 도구를 포함하여 통합되었습니다. 사실, 이제는 많은 프로젝트가 있고, 그들의 저장소 설명 스타일의 혼란이 커져서 특정 주제에 특화된 프로젝트를 찾는 것이 현재 상당히 문제가 됩니다. 

여기에서는 가정이나 사무실 환경에서 사용되는 로봇 및 IoT 장치에 특화된 ROS 기반 프로젝트의 겸손한 목록을 찾을 수 있습니다. 이 주제는 Robonomics 플랫폼의 기둥 중 하나입니다. 우리의 목표는 기술적 통합 관점과 로봇 경제에서 이러한 장치의 흥미로운 응용 프로그램의 관점에서 이러한 프로젝트를 Robonomics와 함께 추진하는 것입니다. 아이디어와 영감을 찾는 데 이 목록을 자유롭게 사용하십시오.

우리의 [학습 섹션](/learn)에서 Robonomics와 통합된 일부 ROS 프로젝트 예제를 확인할 수 있습니다.

<!-- 현재 (**2021년 4월**) Robonomics는 ROS **Melodic** 및 **Noetic** 버전을 대상으로 하고 습니다. 이전 버전도 작동할 수 있지만 추가적인 통합 작업이 필요할 수 있습니다. 미래에는 ROS 버전 2의 지원이 추가될 것입니다. -->

ROS 저장소 및 패키지를 검색하는 주요 자원은 [여기](https://index.ros.org/)에서 액세스할 수 있습니다.

## 시뮬레이션

장치에 주의를 기욀 전에, 많은 ROS 프로젝트를 시뮬레이션에서 테스트할 수 있는 옵션이 있다는 것을 기억하는 것이 가치가 있습니다. ROS 하에서 다양한 로봇을 3D 모델링하는 가장 인기 있는 도구는 [Gazebo](http://gazebosim.org/) 시뮬레이터와 그 파생 프로젝트인 [Ignition](https://index.ros.org/r/ros_ign/)입니다. 두 시뮬레이터 모두 다양한 실내 및 실외 환경에서 장치를 모델링하고 모델 및 환경 자체를 변경하며 제어 알고리즘을 테스트하고 실제 장치로 이동하기 전에 디버깅할 수 있습니다. 또한, 이는 실제 장치가 없을 때 교육 및 상황에 훌륭한 도구입니다.

전반적으로, 이는 어떠한 비용도 들지 않고 Robonomics를 ROS 장치와 통합하려는 최상의 옵션 중 하나입니다. 실제 시나리오에서는 약간의 코드 수정만 필요할 것입니다. Gazebo에 대해서는 Robonomics가 [설정](https://wiki.robonomics.network/docs/en/connect-any-ros-compatible-robot-under-robonomics-parachain-control-1/)과 [통합](https://wiki.robonomics.network/docs/en/connect-any-ros-compatible-robot-under-robonomics-parachain-control-2/)을 다룬 두 부분으로 구성된 자세한 가이드가 있습니다 (드론을 예로 들어 사용). 주요 도전은 Gazebo를 위한 준비된 모델을 찾는 것(예: [여기](https://github.com/osrf/gazebo_models))이거나 시뮬레이터용으로 개발된 [SDFormat](http://sdformat.org/)을 사용하여 자체 모델을 만들어 보는 것입니다. 

## 싱글 보드 컴퓨터 및 기타 보드

이러한 보드는 주로 센서 및 녹음 장치(오디오, 사진 및 비디오 레코더, 카메라, 온도, 압력 및 물질 농도 센서)와 연결하기 위한 기본 구성 요소로 작용합니다. 스마트 공간의 개념은 인프라 객체의 [디지털 트윈](https://gateway.pinata.cloud/ipfs/QmNNdLG3vuTsJtZtNByWaDTKRYPcBZSZcsJ1FY6rTYCixQ/Robonomics_keypoint_March_2021.pdf)을 만드는 것을 의미하므로 보드는 주요 컴퓨팅 장치 및 로봇 이동 장치를 구성하는 컨트롤러로 작용할 수 있습니다. ROS를 지원하는 보드 목록은 아래에 제시되어 있습니다:

| Name and link                                                                                         |                                    Description                                  | ROS version | Last update |
|:-----------------------------------------------------------------------------------------------------:|---------------------------------------------------------------------------------|:-----------:|:-----------:|
|  [Raspberry Pi](http://wiki.ros.org/ROSberryPi/Installing%20ROS%20Melodic%20on%20the%20Raspberry%20Pi)| single board computer; RaspPi versions 2, 3 and 4 are available                 |   melodic   |     2020    |
|    [Arduino](http://wiki.ros.org/rosserial_arduino)                                                   | single board computer                                                           |    noetic   |     2021    |
|    [Phidgets](http://wiki.ros.org/phidgets)                                                           | sets of boards, various sensors and devices: Ph sensor, LED, RFID, motor control|    noetic   |     2020    |
|   [Sense HAT](https://wiki.ros.org/sensehat_ros)                                                      | shield for RaspPi with a set of sensors and LED                                 |    noetic   |     2020    |
|     [Navio2](https://navio2.emlid.com/)                                                               | autopliot shield for RaspPi 2,3,4                                               |    noetic   |     2020    |
|     [OpenCR](http://wiki.ros.org/opencr)                                                              | robot controller                                                                |    noetic   |     2021    |

<br/>

## 스마트 홈 장치 및 가정용 로봇

여기에는 초기 사용 목적이 스마트 홈이나 사무실용이었던 ROS 장치들이 제시되어 있습니다. 청소기 및 로봇 보조부터 홈 컨트롤 시스템까지 다양한 목록이 있습니다.

| Name and link                                             | Description                                                 |          ROS version          | Last update |
|:---------------------------------------------------------:|-------------------------------------------------------------|:-----------------------------:|:-----------:|
|  [Care-O-bot 4](http://wiki.ros.org/care-o-bot)           | household robot-assistant; a simulation is available        |            melodic            |     2021    |
|     [Kobuki](http://wiki.ros.org/kobuki)                  | mobile platform with different use cases (e.g. a waiter)    |            melodic            |     2020    |
|    [QTrobot](http://wiki.ros.org/Robots/qtrobot)          | humanoid social robot                                       | kinetic (melodic can be used) |     2020    |
|      [Nao](http://wiki.ros.org/nao)                       | humanoid robot; a simulation is available                   |            Melodic            |     2020    |
|     [TIAGo](http://wiki.ros.org/Robots/TIAGo)             | service robot with a manipulator; a simulation is available |            kinetic            |     2020    |
|     [Roomba](https://github.com/AutonomyLab/create_robot) | robot vacuum cleaner                                        |            melodic            |     2020    |
|    [OpenHAB](http://wiki.ros.org/iot_bridge)              | home automation system                                      |            kinetic            |     2017    |
|     [Sesame](https://index.ros.org/p/sesame_ros/)         | smart lock                                                  |            melodic            |     2021    |

<br/>

## 이동 플랫폼 및 조작기

우선 ROS는 드론부터 산업용 조작기까지 모바일 로봇을 지원하는 데 알려져 있으며, 이를 위해 동시 위치추적 및 매핑(SLAM)을 실현하는 많은 패키지가 만들어졌으며, 역학의 직접 및 역과제를 해결하고 궤적 계획 및 기타를 실현합니다. 모바일 로봇공학은 점차 일상생활로 침투하고 있으며, 이에 따라 기존 ROS 로봇을 스마트 공간 내에서 사용하는 것이 흥미로울 것입니다. ROS 기반 모바일 플랫폼의 일반 목록은 상당히 크며, 따라서 여기에서는 가정이나 사무실 공간에서 운영하기에 편리한 것들을 선택했습니다. 

| Name and link                                             | Description                                | ROS version | Last update |
|:---------------------------------------------------------:|--------------------------------------------|:-----------:|:-----------:|
|   [turtlebot](http://wiki.ros.org/turtlebot3)             | mobile platform tailored for ROS           |    noetic   |     2020    |
|    [GoPiGo3](http://wiki.ros.org/Robots/gopigo3)          | mobile robot based on RaspPi               |   melodic   |     2020    |
|    [LoCoBot](http://wiki.ros.org/locobot)                 | mobile manipulator                         |   kinetic   |     2020    |
|   [ROSbot 2.0](http://wiki.ros.org/Robots/ROSbot-2.0)     | mobile platform; a simulation is available |    noetic   |     2021    |
|     [VOLTA](http://wiki.ros.org/Robots/Volta)             | mobile platform; a simulation is available |   melodic   |     2021    |
|    [evarobot](http://wiki.ros.org/Robots/evarobot)        | mobile platform; a simulation is available |    noetic   |     2020    |
|    [Freight](http://wiki.ros.org/Robots/freight)          | mobile platform; a simulation is available |   melodic   |     2021    |
|      [PR2](http://wiki.ros.org/Robots/PR2)                | mobile platform; a simulation is available |   melodic   |     2021    |