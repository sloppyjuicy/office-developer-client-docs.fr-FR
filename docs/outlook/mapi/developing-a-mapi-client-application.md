---
title: Développement d’une Application de Client MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 42558fcc3d94b108c0dabb92d62f7c61fdf3039f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783158"
---
# <a name="developing-a-mapi-client-application"></a>Développement d’une Application de Client MAPI

  
  
**S’applique à**: Outlook 
  
Les applications clientes MAPI sont écrites avec l’interface de client orientée objet MAPI. Clients MAPI interagissent avec un ou plusieurs systèmes de messagerie via le sous-système MAPI et les fournisseurs de services compatible MAPI. Cette interaction peut se produire de différentes façons ; Il existe une grande diversité de dans les applications clientes. La plupart des clients sont des clients, l’intégration de messagerie dans leur ensemble de fonctionnalités établies ou l’exécution de messagerie en tant que leur fonctionnalité principale de messagerie. Administration des profils sont les autres fonctionnalités qui peuvent fournir des clients MAPI ou stockent la gestion des messages et le carnet d’adresses.
  
Tous les clients de messagerie initialiser les bibliothèques MAPI et démarrer une **session** avec le sous-système MAPI. Pour plus d’informations, consultez [Accès à des objets à l’aide de la Session](accessing-objects-by-using-the-session.md). Après l’établissement d’une session, un client peut :
  
- Gérer les messages sortants, y compris les réponses, transférée des messages et retransmissions.
    
- Gérer les messages entrants.
    
- Gérer la banque de messages par l’ouverture des dossiers et messages, création, modification, copie, envoyer des messages, le suivi des conversations et un ou plusieurs dossiers de recherche.
    
- Gérer le carnet d’adresses en création et modification des destinataires, localiser les entrées et parcourir la hiérarchie des conteneurs.
    
- Gérer un fournisseur de transport en effectuant la reconfiguration, définition de l’ordre des options et de transport et envoyer des messages à la demande.
    
- Gérer les notifications d’événement.
    
- Gérer les formulaires.
    
- Gérer les profils et les services de messagerie.
    
Utilisez les rubriques de cette section pour vous aider à implémenter ces tâches de base et les fonctionnalités spécifiques qui permette de rendre votre client MAPI unique.
  

