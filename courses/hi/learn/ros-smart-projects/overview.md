---
title: स्मार्ट स्पेस के लिए आरओएस-आधारित परियोजनाएं
lastUpdate: Thu May 04 2023 12:53:19 GMT+0400 (Samara Standard Time)
description: स्मार्ट स्पेस के लिए आरओएस-आधारित परियोजनाएं
metaOptions: [सीखें]
defaultName: ROS-based projects for smart spaces
---

अपने 15 वर्षों के विकास के दौरान, रोबोट ऑपरेटिंग सिस्टम फ्रेमवर्क को दर्जनों [विभिन्न रोबोटिक उपकरणों](https://robots.ros.org/) के साथ एकीकृत किया गया था, और समुदाय द्वारा विकसित अल्गोरिदम और उपकरणों के अधिक पैकेज भी हैं। सच कहा जाए, अब इतने सारे परियोजनाएं हैं, और उनके रिपॉजिटरीज की विवरण शैली की अव्यवस्था इतनी बढ़ गई है कि विशेष विषय विषय पर केंद्रित परियोजनाएं खोजना वर्तमान में काफी समस्यात्मक है। 

यहाँ, आपको घर या कार्यालय वातानुकूलन के लिए उपयोग के लिए निर्मित रोबोट और आईओटी उपकरणों के लिए समर्पित आरओएस-आधारित परियोजनाओं की एक मामूली सूची मिलेगी। यह विषय एक है रोबोनॉमिक्स प्लेटफॉर्म के स्तंभों में से एक। हमारा लक्ष्य यह है कि हम इन परियोजनाओं को रोबोनॉमिक्स के साथ एकत्रित करने का प्रयास करें, तकनीकी एकीकरण दृष्टिकोण से और इन उपकरणों के रोबोट अर्थव्यवस्था में एक रोचक अनुप्रयोग के दृष्टिकोण से। विचारों और प्रेरणा के लिए इस सूची का उपयोग करने में मुक्त महसूस करें।

आप हमारे [सीखें खंड](/learn) में रोबोनॉमिक्स के साथ एकीकृत आरओएस-परियोजनाओं के कुछ उदाहरण देख सकते हैं।

<!-- As of right now (**April 2021**), Robonomics is oriented towards ROS **Melodic** and **Noetic** versions. Older versions can also work, but there may be additional integration work needed. In the future, support for ROS version 2 will be added. -->

आरओएस रिपॉजिटरीज और पैकेजों की खोज के लिए मुख्य संसाधन [यहाँ](https://index.ros.org/) तक पहुंचा जा सकता है।

## सिमुलेशन

अपना ध्यान केवल उपकरणों पर केंद्रित करने से पहले, यह याद रखने योग्य है कि बड़ी मात्रा में आरओएस परियोजनाओं के लिए, सिमुलेशन में उनका परीक्षण करने का विकल्प मौजूद है। आरओएस के तहत विभिन्न रोबोटों के 3डी मॉडलिंग के लिए सबसे लोकप्रिय उपकरण [Gazebo](http://gazebosim.org/) सिम्युलेटर और इसका ऑफशूट प्रोजेक्ट, [Ignition](https://index.ros.org/r/ros_ign/). दोनों सिमुलेटर विभिन्न कठिन इनडोर और आउटडोर वातावरणों में उपकरणों को मॉडल करने, मॉडल और वातावरण को बदलने, वास्तविक डिवाइस पर जाने से पहले नियंत्रण एल्गोरिदम का परीक्षण करने और डीबग करने की अनुमति देते हैं। इसके अलावा, यह प्रशिक्षण और उन स्थितियों के लिए एक उत्कृष्ट उपकरण है जब कोई वास्तविक उपकरण अनुपस्थित होता है।

समग्र रूप से, यह रोबोनॉमिक्स को किसी भी खर्च के बिना आरओएस उपकरण के साथ एकीकरण करने के लिए सबसे अच्छा विकल्पों में से एक है। एक वास्तविक परिदृश्य केवल हल्की सी कोड संशोधन की आवश्यकता होगी। गजेबो के लिए, रोबोनॉमिक्स के पास दो भागों से बना एक विस्तृत गाइड है जो [सेटिंग्स](https://wiki.robonomics.network/docs/en/connect-any-ros-compatible-robot-under-robonomics-parachain-control-1/) और [एकीकरण](https://wiki.robonomics.network/docs/en/connect-any-ros-compatible-robot-under-robonomics-parachain-control-2/) (उड़ान का उदाहरण के रूप में) को कवर करता है। मुख्य चुनौती एक तैयार मॉडल (उदाहरण के लिए, [यहाँ](https://github.com/osrf/gazebo_models)) का खोजना है या गजेबो के लिए अपना मॉडल बनाने की कोशिश करना है ज सिम्युलेटर्स के लिए विकसित [एसडीफॉर्मेट](http://sdformat.org/) का उपयोग करता है। 

## सिंग-बोर्ड कंप्यूटर और अन्य बोर्ड

ऐसे बोर्ड अन्य उपकरणों को आरओएस से कनेक्ट करने के लिए एक मूल घटक के रूप में काम करते हैं, मुख्य रूप से सेंसर्स और रिकॉर्डिंग डिवाइसेस (ऑडियो, फोटो, और वीडियो रिकॉर्डर्स, कैमरे, तापमान, दबाव, और पदार्थ संघटन सेंसर्स) को कनेक्ट करने के लिए क्योंकि एक स्मार्ट स्पेस की अवधारणा ढालने का अर्थ है कि इंफ्रास्ट्रक्चर वस्तुओं का एक [डिजिटल ट्विन](https://gateway.pinata.cloud/ipfs/QmNNdLG3vuTsJtZtNByWaDTKRYPcBZSZcsJ1FY6rTYCixQ/Robonomics_keypoint_March_2021.pdf) बनाया जाए। इसके अलावा, बोर्ड एक रोबोटिक मोबाइल उपकरण निर्माण के लिए मुख्य कंप्यूटिंग उपकरण और नियंत्रक के रूप मं काम कर सकते हैं। नीचे एक सूची प्रस्तुत की गई है जो बोर्ड्स को आरओएस का समर्थन करती हैं:

| Name and link                                                                                         |                                    Description                                  | ROS version | Last update |
|:-----------------------------------------------------------------------------------------------------:|---------------------------------------------------------------------------------|:-----------:|:-----------:|
|  [Raspberry Pi](http://wiki.ros.org/ROSberryPi/Installing%20ROS%20Melodic%20on%20the%20Raspberry%20Pi)| single board computer; RaspPi versions 2, 3 and 4 are available                 |   melodic   |     2020    |
|    [Arduino](http://wiki.ros.org/rosserial_arduino)                                                   | single board computer                                                           |    noetic   |     2021    |
|    [Phidgets](http://wiki.ros.org/phidgets)                                                           | sets of boards, various sensors and devices: Ph sensor, LED, RFID, motor control|    noetic   |     2020    |
|   [Sense HAT](https://wiki.ros.org/sensehat_ros)                                                      | shield for RaspPi with a set of sensors and LED                                 |    noetic   |     2020    |
|     [Navio2](https://navio2.emlid.com/)                                                               | autopliot shield for RaspPi 2,3,4                                               |    noetic   |     2020    |
|     [OpenCR](http://wiki.ros.org/opencr)                                                              | robot controller                                                                |    noetic   |     2021    |

<br/>

## स्मार्ट होम डिवाइस और घरेलू रोबोट

यहाँ पेश किए गए ROS डिवाइस हैं जिनका प्रारंभिक उपयोग स्मार्ट होम या कार्यालय के लिए था। सूची विभिन्न है, वैक्यूम क्लीनर और रोबोटिक सहायता से होम कंट्रोल सिस्टम तक।

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

## मोबाइल प्लेटफॉर्म और मैनिपुलेटर

पहले और सबसे महत्वपूर्ण, ROS को मोबाइल रोबोटिक्स का समर्थन करने के लिए जाना जाता है, ड्रोन से औद्योगिक मैनिपुलेटर तक, जिनके लिए कई पैकेज बनाए गए थे जो समकालिक स्थानांकन और मैपिंग ([SLAM](http://wiki.ros.org/rtabmap_ros)), किनेमेटिक्स के सीधे और उल्टे कार्य को हल करते हैं, [यात्रा नियोजन](https://moveit.ros.org/), और इत्यादि। मोबाइल रोबोिक्स धीरे-धीरे दिनचर्या में प्रवेश कर रहे हैं, इसलिए यह निश्चित रूप से रोज-रोज के जीवन में मौजूदा ROS-रोबोट्स का परीक्षण करना दिलचस्प है। ROS पर आधारित मोबाइल प्लेटफॉर्म की सामान्य सूची बहुत बड़ी है, इसलिए यहाँ हमने उन्हें चुना है जो एक घर या कार्यालय स्थान में उपयोग करने में संभावित आसान हों। 

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