---
title: Objets d’état MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
ms.openlocfilehash: ecab63ca56c47d50707265e3a23f5ef41ad41f39
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372176"
---
# <a name="mapi-status-objects"></a>Objets d’état MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les objets d’état indiquent des informations sur les ressources MAPI. Par exemple, un fournisseur de services, le processus d’envoi/réception MAPI ou le carnet d’adresses.
  
Il existe un objet d’état fournissant des informations sur chaque fournisseur de services individuel dans le profil actuel. MAPI est responsable de l’implémentation des objets d’état pour le sous-système, le processus d’envoi/réception MAPI et le carnet d’adresses. L’objet d’état du sous-système fournit des informations globales. L’objet d’état du carnet d’adresses intégré fournit l’état de tous les fournisseurs de carnet d’adresses actuellement opérationnels.
  
Chaque objet d’état est inclus dans la table d’état, une table maintenue par MAPI qui fournit aux clients toutes les informations d’état de la session. Pour plus d’informations, voir [Tableaux d’état](status-tables.md). Les clients peuvent accéder à un objet d’état particulier par le biais de la table ou, pour un fournisseur de services, via son objet d’accès. Par exemple, pour accéder à l’objet d’état d’un fournisseur de carnet d’adresses, un client peut appeler **IABLogon::OpenStatusEntry**. Pour plus d’informations, [voir IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).
  
Les clients peuvent utiliser des objets d’état pour :
  
- Découvrez l’état d’une session.
    
- Surveillez un fournisseur de services.
    
- Contrôler la transmission des messages.
    
- Afficher ou modifier la configuration et l’état d’une ressource.
    
Chaque objet status implémente **l’interface IMAPIStatus** . Pour plus d’informations, [voir IMAPIStatus : IMAPIProp](imapistatusimapiprop.md). Toutefois, tous les objets d’état ne prend pas entièrement en charge **chaque méthode IMAPIStatus** . Étant donné qu’il existe des variantes dans les méthodes qui sont pris en charge par un objet d’état, les clients doivent en savoir plus sur un objet d’état particulier avant de pouvoir l’utiliser. Les objets d’état sont requis pour publier des informations sur leurs fonctionnalités dans les trois propriétés suivantes : 
  
 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) 
  
 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 
  
 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 
  
Pour plus d’informations sur l’implémentation d’un objet d’état, voir [Status Object Implementation](status-object-implementation.md). Pour plus d’informations sur l’utilisation d’un objet d’état, voir [Status Table and Status Objects](status-table-and-status-objects.md).
  

