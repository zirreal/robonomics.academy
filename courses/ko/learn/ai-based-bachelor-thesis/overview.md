---
title: 개요
description: 인공지능 도구를 활용하여 학사 논문 빠르게 시작하기
metaOptions: [배우다, 인공지능 도구를 활용하여 학사 논문 빠르게 시작하기]
defaultName: Quickstart Your Bachelor's Thesis with AI-powered Tools
---

<RoboAcademyText fWeight="500">
그렇게 두려워했던 일이 일어났습니다.
</RoboAcademyText>

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmW6qohyJvUF2c3EwhVWZXghArAZQ6KkBsbqT41QRgJRAh', type: 'webm'}]" />

당신은 방대한 텍스트 작업을 제출해야 하고 마감 기한이 매우 가깝습니다. 아니면 상황이 다를 수도 있습니다: 제출 기한이 그리 무서운 것은 아니지만, 형식적이고 기술적인 내용을 포함한 대규모 자료를 작성하는 것이 당신을 겁내고 장기간 작업을 미루게 만듭니다. 어쨌든, 당신은 상당히 긴, 단조롭고 종종 매우 지루한 과정을 거쳐야 하며 이는 당신의 동기부여를 어둡게 만듭니다. 아마도 창의적이고 발전적인 작업에 더 많은 시간을 할애하고 싶을 것입니다만, 불행히도 일부 직업과 활동은 그렇게 구조화되어 있습니다.

## 인공지능 진입

우리 모두에게 다행히도 역사를 통해 루틴 작업을 쉽게 만들어주는 진전이 텍스트 작성 분야에 도달했습니다. 이번에는 인공지능의 발전으로 가능해졌으며, 특히 생성 언어 모델이라고 하는 인공지능의 진보 덕분에 가능해졌습니다. 이 모델은 요청을 이해하고 해결하며 대화 형식으로 더나은 또는 그다지 미 있는 답변을 제공할 수 있는 능력을 갖추고 있습니다. Robonomics에서는 의사소통과 생명체 및 기계 사이의 상호작용을 자동화 수준을 높일 수 있는 것을 무시할 수 없었습니다 (또한 우리의 일상 작업을 쉽게 만들어줄 수도 있습니다!).

최신 GPT 모델은 그들의 능력으로 인상을 주지만, 그들을 올바르게 사용하는 방법과, 무엇보다도 얼마나 의지할 수 있는지에 대한 질문이 제기됩니다. 이러한 기술은 프롬프트 엔지니어링이라고 불리며, 이를 위해 현재의 생성적 인공지능의 가능성에 대한 기본적인 이해로 이끌어줄 이 가이드를 제시합니다.

이 가이드에서는 우리의 지식 분야를 기반으로 한 간단한 학사 논문을 작성해보려고 합니다. "학사" 및 학사가 통과한 시작 자료를 기반으로 합니다. 우리는 확실히 최소한의 학술적 규칙을 준수하려고 노력할 것이지만, 이 가이드를 위한 계획된 시간인 두 주는 학사 논문을 성공적으로 고려하기에 충분하지 않을 것입니다 (비록 현실은 때로는 그렇지 않음을 증명하기도 합니다). 

그럼에도 불구하고, 이 가이드는 이미 인공지능이 가장 일상적이고 시간 소모적인 프로스를 어떻게 완화시킬 수 있는지 이해하는 좋은 시작점으로 간주될 수 있습니다. 덧붙여 말하자면, 학사 논문 작업에 제한할 필요는 없습니다: 이 가이드는 IMRaD 표준 (소개, 방법, 결과, 토론)을 따르는 모든 텍스트 작업에 유용할 것입니다: 저널 및 학회 발표, 박사 논문, 기술 보고서, 매뉴얼 등.

<RoboAcademyNote title="DISCLAIMER" type="warning">
  이 가이드는 학사 논문을 최상의 성적으로 성공적으로 제출하는 것을 보장하거나 목표로 하지 않습니다.
</RoboAcademyNote>

## 사용된 도구

가이드에서 사용된 인공지능 서비스 중 일부:

**[ChatGPT](https://chat.openai.com/chat)** — OpenAI가 만든 Generative Pre-trained Transformer 언어 모델 (버전 3.5 및 4)을 기반으로 한 챗봇. 사용자와의 대화 형식으로 작동하며, 사용자의 요청에 답변하고 간단한 질문부터 시를 작성하고 사용자 코드를 디버깅하는 등 다양한 요청에 대응합니다. 그 지식은 2021년 9월까지로 한정되어 있으며 인터넷에 액세스할 수 없습니다. 기본 사용은 무료이지만 전화번호로 등록이 필요합니다 (일부 국가에서는 사용 불가능할 수 있음). 더 강력한 기능과 Wolfram 또는 Slack에 액세스할 수 있는 플러그인 추가 기능이 있는 월 $20의 구독 옵션이 있습니다.

**[Bing Chat](http://www.bing.com)** — Microsoft의 Bing 검색 서비스에 통합된 GPT-4를 기반으로 한 챗봇. 액세스를 위해 Microsoft 계정이 필요합니다. 기본적으로 ChatGPT와 동일한 기능을 갖추고 있지만 인터넷 액세스가 가능하여 더 강력합니다.

**[Auto-GPT](https://news.agpt.co/)** — 사용자가 설정한 작업을 해결하는 자율적인 AI 에이전트를 생성하는 데 GPT-4를 사용하는 소프트웨어. 에이전트는 인터넷, 장기 기억 및 정보를 파일로 저장할 수 있는 능력을 갖추고 있어 복잡한 일련의 작업을 수행할 수 있습니다. 사용하려면 OpenAI 계정이 필요하며 유료 구독이 있는 것이 좋습니다. 설치 지침은 [여기에서](https://docs.agpt.co/setup/) 확인할 수 있습니다.

**[노션 AI](https://www.notion.so/product/ai)** — 동명의 지식 관리 소프트웨어에 통합된 AI 어시스턴트. 제한된 무료 액세스가 있으며, 월 $10의 구독 비용이 발생합니다. 이미 준비된 텍스트를 처리하고 개선하는 데 편리하며 이를 위한 미리 설치된 기능이 있습니다.

추가로 다음 서비스가 필요합니다:

**[Overleaf](http://www.overleaf.com)** — 텍스트 서식을 지정하는 편리한 온라인 LaTeX 편집기. 논 및 기사부터 프레젠테이션까지 모든 유형의 작업을 위한 템플릿 세트가 있습니다. 우리는 [MIT 논문 템플릿](https://www.overleaf.com/latex/templates/mit-thesis-template/ytphktgwpktc)을 사용할 것입니다.

**[Google Scholar](http://scholar.google.com)** — 과학 출판물을 검색하는 검색 엔진입니다. AI 서비스가 제안한 소스를 확인하는 데 사용됩니다.

## AI 도구 사용 방법

### AI 챗봇 (ChatGPT, Bing)

AI 챗봇 (ChatGPT, Bing)은 특히 복잡한 접근 방식이 필요하지 않습니다: 적절한 요청을 형식화하고 챗봇에게 보내기만 하면 됩니다 (메시지 당 문자 수에 제한이 있지만 요청 텍스트 전체가 전송될 때까지 챗봇을 기다리도록 할 수 있습니다).

### 노션 AI

노션 AI의 경우, 어떤 페이지에 텍스트 블록을 삽입하고 AI 어시스턴트에게 요청을 하는 컨텍스트 메뉴를 호출하면 됩니다.

### Auto-GPT

Auto-GPT는 사용자가 다음을 시작하기 전에 명시해야 하는 다른 접근 방식이 필요합니다:

- AI 어시스턴트의 이름
- AI 어시스턴트의 역할
- AI 어시스턴트가 완료해야 하는 최대 5가지 연속적인 목표

이후 Auto-GPT는 사용자에게 현재 반복에서 구현하려는 "생각" 및 수행된 작업을 모두 표시할 에이전트를 시작합니다.

- `THOUGHTS` — 에이전트가 현재 반복에서 구현하려는 일반적인 아이디어
- `REASONING` — 에이전트가 이 아이디어를 선택한 이유
- `PLAN` — 이 아이디어를 달성하기 위한 구체적인 조치 (인터넷 검색, 문서 분석, 파일 작성 등)
- `CRITICISM` — 에이전트가 자신의 작업에 부과하는 특별한 조건 (예: "IEEE 저널의 고품질 참고 자료만 검색")

## 첫 단계

<RoboAcademyNote title="WARNING" type="warning">
  AI 도구는 여전히 개선 중이므로 얻은 결과를 항상 두 번 확인하십시오.
</RoboAcademyNote>

### 서비스에 컨텍스트 제공

최신 AI 서비스의 중요한 장점 중 하나는 한 세션 내에서 요청의 컨텍스트를 상당히 잘 기억한다는 것입니다. 따라서 학사 논문을 시작하려면 먼저 컨텍스트를 고안하고 서비스에 제공해야 합니다 ("전설") 그리고 그것을 서비스에 공급하십시오.

작업의 자료로 Robonomics Academy의 ["Robonomics 및 홈 어시스턴트를 사용한 주권 스마트 홈"](/learn/smart-home-course/overview) 과정이 시작점으로 채택되었습니다. 결과적으로 다음 컨텍스트가 생성되었습니다:

<RoboAcademyDialog>

I am a student of the Department of IoT Engineering and Web3 Science. 

I am going to get Bachelor of Science in Computer Science and Engineering.

I completed an online course called "Smart Home Sovereign". In this course, I went through all the steps necessary to build my own sovereign smart home, the main advantage of which is the security / privacy of user data.
During the course, I set up an IoT hub on a Raspberry Pi and connected smart devices (such as a temperature/humidity sensor, a door sensor, a smart bulb, a motion sensor, etc.) to it via a 지그비 어댑터 using the MQTT protocol. The IoT hub is powered by Home Assistant software. Next, I connected the hub to a decentralized cloud, based on Polkadot web3 technology. This is necessary to securely transfer device data to the network without the need for a centralized cloud service provider. This allows me to securely manage my home remotely.

Now I want to take this course as a basis and write a bachelor's thesis with your help.

</RoboAcademyDialog>

AI 챗봇의 전형적인 반응은 이 컨텍스트를 명확히 하고 서비스가 어떻게 도움을 줄 수 있는지 제안하는 것입니다.

### 제안된 주제 중에서 선택

다음 단계(학사 상황에 대한 전형적인 단계)는 논문의 주제를 선택하는 것입니다. 여기서 `논 주제를 제안하십시오` 링크를 만들면 충분합니다. ChatGPT와 Bing Chat은 다음을 제안했습니다:

<RoboAcademyDialog>

"Designing a Secure and Private Smart Home System using Web3 Technologies" — This topic could involve examining the steps you took to build your sovereign smart home and exploring the security and privacy benefits of using IoT and Web3 technologies.

"Comparing Centralized and Decentralized Approaches to Smart Home Data Management" — This topic could involve comparing and contrasting the benefits and drawbacks of using centralized cloud vendors versus decentralized cloud technologies like Polkadot for managing smart home data.

"Developing a Smart Contract-based Framework for Managing Smart Home Devices" — This topic could involve exploring the use of smart contracts to manage smart home devices and develop a secure and efficient framework for managing them.

"Investigating the Security and Privacy Risks of Smart Home Systems" — This topic could involve examining the potential risks and vulnerabilities of smart home systems, including issues related to data privacy, cybersecurity, and physical safety.

"Exploring the Role of Blockchain in Smart Home Data Management" — This topic could involve examining how blockchain technology could be used to manage smart home data and ensure the security and privacy of user data.

"Investigating the Future of Smart Home Technologies and their Impact on Society" — This topic could involve examining the potential social and economic impacts of smart home technologies, including issues related to privacy, security, and the digital divide.

</RoboAcademyDialog>

가이드로 **"Web3 기술을 사용한 안전하고 개인 정보 보호가 보장된 스마트 홈 시스템 설계"** 주제가 선택되었습니다.

### IMRaD 구조를 갖는 간단한 계획

이제 원칙적으로 IMRaD 구조를 따라 논문의 특정 섹션으로 진행할 수 있습니다. 그러나 학사 작업에 대한 보다 자세한 계획이 필요합니다. 이것도 AI 서비스에 요청할 수 있습니다. ChatGPT는 추가 조건 없이 다음 계획을 제안했습니다:


<RoboAcademyDialog>

<ChatGPT/>

1. 소개duction
    1. Background and motivation
    2. Research questions and objectives
    3. Significance of the study
2. Literature Review
    1. 개요 of smart home technology and its security and privacy issues
    2. 소개duction to web3 technology and its potential benefits for smart homes
    3. Existing research on using web3 technology for smart home security and privacy
3. Methodology
    1. Description of the smart home system design using web3 technology, including hardware and software components
    2. Implementation details and justification for design choices
    3. Evaluation plan for assessing the security and privacy of the system
4. Results and Analysis
    1. Evaluation of the implemented system with respect to security and privacy metrics
    2. Comparison with existing solutions and analysis of strengths and weaknesses
    3. Discussion of limitations and potential areas for improvement
5. Conclusion and Future Work
    1. Summary of the study's contributions and main findings
    2. Implications and significance of the results for the smart home industry and related fields
    3. Recommendations for future research and development
6. 참고

</RoboAcademyDialog>

<RoboAcademyText>
이 준비가 완료되면 이제 논문의 첫 번째 섹션인 소개로 넘어갈 수 있습니다.
</RoboAcademyText>
  

