---
title: Tables des fournisseurs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99709a4c-cb52-436e-a322-02ded5d65ce5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2b81f4aebae692d28ed492df102d59ba34debf63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328461"
---
# <a name="provider-tables"></a>Tables des fournisseurs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table de fournisseurs contient des informations sur les fournisseurs de services. Il existe deux tables de fournisseurs différentes, implémentées par MAPI et utilisées par les clients. Le premier tableau, consulté en appelant la méthode [IMsgServiceAdmin:: GetProviderTable](imsgserviceadmin-getprovidertable.md) , contient des informations sur tous les fournisseurs du profil actuel. La seconde table, accessible via [IProviderAdmin:: GetProviderTable](iprovideradmin-getprovidertable.md), crée une table qui stocke des informations sur tous les fournisseurs de services pour un service de messagerie.
  
Ces deux tables présentent une autre différence. La table du fournisseur disponible via **IMsgServiceAdmin:: GetProviderTable** contient uniquement les lignes qui représentent les fournisseurs de services, tandis que la table disponible par le biais de **IProviderAdmin:: GetProviderTable** peut inclure des lignes qui représentent informations supplémentaires associées à un fournisseur de services. Ces informations supplémentaires sont ajoutées au profil avec le mot clé «sections» du fichier MAPISVC. INF. Lorsqu'un fournisseur dispose de sections de profil supplémentaires, il stocke les valeurs **MAPIUID** de ces sections dans la propriété **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **PR_SERVICE_EXTRA_UIDS** est enregistré dans la section du profil de service de messagerie. 
  
Les propriétés suivantes constituent le jeu de colonnes obligatoire dans les deux types de tables de fournisseur:
  
|||
|:-----|:-----|
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))  <br/> |**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
|**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
La table du fournisseur peut être utilisée pour afficher l'ordre de transport actuel ou pour le modifier. Pour afficher la commande actuelle, générez une restriction pour récupérer uniquement les lignes dont la propriété **PR_RESOURCE_TYPE** a la valeur MAPI_TRANSPORT_PROVIDER. Utilisez ensuite **PR_PROVIDER_ORDINAL** comme clé de tri pour trier le tableau et récupérer toutes les lignes à l'aide de la méthode [IMAPITable:: QueryRows](imapitable-queryrows.md) ou de la fonction [HrQueryAllRows](hrqueryallrows.md) . 
  
Pour modifier l'ordre de transport, appliquez la même restriction et extrayez les lignes. Créez ensuite un tableau de valeurs à partir de la propriété **PR_PROVIDER_UID** qui représente les identificateurs uniques des fournisseurs de transport. Lorsque les identificateurs sont dans l'ordre souhaité, transmettez-les à la méthode [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) . 
  
Une fois qu'une table de fournisseurs est rendue disponible, elle ne reflète pas les modifications ultérieures, telles que l'ajout ou la suppression d'un fournisseur.
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

