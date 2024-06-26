---
title: "쓰기: 방법"
description: AI 도구를 활용하여 학사 논문 빠르게 시작하기
metaOptions: [AI 도구를 활용하여 학사 논문 빠르게 배우기]
defaultName: Quickstart Your Bachelor's Thesis with AI-powered Tools
---

<RoboAcademyText fWeight="500">
학생들이 자신의 기술과 완성된 작업을 증명해야 하는 학사 논문의 주요 섹션을 쓰기 시작합니다.
</RoboAcademyText>

이 섹션은 (현재) 다양한 물리적 장치(주로 센서 및 스마트 기기)를 설정하고 실행할 수 없기 때문에 AI 도우미에 완전히 맡길 수 없다는 이유로 적어도 완전히 AI 도우미에게 맡길 수 없다는 것이 기대된다. 그럼에도 불구하고, 이 섹션의 준비를 쉽게 만들 수 있는 여러 전술을 고려할 것이다.

## 방법 섹션을 위한 텍스트 생성

먼저, 이 섹션에 대한 적어도 일부 텍스트를 얻으려고 시도했다. 이전에 언급했듯이, 학사 논문은 **"Robonomics와 Home Assistant를 이용한 주권 스마트 홈"** 과정을 기반으로 하기 때문에 올바른 맥락을 형성하기 위해 전체 과정을 AI 도우미에게 전달하는 것이 바람직하다. 다시 한 번, 우리는 맥락 제한의 문제에 직면했다:

- Auto-GPT는 자체적으로 강의 웹사이트를 충분히 확인할 수 없었으며, 계속해서 하위 작업으로 전환하거나 맥락을 잃었습니다. 강의 텍스트를 파일로 제공하는 시도도 너무 큰 맥락의 문제를 마주쳤습니다.
- Bing Chat은 2000-4000자의 제한이 있으며, 온라인 강의 웹사이트를 확인하는 요청은 표면적인 개요로 제한되었습니다.
- ChatGPT도 너무 큰 텍스트를 수용하지 않았습니다.

결과적으로, 강의 텍스트를 레슨별로 제공하는 전략이 선택되었으며, 레슨의 맥락을 기억하는 필요성을 명시했습니다. 추가 요청이 없는 경우, AI 어시스턴트는 즉시 Methods 섹션 작성을 제안합니다. 여기에는 몇 가지 예시가 있습니다.

<RoboAcademyDialog>

Methods

This section presents the methods employed to achieve the objectives of the study, which involved building a sovereign smart home with enhanced security and privacy features. The study was conducted as part of an online course titled "Smart Home Sovereign." The methods encompassed the setup of an IoT hub on a Raspberry Pi, connection of various smart devices to the hub using a 지그비 어댑터 and the MQTT protocol, integration of the hub with Home Assistant software, and the establishment of a connection between the hub and a decentralized cloud based on Polkadot web3 technology. These steps were taken to enable secure data transfer to the network and facilitate remote home management.

1\. Online Course: "Smart Home Sovereign"
The initial phase of the study involved the completion of the online course "Smart Home Sovereign." This course provided comprehensive guidance on building a sovereign smart home, emphasizing the importance of user data security and privacy. The bachelor successfully completed all the course modules, gaining a thorough understanding of the fundamental concepts and practical aspects related to the construction of a sovereign smart home.

2\. Setting up the IoT Hub
To establish a centralized control system for the smart home devices, an IoT hub was set up on a Raspberry Pi. The Raspberry Pi was selected due to its versatility, low cost, and compatibility with the desired functionalities. The IoT hub acted as the central communication point, facilitating the interaction between the smart devices and the user.

3\. 연결ing Smart Devices
Various smart devices were integrated into the sovereign smart home system. These devices included a temperature/humidity sensor, a door sensor, a smart bulb, and a motion sensor, among others. A 지그비 어댑터 was utilized to connect these devices to the IoT hub, enabling seamless communication. The MQTT (Message Queuing Telemetry Transport) protocol was employed to establish a reliable and efficient communication channel between the hub and the connected devices.

4\. Integration with Home Assistant
The IoT hub was integrated with Home Assistant, an open-source home automation platform. Home Assistant provided a user-friendly interface for managing and controlling the connected smart devices. This integration allowed the bachelor to monitor and control the devices remotely, enhancing the convenience and functionality of the sovereign smart home system.

5\. 연결ion to Decentralized Cloud
To ensure secure data transfer without relying on a centralized cloud service provider, a decentralized cloud based on Polkadot web3 technology was employed. This connection facilitated the secure transfer of device data to the network, protecting user privacy and enabling remote home management. The bachelor established a connection between the IoT hub and the decentralized cloud, enabling seamless data transfer and access.

6\. Data Security and Privacy Measures
Throughout the implementation process, stringent data security and privacy measures were implemented. The bachelor ensured the adoption of industry-standard encryption protocols and authentication mechanisms to safeguard the integrity and confidentiality of the user's personal and device data. Additionally, measures such as secure network configurations and regular software updates were implemented to mitigate potential vulnerabilities and security risks.

</RoboAcademyDialog>

<RoboAcademyDialog>

1\. Description of the Smart Home System Design using web3 technology, including hardware and software components:

\- Describe the overall architecture of the smart home system.

\- Explain the hardware components involved, such as the Raspberry Pi, sensors, actuators, and communication modules.

\- Discuss the software components, including the operating system, middleware, and applications used to control and manage the smart home system.

\- Highlight the role of web3 technology, such as blockchain, decentralized networks, and protocols, in enhancing the security and privacy of the system.


2\. Implementation details and justification for design choices:

\- Provide a step-by-step account of how the smart home system was implemented, including the installation and configuration processes.

\- Justify the selection of specific hardware and software components based on their compatibility, reliability, security features, and suitability for the project's objectives.

\- Discuss any modifications or customization made to the hardware or software components to meet the specific requirements of the smart home system.

\- Explain how the chosen web3 technology (e.g., blockchain, decentralized networks) addresses security and privacy concerns compared to traditional approaches.

3\. Evaluation plan for assessing the security and privacy of the system:

\- Outline the goals and objectives of the security and privacy evaluation.

\- Identify the specific security and privacy aspects to be evaluated, such as data encryption, access control, authentication, and data integrity.

\- Describe the evaluation methods and techniques to be used, such as penetration testing, vulnerability assessments, or simulations.

\- Explain how data will be collected, analyzed, and interpreted to assess the effectiveness of the implemented security and privacy measures.

\- Discuss any ethical considerations and potential risks associated with the evaluation process.

</RoboAcademyDialog>

결과적으로, 섹션을 위해 다른 계획에서 항목을 수동으로 선택하고 순차적으로 부분적으로 제공하는 것이 최선의 전략이었습니다. AI 어시스턴트가 소스 자료를 기반으로 작업을 수행해야 한다는 점을 잊지 말아야 합니다.

## 일러스트 생성

좋은 논문은 자료를 그래픽 형태로 제시할 수 있으므로 AI의 도움으로 적어도 시도해 보는 것이 좋습니다. MidJourney, DALL-E, Stable Diffusion 및 기타 서비스와 같은 다양한 모델의 기능에 대해 많이 쓰여 있지만, 이들은 주로 예술을 생성하기 위해 설계되었으며 엄격한 다이어그램과 차트를 생성하는 것이 아닙니다. 매우 자주 올바른 텍스트를 삽입할 수 없으며 일반적으로 얻은 일러스트는 너무 서툴러집니다.

예를 들어, Bing Chat에서 다음 내용의 다이어그램을 생성해 보겠습니다. 이는 Bing Image Creator로 요청을 재전송할 것입니다.

<RoboAcademyDialog>

Make image with diagram based on this description:

There are 4 main blocks: Raspberry Pi, Smart Devices, Zigbee Adapter and Web3 Decentalized Cloud. Zigbee Adapter is connected by a double-ended arrow to Smart Devices, the arrow has the name "Zigbee".

Inside Raspberry Pi there are 4 more internal blocks: Zigbee2MQTT, MQTT Broker, Home Assistant and "robonomics-interface". Zigbee2MQTT is connected by a double-ended arrow to MQTT Broker, the arrow has the name "MQTT". MQTT Broker is connected by a double-ended arrow to Home Assistant, the arrow has the name "MQTT". Home Assistant is connected by a double-ended arrow to "robonomics-interface", the arrow has the name "Robonomics Data".

Also, internal block Zigbee2MQTT is connected by a double-ended arrow to Zigbee Adapter, the arrow has the name "Zigbee". Internal block "robonomics-interface" is connected by a double-ended arrow to Web3 Decentalized Cloud, the arrow has the name "data & events".

</RoboAcademyDialog>

결과:

<robo-academy-grid :columns="3" textAlign="center">
    <robo-academy-grid-element>
      <LessonImages src="ai-based-bachelor-thesis/bad-diagram1.jpeg" alt="Diagram example from Bing"/>
    </robo-academy-grid-element>
    <robo-academy-grid-element>
      <LessonImages src="ai-based-bachelor-thesis/bad-diagram2.jpeg" alt="Diagram example from Bing"/>
    </robo-academy-grid-element/>
    <robo-academy-grid-element>
      <LessonImages src="ai-based-bachelor-thesis/bad-diagram3.jpeg" alt="Diagram example from Bing"/>
    </robo-academy-grid-element/>
</robo-academy-grid>

예를 들어, ChatGPT에서 `이 설명을 기반으로 UML 다이어그램 코드를 만드는 요청`을 추가한 유사한 요청은 여러 번의 시도 끝에 다음 결과를 얻었습니다:

<robo-academy-grid :columns="2" textAlign="center">
    <robo-academy-grid-element>
<LessonCodeWrapper language="uml" noCopyIcon noLines codeClass="big-code">
        @startuml
        package "Raspberry Pi" {
            [Zigbee2MQTT]
            [MQTT Broker]
            [Home Assistant]
            [robonomics-interface]
        }
        Zigbee2MQTT o--o "MQTT Broker" : MQTT
        "MQTT Broker" o--o "Home Assistant" : MQTT
        "Home Assistant" o--o "robonomics-interface" : "Robonomics Data"
        rectangle "Smart Devices"
        rectangle "Zigbee Adapter"
        "Zigbee Adapter" o--o "Smart Devices" : Zigbee
        "robonomics-interface" o--o "Web3 Decentalized Cloud" : "data & events"
        Zigbee2MQTT o--o "Zigbee Adapter" : Zigbee
        @enduml

</LessonCodeWrapper>
    </robo-academy-grid-element>
    <robo-academy-grid-element>
      <LessonImages src="ai-based-bachelor-thesis/system-diagram.png" alt="Diagram after producing UML code"/>
    </robo-academy-grid-element/>
</robo-academy-grid>

## 코드 생성

AI 어시스턴트는 자체적으로 장치를 설정할 수 없지만, 해당 소프트웨어를 작성하는 데 도움을 요청할 수 있습니다. 학사 논문을 위해, 설치된 스마트 홈 소프트웨어의 기능을 테스트하기 위해 Home Assistant를 기반으로 시나리오에 대한 자동화를 생성하기로 결정했습니다. 다음 요청이 AutoGPT로 전송되었습니다:

<RoboAcademyTerminal title="AutoGPT Terminal">

AI Name: Hass-GPT 

Hass-GPT is: an AI that creates automation scripts for Home Assistant based on the text description

Goal 1: Open https://www.home-assistant.io/examples/ and analyze script codes of automations

Goal 2: Create automation script code with following scenario: turn on the bulb when motion sensor detects someone; while motion is present, keep the bulb turned on; when the motion stops, turn the bulb off

Goal 3: Write this code to the file and return it back

</RoboAcademyTerminal>

AutoGPT의 결과로 다음 스크립트가 생성되었습니다:

<LessonCodeWrapper language="yaml" noCopyIcon codeClass="big-code">
    - alias: "모션 센서 Bulb Control"
      trigger:
        platform: state
        entity_id: binary_sensor.motion_sensor
        to: "on"
      action:
        service: light.turn_on
        entity_id: light.bulb
    - alias: "Motion Sensor Bulb Keep On"
      trigger:
        platform: state
        entity_id: binary_sensor.motion_sensor
        to: "on"
      action:
        service: light.turn_on
        entity_id: light.bulb
    - alias: "Motion Sensor Bulb Off"
      trigger:
        platform: state
        entity_id: binary_sensor.motion_sensor
        to: "off"
        for:
          minutes: 1
      action:
        service: light.turn_off
        entity_id: light.bulb
</LessonCodeWrapper>

물론, 스크립트는 특정 센서 및 장치 엔티티에 대한 추가 조이 필요했지만, 전반적으로 요청은 올바르게 처리되었습니다.

<RoboAcademyText>

그래서 실무는 AI가 이 섹션을 완전히 자체적으로 처리할 수 없다는 사실에도 불구하고, 일부 작업에 대해 큰 도움을 줄 수 있거나 그들의 해결책에 대한 아이디어를 제공할 수 있다는 것을 보여 주었습니다. 다음 섹션에서는 AI 도구가 어떻게 얻은 결과를 분석하고 해당 섹션을 형식화하는 데 도움을 줄 수 있는지 탐구할 것입니다.

</RoboAcademyText>