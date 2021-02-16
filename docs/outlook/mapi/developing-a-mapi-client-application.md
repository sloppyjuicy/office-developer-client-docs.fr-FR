---
title: Développement d’une application cliente MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7f66d2e4d46519dd186a676a0d0fbb836322893b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410034"
---
# <a name="developing-a-mapi-client-application"></a>Développement d’une application cliente MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes MAPI sont écrites avec l’interface cliente MAPI orientée objet. Les clients MAPI interagissent avec un ou plusieurs systèmes de messagerie via le sous-système MAPI et les fournisseurs de services conformes MAPI. Cette interaction peut se produire de nombreuses manières différentes . il existe une grande variété dans les applications clientes. La plupart des clients sont des clients de messagerie, soit en intégrant la messagerie dans leur ensemble de fonctionnalités établi, soit en les intégrant comme fonctionnalité principale. Les clients MAPI peuvent également fournir d’autres fonctionnalités, notamment l’administration des profils, le carnet d’adresses et la gestion des magasins de messages.
  
Tous les clients de messagerie initialisent les bibliothèques MAPI et démarrent une **session** avec le sous-système MAPI. Pour plus d’informations, [voir Accès aux objets à l’aide de la session.](accessing-objects-by-using-the-session.md) Une fois qu’une session a été établie, un client peut :
  
- Gérer les messages sortants, y compris les réponses, les messages transmis et les retransmissions.
    
- Gérer les messages entrants.
    
- Gérer la magasin de messages en ouvrant des dossiers et des messages, en créant, modifiant, copiant et envoyant des messages, en suivant les conversations et en recherchant un ou plusieurs dossiers.
    
- Gérer le carnet d’adresses en créant et en modifiant des destinataires, en localisant des entrées et en parcourant la hiérarchie des conteneurs.
    
- Gérer un fournisseur de transport en effectuer la reconfiguration, définir des options et un ordre de transport et envoyer des messages à la demande.
    
- Gérer les notifications d’événement.
    
- Gérer les formulaires.
    
- Gérer les profils et les services de message.
    
Utilisez les rubriques de cette section pour vous aider à implémenter ces tâches de base et les fonctionnalités spécifiques qui rendent votre client MAPI unique.
  

