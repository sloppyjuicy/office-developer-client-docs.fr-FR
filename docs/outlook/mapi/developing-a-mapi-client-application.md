---
title: Développement d'une application cliente MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 7f66d2e4d46519dd186a676a0d0fbb836322893b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316687"
---
# <a name="developing-a-mapi-client-application"></a>Développement d'une application cliente MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes MAPI sont écrites avec l'interface client MAPI orientée objet. Les clients MAPI interagissent avec un ou plusieurs systèmes de messagerie via le sous-système MAPI et les fournisseurs de services compatibles MAPI. Cette interaction peut se produire de plusieurs façons différentes; Il existe une variété énorme dans les applications clientes. La plupart des clients sont des clients de messagerie, soit l'intégration de la messagerie dans l'ensemble des fonctionnalités établies, soit l'exécution de la messagerie comme fonctionnalité principale. Les autres fonctionnalités que les clients MAPI peuvent fournir incluent l'administration des profils, la gestion des carnets d'adresses et de la Banque de messages.
  
Tous les clients de messagerie initialisent les bibliothèques MAPI et démarrent une **session** avec le sous-système MAPI. Pour plus d'informations, consultez [la rubrique accès aux objets à l'aide de la session](accessing-objects-by-using-the-session.md). Une fois qu'une session a été établie, un client peut:
  
- Gérer les messages sortants, y compris les réponses, les messages transférés et les retransmissions.
    
- Gérer les messages entrants.
    
- Gérez la Banque de messages en ouvrant des dossiers et des messages, en créant, modifiant, copiant et envoyant des messages, en suivi des conversations et en recherchant dans un ou plusieurs dossiers.
    
- Gérez le carnet d'adresses en créant et en modifiant des destinataires, en localisant des entrées et en parcourant la hiérarchie de conteneurs.
    
- Gérez un fournisseur de transport en effectuant une reconfiguration, en définissant les options et l'ordre de transport, et en envoyant des messages à la demande.
    
- Gérer la notification d'événement.
    
- Gérer les formulaires.
    
- Gérer les profils et les services de messagerie.
    
Utilisez les rubriques de cette section pour vous aider à implémenter ces tâches de base et les fonctionnalités spécifiques qui feront de votre client MAPI un usage unique.
  

