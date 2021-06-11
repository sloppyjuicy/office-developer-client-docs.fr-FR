---
title: Écriture d’un client automatisé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f9ce3452bbc2d3297cc67168835a9387235746a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439764"
---
# <a name="writing-an-automated-client"></a>Écriture d’un client automatisé

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une application cliente automatisée est une application qui s’exécute sans surveillance et n’affiche aucune interface utilisateur.
  
 Par défaut, de nombreuses méthodes d’interface MAPI montrent une interface utilisateur. Toutes ces méthodes ont des indicateurs qui permettent à un client d’autoriser ou de supprimer cet affichage. Bien que MAPI s’attende à ce que les fournisseurs de services respectent ces indicateurs, certains fournisseurs ne répondent pas toujours à ces attentes. Une raison légitime de ne pas respecter les indicateurs est la dépendance du fournisseur de services vis-à-vis d’un autre service qui n’autorise pas la suppression de l’interface utilisateur. Si vous développez un client automatisé, soyez attentif aux fournisseurs de services que vous utilisez et à leur configuration. Ne supposez pas que tous vos appels pour supprimer une interface utilisateur seront réussis. 
  
Les clients automatisés doivent avoir les informations nécessaires pour une configuration appropriée de chacun des services de message dans le profil. Il existe deux façons de fournir des informations de configuration au moment de l’logo :
  
- Le fournisseur de services peut récupérer des informations à partir du profil.
    
- Le fournisseur de services peut fournir des informations à l’utilisateur. 
    
Étant donné que la deuxième option n’est pas disponible pour les clients automatisés, ces clients doivent utiliser la première option. Les clients doivent configurer leurs profils avec soin pour s’assurer que cette option fonctionne toujours.
  
Les clients automatisés définissent toujours l MAPI_NO_MAIL dans l’appel de fonction [MAPILogonEx](mapilogonex.md) pour démarrer une session MAPI. 
  

