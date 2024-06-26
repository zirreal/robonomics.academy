---
title: "सबक #4b, गेटवे सेटअप: रोबोनॉमिक्स एसएलएस गेटवे"
lastUpdate: Thu May 18 2023 16:16:20 GMT+0400 (Samara Standard Time)
description: होम असिस्टेंट कोर्स
lessonNumber: 5
metaOptions: [रोबोनॉमिक्स और होम असिस्टेंट के साथ साम्राजिक स्मार्ट होम सीखें]
defaultName: Sovereign Smart Home with Robonomics and Home Assistant
---

## यह किसके बारे में है

यह रोबोनॉमिक्स एसएलएस गेटवे का उपकरण जोड़ने के लिए एक स्थिति सेटअप है। रोबोनॉमिक्स ने [स्मार्ट लॉजिक सिस्टम](https://github.com/slsys/Gateway) परियोजना द्वारा विकसित गेटवे से डिज़ाइन प्रेरणा ली और सर्किट्री का हिस्सा संशोधित किया। आप रोबोनॉमिक्स से एक गेटवे आदेश कर सकते हैं या हमारे [ब्लूप्रिंट्स](https://oshwlab.com/ludovich88/robonomics_sls_gateway_v01) का उपयोग करके अपना खुद का गेटवे बना सकते हैं।

आप गेटवे के लिए आश्यक सॉफ़्टवेयर को स्थापित करेंगे, इसे कॉन्फ़िगर करेंगे और होम असिस्टेंट से जोड़ेंगे।

<robo-academy-note type="note" title="ध्यान दें">
  स्मार्टआरएफ फ्लैश प्रोग्रामर, फर्मवेयर अपडेट करने के लिए एक प्रोग्राम, विंडोज ऑपरेटिंग सिस्टम की आवश्यकता है।
</robo-academy-note>

## निर्देश

<List type="numbers">

<li>

Zigbee माइक्रोकंट्रोलर फर्मवेयर स्थापित करना

<List>

<li>

पहले आपको गेटवे के CC2652P माइक्रोकंट्रोलर को फ्लैश करना होगा। SLS गेटवे के निचले हिस्से में स्विच <code>2</code>, <code>4</code> और <code>7</code> को <code>ON</code> पर सेट करें, अन्य <code>OFF</code> होने चाहिए।

<LessonImages src="smart-house-course/lesson-4-b-1.png" alt="controllers"/>
</li>

<li>

गेटवे को अपने कंप्यूटर से एक USB-A<>USB-C केबल के साथ कनेक्ट करें।

<robo-academy-note type="warning" title="चेतावनी">
  कृपया केबल के लिए केवल USB-A<>USB-C प्रकार का उपयोग करें, क्योंकि इस समय गेटवे USB-C<>USB-C प्रकार का समर्थन नहीं करता।
</robo-academy-note>

</li>

<li>

CC2652 फर्मवेयर के लिए स्मार्टआरएफ फ्लैश प्रोग्रामर v2 टेक्सास इंस्ट्रूमेंट से आवश्यक है। इसे [आधिकारिक साइट](https://www.ti.com/tool/download/FLASH-PROGRAMMER-2) से डाउनलोड करें और फिर स्थापित करें।

</li>

<li>

CC2652P माइक्रोकंट्रोलर के लिए फर्मवेयर डाउनलोड करें [GitHub भंडार](https://github.com/egony/cc2652p_cc1352p_RF-STAR/tree/main/firmware/coordinator).

</li>

<li>

कार्यक्रम चलाएं। <code>कनेक्टेड डिवाइस</code> विंडो में सीसी2652पी माइक्रोकंट्रोलर का चयन करें, फर्मवेयर का पथ सेट करें, झंडे को <code>मिटाएं, प्रोग्राम करें, सत्यापित करें</code> जैसा चित्र में है और <code>स्टार्ट</code> दबाएं।

<LessonImages src="smart-house-course/lesson-4-b-2.png" alt="tutorial" imageClasses="mb"/>

सफलतापूर्वक फ्लैशिंग के बाद, आपको एक <code>सफलता!</code> संदेश दिखाई देगा। अब आप यूएसबी केबल निकाल सकते हैं।

</li>
</List>
</li>

<li>

माइक्रोकंट्रोलर फर्मवेयर इंस्टॉल करना

<List>

<li>

अब आपको सॉफ्टवेयर इंस्टॉलेशन के लिए गेटवे सेट करने की आवश्यकता है। हम आपको सलाह देते हैं कि आप फर्मवेयर को अपडेट करने के लिए गेटवे को सीधे अपने रास्पबेरी पाई से कनेक्ट करें और उस डवाइस पर निम्नलिखित सभी कमांड्स दर्ज करें। 

</li>

<li>

नीचे भाग में SLS गेटवे पर <code>1</code> और <code>3</code> स्विच को <code>ऑन</code> करें, अन्य को <code>ऑफ</code> करें। फिर गेटवे को अपने रास्पबेरी पाई से यूएसबी टाइप-सी पोर्ट से कनेक्ट करें।

<LessonImages src="smart-house-course/lesson-4-b-3.gif" alt="tutorial" imageClasses="mb"/>

</li>

<li>

एसएसएच के माध्यम से रास्पबेरी पाई से कनेक्ट करें।

<LessonCodeWrapper language="bash" noLines>
ssh ubuntu@192.168.xxx.xxx
</LessonCodeWrapper>

</li>

<li>

फर्मवेयर के साथ रिपॉजिटरी क्लोन करें:

<LessonCodeWrapper language="bash" codeClass="big-code" noLines>
git clone https://github.com/airalab/robonomics-hass-utils.git
</LessonCodeWrapper>
</li>

<li>

SLS गेटवे को फ्लैश करने के लिए आपको <code>क्लियर</code> और <code>फ्लैश_16एमबी</code> स्क्रिप्ट चलाने की आवश्यकता है:

<LessonCodeWrapper language="bash" noLines>
cd robonomics-hass-utils/esp_firmware/linux
</LessonCodeWrapper>

<LessonCodeWrapper language="bash" noLines>
sudo chmod +x Clear.sh
</LessonCodeWrapper>

<LessonCodeWrapper language="bash" noLines>
sudo chmod +x Flash_16mb.sh
</LessonCodeWrapper>

<LessonCodeWrapper language="bash" noLines>
./Clear.sh
</LessonCodeWrapper>

<LessonCodeWrapper language="bash" noLines>
./Flash_16mb.sh
</LessonCodeWrapper>
</li>

<li class="no-bullet">

\- **समस्या निवारण**

यदि आप गेटवे फर्मवेयर को अपडेट करने में समस्या आ रही है, तो आपको अतिरिक्त कदम उठाने की आवश्यकता है:

<List>

<li>

सुनिश्चित करें कि पाईसीरियल मॉड्यूल स्थापित है:

<LessonCodeWrapper language="bash" noLines>
pip install pyserial
</LessonCodeWrapper>

</li>

<li>

अपने उपयोगकर्ता को यूएसबी पोर्ट का उपयोग करने के लिए अधिकार दें:

<LessonCodeWrapper language="bash" noLines>
sudo usermod -a -G dialout $USER
</LessonCodeWrapper>

</li>

<li>

कुछ मामलों में, स्क्रिप्ट में फर्मवेयर को अपडेट करने के लिए बैंडविड्थ सेटिंग बदलने की आवश्यकता होती है। नैनो संपादक के साथ <code>फ्लैश_16एमबी.श</code> स्क्रिप्ट खोलें और बॉड पैरामीटर को <code>921600</code> से छोटे मान (उदाहरण के लिए, <code>115200</code>) पर बदलें।
</li>
</List>
</li>

<li class="no-bullet">

\- **अतिरक्त**

हम अन्य ऑपरेटिंग सिस्टम (macOS और Windows) का उपयोग करके फर्मवेयर को अपडेट करने के लिए विकल्प भी प्रदान करते हैं। आपको एक फ़ोल्डर में संबंधित स्क्रिप्ट्स मिलेंगे, जिसका नाम आपके ओएस पर निर्भर करता है।

</li>
</List>
</li>

<li>

गेटवे सेटअप करना

<List>

<li>

गेटवे के पीठ की स्विच को उनकी नई स्थिति में सेट करें। स्विच <code>5</code> (RX Zigbee से ESP) और <code>6</code> (TX Zigbee से ESP) <code>ON</code> स्थिति में होना चाहिए, बाकी <code>OFF</code> होने चाहिए।


<LessonImages src="smart-house-course/lesson-4-b-4.gif" alt="tutorial" imageClasses="mb"/>

</li>

<li>

टाइप-सी पावर केबल कनेक्ट करें। केंद्र में इंडिकेटर लाइट हरा होना चाहिए।

</li>

<li>

पहली बार स्टार्टअप पर, गेटवे Wi-Fi को SSID <code>zgw****</code> के साथ साझा करना शुरू करेगा। इस नेटवर्क से कनेक्ट करें। ध्यान दें कि सिग्नल काफी कमजोर हो सकता है, इसलिए अपने कंप्यूटर के पास SLS गेटवे रखना बेहतर है।

यदि कनेक्शन सफल है, तो वेब इंटरफेस खुलेगा (या आप इसे 192.168.1.1 पते पर खोज सकते हैं)।

</li>

<li>

वाई-फाई पेज पर जाएं और अपने वाई-फाई क्रेडेंशियल डालें जिसके लिए उपयोगकर्ता / पास दर्ज करें और <code>Save</code> बटन दबाएं। इसके बाद <code>Reboot</code> बटन दबाएं। गेटवे पुनः आरंभ होगा और आपके वाई-फाई नेटवर्क से कनेक्ट होगा।

<LessonVideo  :videos="[{src: 'https://crustipfs.info/ipfs/QmSht6roENzrV6oqsQ1a5gp6GVCz54EDZdPAP8XVh9SCwH', type:'mp4'}]" />

</li>

<li>

वेब इंटरफ़ेस तक पहुंचने के लिए एसएलएस गेटवे का स्थानीय आईपी ढूंढें। इसके लिए आप अपने टर्मिनल या एनएमएपी में [Fing](https://www.fing.com/products) ऐप या <code>arp -a</code> का उपयोग कर सकते हैं:

<LessonCodeWrapper language="bash" noLines>
sudo nmap -sP 192.168.xxx.0/24
</LessonCodeWrapper>

कहाँ <code class="bold">xxx</code> आपका आईपी पता है लोकल नेटवर्क में। गेटवे नाम इस तरह दिखना चाहिए: <code>zgw****</code>। गेटवे का वेब इंटरफेस खोलें गेटवे आईपी को ब्राउज़र में पेस्ट करके।
</li>

<li>

<code>Setting</code> -> <code>Hardware</code> जाएं और सुनिश्चित करें कि सेटिंग्स छवि पर जैसे दिख रहे हैं। यदि आवश्यक हो तो सेटिंग्स सही करें और <code>Save</code> बटन पर क्लिक करें:

<LessonVideo  :videos="[{src: 'https://crustipfs.info/ipfs/QmeSksMxU9xkvvK7f81WDAYULiMFokK7P7KDVYEjv2MHjn', type:'mp4'}]" />

आवश्यक मानों के साथ तालिका:


| Field        	         | **Value**          |                                                                     	
|------------------------|--------------------|
| Zigbee module          | TI                 |
| Zigbee UART RX         | 22                 |
| Zigbee UART TX         | 23                 |
| Zigbee RST Pin         | 18                 |
| Zigbee BSL Pin         | 19                 |
| Button Mode            | 33 (pullUP - true) |
| Number addressable leds| 0                  |
| Led Red (or addr)      | 21                 |
| Led Green              | 5                  |
| Led Blue               | 27                 |
| I2C SDA                | 255                |
| I2C SCL                | 255                |

</li>

<li>

फिर गेटवे को रिबूट करें। <code>Actions</code> -> <code>Reboot system</code> का चयन करें उपरी कोने में। सुनिश्चित करें कि गेटवे CC2652P माइक्रोकंट्रोलर के साथ Zigbee जानकारी विंडो में ठीक काम कर रहा है। DeviceState <code>OK</code> होना चाहिए।

</li>

<li>

गेटवे को रिबूट करें। <code>Actions</code> -> <code>Reboot</code> सिस्टम उपरी कोने में करें।

</li>

<li>

होम असिस्टेंट में डिवाइसेस को स्वचालित रूप से जोड़ने को कॉन्फ़िगर करें। <code>Zigbee</code> -> <code>Config</code> जाएं फिर <code>Home Assistant MQTT Discovery</code> और <code>Clear States</code> का चयन करें। परिवर्तन सहेजें और फिर से SLS गेटवे को रिबूट करें।

<LessonVideo  :videos="[{src: 'https://crustipfs.info/ipfs/QmVZMB1xQeB6ZLfSR6aUrN6cRSF296s8CMJt7E2jBJ5MjZ', type:'mp4'}]" />

</li>

<li class="no-bullet">

\- **अतिरिक्त**:

यदि आपके घर में पहले से ही एक सक्रिय SLS गेटवे है, और अब आप एक और कॉन्फ़िगर कर रहे हैं, तो वे एक दूसरे के साथ टकराएंगे। इस समस्या को हल करने के लिए आपको नए उपकरण पर चैनल बदलने की आवश्यकता है।

इसे करे के लिए, <code>Zigbee</code> -> <code>Config</code> जाएं और चैनल को दूसरे को बदलें (जैसे कि चैनल 15)।

</li>

<li>

अपने डिवाइसेस को जोड़ने के लिए <code>Zigbee</code> -> <code>Join</code> जाएं। अपने सेंसर्स को पेयरिंग मोड में डालें, किसी डिवाइस को कनेक्ट मोड में स्विच करने का सबसे सामान्य तरीका उसके पावर बटन को पकड़ना है या उन्हें 5 बार ऑन/ऑफ करना है। <code>Enable Join</code> बटन दबाएं जिससे Zigbee डिवाइसेस की खोज शुरू हो। आप सक्रिय सेंसर्स देखेंगे।

</li>
</List>
</li>

<li>

SLS गेटवे को होम असिस्टेंट से कनेक्ट करना

<List>

<li>

आपको SLS गेटवे पर MQTT कॉन्फ़िगर करने की आवश्यकता है। अपने SLS गेटवे वेब इंटरफेस पर वापस आएं और <code>Settings</code> -> <code>Link</code> -> <code>MQTT Setup</code> जाएं।

<LessonVideo  :videos="[{src: 'https://crustipfs.info/ipfs/QmdNKDqwwy87VQEDDVsX5kpaDQm9wKKPEJUNJnhnjx6e5y', type:'mp4'}]" />

</li>

<li>

अपने ्रोकर पते को जोड़ें (होम असिस्टेंट के साथ रैस्पबेरी पाई का पता लोकल नेटवर्क में, आप इसे [Fing](https://www.fing.com/products) ऐप के साथ या अपने RPi पर <code>ip -a</code> कमांड का उपयोग करके पा सकते हैं), पोर्ट (डिफ़ॉल्ट 1883 है) अपने ब्रोकर उपयोगकर्ता नाम और पासवर्ड (जिसे आपने पहले बनाया है) और विषय का नाम (आप कोई भी चुन सकते हैं)। साथ ही, स्थानीय रैस्पबेरी पाई आईपी पता स्थिर होना चाहिए।

<code>Enable</code> और <code>Retain states</code> क्लिक करना न भूलें।

</li>

<li>

परिवर्तन सहेजें। अब उपकरण खुद होम असिस्टेंट में दिखाए जाएंगे।

</li>
</List>

</li>

<li>

उपकरण जोड़ें 

<List>

<li>

अपने उपकरणों को जोड़ने के लिए <code>Zigbee</code> -> <code>Join</code> पर जाएं। अपने सेंसर्स को पेयरिंग मोड में डालें, उपकरण को कनेक्ट मोड में स्विच करने का सबसे सामान्य तरीका है उसके पावर बटन को धारित करना या उन्हें 5 बार चालू/बंद करना।

<LessonImages src="smart-house-course/lesson-4-a-4.gif" alt="tutorial" imageClasses="mb"/>

<LessonVideo  :videos="[{src: 'https://crustipfs.info/ipfs/Qmdq3PBNY88QbYYqakwSLG2vn3mVUom3w3wsSWfTd1pzJA', type:'mp4'}]" />

</li>

<li>

जॉइन करने के लिए सक्षम जॉइन बटन दबाएं। आप सक्रिय सेंसर्स देखेंगे।

</li>

</List>
</li>

</List>