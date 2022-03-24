---
title: Tables des services de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: Le tableau des services de message contient des informations sur les services de message dans le profil actuel. Il existe une table de service de message pour chaque session MAPI.
ms.openlocfilehash: 6cf7cb698244a73f435d69752246ef2a45d761fb
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63763375"
---
# <a name="message-service-tables"></a>Tables des services de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le tableau des services de message contient des informations sur les services de message dans le profil actuel. Il existe une table de service de message pour chaque session MAPI, implémentée par MAPI et utilisée par des applications clientes à usage spécifique qui fournissent la prise en charge de la configuration. 
  
La table de service de message est une table statique.
  
Les clients accèdent à la table de service de message en appelant la méthode [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) . 
  
Les propriétés suivantes définissent la colonne requise dans la table de service de message :
  
|Property |... |
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))  <br/> |
|**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))  <br/> |**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |
|**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** est le nom affichable pour le service de message et la colonne de clé de tri par défaut. 
  
 **PR_INSTANCE_KEY** sert de colonne d’index pour la table, identifiant de manière unique une ligne. 
  
 **PR_RESOURCE_FLAGS** décrit les fonctionnalités du service de message. 
  
 **PR_SERVICE_DLL_NAME** est le nom de la DLL qui contient l’implémentation du service de message. 
  
 **PR_SERVICE_ENTRY_NAME** est le nom de la fonction de point d’entrée du service de message conforme au prototype [MSGSERVICEENTRY](msgserviceentry.md) . 
  
 **PR_SERVICE_NAME** est une entrée obligatoire dans la section **[Services]** de MAPISVC.INF. La valeur de cette propriété ne sera jamais modifiée ni localisée. **PR_SERVICE_NAME** permet d’identifier par programme le service de message. 
  
 **PR_SERVICE_SUPPORT_FILES** liste des fichiers qui doivent être installés avec le service de message. 
  
 **PR_SERVICE_UID** est un identificateur unique pour le service de message. 
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

