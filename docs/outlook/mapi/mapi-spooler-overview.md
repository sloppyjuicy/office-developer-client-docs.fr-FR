---
title: Présentation du spouleur MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 162957ea17b5a82d4da68340e971d328c85cd9f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432715"
---
# <a name="mapi-spooler-overview"></a>Présentation du spouleur MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lepooler MAPI est une fonction du processus Microsoft Office Outlook qui est responsable de l’envoi et de la réception de messages à partir d’un système de messagerie. Lepooler MAPI joue un rôle vital dans la réception et la remise des messages. Lorsqu’un système de messagerie n’est pas disponible, lepooler MAPI stocke les messages et les a automatiquement transmis ultérieurement. Cette possibilité de conserver ou d’envoyer des données lorsque cela est nécessaire est appelée stocker et transmettre, une fonctionnalité essentielle dans les environnements où les connexions distantes sont courantes et où le trafic réseau est élevé. Lepooler MAPI s’exécute en tant que thread d’arrière-plan dans Outlook.
  
Lepooler MAPI a des responsabilités supplémentaires liées à la distribution des messages. Ces tâches supplémentaires sont les suivantes :
  
- Suivi des types de destinataires gérés par des fournisseurs de transport spécifiques.
    
- Informer une application cliente lorsqu’un nouveau message a été remis.
    
- L’facturation du prétraitment et du post-traitement des messages.
    
- Génération de rapports qui indiquent que la remise du message s’est produite.
    
- Maintien de l’état sur les destinataires traitées.
    
L’illustration suivante montre à un niveau élevé comment un message circule d’un client vers le système de messagerie.
  
**Flux de message sortant**
  
![Flux de messages sortants](media/amapi_46.gif "Flux de messages sortants")
  
L’utilisateur d’une application cliente envoie un message à un ou plusieurs destinataires. Le fournisseur de la boutique de messages lance le processus d’envoi, en formatant le message avec des informations supplémentaires nécessaires pour la transmission.
  
Lepooler MAPI reçoit le message à traiter si l’une des conditions suivantes se produit :
  
- Le fournisseur de la boutique de messages n’est pas étroitement associé à un fournisseur de transport.
    
- Le message nécessite un prétraitment.
    
- La magasin de messages et le fournisseur de transport sont étroitement associés, mais ils ne peuvent pas gérer tous les destinataires auxquels le message est adressé.
    
Si lepooler MAPI reçoit le message, il effectue les prétraitations requises et le remettre au fournisseur de transport approprié. Le fournisseur de transport envoie le message à son système de messagerie, qui l’envoie à son destinataire prévu.
  
Avec les messages entrants, le flux est inversé. Le fournisseur de transport reçoit un message de son système de messagerie et avertit lepooler MAPI. Spooler effectue tout post-traitement nécessaire et informe le fournisseur de la boutique de messages qu’un nouveau message est arrivé. Cette notification entraîne l’actualisation de l’affichage du message par le client, ce qui permet à l’utilisateur de lire le nouveau message.
  
## <a name="see-also"></a>Voir aussi

- [Fonctionnalités et architecture MAPI](mapi-features-and-architecture.md)

