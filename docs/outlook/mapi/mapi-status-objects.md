---
title: Objets d'État MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 816d1b7c9c0b8c5a80a2351580ce3224fccf0b14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309533"
---
# <a name="mapi-status-objects"></a>Objets d'État MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les objets d'État indiquent des informations sur les ressources MAPI. Par exemple, un fournisseur de services, le processus d'envoi/réception MAPI ou le carnet d'adresses.
  
Un objet d'État fournit des informations sur chaque fournisseur de services dans le profil actuel. MAPI est responsable de l'implémentation des objets d'État pour le sous-système, le processus d'envoi/réception MAPI et le carnet d'adresses. L'objet état du sous-système fournit des informations globales. L'objet Status du carnet d'adresses intégré fournit l'état de tous les fournisseurs de carnet d'adresses en cours d'utilisation.
  
Chaque objet Status est inclus dans le tableau d'État, une table gérée par MAPI qui fournit aux clients toutes les informations d'état de la session. Pour plus d'informations, consultez la rubrique [tables d'État](status-tables.md). Les clients peuvent accéder à un objet d'état particulier via la table ou, pour un fournisseur de services, par le biais de son objet d'ouverture de session. Par exemple, pour accéder à l'objet d'état d'un fournisseur de carnet d'adresses, un client peut appeler **IABLogon:: OpenStatusEntry**. Pour plus d'informations, voir [IABLogon:: OpenStatusEntry](iablogon-openstatusentry.md).
  
Les clients peuvent utiliser des objets d'État pour:
  
- Découvrez l'état d'une session.
    
- SurVeillez un fournisseur de services.
    
- Contrôler la transmission des messages.
    
- Afficher ou modifier la configuration et l'état d'une ressource.
    
Chaque objet Status implémente l'interface **IMAPIStatus** . Pour plus d'informations, voir [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md). Toutefois, tous les objets d'État ne prennent pas totalement en charge toutes les méthodes **IMAPIStatus** . Étant donné qu'il existe des variantes des méthodes prises en charge par un objet Status, les clients doivent en savoir plus sur un objet Status particulier avant de pouvoir l'utiliser. Les objets d'État sont requis pour publier des informations sur leurs fonctionnalités dans les trois propriétés suivantes: 
  
 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) 
  
 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 
  
 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 
  
Pour plus d'informations sur l'implémentation d'un objet [](status-object-implementation.md)Status, voir Status Implementation. Pour plus d'informations sur l'utilisation d'un objet Status, consultez la rubrique [table d'État et objets d'État](status-table-and-status-objects.md).
  

