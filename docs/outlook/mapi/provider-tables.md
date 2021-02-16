---
title: Tables des fournisseurs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99709a4c-cb52-436e-a322-02ded5d65ce5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2b81f4aebae692d28ed492df102d59ba34debf63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408970"
---
# <a name="provider-tables"></a>Tables des fournisseurs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table de fournisseurs contient des informations sur les fournisseurs de services. Il existe deux tables de fournisseurs différentes, toutes deux implémentées par MAPI et utilisées par les clients. Le premier tableau, accessible en appelant la méthode [IMsgServiceAdmin::GetProviderTable,](imsgserviceadmin-getprovidertable.md) contient des informations sur tous les fournisseurs pour le profil actuel. Le deuxième tableau, accessible via [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md), crée une table qui stocke des informations sur tous les fournisseurs de services pour un service de messagerie.
  
Ces deux tableaux ont une autre différence. La table fournisseur disponible via **IMsgServiceAdmin::GetProviderTable** contient uniquement des lignes qui représentent des fournisseurs de services, tandis que la table disponible via **IProviderAdmin::GetProviderTable** peut inclure des lignes qui représentent des informations supplémentaires associées à un fournisseur de services. Ces informations supplémentaires sont ajoutées au profil avec le mot clé « Sections » de MAPISVC.INF. Lorsqu’un fournisseur possède des sections de profil supplémentaires, il stocke les valeurs **MAPIUID** de ces sections dans la propriété **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **PR_SERVICE_EXTRA_UIDS** est enregistré dans la section profil du service de message. 
  
Les propriétés suivantes définissent la colonne requise dans les deux types de tables de fournisseurs :
  
|||
|:-----|:-----|
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))  <br/> |**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
|**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
La table fournisseur peut être utilisée pour afficher l’ordre de transport actuel ou pour le modifier. Pour afficher l’ordre actuel, créez une restriction pour récupérer uniquement ces lignes avec la propriété **PR_RESOURCE_TYPE** définie sur MAPI_TRANSPORT_PROVIDER. Utilisez ensuite **PR_PROVIDER_ORDINAL** comme clé de tri pour trier le tableau et récupérer toutes les lignes avec la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) ou la fonction [HrQueryAllRows.](hrqueryallrows.md) 
  
Pour modifier l’ordre de transport, appliquez la même restriction et récupérez les lignes. Ensuite, créez un tableau de valeurs à partir **de la propriété PR_PROVIDER_UID** qui représente les identificateurs uniques pour les fournisseurs de transport. Lorsque les identificateurs sont dans l’ordre souhaité, passez-les à la méthode [IMsgServiceAdmin::MsgServiceTransportOrder.](imsgserviceadmin-msgservicetransportorder.md) 
  
Une fois qu’une table de fournisseurs a été rendue disponible, elle ne reflète pas les modifications ultérieures, telles que l’ajout ou la suppression d’un fournisseur.
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

