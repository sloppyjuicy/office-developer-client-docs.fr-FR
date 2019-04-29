---
title: Tables des services de messagerie
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c644e89511033234aa45c5f82738e4c471ef646d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422494"
---
# <a name="message-service-tables"></a>Tables des services de messagerie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La table service de messagerie contient des informations sur les services de messagerie dans le profil actif. Il existe une table de service de messagerie pour chaque session MAPI, implémentée par MAPI et utilisée par des applications clientes à vocation spéciale qui fournissent la prise en charge de la configuration. 
  
La table des services de messagerie est une table statique.
  
Les clients accèdent à la table de service de message en appelant la méthode [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) . 
  
Les propriétés suivantes constituent le jeu de colonnes obligatoire dans le tableau service de message:
  
|||
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))  <br/> |
|**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))  <br/> |**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |
|**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** est le nom affichable pour le service de messagerie et la colonne clé de tri par défaut. 
  
 **PR_INSTANCE_KEY** sert de colonne d'index pour la table et identifie de manière unique une ligne. 
  
 **PR_RESOURCE_FLAGS** décrit les fonctionnalités du service de messagerie. 
  
 **PR_SERVICE_DLL_NAME** est le nom de la dll qui contient l'implémentation du service de messagerie. 
  
 **PR_SERVICE_ENTRY_NAME** est le nom de la fonction de point d'entrée du service de messagerie conforme au prototype [MSGSERVICEENTRY](msgserviceentry.md) . 
  
 **PR_SERVICE_NAME** est une entrée obligatoire dans la section **[services]** du fichier MAPISVC. inf. La valeur de cette propriété ne sera jamais changée ou localisée. **PR_SERVICE_NAME** peut être utilisé pour identifier le service de messagerie par programme. 
  
 **PR_SERVICE_SUPPORT_FILES** est une liste de fichiers qui doit être installée avec le service de messagerie. 
  
 **PR_SERVICE_UID** est un identificateur unique pour le service de messagerie. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

