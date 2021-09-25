---
title: Types d’applications clientes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 52ce22a9-3ec2-481c-bb91-7a5bcca817f5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4e3aaf8de7726ca75816105fbe81b2019fcaa107
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578451"
---
# <a name="types-of-client-applications"></a>Types d’applications clientes

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe principalement deux types de clients de messagerie : ceux qui gèrent les messages interpersonnels (IPM) et ceux qui gèrent les messages de communication interprocessus (IPC). Dans ces types, les applications clientes de messagerie peuvent être classées comme suit :
  
- Personne à personne
    
- Personne à ordinateur
    
- Ordinateur à personne
    
- Ordinateur à ordinateur
    
- Combinaison de personnes et d’ordinateurs
    
Les applications de personne à personne impliquent une personne qui lance l’échange de messages et une autre personne répond. Cette catégorie d’applications inclut les applications de messagerie traditionnelles, ainsi que des échanges plus structurés tels que le routage des documents ou l’approbation des dépenses.
  
Les applications de personne à ordinateur impliquent qu’une personne lance l’échange de messages et qu’un ordinateur répond. Cette catégorie inclut les applications qui utilisent le courrier électronique pour, par exemple, soumettre une requête de base de données ou s’abonner à une liste de diffusion.
  
Les applications d’ordinateur à personne impliquent un ordinateur qui lance l’échange de messages et une personne qui répond. Cette catégorie inclut les applications qui distribuent des documents tels que des flux d’actualités et des enquêtes d’opinion.
  
Les applications d’ordinateur à ordinateur impliquent un ordinateur qui lance l’échange de messages et une réponse de l’ordinateur. Cette catégorie inclut des applications telles que la surveillance des pulsations de liens et la réplication des répertoires et des bases de données.
  
La dernière catégorie, un mélange de personnes et d’ordinateurs, implique un scénario plus complexe. Cette catégorie inclut les applications qui ne transmettent pas nécessairement des messages entre les expéditeurs et les destinataires. Au lieu de cela, ils peuvent les publier directement dans un dossier public ou sur un forum de site web pris en charge par une magasin de messages. Les messages peuvent ensuite être consommés à la demande par d’autres lecteurs, un administrateur ou un agent logiciel.
  
Si vous écrivez une application de personne à personne, une application d’ordinateur à personne ou une application qui publie des messages sur des forums publics, concevez votre application pour envoyer et recevoir des messages IPM. Si vous écrivez une application de personne à ordinateur ou d’ordinateur à ordinateur, elle peut être conçue pour envoyer et recevoir des messages IPC. Toute application nécessitant l’interaction d’un utilisateur humain doit prendre en charge les messages IPM. Les applications qui impliquent des personnes et des ordinateurs dans divers scénarios doivent souvent prendre en charge les messages IPM et IPC. La seule différence réelle entre les deux classes est que les messages IPM dans une magasin de messages sont visibles par les utilisateurs des clients de messagerie, tandis que les messages IPC ne sont généralement pas visibles pour les utilisateurs de l’application cliente. 
  
Au lieu de limiter vos messages aux fonctionnalités fournies par les superclasses MAPI, IPM et IPC, vous pouvez personnaliser et améliorer ces classes en créant de nouvelles sous-classes IPM ou IPC. La création de sous-classes de message implique l’inventation de nouvelles classes de message qui héritent des superclasses. Par exemple, si votre application de personne à personne est spécialisée dans la gestion de la relation client, vous pouvez sous-classer la superclasse IPM en définissant un IPM. Classe Contact.Customer et créez des propriétés qui décrivent un client. En plus de prendre en charge ces propriétés personnalisées, votre IPM. Les messages Contact.Customer héritent des propriétés pris en charge par tous les messages IPM.
  

