---
title: "Schreiben: Einführung"
description: Starten Sie Ihre Bachelorarbeit mit KI-gestützten Tools
metaOptions: [Lernen, Starten Sie Ihre Bachelorarbeit mit KI-gestützten Tools]
defaultName: Quickstart Your Bachelor's Thesis with AI-powered Tools
---

<RoboAcademyText fWeight="500">
In diesem Leitfaden werden wir eine Einführung für unsere Bachelorarbeit schreiben.
</RoboAcademyText>

Oft kann dieser Abschnitt einer der langweiligsten sein, der geschrieben werden muss. Neben der Planung und Beschreibung der allgemeinen Vision der Arbeit müssen wir eine bestimmte Menge an Text erstellen. Typischerweise versuchen Studenten, diesen Raum mit allem zu füllen, was sie können, was dazu führt, dass der Abschnitt wie ein Wortsalat aussieht. Dies ist genau das Problem, das KI-Assistenten gut bewältigen können.

Eine der interessanten Beobachtungen, die während des Testens von KI-Diensten gemacht wurden, ist, dass KI nicht danach strebt, Aufgaben in größerem Umfang als notwendig auszuführen. Ehrlich gesagt sind die Dienste fast "faul" und führen die Aufgabe nur in dem Umfang aus, der in der Anfrage angegeben ist. Wenn beispielsweise darum gebeten wird, Quellen für einen Textabsatz zu finden, wird KI 1-3 Quellen finden, nicht 5 oder 10. Daher ist es am besten, bei der Formulierung einer Anfrage die genaue Anzahl der zurückzugebenden Ergebnisse anzugeben.

## Eine Einführung mit Auto-GPT schreiben

### Einen Agenten erstellen

Wir werden einen Agenten mit folgender Beschreibung und Zielen erstellen:

<RoboAcademyTerminal title="Auto-GPT Terminal">

**Name your AI:** Bachelor-AI

**Describe your AI's role:** an AI that helps bachelors write their bachelor's thesis

**Enter up to 5 goals for your AI:**

*Goal 1:* Remember the context about the bachelor's thesis: "A bachelor is going to get Bachelor of Science in Computer Science and Engineering. The bachelor completed an online course called "Smart Home Sovereign". In this course, the bachelor went through all the steps necessary to build a sovereign smart home, the main advantage of which is the security / privacy of user data. During the course, The bachelor set up an IoT hub on a Raspberry Pi and connected smart devices (such as a temperature/humidity sensor, a door sensor, a smart bulb, a motion sensor, etc.) to it via a Zigbee-Adapter using the MQTT protocol. The IoT hub is powered by Home Assistant software. Next, the bachelor connected the hub to a decentralized cloud, based on Polkadot web3 technology. This is necessary to securely transfer device data to the network without the need for a centralized cloud service provider. This allows to securely manage the home remotely"

*Goal 2:* Write an Einführungduction part for this thesis in 500 words. It should contain: background and motivation; some context about web3 technology, what it is, why it should be used in smart home; research questions and objectives; significance of the work.

*Goal 3:* Save Einführungduction text in file called "Einführungduction.txt".

</RoboAcademyTerminal>

Als unser erstes Ziel haben wir den Agenten gebeten, den Kontext unserer Arbeit zu behalten. Wir haben auch die Länge des Einführungsabschnitts angegeben, darum gebeten, bestimmte Punkte (aus dem Arbeitsplan) einzubeziehen und darum gebeten, den Text in einer .txt-Datei zu speichern.

### Ergebnis erhalten

Agentenausgabe (verkürzte Version):

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

**THOUGHTS:**  Our draft summary has very few words and is within the word limit. We can use this information for our introduction and expand on the summary to create the final draft. We can use the 'write_to_file' command to write the final draft to the Einführungduction file.

**REASONING:**  We have counted the words in the introductory draft and confirmed that it is within the word limit. Now we can expand the draft summary to create the final draft of the introduction and write it to the Einführungduction file.

**PLAN:**

<br/>&mdash;  Expand the drafted summary to create the final draft
<br/>&mdash;  Save the final draft of the introduction to Einführungduction.txt using the 'write_to_file' command.

**CRITICISM:**  None

**NEXT ACTION:**  COMMAND = write_to_file ARGUMENTS = {'file': 'Introduction.txt', 'text': 'Introduction:\\n\\n The rise of smart home technology has led to a proliferation of internet-connected devices that can automate and optimize many aspects of our daily lives. A smart home system consists of a network of interconnected devices that can sense, communicate, and act on various environmental parameters such as temperature, humidity, motion, light, and sound. These devices can be controlled remotely or operate autonomously based on predefined rules and algorithms. \\n\\nHowever, smart home systems also present significant challenges and risks in terms of data privacy and security. Most smart home devices rely on centralized cloud platforms to store and process the data they collect from users' homes, which exposes users to potential data breaches, unauthorized access, surveillance, manipulation, or misuse by third parties such as hackers, service providers, governments, or advertisers. Furthermore, users often have limited control and ownership over their data, as they are required to agree to the terms and conditions of the cloud providers, which may not respect their preferences or rights. \\n\\nWeb3 technology refers to a suite of decentralized technologies that use blockchain to enable secure, transparent, and immutable transactions and records without intermediaries or central authorities. This allows for the creation of trustless, compromise-resistant IoT networks, and supports the creation of decentralized applications (dapps) that run on top of the blockchain. This enables users to transact in a secure and decentralized manner. \\n\\nThe main goal of this bachelor's thesis is to design a smart home system that is both secure and private. This system will use web3 technologies to create a decentralized, sovereign ecosystem. To achieve this goal, this work will explore the use of a Raspberry Pi as an IoT hub, connected to various smart home devices using the MQTT protocol. Then, a decentralized cloud based on Polkadot web3 technology will be integrated into the IoT system. This will enable secure and private data transfer between the smart home devices. Finally, the privacy and security implications of this setup will be evaluated and compared to traditional smart home setups that rely on centralized cloud vendors. \\n\\nThe significance of this study lies in its exploration of the use of Web3 technologies to design a secure and private smart home system. This work identifies the potential benefits and challenges of using Web3 technologies in smart homes. By examining these issues, this study contributes to the development of guidelines for the use of these technologies in IoT environments.'}

**SYSTEM:**  Command write_to_file returned: File written to successfully.

</RoboAcademyTerminal>

Laut den Agentenprotokollen hat der Agent vor dem Schreiben des Textes einige Zeit mit der Suche nach Informationen verbracht. Darüber hinaus hat der Agent die Einführung iterativ erstellt und allmählich Text hinzugefügt, um die Wortgrenze zu erreichen.

### Ergebnis verbessern

Insgesamt hat die KI die Aufgabe gut genug erledigt, um diesen Text als Grundlage für eine Einführung zu verwenden. Er kann auch weiter verbessert werden, indem der Text in **Notion AI** eingespeist wird (unter Verwendung der Tools `Schreiben verbessern` oder `Ton ändern`).

<RoboAcademyText>
Im Allgemeinen ist es im Einführungsabschnitt bereits erforderlich, Quellen für relevante Arbeiten hinzuzufügen, aber bevor wir mit der Suche und Analyse von Quellen fortfahren, ist es besser, zunächst den folgenden Leitfaden durchzugehen — Literaturüberprüfung.
</RoboAcademyText>