---
title: Écriture d’un client automatisé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
ms.openlocfilehash: c92457fd333d9aad21e97a2a97a6e6874ae0f2b4
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373612"
---
# <a name="writing-an-automated-client"></a>Écriture d’un client automatisé

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une application cliente automatisée est une application qui s’exécute sans surveillance et n’affiche aucune interface utilisateur.
  
 Par défaut, de nombreuses méthodes d’interface MAPI montrent une interface utilisateur. Toutes ces méthodes ont des indicateurs qui permettent à un client d’autoriser ou de supprimer cet affichage. Bien que MAPI s’attende à ce que les fournisseurs de services respectent ces indicateurs, certains fournisseurs ne répondent pas toujours à ces attentes. Une raison légitime de ne pas respecter les indicateurs est la dépendance du fournisseur de services vis-à-vis d’un autre service qui n’autorise pas la suppression de l’interface utilisateur. Si vous développez un client automatisé, faites attention aux fournisseurs de services que vous utilisez et à leur configuration. Ne supposez pas que tous vos appels pour supprimer une interface utilisateur seront réussis. 
  
Les clients automatisés doivent avoir les informations nécessaires pour une configuration appropriée de chacun des services de message dans le profil. Il existe deux façons de fournir des informations de configuration au moment de l’logo :
  
- Le fournisseur de services peut récupérer des informations à partir du profil.
    
- Le fournisseur de services peut fournir des informations à l’utilisateur. 
    
Étant donné que la deuxième option n’est pas disponible pour les clients automatisés, ces clients doivent utiliser la première option. Les clients doivent configurer leurs profils avec soin pour s’assurer que cette option fonctionne toujours.
  
Les clients automatisés définissent toujours l MAPI_NO_MAIL dans l’appel de fonction [MAPILogonEx](mapilogonex.md) pour démarrer une session MAPI. 
  

