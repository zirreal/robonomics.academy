---
title: "Introduzione alla soluzione open source per smart home private"
lastUpdate: Tue May 09 2023 13:56:49 GMT+0400 (Samara Standard Time)
description: Imparerai come integrare soluzioni open source con dispositivi smart economici per rendere la tua smart home orientata alla privacy e non dipendente dai cloud nel suo funzionamento.
metaOptions: [Imparare]
defaultName: Introduction to open source solution for private smart homes
---

<LessonImages src="smart-home-intro/open-source-private-smart-home-intro.png" imageClasses="mb full" />

<RoboAcademyText>
  Ciao a tutti! Oggi voglio portarvi in una conversazione su una smart home, quando c'è la necessità, di cosa è composta e cosa può dare.
</RoboAcademyText>

## Smart homes: Risolvere i problemi di riscaldamento e acqua calda

Nel 2022, mi sono trasferito a Cipro e ho dovuto abituarmi rapidamente alle condizioni di vita in un posto nuovo. Dopo la Russia, la differenza di atteggiamento verso l'uso delle risorse energetiche si sente particolarmente nettamente. Ad esempio, a Cipro non c'è il riscaldamento centralizzato. E fino a dicembre, non ci si poteva pensare. E poi è emerso che la temperatura della mia camera da letto è la stessa della temperatura fuori dalla finestra. Ad essere onesti, è scomodo dormire a +10 °C ... brrr!

## Potenzia i tuoi risparmi con il monitoraggio della smart home

Inoltre, non c'è neanche un sistema centralizzato di fornitura di acqua calda. Ci sono caldaie che vengono installate sul tetto e vengono riscaldate dal sole. Ma in inverno il sole non è sufficiente per riscaldare il serbatoio dell'acqua. L'appartamento ha un interruttore che avvia l'elemento riscaldante all'interno del serbatoio. La prima cosa che è scomoda è che devi accenderlo in anticipo. Mezz'ora o un'ora prima di fare la doccia. La sera, questo scenario è ancora accettabile, ma al mattino non avrai mai acqua calda. In secondo luogo, puoi facilmente dimenticare di spegnerlo. Di conseguenza - un elemento riscaldante bruciato e una bolletta dell'elettricità.

A proposito, l'elettricità è molto costosa qui, e devi pagarla ogni 2 mesi. Al momento, è impossibile determinare il principale consumatore. Sarebbe bello avere statistiche sui principali consumatori di elettricità, come l'aria condizionata, il riscaldamento a pavimento, l'illuminazione, ecc. Avendo i dati in tempo reale sul consumo di energia a portata di mano, almeno puoi iniziare ad analizzare su cosa viene speso.

## Componenti essenziali di una smart home: interruttori, sensori e contatori intelligenti

Risulta che i primi candidati per i dispositivi smart sono vari interruttori e il monitoraggio del consumo energetico. Successivamente, probabilmente penserai a controllare il condizionatore d'aria e il riscaldamento a pavimento secondo un programma o secondo le letture della temperatura. Questo significa che avremo bisogno di sensori di temperatura e umidità, relè per controllare il riscaldamento a pavimento e telecomandi IR per i condizionatori d'aria. Ogni casa ha anche finestre, e le finestre di solito hanno tende - sarebbe bello quando vai a letto che le tende cadano automaticamente. Così, interruttori, sensori e contatori intelligenti formano la base di una smart home. E poi puoi sognare in base alle esigenze specifiche.

## Scegliere la soluzione smart home giusta: KNX vs. Sonoff vs. Xiaomi

Quali soluzioni smart home e di automazione ci sono sul mercato? Possiamo pensare a KNX, che oggi è una delle soluzioni più comuni per l'uso in sistemi di automazione di medie e grandi dimensioni per case, uffici e locali commerciali. È sul mercato da oltre vent'anni ed è ora supportato da molti dei principali produttori di apparecchiature elettriche. Tuttavia, per assemblare una soluzione KNX, è necessario fare molto lavoro di ingegneria. La logica principale è assemblata, di solito, in un armadio di distribuzione separato. Se non è stato previsto originariamente, l'installazione in un appartamento esistente potrebbe essere difficile o impossibile del tutto, senza apportare opportune modifiche alla disposizione. Inoltre, le soluzioni basate su KNX sono piuttosto costose.

Un altro approccio potrebbe essere quello di acquistare dispositivi da produttori cinesi come Sonoff o Xiaomi. Il loro principale vantaggio è il prezzo, la facilità di installazione e configurazione. Chiunque sarà in grado di installare la maggior parte dei sensori e dei dispositivi nelle proprie case. In alcuni casi potrebbe essere necessario un elettricista, ad esempio, per installare interruttori intelligenti, ma prenderanno il posto dei vecchi e non sarà necessario apportare modifiche alla disposizione dell'appartamento. Il produttore offre un'applicazione unica per gestire i dispositivi. Tuttavia, devi sempre ricordare che i tuoi dati vengono inviati da qualche parte al server, e tutta la comunicazione con i dispositivi è impossibile senza una connessione Internet.


## Smart home fai da te: Costruire un server domestico per il pieno controllo

E un altro approccio alla costruzione di una smart home si basa sul secondo, cioè utilizzare dispositivi disponibili dagli stessi produttori cinesi, ma installare in aggiunta un server domestico nel tuo appartamento/casa per liberarti dai cloud. Questo è il percorso che abbiamo intrapreso nella nostra soluzione smart home. Nei prossimi articoli, parlerò dettagliatamente del montaggio del nostro stand dimostrativo e delle sue capacità.

<RoboAcademyText fWeight="500">
  Questo è tutto per ora! Nella prossima lezione, approfondiremo il lato pratico della costruzione di una smart home e ti mostreremo come assemblare una Smart Home Board. Resta sintonizzato e preparati a fare il tuo primo passo verso la creazione di una casa completamente funzionale e automatizzata.
</RoboAcademyText>