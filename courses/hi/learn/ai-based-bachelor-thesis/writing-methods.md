---
title: "लेखन: विधि"
description: एआई-संचालित उपकरणों के साथ अपने स्नातक थीसिस को शीघ्र प्रारंभ करें
metaOptions: [सीखें, एआई-संचालित उपकरणों के साथ अपने स्नातक थीसिस को शीघ्र प्रारंभ करें]
defaultName: Quickstart Your Bachelor's Thesis with AI-powered Tools
---

<RoboAcademyText fWeight="500">
अब हम बैचलर के पूरे थीसिस के मुख्य अनुभाग को लिखने की शुरुआत कर रहे हैं, जिसमें छात्रों को अपने कौशल और पूरे काम का प्रदर्शन करना चाहिए।
</RoboAcademyText>

यह सेक्शन पूरी तरह से एआई सहायक को सौंपा नहीं जा सकता, कम से कम इस कारण के लिए कि ये उपकरण (वर्तमान में) विभिन्न भौतिक उपकरणों (प्राथमिकतः सेंसर और स्मार्ट उपकरण) को कॉन्फ़िगर और लॉन्च नहीं कर सकते। फिर भी, हम कुछ उपाय का विचार करेंगे जो इस खंड की तैयारी को आसान बना सकते हैं।

## विधियों अनुभाग के लिए पाठ उत्पन्न करना

पहले, इस खंड के लिए कम से कम कुछ पाठ प्राप्त करने का प्रयास किया गया। जैसा पहले से ही उल्लिखित है, बैचलर की थीसिस **"रोबोनॉमिक्स और होम असिस्टेंट के साथ सार्वभौमिक स्मार्ट होम"** कोर्स पर आधारित है, इसलिए सही संदर्भ बनाने के लिए पूरे कोर्स को एआई सहायक को प्रदान करना अधिकतम उपयुक्त है। फिर भी, हमें संदर्भ सीमाओं की समस्या का सामना करना पड़ा:

- ऑटो-जीपीटी अपने आप ठीक से पाठ्यक्रम वेबसाइट की जाँच करने में सक्षम नहीं था, लगातार उप-कार्यों में स्विच करता रहता था या संदर्भ खो देता था। पाठ को फ़ाइल के रूप में प्रदान करने का प्रयास भी बड़े संदर्भ की समस्या का सामना किया।
- बिंग चैट की एक सीमा 2000-4000 वर्ण होती है, और ऑनलाइन कोर्स वेबसाइट की जाँच के लिए अनुरूप एक थलथलाहटपूर्ण अवलोकन के लिए प्रतिबंध था।
- चैटजीपीटी ने भी एक बहुत बड़े पाठ को स्वीकार नहीं किया।

नतीजतन, पाठ्यक्रम के पाठों द्वारा पाठ प्रदान करने का तरीका चुना गया, जबकि पाठों के संदर्भ को याद रखने की आवश्यकता को निर्दिष्ट किया गया। यदि कोई अतिरिक्त अनुरोध नहीं किया गया है, तो एआई सहायक सीधे विधियों अनुभाग के लिए लिखने की योजना सुझाते हैं। यहाँ कुछ उदाहरण हैं:

<RoboAcademyDialog>

Methods

This section presents the methods employed to achieve the objectives of the study, which involved building a sovereign smart home with enhanced security and privacy features. The study was conducted as part of an online course titled "Smart Home Sovereign." The methods encompassed the setup of an IoT hub on a Raspberry Pi, connection of various smart devices to the hub using a जिगबी एडाप्टर and the MQTT protocol, integration of the hub with Home Assistant software, and the establishment of a connection between the hub and a decentralized cloud based on Polkadot web3 technology. These steps were taken to enable secure data transfer to the network and facilitate remote home management.

1\. Online Course: "Smart Home Sovereign"
The initial phase of the study involved the completion of the online course "Smart Home Sovereign." This course provided comprehensive guidance on building a sovereign smart home, emphasizing the importance of user data security and privacy. The bachelor successfully completed all the course modules, gaining a thorough understanding of the fundamental concepts and practical aspects related to the construction of a sovereign smart home.

2\. Setting up the IoT Hub
To establish a centralized control system for the smart home devices, an IoT hub was set up on a Raspberry Pi. The Raspberry Pi was selected due to its versatility, low cost, and compatibility with the desired functionalities. The IoT hub acted as the central communication point, facilitating the interaction between the smart devices and the user.

3\. Connecting Smart Devices
Various smart devices were integrated into the sovereign smart home system. These devices included a temperature/humidity sensor, a door sensor, a smart bulb, and a motion sensor, among others. A जिगबी एडाप्टर was utilized to connect these devices to the IoT hub, enabling seamless communication. The MQTT (Message Queuing Telemetry Transport) protocol was employed to establish a reliable and efficient communication channel between the hub and the connected devices.

4\. Integration with Home Assistant
The IoT hub was integrated with Home Assistant, an open-source home automation platform. Home Assistant provided a user-friendly interface for managing and controlling the connected smart devices. This integration allowed the bachelor to monitor and control the devices remotely, enhancing the convenience and functionality of the sovereign smart home system.

5\. Connection to Decentralized Cloud
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

नतीजतन, सबसे अच्छा उपाय खंड के लिए विभिन्न योजनाओं से वस्तुओं का मैन्युअल चयन था, और उन्हें क्रमशः और भागों में प्रदान किया जाना था। संदर्भ को भूलना महत्वपूर्ण है, याद दिलाना कि एआई सहायक को अपने काम को मूल सामग्री पर आधारित करना चाहिए।

## चित्रों का उत्पादन

एक अच्छी थीसिस सामग्री को ग्राफिकल रूप में प्रस्तुत कर सकती है, इसलिए कम से कम एआई की मदद से इसे करने का प्रयास करना आवश्यक है। विभिन्न मॉडल्स की क्षमताओं के बारे में बहुत कुछ लिखा गया है, जैसे कि मिडजर्नी, डैल-ई, स्थिर विकिरण, और अन्य सेवाएं, लेकिन वे प्राथमिकतः कला उत्पन्न करने के लिए डिज़ाइन किए गए हैं, सख्त आरेख और चार्ट्स नहीं। बहुत बार, वे सही पाठ नहीं डाल सकते हैं, और सामान्य रूप से, प्राप्त चित्र बहुत अदम्य होते हैं।

उदाहरण के रूप में, चलो बिंग चैट में निम्नलिखित सामग्री का एक आरेख बनाने का प्रयास करें, जो बिंग इमेज क्रिएटर को रीडायरेक्ट करेगा:

<RoboAcademyDialog>

Make image with diagram based on this description:

There are 4 main blocks: Raspberry Pi, Smart Devices, Zigbee Adapter and Web3 Decentalized Cloud. Zigbee Adapter is connected by a double-ended arrow to Smart Devices, the arrow has the name "Zigbee".

Inside Raspberry Pi there are 4 more internal blocks: Zigbee2MQTT, MQTT Broker, Home Assistant and "robonomics-interface". Zigbee2MQTT is connected by a double-ended arrow to MQTT Broker, the arrow has the name "MQTT". MQTT Broker is connected by a double-ended arrow to Home Assistant, the arrow has the name "MQTT". Home Assistant is connected by a double-ended arrow to "robonomics-interface", the arrow has the name "Robonomics Data".

Also, internal block Zigbee2MQTT is connected by a double-ended arrow to Zigbee Adapter, the arrow has the name "Zigbee". Internal block "robonomics-interface" is connected by a double-ended arrow to Web3 Decentalized Cloud, the arrow has the name "data & events".

</RoboAcademyDialog>

परिणाम:

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

यह बेहतर है कि आप एक आरेख के लिए कोड बनाने के लिए पूछें, उदाहरण के लिए, UML में, और फिर डायग्राम संपादक में एक चित्र उत्पन्न करें। उदाहरण के रूप में, ChatGPT में एक समान अनुरोध के साथ `Make UML diagram code based on this description` जोड़ने के बाद, कई प्रयासों के बाद, निम्नलिखित परिणाम प्राप्त हुआ:

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

## कोड उत्पन्न करना

हालांकि, एक एआई सहायक अपने आप एक उपकरण सेट नहीं कर सकता, लेकिन उससे उसके लिए सॉफ़्टवेयर लिखने में मदद मांगी जा सकती है। हमारे स्नातक थीसिस के लिए, स्थापित स्मार्ट होम सॉफ़्टवेयर के कार्यक्षमता को परीक्षण करने के लिए, हमने एक घटनाक्रम पर आधारित होम असिस्टेंट के लिए एक स्वचालन बनाने का निर्णय लिया। निम्नलिखित अनुरोध ऑटोजीपीटी को भेजा गया:

<RoboAcademyTerminal title="AutoGPT Terminal">

AI Name: Hass-GPT 

Hass-GPT is: an AI that creates automation scripts for Home Assistant based on the text description

Goal 1: Open https://www.home-assistant.io/examples/ and analyze script codes of automations

Goal 2: Create automation script code with following scenario: turn on the bulb when motion sensor detects someone; while motion is present, keep the bulb turned on; when the motion stops, turn the bulb off

Goal 3: Write this code to the file and return it back

</RoboAcademyTerminal>

ऑटोजीपीटी के परिणामस्वरूप, निम्नलिखित स्क्रिप्ट उत्पन्न हुआ था:

<LessonCodeWrapper language="yaml" noCopyIcon codeClass="big-code">
    - alias: "Motion Sensor Bulb Control"
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

बेशक, स्क्रिप्ट को विशेष रूप से सेंसर और डिवाइस एंटिटी के लिए अतिरिक्त समायोजन की आवश्यकता थी, लेकिन समग्र अनुरोध सही ढंग से प्रसंस्कृत किया गया था।

<RoboAcademyText>

इसलिए, अभ्यास ने दिखाया है कि यहाँ तक कि यदि ए.आई. इस खंड को पूरी तरह से अपने आप संभाल नहीं सकती, तो यह कम से कम कुछ कार्यों में बड़ी मदद कर सकती है या उनके समाधान के लिए विचार प्रदान कर सकती है। अगले खंड में, हम जांचेंगे कि ए.आई. उपकरण कैसे प्राप्त परिणामों का विश्लेषण करने में मदद कर सकते हैं और संबंधित खंड का स्वरूप तयार कर सकते हैं।

</RoboAcademyText>