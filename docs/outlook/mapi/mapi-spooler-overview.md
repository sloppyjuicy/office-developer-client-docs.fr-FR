---
title: Vue d’ensemble du spouleur MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ec581e2170b92721410106eae00e2d36b3c775a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591337"
---
# <a name="mapi-spooler-overview"></a>Vue d’ensemble du spouleur MAPI
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Spouleur MAPI est une fonction du processus de Microsoft Office Outlook qui est responsable de l’envoi des messages et réception de messages à partir d’un système de messagerie. Spouleur MAPI joue un rôle essentiel dans la remise et de réception du message. Lorsqu’un système de messagerie n’est pas disponible, spouleur MAPI stocke les messages et les transfère automatiquement à une date ultérieure. Cette capacité d’envoyer des données lorsqu’il est nécessaire de façon permanente sur est appelée stocker et transférer, une fonctionnalité essentielle dans les environnements où les connexions à distance sont courants et le trafic réseau est élevé. Spouleur MAPI s’exécute comme un thread d’arrière-plan dans Outlook.
  
Spouleur MAPI a des responsabilités supplémentaires liées à la distribution du message. Ces droits supplémentaires sont les suivantes :
  
- Suivi des types de destinataires qui sont gérés par les fournisseurs de transport spécifique.
    
- Informe une application cliente lorsqu’un nouveau message a été remis.
    
- Message d’appel de prétraitement et de post-traitement.
    
- Génération de rapports qui indiquent que la remise des messages s’est produite.
    
- Maintien du statut des destinataires traités.
    
L’illustration suivante montre un haut niveau le flux d’un message à partir d’un client pour le système de messagerie.
  
**Flux de message sortant**
  
![Flux des messages de sortie] (media/amapi_46.gif "Flux des messages de sortie")
  
L’utilisateur d’une application cliente envoie un message à un ou plusieurs destinataires. La banque de messages fournisseur lance le processus d’envoi, le message de mise en forme avec des informations supplémentaires nécessaires pour la transmission.
  
Spouleur MAPI reçoit le message à traiter si une des conditions suivantes se produisent :
  
- Le fournisseur de banque de messages n’est pas étroitement avec un fournisseur de transport.
    
- Le message nécessite un prétraitement.
    
- La banque de messages et de transport fournisseur sont étroitement, mais ils ne peuvent pas gérer tous les destinataires auxquels le message est adressé.
    
Si le spouleur MAPI reçoit le message, il effectue tout prétraitement requis et remet le message au fournisseur de transport approprié. Le fournisseur de transport donne le message à son système de messagerie, qui envoie à son destinataire.
  
Avec les messages entrants, le flux est rétablie. Le fournisseur de transport reçoit un message à partir de son système de messagerie et avertit spouleur MAPI. Spouleur effectue un post-traitement nécessaire et informe le fournisseur de banque de messages qu’un nouveau message est arrivé. Cette notification, le client actualiser son affichage du message, l’activation de l’utilisateur de lire le nouveau message.
  
## <a name="see-also"></a>Voir aussi

- [Architecture et des fonctionnalités MAPI](mapi-features-and-architecture.md)

