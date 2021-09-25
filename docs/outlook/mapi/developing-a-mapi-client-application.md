---
title: Développement d’une application cliente MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6f33616b8dcf37179ea1acf33416ee3e1e0ad617
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561851"
---
# <a name="developing-a-mapi-client-application"></a>Développement d’une application cliente MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes MAPI sont écrites avec l’interface cliente MAPI orientée objet. Les clients MAPI interagissent avec un ou plusieurs systèmes de messagerie via le sous-système MAPI et les fournisseurs de services conformes MAPI. Cette interaction peut se produire de nombreuses manières différentes . il existe une grande variété dans les applications clientes. La plupart des clients sont des clients de messagerie, soit en intégrant la messagerie dans leur ensemble de fonctionnalités établi, soit en intégrant la messagerie comme fonctionnalité principale. Les clients MAPI peuvent également fournir d’autres fonctionnalités, notamment l’administration des profils, le carnet d’adresses et la gestion de la boutique de messages.
  
Tous les clients de messagerie initialisent les bibliothèques MAPI et démarrent une **session** avec le sous-système MAPI. Pour plus d’informations, [voir Accès aux objets à l’aide de la session.](accessing-objects-by-using-the-session.md) Une fois qu’une session a été établie, un client peut :
  
- Gérer les messages sortants, y compris les réponses, les messages transmis et les retransmissions.
    
- Gérer les messages entrants.
    
- Gérer la magasin de messages en ouvrant des dossiers et des messages, en créant, modifiant, copiant et envoyant des messages, en suivant les conversations et en recherchant un ou plusieurs dossiers.
    
- Gérer le carnet d’adresses en créant et en modifiant des destinataires, en localisant des entrées et en parcourant la hiérarchie des conteneurs.
    
- Gérer un fournisseur de transport en reconfigurant, en dédiant des options et un ordre de transport et en envoyant des messages à la demande.
    
- Gérer les notifications d’événement.
    
- Gérer les formulaires.
    
- Gérer les profils et les services de message.
    
Utilisez les rubriques de cette section pour vous aider à implémenter ces tâches de base et les fonctionnalités spécifiques qui rendent votre client MAPI unique.
  

