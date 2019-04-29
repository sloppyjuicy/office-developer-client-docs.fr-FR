---
title: Types d'applications clientes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 52ce22a9-3ec2-481c-bb91-7a5bcca817f5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 167710243c61a7226375b88977c94ff4a517c1c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417055"
---
# <a name="types-of-client-applications"></a>Types d'applications clientes

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe principalement deux types de clients de messagerie: ceux qui gèrent les messages interpersonnels (IPM) et ceux qui gèrent les messages de communication interprocessus (IPC). Au sein de ces types, les applications clientes de messagerie peuvent être classées comme suit:
  
- De personne à personne
    
- De personne à ordinateur
    
- Ordinateur à personne
    
- Ordinateur à ordinateur
    
- Mélange de personnes et d'ordinateurs
    
Les applications de personne à personne impliquent une personne qui initie l'échange de messages et qu'une autre personne répond. Cette catégorie d'applications inclut des applications de messagerie traditionnelles, ainsi que des échanges plus structurés, tels que le routage de documents ou l'approbation des dépenses.
  
Les applications de personne à ordinateur impliquent une personne qui initie l'échange de messages et qu'un ordinateur répond. Cette catégorie inclut les applications qui utilisent la messagerie électronique, par exemple, envoyer une requête de base de données ou s'abonner à une liste de publipostage.
  
Les applications ordinateur à personne impliquent un ordinateur qui initie l'échange de messages et une personne qui répond. Cette catégorie comprend les applications qui distribuent des documents tels que des flux d'actualités et des enquêtes sur les opinions.
  
Les applications ordinateur à ordinateur impliquent un ordinateur qui initie l'échange de messages et sur lequel un ordinateur répond. Cette catégorie inclut des applications telles que la surveillance des pulsations de liaison et la réplication des bases de données et des répertoires.
  
La dernière catégorie, un mélange de personnes et d'ordinateurs, implique un scénario plus complexe. Cette catégorie inclut les applications qui ne transmettent pas nécessairement les messages entre les expéditeurs et les destinataires. Au lieu de cela, ils peuvent les publier directement dans un dossier public ou un forum de site Web pris en charge par une banque de messages. Les messages peuvent ensuite être utilisés à la demande par d'autres lecteurs, un administrateur ou un agent logiciel.
  
Si vous écrivez une application de personne à personne, une application d'ordinateur à personne ou une application qui publie des messages dans des forums publics, concevez votre application pour envoyer et recevoir des messages IPM. Si vous écrivez une application de personne à ordinateur ou une application de machine à ordinateur, elle peut être conçue pour envoyer et recevoir des messages IPC. Toute application nécessitant l'interaction d'un utilisateur humain doit prendre en charge les messages IPM. Les applications qui impliquent à la fois des personnes et des machines dans un grand nombre de scénarios doivent souvent prendre en charge les messages IPM et IPC. La seule vraie différence entre les deux classes est que les messages IPM dans une banque de messages sont visibles pour les utilisateurs de clients de messagerie, tandis que les messages IPC ne sont généralement pas visibles par les utilisateurs de l'application cliente. 
  
Au lieu de limiter vos messages aux fonctionnalités fournies par les superclasses MAPI, IPM et IPC, vous pouvez personnaliser et améliorer ces classes en créant de nouvelles sous-classes IPM ou IPC. La création de sous-classes de message implique l'invente de nouvelles classes de message qui héritent des superclasses. Par exemple, si votre application de personne à personne est spécialisée dans la gestion des relations client, vous pouvez sous-classe la superclasse IPM en définissant un IPM. La classe contact. Customer et créer des propriétés qui décrivent un client. En plus de prendre en charge ces propriétés personnalisées, votre IPM. Contacts. les messages client héritent des propriétés prises en charge par tous les messages IPM.
  

