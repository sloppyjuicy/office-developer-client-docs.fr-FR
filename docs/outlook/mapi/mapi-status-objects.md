---
title: Objets d’état MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: f5b48f8cd4ef6ff41733ec9a18d1ab682f5e6bcb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784717"
---
# <a name="mapi-status-objects"></a>Objets d’état MAPI

  
  
**S’applique à**: Outlook 
  
Objets d’état signalent des informations sur les ressources MAPI. Par exemple, un fournisseur de services, le processus d’envoi/réception MAPI ou le carnet d’adresses.
  
Il existe un objet de l’état en fournissant des informations sur chaque fournisseur de services individuels dans le profil actif. MAPI est responsable de l’implémentation d’objets d’état pour le carnet d’adresses, le processus d’envoi/réception MAPI et du sous-système. L’objet de l’état du sous-système fournit des informations globales. L’objet d’état pour le carnet d’adresses intégré fournit l’état de tous les fournisseurs de carnet d’adresses en cours d’exécution.
  
Chaque objet de l’état est inclus dans la table d’état, une table gérée par MAPI qui fournit aux clients avec toutes les informations d’état de la session. Pour plus d’informations, voir [Tableaux d’état](status-tables.md). Clients peuvent accéder à un objet d’état spécifique par le biais de la table ou, pour un fournisseur de service, par le biais de son objet d’ouverture de session. Par exemple, pour accéder aux objets de l’état d’un fournisseur de carnet d’adresses, un client peut appeler **IABLogon::OpenStatusEntry**. Pour plus d’informations, voir [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).
  
Clients peuvent utiliser les objets d’état :
  
- Obtenir des informations sur l’état d’une session.
    
- Surveiller un fournisseur de services.
    
- Contrôle la transmission des messages.
    
- Afficher ou modifier la configuration et l’état d’une ressource.
    
Chaque objet état implémente l’interface **IMAPIStatus** . Pour plus d’informations, voir [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md). Toutefois, non à chaque objet état prend entièrement en charge chaque méthode **IMAPIStatus** . Étant donné que les variantes dans les méthodes qui sont pris en charge par un objet d’état, les clients ont besoin pour en savoir plus sur un objet d’état spécifique avant de pouvoir l’utiliser. Objets d’état sont requises pour publier des informations sur les fonctionnalités dans les trois propriétés suivantes : 
  
 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) 
  
 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 
  
 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 
  
Pour plus d’informations sur l’implémentation d’un objet d’état, voir [Implémentation d’objet état](status-object-implementation.md). Pour plus d’informations sur l’utilisation d’un objet d’état, voir la [Table d’état et les objets d’état](status-table-and-status-objects.md).
  

