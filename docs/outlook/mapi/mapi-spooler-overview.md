---
title: Présentation du spouleur MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 162957ea17b5a82d4da68340e971d328c85cd9f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309578"
---
# <a name="mapi-spooler-overview"></a>Présentation du spouleur MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le spouleur MAPI est une fonction du processus Microsoft Office Outlook responsable de l'envoi et de la réception de messages à partir d'un système de messagerie. Le spouleur MAPI joue un rôle vital dans la réception et la remise des messages. Lorsqu'un système de messagerie est indisponible, le spouleur MAPI stocke les messages et les transfère automatiquement ultérieurement. Cette possibilité de conserver ou d'envoyer des données lorsque cela est nécessaire est appelée Store et Forward, une fonctionnalité essentielle dans les environnements où les connexions distantes sont courantes et où le trafic réseau est élevé. Le spouleur MAPI s'exécute comme un thread d'arrière-plan dans Outlook.
  
Le spouleur MAPI dispose de responsabilités supplémentaires liées à la distribution des messages. Ces droits supplémentaires sont les suivants:
  
- Assurer le suivi des types de destinataires qui sont gérés par des fournisseurs de transport spécifiques.
    
- Informer une application cliente lorsqu'un nouveau message a été remis.
    
- Appel du prétraitement des messages et du post-traitement.
    
- Génération de rapports indiquant que la remise des messages s'est produite.
    
- Gestion de l'état des destinataires traités.
    
L'illustration suivante montre à un niveau élevé le flux d'un message d'un client vers le système de messagerie.
  
**Flux de message sortant**
  
![Flux de messages sortants] (media/amapi_46.gif "Flux de messages sortants")
  
L'utilisateur d'une application cliente envoie un message à un ou plusieurs destinataires. Le fournisseur de banque de messages lance le processus d'envoi, en mettant en forme le message avec des informations supplémentaires nécessaires pour la transmission.
  
Le spouleur MAPI reçoit le message à traiter si l'une des conditions suivantes se produit:
  
- Le fournisseur de banque de messages n'est pas étroitement couplé à un fournisseur de transport.
    
- Le message doit être prétraité.
    
- La Banque de messages et le fournisseur de transport sont étroitement couplés, mais ils ne peuvent pas gérer tous les destinataires auxquels le message est adressé.
    
Si le spouleur MAPI reçoit le message, il effectue tout prétraitement requis et remet le message au fournisseur de transport approprié. Le fournisseur de transport transmet le message à son système de messagerie, qui l'envoie à son destinataire.
  
Avec les messages entrants, le flux est inversé. Le fournisseur de transport reçoit un message de son système de messagerie et avertit le spouleur MAPI. Spooler effectue le post-traitement nécessaire et informe le fournisseur de banque de messages qu'un nouveau message est arrivé. Cette notification fait en sorte que le client actualise son affichage de messages, ce qui permet à l'utilisateur de lire le nouveau message.
  
## <a name="see-also"></a>Voir aussi

- [Architecture et fonctionnalités MAPI](mapi-features-and-architecture.md)

