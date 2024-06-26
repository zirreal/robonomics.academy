---
title: "Les #1, Theoretische briefing"
lastUpdate: Thu May 04 2023 12:54:41 GMT+0400 (Samara Standard Time)
description: thuiscursus assistent
lessonNumber: 1
metaOptions: [Leer, Soevereine Slimme Woning met Robonomics en Home Assistant]
defaultName: Sovereign Smart Home with Robonomics and Home Assistant
---

## Belangrijke componenten van Sovereign Smart Home 

<List>

1. **[Raspberry Pi](https://www.raspberrypi.org/), een single board computer**.

We kunnen het apparaat omzetten in een IoT-hub nadat alle benodigde software is geïnstalleerd. Het hoofddoel van de hub is om de protocollen, netwerken, toepassingen en verschillende apparaten van het slimme huis te orchestreren.

2. **[Home Assistant](https://www.home-assistant.io/), een open source besturingssoftware**.

Het is ontworpen om een centrale hub te zijn voor slimme apparaten. Het kan automatisch het netwerk scannen op bekende apparaten en gebruikers in staat stellen om alle benodigde automatiseringen eenvoudig te configureren. We zullen Home Assistant installeren op de Raspberry Pi.

Home Assistant communiceert met apparaten en slaat hun gegevens lokaal op, wat helaas niet toestaat om uw apparaten op afstand te bedienen. Om dit probleem op te lossen gebruiken we Robonomics Network.

3. **[Robonomics Network](https://robonomics.network/), een gedecentraliseerde cloud voor veilige en betrouwbare controle van IoT-toepassingen**.

Het maakt gebruik van web3-technologieën, die decentralisatie en blockchain-technologieën omvatten voor de bescherming van slimme apparaten en hun gegevens.

De belangrijkste functionaliteit van Robonomics is geïmplementeerd op basis van een blockchain (parachain) van het Polkadot/Kusama-ecosysteem. Onder de belangrijkste functies van de parachain is het vermogen om een opdracht te sturen om het apparaat te starten en gebruikersgegevens op de blockchain op te slaan.

De Robonomics parachain heeft een IoT-abonnementsfunctie waarmee gebruikers transacties naar de parachain kunnen sturen, zonder kosten, gedurende een maand. In het praktische gedeelte van deze cursus zult u de abonnementsmethode gebruiken.

De interactie tussen de IoT-hub en de Robonomics parachain wordt tot stand gebracht met [robonomics-interface](https://github.com/Multi-Agent-io/Robonomics-interface) — Python-bibliotheek die gespecialiseerd is in de interface met Robonomics voor handig programmeren.

4. **[InterPlanetary File System](https://ipfs.tech/) (IPFS), een peer-to-peer software voor het opslaan en delen van gegevens in een gedistribueerd bestandssysteem**.

IPFS is nodig om te voorkomen dat grote bestanden op de blockchain worden opgeslagen (omdat dit te duur zou zijn), maar in plaats daarvan kunnen we de IPFS-hashes van de bestanden opslaan, die fungeren als links naar deze bestanden.

## Protocollen voor slimme apparaten
U zult twee hoofdprotocollen gebruiken voor slimme apparaten:

1. **[Zigbee](https://csa-iot.org/all-solutions/zigbee/), een draadloos communicatieprotocol.**

Het wordt zeer vaak gebruikt voor het verbinden van slimme apparaten. Het is ontworpen voor een laag energieverbruik, gebruiksgemak en flexibiliteit van configuratie, en ondersteunt zelforganiserende en zelfherstellende mesh-netwerktopologie. Duizenden apparaten zijn beschikbaar op de markt met Zigbee-ondersteuning, wat het zeer aantrekkelijk maakt voor het bouwen van slimme oplossingen voor thuis. Om Zigbee-apparaten te bedienen heeft u een gateway nodig die gegevens overdraagt tussen het Zigbee-netwerk en een ander netwerk (bijv. Wi-Fi).

2. **[Message Queuing Telemetry Transport](https://mqtt.org/) (MQTT), een publiceer-abonneeprotocol ontworpen om IoT-toepassingen te besturen.**

Het protocol is lichtgewicht, vereist minimale middelen en zorgt voor betrouwbaarheid van berichtaflevering. Het protocol is ontworpen voor netwerken met een lage bandbreedte, hoge latentie en onbetrouwbaarheid, wat het een uitstekende optie maakt voor het verwerken van grote hoeveelheden sensorberichten. MQTT vereist een server die de MQTT-broker uitvoert (in ons geval zal het werken met onze Raspberry Pi). De broker ontvangt alle berichten van de MQTT-clients en routeert vervolgens de berichten naar de juiste abonnerende clients.

## Opties voor Zigbee-verbinding
U zult twee scenario's verkennen voor het verbinden van apparaten met Home Assistant met Robonomics.

1. Het eerste scenario maakt geen gebruik van een aparte Zigbee-gateway om apparaten te verbinden. In plaats daarvan wordt een combinatie van een [Zigbee-adapter](https://www.zigbee2mqtt.io/guide/adapters/) en de [Zigbee2MQTT](https://www.zigbee2mqtt.io/guide/adapters/) software gebruikt.

<LessonImages figure figureCaption="Architectural scheme of the scenario with Zigbee adapter" src="smart-house-course/lesson-1-1.png" alt="Architectural scheme of the scenario with Zigbee adapter"/>

Een adapter (zoals de JetHome USB JetStick Z2) verbindt met de Raspberry Pi en fungeert als interface tussen de computer en de Zigbee-radiocommunicatie. Zigbee2MQTT is software die het mogelijk maakt om Zigbee te verbinden met MQTT-netwerken. Het neemt berichten van het Zigbee-netwerk en vertaalt ze naar gemakkelijk te gebruiken en goed gestructureerde berichten van MQTT.

2. In het tweede scenario worden apparaten verbonden met behulp van de [SLS Gateway](https://github.com/slsys/Gateway) gebaseerd op de ESP32 microcontroller. Voor gebruiksgemak heeft Robonomics onze [eigen modificatie](https://oshwlab.com/ludovich88/robonomics_sls_gateway_v01) van de gateway ontwikkeld.

<LessonImages figure figureCaption="Architectural scheme of the scenario with SLS Gateway" src="smart-house-course/lesson-1-2.png" alt="Architectural scheme of the scenario with SLS Gateway"/>

De SLS-gateway fungeert als coördinator van Zigbee-protocolberichten en maakt het gebruik van de meeste beschikbare Zigbee-apparatuur mogelijk. Voor integratie met Home Assistant wordt het MQTT-protocol gebruikt.

## Afstandsbediening

Afstandsbediening van een slim huis wordt uitgevoerd met behulp van de [Robonomics gedecentraliseerde applicatie](https://dapp.robonomics.network/) (dapp), die toegang biedt tot parachain-functies op een gebruiksvriendelijke manier. De beveiliging en onveranderlijkheid van gebruikersgegevens wordt aan de ene kant gewaarborgd door het verzenden van versleutelde gegevens naar IPFS (die alleen door de sleutel van de gebruiker kunnen worden gedecodeerd), en aan de andere kant door het plaatsen van de IPFS-hash van deze gegevens op de blockchain.

</List>



