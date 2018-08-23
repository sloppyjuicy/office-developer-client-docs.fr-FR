---
title: Tables de services de messagerie
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 569c1bd7ee2f4ac6c321f234be2954a57715549b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576667"
---
# <a name="message-service-tables"></a>Tables de services de messagerie

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Le tableau de service de message contient des informations sur les services de messagerie dans le profil actif. Il existe une table de service de message pour chaque session MAPI, implémentés par MAPI et utilisé par les applications clientes spécial qui fournissent la prise en charge de la configuration. 
  
Le tableau de service de message est une table statique.
  
Clients accèdent à la table de service de message en appelant la méthode [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) . 
  
Les propriétés suivantes constituent la colonne requise dans la table de service de message :
  
|||
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))  <br/> |
|**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))  <br/> |**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |
|**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** est le nom complet pour le service de message et la colonne de clé de tri par défaut. 
  
 **PR_INSTANCE_KEY** sert de la colonne d’index de la table, identifie de manière unique une ligne. 
  
 **PR_RESOURCE_FLAGS** décrit les fonctionnalités du service de message. 
  
 **PR_SERVICE_DLL_NAME** est le nom de la DLL qui contient l’implémentation de service de message. 
  
 **PR_SERVICE_ENTRY_NAME** est le nom de la fonction de point d’entrée du service de message qui est conforme au prototype [MSGSERVICEENTRY](msgserviceentry.md) . 
  
 **PR_SERVICE_NAME** est obligatoire dans la section **[Services]** dans MAPISVC.INF. La valeur de cette propriété ne sera jamais modifiée ou localisée. **PR_SERVICE_NAME** peuvent servir à identifier par programme le service de message. 
  
 **PR_SERVICE_SUPPORT_FILES** est une liste de fichiers qui doivent être installés avec le service de message. 
  
 **PR_SERVICE_UID** est un identificateur unique pour le service de message. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

