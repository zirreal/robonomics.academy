---
title: सारांश
description: एआई-संचालित उपकरणों के साथ अपने बैचलर थीसिस को शीघ्र शुरू करें
metaOptions: [Learn, एआई-संचालित उपकरणों के साथ अपने बैचलर थीसिस को शीघ्र शुरू करें]
defaultName: Quickstart Your Bachelor's Thesis with AI-powered Tools
---

<RoboAcademyText fWeight="500">
तो, जो आपको डर था, वह हो गया।
</RoboAcademyText>

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmW6qohyJvUF2c3EwhVWZXghArAZQ6KkBsbqT41QRgJRAh', type: 'webm'}]" />

आपको एक बहुत बड़े पाठ कार्य को सबमिट करना है और आखिरी तारीख बहुत करीब है। या शायद स्थिति अलग हो सकती है: सबमिशन अंतिम तिथि इतनी डरावनी नहीं हो सकती, लेकिन बड़े सामग्री लिखना, विशेष रूप से औपचारिक, तकनीकी सामग्री के साथ, आपको घबराता है और आप कार्य को बहुत लंबे समय तक स्थगित करते हैं। एक तरह या दूसरे तरह, आपको एक काफी लंबा, एकरेतम और अक्सर बहुत उबाऊ प्रक्रिया से गुजरना होगा जो आपकी प्रेरणा को अंधेरे में डाल देता है। शायद आप अधिक समय सृजनात्मक और विकासात्मक कार्यों में देना चाहेंगे, लेकिन दुर्भा्य से, कुछ पेशेवर और गतिविधियाँ उसी तरह संरचित हैं।

## AI में प्रवेश

हम सभी के लिए भाग्यशाली रूप से, जो प्रगति हमारे इतिहास में हमारे रूटीन कार्यों को आसान बना रही है, वह पाठ लेखन क्षेत्र तक पहुंच गया है। इस बार यह संभव है क्योंकि कृत्रिम बुद्धिमत्ता में उन्नतियां, विशेष रूप से उत्पादक भाषा मॉडल, समझने और अनुरोधों को हल करने की क्षमता हैं और एक चैट प्रारूप में अधिक या कम अर्थपूर्ण उत्तर प्रदान करने की क्षमता हैं। Robonomics में, हम बस उस चीज को नजरअंदाज नहीं कर सकते थे जो संचार और जीवित और मशीन वस्तुओं के बीच संवाद और अंतर्क्रिया क स्तर को उच्च कर सकता था (और हमारे दैनिक कार्यों को भी आसान बना सकता था!)।

नवीनतम GPT मॉडल अपनी क्षमताओं से प्रभावित करते हैं, लेकिन सवाल उठता है कि उन्हें सही ढंग से कैसे उपयोग किया जा सकता है और, सबसे महत्वपूर्ण, उन पर कितना भरोसा किया जा सकता है। ऐसी कौशलताएँ प्रॉम्प्ट इंजीनियरिंग कहलाती हैं, और इस उद्देश्य के लिए, हम यह गाइड प्रस्तुत करते हैं, जो आपको वर्तमान उत्पादक कृत्रिम बुद्धिमत्ता की संभावनाओं की मूल समझ की ओर धकेलेगा।

इस गाइड में, हम एक सरल बैचलर थीसिस लिखने का प्रयास करेंगे, हमारे "बैचलर" के ज्ञान शाखा पर आधारि और जिस प्रारंभिक सामग्री को बैचलर ने पास किया है। हम निश्चित रूप से न्यूनतम शैक्षिक नियमों का पालन करने का प्रयास करेंगे, लेकिन दो सप्ताह (जो इस गाइड के लिए नियोजित समय है) निश्चित रूप से बैचलर थीसिस को सफल मानना उचित नहीं है (हालांकि वास्तविकता कभी-कभी इसका विपरीत साबित करती है)। 

फिर भी, इस गाइड को उन व्यावसायिक और समय-ग्राहक प्रक्रियाओं को समझने के लिए एक अच्छा आरंभ माना जा सकता है जिन्हें AI पहले से ही समान कर सकता है। वैसे, आपको बैचलर थीसिस कार्य से सीमित करने की आवश्यकता नहीं है: यह गाइड IMRaD मानक (परिचय, विधि, परिणाम, चर्च) का पालन करने वाले किसी भी पाठ कार्य के लिए उपयोगी होगा: जर्नल और सम्मेलन प्रकाशन, डॉक्टरेट थीसिस, तकनीकी रिपोर्ट, मैनुअल, आदि।

<RoboAcademyNote title="DISCLAIMER" type="warning">
  गाइड एक बैचलर थीसिस को शीर्ष ग्रेड के साथ सफल सबमिशन के लिए गारंटी और उद्देश्य नहीं है।
</RoboAcademyNote>

## उपयोग किए गए उपकरण

गाइड में उपयोग किए गए AI सेवाओं में से:

**[चैटीपीटी](https://chat.openai.com/chat)** — जनरेटिव प्री-ट्रेन्ड ट्रांसफार्मर भाषा मॉडल (संस्करण 3.5 और 4) पर आधारित एक चैटबॉट जो ओपनएआई द्वारा बनाया गया है। यह उपयोगकर्ता के साथ चैट प्रारूप में काम करता है, उनके अनुरोधों का उत्तर देता है जो साधारण सवालों से लेकर कविता रचना और उपयोगकर्ता कोड को डीबग करने जैसे विभिन्न हो सकते हैं। इसकी ज्ञान सितंबर 2021 तक सीमित है, क्योंकि इसे इंटरनेट तक पहुंच नहीं है। मूल उपयोग मुफ्त है, लेकिन फोन नंबर के साथ पंजीकरण की आवश्यकता है (कुछ देशों में उपलब्ध नहीं है)। इसमें एक सदस्यता विकल्प ($20 प्रति माह) है जिसमें अधिक शकतिशाली सुविधाएं और प्लगइन जोड़ने की क्षमता, जैसे Wolfram या Slack के लिए।

**[बिंग चैट](http://www.bing.com)** — माइक्रोसॉफ्ट के बिंग सर्च सेवा में एकीकृत GPT-4 पर आधारित एक चैटबॉट। पहुंच के लिए एक माइक्रोसॉफ्ट खाता आवश्यक है। मूल रूप से, इसकी उसी क्षमताएं हैं जैसे चैटजीपीटी, लेकिन इंटरनेट पहुंच के साथ, इसे अधिक शक्तिशाली बनाता है।

**[ऑटो-जीपीटी](https://news.agpt.co/)** — एक सॉफ्टवेयर जो उपयोगकर्ता द्वारा निर्धारित कार्य समाधान करने वाले स्वतंत्र एआई एजेंट बनाने के लिए GPT-4 का उपयोग करता है। एजेंट को इंटरनेट, लंबी समय तक की याद, और जानकारी को फ़ाइलों में सहेजने की क्षमता है, जिससे यह जटिल क्रमों के कार्रवाई कर सकता है। इसका उपयोग करने के लिए, ओपनएआई पर एक खाता आवश्यक है, जिसे सर्वोत्तम रूप से एक भुगतान की सदस्यता के साथ किया जाए। स्थापना निर्देशिका [यहाँ उपलब्ध है](https://docs.agpt.co/setup/)।

**[नोशन एआई](https://www.notion.so/product/ai)** — एक एआई सहायक जो उपनामित ज्ञान प्रबंधन सॉफ्टवेयर में एकीकृत है। इसका सीमित मुफ्त पहुंच है, जबकि एक सदस्यता $10 प्रति माह की लागत है। यह पहले से तैयार पाठ को प्रसंस्करण और सुधारने के लिए सुविधाजनक है, और इस उद्देश्य के लिए पूर्व-स्थापित कार्यों के लिए पूर्व-स्थापित कार्यों हैं।

इसके अिरिक्त, हमें निम्नलिखित सेवाएं चाहिए:

**[ओवरलीफ](http://www.overleaf.com)** — पाठ का स्वरूपण करने के लिए सुविधाजनक ऑनलाइन लेटेक्स संपादक। यह किसी भी प्रकार के काम के लिए टेम्पलेट सेट है (थीसिस और लेख से प्रस्तुतियों तक)। हम [MIT थीसिस टेम्पलेट](https://www.overleaf.com/latex/templates/mit-thesis-template/ytphktgwpktc) का उपयोग करेंगे।

**[गूगल स्कॉलर](http://scholar.google.com)** — वैज्ञानिक प्रकाशनों के लिए एक खोज इंजन। यह एआई सेवाओं द्वारा सुझाए गए स्रोतों की पुष्टि के लिए उपयोग किया जाता है।

## AI उपकरण का उपयोग कैसे करें

### AI चैटबॉट्स (ChatGPT, Bing)

AI चैटबॉट्स (ChatGPT, Bing) को विशेष रूप से जटिल दृष्टिकोण की आवश्यकता नहीं है: आपको केवल उचित अनुरोध का स्वरूप सूचित करना है और इसे चैटबॉट को भेजना है (प्रति संदेश अक्षरों की संख्या पर केवल एक सीमा है, लेकिन आप चैटबॉट से अनुरोध कर सकते हैं कि वह पूरे अनुरोध का पाठ भेजने तक प्रतीक्षा करे।)

### Notion AI

Notion AI के लिए, किसी भी पृष्ठ पर एक पाठ ब्लॉक डालना पर्याप्त है और AI सहायक को अनुरोधों के साथ संदर्भ मेनू बुलाना है।

### Auto-GPT

Auto-GPT को एक विभिन्न दृष्टिकोण की आवश्यकता है, क्योंकि उपयोगकर्ता को निम्नलिखित शुर करने से पहले निर्दिष्ट करने की आवश्यकता है:

- AI सहायक का नाम
- AI सहायक की भूमिका
- AI सहायक द्वारा पूरा किए जाने वाले 5 लगातार लक्ष्य

इसके बाद, Auto-GPT एक एजेंट लॉन्च करेगा जो उपयोगकर्ता के लिए सभी "विचार" और क्रियाएँ प्रदर्शित करेगा, अर्थात:

- `विचार` — एक सामान्य विचार जो एजेंट वर्तमान अवतरण में लागू करना चाहता है
- `तर्क` — एजेंट ने इस विचार को क्यों चुना
- `योजना` — विचार को प्राप्त करने के लिए विशेष क्रियाएँ (इंटरनेट पर खोज करना, दस्तावेजों का विश्लेषण करना, फ़ाइल में लिखना इत्यादि)
- `आलोचना` — एजेंट अपनी क्रियाओं पर लगातार शर्तें लगाता है (उदाहरण के लिए, "केवल IEEE जर्नल से उच्च गुणवत्ता वाले संदर्भों की खोज करें")।

## पहले कदम

<RoboAcademyNote title="चेतावनी" type="warning">
  AI उपकरण अभी भी सुधारे जा रहे हैं, इसलिए आपको प्राप्त परिणामों की जांच दोबारा करनी चाहिए।
</RoboAcademyNote>

### सेवा को संदर्भ दें

नवीनतम AI सेवाओं के महत्वपूर्ण लाभों में से एक यह है कि वे एक सत्र के भीतर एक अनुरोध के संदर्भ को बहुत अच्छे से याद रखते हैं। इसलिए, बैचलर थीसिस शुरू करने के लिए पहली चीज यह है कि एक संदर्भ (एक "कथा") तैयार करें।") and feed it to the service.

काम के लिए सामग्री, Robonomics Academy पर Robonomics और होम असिस्टेंट के साथ ["सामराज्य स्मार्ट होम कोर्स"](/learn/smart-home-course/overview) को एक आरंभिक बिंदु के रूप में लिया गया था। इसके परिणामस्वरूप, निम्नलिखित संदर्भ बनाया गया था:

<RoboAcademyDialog>

I am a student of the Department of IoT Engineering and Web3 Science. 

I am going to get Bachelor of Science in Computer Science and Engineering.

I completed an online course called "Smart Home Sovereign". In this course, I went through all the steps necessary to build my own sovereign smart home, the main advantage of which is the security / privacy of user data.
During the course, I set up an IoT hub on a Raspberry Pi and connected smart devices (such as a temperature/humidity sensor, a door sensor, a smart bulb, a motion sensor, etc.) to it via a जिगबी एडाप्टर using the MQTT protocol. The IoT hub is powered by Home Assistant software. Next, I connected the hub to a decentralized cloud, based on Polkadot web3 technology. This is necessary to securely transfer device data to the network without the need for a centralized cloud service provider. This allows me to securely manage my home remotely.

Now I want to take this course as a basis and write a bachelor's thesis with your help.

</RoboAcademyDialog>

इस संदर्भ के लिए AI चैटबॉट की सामान्य प्रतिक्रिया यह होगी कि अनुरोध को स्पष्ट करने और सेवा कैसे सहायता कर सकती है इसका सुझाव देना।

### सुझाए गए में से एक विषय चुनें

अगला कदम (बैचलर की स्थिति के लिए सामान्य) थीसिस के लिए एक विषय चुनना है। यहाँ, एक अनुरोध लिंक `मेरी थीसिस के लिए प्रस्तावित N विषयों का प्रस्ताव दें` बनाना पर्याप्त है। ChatGPT और Bing Chat ने निम्नलिखित प्रस्तावित किया:

<RoboAcademyDialog>

"Designing a Secure and Private Smart Home System using Web3 Technologies" — This topic could involve examining the steps you took to build your sovereign smart home and exploring the security and privacy benefits of using IoT and Web3 technologies.

"Comparing Centralized and Decentralized Approaches to Smart Home Data Management" — This topic could involve comparing and contrasting the benefits and drawbacks of using centralized cloud vendors versus decentralized cloud technologies like Polkadot for managing smart home data.

"Developing a Smart Contract-based Framework for Managing Smart Home Devices" — This topic could involve exploring the use of smart contracts to manage smart home devices and develop a secure and efficient framework for managing them.

"Investigating the Security and Privacy Risks of Smart Home Systems" — This topic could involve examining the potential risks and vulnerabilities of smart home systems, including issues related to data privacy, cybersecurity, and physical safety.

"Exploring the Role of Blockchain in Smart Home Data Management" — This topic could involve examining how blockchain technology could be used to manage smart home data and ensure the security and privacy of user data.

"Investigating the Future of Smart Home Technologies and their Impact on Society" — This topic could involve examining the potential social and economic impacts of smart home technologies, including issues related to privacy, security, and the digital divide.

</RoboAcademyDialog>

गाइड के लिए **"Web3 तकनीकों का उपयोग करके एक सुरक्षित और निजी स्मार्ट होम सिस्टम डिज़ाइन करना"** विषय चुना गया।

### IMRaD संरचना के साथ सरल योजना

अगला, सिद्धांत में, हम थीसिस के विशेष खंडों की ओर बढ़ सकते हैं, IMRaD संरचना का पालन करते हुए। हालांकि, बैचलर काम के लिए एक अधिक विस्तृत योजना होना अच्छा होगा। इसे भी AI सेवा से अनुरोध किया जा सकता है। ChatGPT ने किसी भी अतिरिक्त शर्त के बिना निम्नलिखित योजना का सुझाव दिया:


<RoboAcademyDialog>

<ChatGPT/>

1. Introduction
    1. Background and motivation
    2. Research questions and objectives
    3. Significance of the study
2. Literature Review
    1. अवलोन of smart home technology and its security and privacy issues
    2. Introduction to web3 technology and its potential benefits for smart homes
    3. Existing research on using web3 technology for smart home security and privacy
3. Methodology
    1. Description of the smart home system design using web3 technology, including hardware and software components
    2. Implementation details and justification for design choices
    3. Evaluation plan for assessing the security and privacy of the system
4. परिणाम and Analysis
    1. Evaluation of the implemented system with respect to security and privacy metrics
    2. Comparison with existing solutions and analysis of strengths and weaknesses
    3. Discussion of limitations and potential areas for improvement
5. Conclusion and Future Work
    1. Summary of the study's contributions and main findings
    2. Implications and significance of the results for the smart home industry and related fields
    3. Recommendations for future research and development
6. संदर्भ

</RoboAcademyDialog>

<RoboAcademyText>
इस तैयारी के साथ पूरी होने पर, हम अब थीसिस के पहले खंड — परिचय में आगे बढ़ सकते हैं।
</RoboAcademyText>
  

