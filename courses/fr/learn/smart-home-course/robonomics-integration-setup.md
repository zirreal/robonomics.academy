---
title: "Leçon n°6, Configuration de l'intégration de la robotique"
lastUpdate: Thu May 18 2023 10:46:29 GMT+0400 (Samara Standard Time)
description: cours d'assistant domestique
lessonNumber: 7
metaOptions: [Apprenez, Maison Intelligente Souveraine avec Robonomics et Home Assistant]
defaultName: Sovereign Smart Home with Robonomics and Home Assistant
---


## De quoi s'agit-il

Dans cette leçon, vous ajouterez Robonomics à Home Assistant et créerez un compte associé à l'abonnement. Cette intégration permet à Home Assistant d'utiliser les fonctions de la parachain Robonomics, tout d'abord, envoyer des données de maison intelligente chiffrées vers un cloud décentralisé.


## Théorie

Vos données de maison intelligente sont envoyées en utilisant l'extrinsèque <code>record()</code> du paquet <code>datalog</code> qui vous permet de sauvegarder des données de périphérique chiffrées sur la blockchain. 

Pour être plus précis, l'intégration utilise IPFS pour stocker les données puis envoie les hachages IPFS à l'extrinsèque datalog, qui est à son tour stocké dans la blockchain. Mais comme cette fonction est appelée via un abonnement IoT, toute la fonction ressemble à ceci : <code>rws.call(datalog.record(VOTRE_HACHAGE_IPFS))</code>.

## Instructions

<List type="numbers">

<li>

Ajout de Robonomics à Home Assistant

<List>

<li>

Dans l'interface web de Home Assistant, allez dans <code>Paramètres</code>-><code>Appareils & Services</code> et appuyez sur <code>AJOUTER UNE INTÉGRATION</code>. Recherchez <code>Robonomics</code>.

<LessonVideo  :videos="[{src: 'https://crustipfs.info/ipfs/QmQp66J943zbF6iFdkKQpBikSbm9jV9La25bivKd7cz6fD', type:'mp4'}]" />

</li>

<li>

Cliquez sur Robonomics et remplissez la configuration : 

\- Ajoutez la graine du compte <code>SUB_CONTROLLER</code> au compte administrateur

\- Ajoutez l'adresse publique du compte <code>SUB_OWNER</code> (que vous avez créé précédemment) à l'adresse du propriétaire de l'abonnement

\- Définissez l'intervalle d'envoi des données (par défaut, c'est 10 minutes)

\- (Facultatif) Vous pouvez ajouter des identifiants pour le service de mise en mémoire tampon Pinata pour diffuser vos données plus largement sur le réseau IPFS

</li>

<li>

Appuyez sur <code>SOUMETTRE</code> après avoir terminé la configuration. Si vous avez tout rempli correctement, vous verrez la fenêtre de réussite.

</li>
</List>
</li>

<li>

Ajout d'utilisateurs dans Robonomics Dapp 

<List>

<li>

Vous devez créer un utilisateur séparé pour Home Assistant, qui contrôlera les appareils domotiques. Vous ne pouvez pas utiliser les comptes précédemment créés car <code>SUB_OWNER</code> et <code>SUB_CONTROLLER</code> assurent la sécurité, et le premier utilisateur que vous avez créé lorsque vous avez démarré Home Assistant n'a pas de compte Robonomics Parachain.

</li>

<li>
Commencez par créer un compte sur Robonomics Parachain, comme vous l'avez fait dans la leçon précédente.
</li>

<li>

Ajoutez ce compte à l'abonnement dans le [dapp](https://dapp.robonomics.network/#/subscription/devices). Maintenant, il devrait y avoir trois adresses dans la liste d'accès: <code>SUB_OWNER</code>, <code>SUB_CONTROLLER</code> et <code>USER</code>.

<LessonVideo  :videos="[{src: 'https://crustipfs.info/ipfs/QmSxzram7CF4SXpVgEyv98XetjYsxNFQY2GY4PfyhJak7H', type:'mp4'}]" />

</li>

<li>

Allez sur le service dapp appelé [Compte Home Assistant](https://dapp.robonomics.network/#/home-assistant). Choisissez le compte que vous venez de créer dans la barre latérale droite (vérifiez que vous avez choisi le compte prévu en appuyant sur l'icône de profil).

Entrez la graine <code>USER</code> dans le champ requis. Ajoutez les adresses <code>SUB_OWNER</code> et <code>SUB_CONTROLLER</code> dans les champs de crédits administrateurs. Si tout est correct, vous verrez l'état de vérification <code>VERIFIED</code>.

</li>

<li>

Créez un mot de passe pour un nouvel utilisateur que vous venez d'enregistrer, puis confirmez la transaction, qui sera désormais sans frais en raison de l'abonnement. Plus tard, vous pourrez restaurer le mot de passe dans l'onglet <code>Restaurer</code>.

<LessonVideo  :videos="[{src: 'https://crustipfs.info/ipfs/QmW2TXuwCYXzgcRfEUx4imZU5ZerEzkuD5P53u9g2WnxDh', type:'mp4'}]" />

</li>

<li>

Après le processus d'inscription, connectez-vous à Home Assistant avec votre adresse utilisateur comme identifiant et un mot de passe nouvellement créé. Maintenant, vous pouvez utiliser l'application Robonomics pour contrôler votre maison via Robonomics.

</li>
</List>
</li>
</List>