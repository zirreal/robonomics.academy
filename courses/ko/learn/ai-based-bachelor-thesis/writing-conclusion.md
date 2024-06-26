---
title: "쓰기: 결론"
description: 인공지능 도구를 활용하여 학사 논문 빠르게 시작하기
metaOptions: [배우다, 인공지능 도구를 활용하여 학사 논문 빠르게 시작하기]
defaultName: Quickstart Your Bachelor's Thesis with AI-powered Tools
---

<RoboAcademyText fWeight="500">
우리는 학사 논문의 마지막 섹션에 도달했습니다. 이제 결론을 쓰고 학술 작업에 AI 도구를 적용한 작은 연구를 요약할 시간입니다. 결국, 이 경험이 성공적이었습니까? 그리고 현대 AI 어시스턴트에서 아직 부족한 것은 무엇인가요?
</RoboAcademyText>

## 논문을 마무리하며

기본적으로, 우리는 이미 AI가 필요한 요청을 구성함으로써 자료를 요약하는 데 어떻게 도움이 될 수 있는지 알고 있습니다. 유일한 문제는 전체 소스 텍스트로 그것을 공급하는 것입니다. 긴 PDF 파일에 적절한 지원이 있을 때까지, 우리는 소스 텍스트를 조각으로 나누고 각각에 대한 요약을 요청한 후 조각들을 함께 보내야 합니다:

<RoboAcademyDialog>

Give me a summary for the following text in 500 words. 
</RoboAcademyDialog>

호기심에 따라, LaTeX에서 사용할 수 있도록 결과 텍스트를 서식화하도록 요청해보겠습니다. 이렇게 AI 어시스턴트가 이 작업을 처리하는 방법을 확인해보세요:

<RoboAcademyDialog>

Write a Conclusions section from the text below in 1000 words. Be sure to add summary of the thesis's contributions and main findings, implications and significance of the results for the smart home industry and related fields, recommendations for future research and development.

Take the resulting text and design it for LaTeX.
</RoboAcademyDialog>

결과:

<LessonCodeWrapper language="uml" noCopyIcon noLines codeClass="big-code">
    \documentclass{article}
    \usepackage{lipsum}
    \begin{document}
    \section*{Conclusion}
    This bachelor's thesis aimed to design a secure and private 
    smart home system using Web3 technologies, specifically leveraging 
    blockchain and decentralized technologies.
    ...
    \end{document}

</LessonCodeWrapper>

이제 우리는 일반적인 방식으로 초록을 작성하여 논문을 완성할 수 있습니다:

<RoboAcademyDialog>

Make an abstract for the bachelor's thesis based on this text in 100 words.
</RoboAcademyDialog>

## 결론 안내

원칙적으로, 우리의 작업은 완료되었습니다. 다음으로 다양한 도구를 사용하여 텍스트를 처리하고 문장을 개선하거나 일부 단락을 확장해볼 수 있습니다. 아래 링크에서 결과 PDF 파일을 찾을 수 있습니다:

https://cloudflare-ipfs.com/ipfs/Qme6rzPwiDGLLkUmWVLrCqgGMjcbqitYNcndznjNPb21E8

학사 논문이나 유사한 학술 자료를 준비하는 작업에 AI 도구의 적용 가능성에 대해 어떤 결론을 내릴 수 있을까요? 먼저 장점을 살펴보겠습니다:

1. AI는 일반화된 작업 설명을 처리할 수 있습니다. 계획을 수립하고 출판 섹션을 구조화하며 작업 방향을 제안하는 것은 모두 시작할 곳이 분명하지 않거나 아이디어가 부족할 때 심각하게 도움이 될 수 있습니다. 이 의미에서 AI 어시스턴트는 주요 아이디어를 제공할 '백업 뇌'가 될 수 있습니다. "주요 두뇌"가 아이디어를 제공할 것입니다.
2. AI는 일반적인 콘텐츠를 생성하는 데 능숙합니다. 텍스트의 기반을 잘 형성할 수 있지만 필요한 양에 도달하기 위해 "플러프를 추가"하는 데 어려움을 겪는 사람들에게 이겢은 훌륭한 지원이 될 수 있습니다.
3. 일부 예약 사항이 있지만, AI는 텍스트를 신속하게 분석하고 주요 아이디어의 요약을 사용자에게 제공할 수 있습니다. 그러나 AI 어시스턴트 개발자들이 아직 맥락을 기억하는 능력을 향상시키고 있기 때문에 아직 몇 가지 제한 사항이 있습니다.
4. 이미 AI가 데이터 세트를 분석하고 구두 설명을 기반으로 프로그램 코드를 작성하려고 시도하는 것은 인상적입니다. 그러나 결과에 대해 극도로 주의해야 합니다.
5. 물론, 고급 검색 도구로서 AI 어시스턴트는 일반적인 검색 엔진을 능가합니다.

그러나 식별된 단점 중에는:

1. AI 환각은 종종 사용자가 답변을 철저히 확인해야 하기 때문에 AI로부터 얻은 결과의 속도의 이점을 무효화합니다. 때로는 작업을 직접 수행하는 것이 더 쉽고 빠를 수 있습니다.
2. 더 깊이 있는 답변을 얻는 데 어려움이 있습니다. AI 도구의 "게으름"으로 인해 사용자는 AI가 작업을 더 잘 수행하도록 하는 더 환상적인 요청으로 고민해야 합니다. 이는 결국 선임 직원과 인턴 간의 관계를 닮은 꽤 익살스러운 상황으로 이어지며, 결국 전자가 스스로 작업을 수행하는 것이 후자가 작업을 수행하도록 시도하는 것보다 쉽습니다. 이로 인해 속도와 편의성의 장점이 무효화됩니다.
3. 받은 결과의 품질의 불안정성. AI는 종종 다른 세션에서 동일한 쿼리에 대해 완전히 다른 결과를 제공하며, 이는 본질적으로 사용자가 승리를 기대하며 슬롯 머신을 돌리도록 강요합니다. 게다가, 받은 응답이 최상의 가능한 것인지 확신할 수 없습니다.
4. AI 도구 개발자에 대한 불만: 현재 도구는 대량의 텍스트와 데이터와 적절한 작업을 허용하지 않는 형편없는 인터페이스를 가지고 있습니다.

<RoboAcademyDialog>
“As a result, it can be said that AI tools can already be a good addition to manual, monotonous work in creating academic materials, but they still have many problems and shortcomings that prevent them from fully replacing human labor. In the future, these problems may be solved, and AI assistants will be able to significantly speed up and improve the process of creating scientific materials.”
</RoboAcademyDialog>

*(위 결과는 Notion AI에 의해 생성되었습니다)*