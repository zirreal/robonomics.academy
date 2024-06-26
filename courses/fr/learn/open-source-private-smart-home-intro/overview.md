---
title: "Introduction aux solutions open source pour les maisons intelligentes privées"
lastUpdate: Tue May 09 2023 13:56:49 GMT+0400 (Samara Standard Time)
description: Vous apprendrez comment intégrer des solutions open source avec des appareils intelligents bon marché pour rendre votre maison intelligente orientée vers la vie privée et non dépendante des clouds dans son fonctionnement.
metaOptions: [Apprendre]
defaultName: Introduction to open source solution for private smart homes
---

<LessonImages src="smart-home-intro/open-source-private-smart-home-intro.png" imageClasses="mb full" />

<RoboAcademyText>
  Salut à tous! Aujourd'hui, je veux vous emmener dans une conversation sur une maison intelligente, quand il y a un besoin, de quoi elle est composée et ce qu'elle peut apporter.
</RoboAcademyText>

## Maisons intelligentes: Résoudre les problèmes de chauffage et d'eau chaude

En 2022, j'ai déménagé à Chypre et j'ai dû rapidement m'habituer aux conditions de vie dans un nouvel endroit. Après la Russie, la différence d'attitude envers l'utilisation des ressources énergétiques se fait particulièrement sentir. Par exemple, à Chypre, il n'y a pas de chauffage central. Et jusqu'en décembre, vous ne pouviez pas y penser. Et puis il s'est avéré que la température de ma chambre est la même que la température à l'extérieur de la fenêtre. Pour être honnête, il est inconfortable de dormir à +10 С ... brrr!

## Augmentez vos économies avec la surveillance de la maison intelligente

De plus, il n'y a pas non plus d'approvisionnement central en eau chaude. Il y a des chaudières qui sont installées sur le toit et chauffées par le soleil. Mais en hiver, le soleil ne suffit pas à chauffer le réservoir d'eau. L'appartement dispose d'un interrupteur qui démarre l'élément chauffant à l'intérieur du réservoir. La première chose qui est gênante, c'est qu'il faut le mettre en marche à l'avance. Une demi-heure à une heure avant de prendre une douche. Le soir, ce scénario est encore acceptable, mais le matin, vous n'aurez jamais d'eau chaude. Deuxièmement, vous pouvez facilement oublier de l'éteindre. Résultat - un élément chauffant grillé et une facture d'électricité.

Au fait, l'électricité est très chère ici, et vous devez la payer tous les 2 mois. Il est impossible, pour le moment, de déterminer le principal consommateur. Il serait bien d'avoir des statistiques sur les principaux consommateurs d'électricité, tels que la climatisation, le chauffage au sol, l'éclairage, etc. En ayant des données en temps réel sur la consommation d'énergie à portée de main, vous pouvez au moins commencer à analyser sur quoi elle est dépensée.

## Composants essentiels d'une maison intelligente: interrupteurs, capteurs et compteurs intelligents

Il s'avère que les premiers candidats pour les appareils intelligents sont divers interrupteurs et la surveillance de la consommation d'énergie. Ensuite, vous penserez probablement à contrôler la climatisation et le chauffage au sol selon un horaire ou selon les relevés de température. Cela signifie que nous aurons besoin de capteurs de température et d'humidité, de relais pour contrôler le chauffage au sol et de télécommandes IR pour les climatiseurs. Chaque maison a également des fenêtres, et les fenêtres ont généralement des rideaux - ce serait cool que les rideaux tombent automatiquement en allant se coucher. Ainsi, les interrupteurs, les capteurs et les compteurs intelligents forment la base d'une maison intelligente. Et ensuite, vous pouvez rêver en fonction des besoins spécifiques.

## Choisir la bonne solution pour la maison intelligente: KNX vs. Sonoff vs. Xiaomi

Quelles solutions de maison intelligente et d'automatisation sont sur le marché? Nous pouvons penser à KNX, qui est aujourd'hui l'une des solutions les plus courantes pour une utilisation dans les systèmes d'automatisation de taille moyenne et grande pour les maisons, les bureaux et les locaux commerciaux. Il est sur le marché depuis plus de vingt ans et est maintenant soutenu par de nombreux grands fabricants d'équipements électriques. Cependant, pour assembler une solution KNX, beaucoup de travail d'ingénierie doit être fait. La logique principale est assemblée, en règle générale, dans un armoire électrique séparée. Si cela n'était pas prévu à l'origine, l'installation dans un appartement existant peut être difficile, voire impossible, sans apporter les modifications appropriées à la disposition. De plus, les solutions basées sur KNX sont assez chères.

Une autre approche pourrait être d'acheter des appareils auprès de fabricants chinois tels que Sonoff ou Xiaomi. Leur principal avantage est le prix, la facilité d'installation et de configuration. Tout le monde pourra installer la plupart des capteurs et des appareils dans leur maison. Dans certains cas, vous pourriez avoir besoin d'un électricien, par exemple, pour installer des interrupteurs intelligents, mais ils prendront la place des anciens et vous n'aurez pas à apporter de modifications à la disposition de l'appartement. Le fabricant propose une seule application pour gérer les appareils. Cependant, vous devez toujours vous rappeler que vos données sont envoyées quelque part sur le serveur, et toute communication avec les appareils est impossible sans connexion Internet.


## Maison intelligente DIY: Construction d'un serveur domestique pour un contrôle total

Et une autre approche pour construire une maison intelligente est basée sur la deuxième, c'est-à-dire utiliser des appareils disponibles auprès des mêmes fabricants chinois, mais installer en plus un serveur domestique dans votre appartement / maison pour vous débarrasser des clouds. C'est le chemin que nous avons pris dans notre solution de maison intelligente. Dans les parties suivantes, je parlerai en détail de l'assemblage de notre stand de démonstration et de ses capacités.

<RoboAcademyText fWeight="500">
  C'est tout pour le moment! Dans la prochaine leçon, nous plongerons plus en profondeur dans le côté pratique de la construction d'une maison intelligente et vous montrerons comment assembler un tableau de maison intelligente. Restez à l'écoute et préparez-vous à faire votre premier pas vers la création d'une maison entièrement fonctionnelle et automatisée.
</RoboAcademyText>