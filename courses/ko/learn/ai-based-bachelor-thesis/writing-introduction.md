---
title: "글쓰기: 소개"
description: 인공지능 도구를 활용하여 학사 논문 빠르게 시작하기
metaOptions: [배우다, 인공지능 도구를 활용하여 학사 논문 빠르게 시작하기]
defaultName: Quickstart Your Bachelor's Thesis with AI-powered Tools
---

<RoboAcademyText fWeight="500">
이 가이드에서는 학사 논문을 위한 소개를 쓸 것입니다.
</RoboAcademyText>

이 섹션은 쓰기가 가장 지루할 수 있는 부분 중 하나일 수 있습니다. 작업의 일반적인 비전을 계획하고 설명하는 것 외에도 일정량의 텍스트를 작성해야 합니다. 일반적으로 학생들은 이 공간을 무엇이든 채우려고 하며, 결과적으로 이 섹션이 단어 샐러드처럼 보일 수 있습니다. 이것이 바로 AI 어시스턴트가 잘 다룰 수 있는 문제입니다.

AI 서비스 테스트 중에 한 가지 흥미로운 관찰은 AI가 필요 이상으로 작업을 수행하려고 하지 않는다는 것입니다. 솔직히 말해서, 서비스는 거의 "게으르게" 작업을 수행하며 요청에 명시된 범위만큼만 작업을 수행합니다. 예를 들어, 텍스트 단락의 소스를 찾도록 요청하면, AI는 1-3개의 소스를 찾아줍니다. 따라서 요청을 작성할 때는 반환할 결과의 정확한 수를 지정하는 것이 가장 좋습니다.

## Auto-GPT를 사용하여 소개 쓰기

### 에이전트 생성

다음 설명과 목표를 가진 에이전트를 생성할 것입니다:

<RoboAcademyTerminal title="Auto-GPT Terminal">

**Name your AI:** Bachelor-AI

**Describe your AI's role:** an AI that helps bachelors write their bachelor's thesis

**Enter up to 5 goals for your AI:**

*Goal 1:* Remember the context about the bachelor's thesis: "A bachelor is going to get Bachelor of Science in Computer Science and Engineering. The bachelor completed an online course called "Smart Home Sovereign". In this course, the bachelor went through all the steps necessary to build a sovereign smart home, the main advantage of which is the security / privacy of user data. During the course, The bachelor set up an IoT hub on a Raspberry Pi and connected smart devices (such as a temperature/humidity sensor, a door sensor, a smart bulb, a motion sensor, etc.) to it via a 지그비 어댑터 using the MQTT protocol. The IoT hub is powered by Home Assistant software. Next, the bachelor connected the hub to a decentralized cloud, based on Polkadot web3 technology. This is necessary to securely transfer device data to the network without the need for a centralized cloud service provider. This allows to securely manage the home remotely"

*Goal 2:* Write an 소개duction part for this thesis in 500 words. It should contain: background and motivation; some context about web3 technology, what it is, why it should be used in smart home; research questions and objectives; significance of the work.

*Goal 3:* Save 소개duction text in file called "소개duction.txt".

</RoboAcademyTerminal>

첫 번째 목표로, 에이전트에게 논문의 맥을 기억하도록 요청했습니다. 또한 소개 섹션의 길이를 지정하고, 논문 계획에서 가져온 특정 포인트를 포함하도록 요청했으며, 텍스트를 .txt 파일에 저장하도록 요청했습니다.

### 출력 받기

에이전트 출력 (줄임 버전):

<RoboAcademyTerminal title="AutoGPT">

**THOUGHTS:**  For the next command, we can start with some background research to get more information about web3 technology and smart homes.

**REASONING:**  Gathering more information about web3 technology and smart homes will help us to write an informative introduction.

**PLAN:** 
<br/>&mdash;  Use the 'google' command to search for articles related to 'web3 technology and smart homes'
<br/>&mdash;  Skim the articles and websites listed
<br/>&mdash;  Use the 'browse_website' command and navigate to relevant websites to collect more information
<br/>&mdash;  Take notes of important points
<br/>&mdash;  Summarize findings

**CRITICISM:**  We should keep in mind the word limit for the introduction while researching.

**NEXT ACTION:  COMMAND = google ARGUMENTS = {'input': 'web3 technology and smart homes'}

**SYSTEM:**  Command google returned: ['https://cointelegraph.com/news/unique-web3-tech-primed-to-democratize-internet-of-things-industry', 'https://blog.aira.life/smart-home-based-on-web3-technologies-e378adfffb6a?source=publication_recirc-----d59e3007e78f----4----------------------------', 'https://www.ledgerinsights.com/bosch-fetch-ai-blockchain-web3-foundation/', 'https://www.forbes.com/sites/nataliakarayaneva/2022/04/16/click-click-close-how-web3-is-re-engineering-real-estate/', 'https://academy.binance.com/en/articles/the-evolution-of-the-internet-web-3-0-explained', 'https://dribbble.com/shots/20091453-Artificial-intelligence-robotics-smart-home-technology-web3-app', 'https://ieeexplore.ieee.org/document/8589489', 'https://www.ces.tech/topics/topics/smart-home']

...

**THOUGHTS:**  Our draft summary has very few words and is within the word limit. We can use this information for our introduction and expand on the summary to create the final draft. We can use the 'write_to_file' command to write the final draft to the 소개duction file.

**REASONING:**  We have counted the words in the introductory draft and confirmed that it is within the word limit. Now we can expand the draft summary to create the final draft of the introduction and write it to the 소개duction file.

**PLAN:**

<br/>&mdash;  Expand the drafted summary to create the final draft
<br/>&mdash;  Save the final draft of the introduction to 소개duction.txt using the 'write_to_file' command.

**CRITICISM:**  None

**NEXT ACTION:**  COMMAND = write_to_file ARGUMENTS = {'file': 'Introduction.txt', 'text': 'Introduction:\\n\\n The rise of smart home technology has led to a proliferation of internet-connected devices that can automate and optimize many aspects of our daily lives. A smart home system consists of a network of interconnected devices that can sense, communicate, and act on various environmental parameters such as temperature, humidity, motion, light, and sound. These devices can be controlled remotely or operate autonomously based on predefined rules and algorithms. \\n\\nHowever, smart home systems also present significant challenges and risks in terms of data privacy and security. Most smart home devices rely on centralized cloud platforms to store and process the data they collect from users' homes, which exposes users to potential data breaches, unauthorized access, surveillance, manipulation, or misuse by third parties such as hackers, service providers, governments, or advertisers. Furthermore, users often have limited control and ownership over their data, as they are required to agree to the terms and conditions of the cloud providers, which may not respect their preferences or rights. \\n\\nWeb3 technology refers to a suite of decentralized technologies that use blockchain to enable secure, transparent, and immutable transactions and records without intermediaries or central authorities. This allows for the creation of trustless, compromise-resistant IoT networks, and supports the creation of decentralized applications (dapps) that run on top of the blockchain. This enables users to transact in a secure and decentralized manner. \\n\\nThe main goal of this bachelor's thesis is to design a smart home system that is both secure and private. This system will use web3 technologies to create a decentralized, sovereign ecosystem. To achieve this goal, this work will explore the use of a Raspberry Pi as an IoT hub, connected to various smart home devices using the MQTT protocol. Then, a decentralized cloud based on Polkadot web3 technology will be integrated into the IoT system. This will enable secure and private data transfer between the smart home devices. Finally, the privacy and security implications of this setup will be evaluated and compared to traditional smart home setups that rely on centralized cloud vendors. \\n\\nThe significance of this study lies in its exploration of the use of Web3 technologies to design a secure and private smart home system. This work identifies the potential benefits and challenges of using Web3 technologies in smart homes. By examining these issues, this study contributes to the development of guidelines for the use of these technologies in IoT environments.'}

**SYSTEM:**  Command write_to_file returned: File written to successfully.

</RoboAcademyTerminal>

에이전트 로그에 따르면, 텍스트를 쓰기 전에 정보를 찾는 데 시간을 소비했습니다. 게다가, 에이전트는 소개를 점진적으로 만들어가며 단어 제한을 충족시키기 위해 텍스트를 추가했습니다.

### 출력 개선

전반적으로, AI는 소개를 기반으로 사용할 만큼 작업을 잘 수행했습니다. 또한 **Notion AI**에 텍스트를 입력하여 (`글쓰기 개선` 또는 `어조 변경` 도구 사용) 더 개선할 수도 있습니다.

<RoboAcademyText>
일반적으로, 소개 섹션에는 이미 관련 작품의 소스를 추가해야 하지만, 소스를 검색하고 분석하기 전에 다음 가이드 — 문헌 검토를 먼저 살펴보는 것이 좋습니다.
</RoboAcademyText>