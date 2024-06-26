---
title: "Schrijven: Methoden"
description: Start snel uw bachelorscriptie met door AI aangedreven tools
metaOptions: [Leer, start snel uw bachelorscriptie met door AI aangedreven tools]
defaultName: Quickstart Your Bachelor's Thesis with AI-powered Tools
---

<RoboAcademyText fWeight="500">
We beginnen met het schrijven van de hoofdsectie van de gehele bachelorscriptie, waarin de studenten hun vaardigheden en voltooide werk moeten aantonen.
</RoboAcademyText>

Er wordt verwacht dat deze sectie niet volledig aan de AI-assistent kan worden toevertrouwd, althans om de reden dat deze tools (momenteel) niet verschillende fysieke apparaten kunnen configureren en lanceren (voornamelijk sensoren en slimme apparaten). Desalniettemin zullen we verschillende tactieken overwegen die de voorbereiding van deze sectie gemakkelijker kunnen maken.

## Genereren van tekst voor Methoden sectie

Allereerst werd geprobeerd om op zijn minst wat tekst voor deze sectie te verkrijgen. Zoals eerder vermeld, is de bachelorscriptie gebaseerd op de cursus **"Soevereine Smart Home met Robonomics en Home Assistant"**, dus het is wenselijk om de hele cursus aan de AI-assistent te voeren om de juiste context te vormen. Opnieuw stuitten we op het probleem van contextbeperkingen:

- Auto-GPT kon de cursuswebsite niet adequaat controleren, constant overschakelend naar subtaken of de context verliezend. Een poging om de cursustekst als bestand te voeden stuitte ook op het probleem van te grote context.
- Bing Chat heeft een limiet van 2000-4000 tekens, en het verzoek om de online cursuswebsite te controleren was beperkt tot een oppervlakkig overzicht.
- ChatGPT accepteerde ook geen te grote tekst.

Als gevolg daarvan werd de tactiek van het voeden van de cursustekst per les gekozen, waarbij de noodzaak om de context van de lessen te onthouden werd gespecificeerd. Als er geen aanvullende verzoeken worden gedaan, stellen AI-assistenten onmiddellijk een plan voor om de Methoden sectie te schrijven. Hier zijn een paar voorbeelden:

<RoboAcademyDialog>

Methods

This section presents the methods employed to achieve the objectives of the study, which involved building a sovereign smart home with enhanced security and privacy features. The study was conducted as part of an online course titled "Smart Home Sovereign." The methods encompassed the setup of an IoT hub on a Raspberry Pi, connection of various smart devices to the hub using a Zigbee-adapter and the MQTT protocol, integration of the hub with Home Assistant software, and the establishment of a connection between the hub and a decentralized cloud based on Polkadot web3 technology. These steps were taken to enable secure data transfer to the network and facilitate remote home management.

1\. Online Course: "Smart Home Sovereign"
The initial phase of the study involved the completion of the online course "Smart Home Sovereign." This course provided comprehensive guidance on building a sovereign smart home, emphasizing the importance of user data security and privacy. The bachelor successfully completed all the course modules, gaining a thorough understanding of the fundamental concepts and practical aspects related to the construction of a sovereign smart home.

2\. Setting up the IoT Hub
To establish a centralized control system for the smart home devices, an IoT hub was set up on a Raspberry Pi. The Raspberry Pi was selected due to its versatility, low cost, and compatibility with the desired functionalities. The IoT hub acted as the central communication point, facilitating the interaction between the smart devices and the user.

3\. Verbindening Smart Devices
Various smart devices were integrated into the sovereign smart home system. These devices included a temperature/humidity sensor, a door sensor, a smart bulb, and a motion sensor, among others. A Zigbee-adapter was utilized to connect these devices to the IoT hub, enabling seamless communication. The MQTT (Message Queuing Telemetry Transport) protocol was employed to establish a reliable and efficient communication channel between the hub and the connected devices.

4\. Integration with Home Assistant
The IoT hub was integrated with Home Assistant, an open-source home automation platform. Home Assistant provided a user-friendly interface for managing and controlling the connected smart devices. This integration allowed the bachelor to monitor and control the devices remotely, enhancing the convenience and functionality of the sovereign smart home system.

5\. Verbindenion to Decentralized Cloud
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

Als gevolg daarvan was de beste tactiek het handmatig selecteren van items uit verschillende plannen voor de sectie, en ze vervolgens sequentieel en in delen te voeden. Het is belangrijk om de context niet te vergeten, eraan herinnerend dat de AI-assistent zijn taak moet uitvoeren op basis van het bronmateriaal.

## Genereren van illustraties

Een goede scriptie kan materiaal in grafische vorm presenteren, dus het is noodzakelijk om op zijn minst te proberen dit te doen met behulp van AI. Er is veel geschreven over de mogelijkheden van verschillende modellen, zoals MidJourney, DALL-E, Stable Diffusion, en andere diensten, maar ze zijn voornamelijk ontworpen voor het genereren van kunst, niet strikte diagrammen en grafieken. Vaak kunnen ze de juiste tekst niet invoegen, en over het algemeen zijn de verkregen illustraties vaak te onhandig.

Als voorbeeld, laten we proberen een diagram te maken van de volgende inhoud in Bing Chat, dat het verzoek zal doorsturen naar Bing Image Creator:

<RoboAcademyDialog>

Make image with diagram based on this description:

There are 4 main blocks: Raspberry Pi, Smart Devices, Zigbee Adapter and Web3 Decentalized Cloud. Zigbee Adapter is connected by a double-ended arrow to Smart Devices, the arrow has the name "Zigbee".

Inside Raspberry Pi there are 4 more internal blocks: Zigbee2MQTT, MQTT Broker, Home Assistant and "robonomics-interface". Zigbee2MQTT is connected by a double-ended arrow to MQTT Broker, the arrow has the name "MQTT". MQTT Broker is connected by a double-ended arrow to Home Assistant, the arrow has the name "MQTT". Home Assistant is connected by a double-ended arrow to "robonomics-interface", the arrow has the name "Robonomics Data".

Also, internal block Zigbee2MQTT is connected by a double-ended arrow to Zigbee Adapter, the arrow has the name "Zigbee". Internal block "robonomics-interface" is connected by a double-ended arrow to Web3 Decentalized Cloud, the arrow has the name "data & events".

</RoboAcademyDialog>

Resultaten:

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

Het is beter om te vragen om code te maken voor een diagram, bijvoorbeeld in UML, en vervolgens een illustratie te genereren in een diagrameditor. Een vergelijkbaar verzoek in ChatGPT met de toevoeging van `Maak UML-diagramcode op basis van deze beschrijving`, produceerde na enkele pogingen het volgende resultaat:

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

## Genereren van code

Hoewel een AI-assistent niet zelf een apparaat kan instellen, kan worden gevraagd om te helpen bij het schrijven van software ervoor. Voor onze bachelorscriptie, om de functionaliteit van de geïnstalleerde slimme thuissoftware te testen, besloten we een automatisering te maken voor Home Assistant op basis van een scenario. Het volgende verzoek werd naar AutoGPT gestuurd:

<RoboAcademyTerminal title="AutoGPT Terminal">

AI Name: Hass-GPT 

Hass-GPT is: an AI that creates automation scripts for Home Assistant based on the text description

Goal 1: Open https://www.home-assistant.io/examples/ and analyze script codes of automations

Goal 2: Create automation script code with following scenario: turn on the bulb when motion sensor detects someone; while motion is present, keep the bulb turned on; when the motion stops, turn the bulb off

Goal 3: Write this code to the file and return it back

</RoboAcademyTerminal>

Als resultaat van AutoGPT werd het volgende script gegenereerd:

<LessonCodeWrapper language="yaml" noCopyIcon codeClass="big-code">
    - alias: "Bewegingssensor Bulb Control"
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

Natuurlijk vereiste het script aanvullende aanpassingen voor specifieke sensoren en apparaatentiteiten, maar over het algemeen werd het verzoek correct verwerkt.

<RoboAcademyText>

Dus, de praktijk heeft aangetoond dat ondanks het feit dat AI deze sectie niet volledig alleen kan afhandelen, het op zijn minst aanzienlijk kan helpen bij sommige taken of ideeën kan bieden voor hun oplossingen. In de volgende sectie zullen we verkennen hoe AI-tools kunnen helpen bij het analyseren van de verkregen resultaten en het formatteren van de overeenkomstige sectie.

</RoboAcademyText>