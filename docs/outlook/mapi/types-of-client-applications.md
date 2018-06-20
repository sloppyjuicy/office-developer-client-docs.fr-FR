---
title: Types d’Applications clientes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 52ce22a9-3ec2-481c-bb91-7a5bcca817f5
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 17b55de84c38deb515dfb528e0ed01306934739d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787386"
---
# <a name="types-of-client-applications"></a>Types d’Applications clientes

  
  
**S’applique à**: Outlook 
  
Il existe principalement deux types de clients de messagerie : celles qui gèrent les messages interpersonnels (IPM) et celles qui gèrent les messages de communication interprocessus (IPC). Au sein de ces types, les applications de client de messagerie peuvent être classées comme suit :
  
- Personne à personne
    
- Personne sur l’ordinateur
    
- Ordinateur à l’autre
    
- Ordinateur à
    
- Combinaison des personnes et des machines
    
Les applications mettent en œuvre une personne à l’origine de l’échange de messages et une autre personne répondre. Cette catégorie d’applications inclut les applications de messagerie traditionnel ainsi plus structurées échanges de dépenses ou routage des documents.
  
Personne-à-machine applications mettent en œuvre une personne à l’origine de l’échange de messages et une réponse de l’ordinateur. Cette catégorie inclut les applications qui permet de courrier électronique, par exemple, envoyer une requête de base de données ou de s’abonner à une liste de publipostage.
  
Applications de l’ordinateur à l’autre mettent en œuvre un ordinateur initier l’échange de messages et d’une personne répond. Cette catégorie comprend les applications qui distribuent des documents tels que les échanges de news et enquêtes avis.
  
Applications de l’ordinateur à mettent en œuvre un ordinateur initier l’échange de messages et une réponse de l’ordinateur. Cette catégorie comprend des applications telles que la réplication lien pulsation de surveillance et d’annuaire et de base de données.
  
La catégorie finale, un mélange de personnes et des machines implique un scénario plus complexe. Cette catégorie comprend les applications qui ne transmettent pas nécessairement des messages entre les expéditeurs et destinataires. Au lieu de cela ils peuvent les publier directement dans un dossier public ou sur un forum de site web pris en charge par une banque de messages. Les messages peuvent ensuite être consommés à la demande par les autres lecteurs, un administrateur ou un agent logiciel.
  
Si vous écrivez une application de personne à personne, ordinateur à l’autre application ou une application qui publie des messages aux forums publics, concevez votre application pour envoyer et recevoir des messages IPM. Si vous écrivez une personne sur l’ordinateur ou d’ordinateur à l’autre application, il peut conçu pour envoyer et recevoir des messages IPC. Les applications qui nécessitent l’interaction d’un utilisateur doivent prendre en charge des messages IPM. Les applications qui impliquent des personnes et des ordinateurs dans divers scénarios souvent doivent prendre en charge des messages IPM et IPC. La seule différence entre les deux classes est que les messages IPM dans une banque de messages sont visibles pour les utilisateurs de clients de messagerie, tandis que les messages IPC généralement ne sont pas visibles pour les utilisateurs d’applications clientes. 
  
Au lieu de limiter vos messages pour les fonctionnalités fournies par le superclasse MAPI, IPM et IPC, vous pouvez personnaliser et améliorer ces classes en créant des nouvelles sous-classes IPM ou IPC. Création de sous-classes message implique inventer de nouvelles classes de message qui héritent de la superclasse. Par exemple, si votre application de personne à personne spécialisée dans la gestion des relations client, vous pouvez sous-classe de la superclasse IPM en définissant une IPM. Contact.Customer de classe et créer des propriétés qui décrivent un client. Outre ces propriétés personnalisées, votre IPM de prise en charge. Messages Contact.Customer hérite des propriétés prises en charge par tous les messages IPM.
  

