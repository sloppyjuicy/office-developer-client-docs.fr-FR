---
title: Tables du fournisseur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99709a4c-cb52-436e-a322-02ded5d65ce5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a613bd744a113b4378c5bef94fb51f6ae3aa4041
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786953"
---
# <a name="provider-tables"></a>Tables du fournisseur

  
  
**S’applique à**: Outlook 
  
Une table fournisseur contient des informations sur les fournisseurs de services. Il existe deux tables autre fournisseur, implémentés par MAPI et utilisé par les clients. La première table, accédée en appelant la méthode [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) , conserve des informations sur tous les fournisseurs pour le profil actuel. Le deuxième tableau, accédé via [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md), crée une table qui stocke des informations sur tous les fournisseurs de services d’un service de message.
  
Ces deux tables ont une autre différence. Le tableau de fournisseur disponible par le biais de **IMsgServiceAdmin::GetProviderTable** contient uniquement les lignes qui représentent les fournisseurs de services pendant la table disponible par le biais de **IProviderAdmin::GetProviderTable** peut inclure des lignes qui représentent les informations supplémentaires associées à un fournisseur de services. Cette information supplémentaire est ajoutée au profil avec le mot clé « Sections » du fichier MAPISVC.INF. Lorsqu’un fournisseur comporte des sections de profil supplémentaires, il stocke les valeurs **MAPIUID** pour ces sections dans la propriété **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **PR_SERVICE_EXTRA_UIDS** est enregistré dans la section de profil de service de message. 
  
Les propriétés suivantes constituent la colonne obligatoire définie dans les deux types de tables du fournisseur :
  
|||
|:-----|:-----|
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))  <br/> |**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
|**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
La table fournisseur peut être utilisée pour afficher l’ordre de transport actuel ou pour le modifier. Pour afficher l’ordre actuel, créez une restriction pour récupérer uniquement les lignes avec la propriété **PR_RESOURCE_TYPE** MAPI_TRANSPORT_PROVIDER. Utilisez ensuite **PR_PROVIDER_ORDINAL** comme clé de tri pour trier le tableau et extraire toutes les lignes avec la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) ou de la fonction [HrQueryAllRows](hrqueryallrows.md) . 
  
Pour modifier l’ordre de transport, appliquer la même restriction et extraire les lignes. Ensuite, créez un tableau de valeurs à partir de la propriété **PR_PROVIDER_UID** qui représente les identificateurs uniques pour les fournisseurs de transport. Lorsque les identificateurs sont dans l’ordre souhaité, les passer à la méthode [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) . 
  
Après une table fournisseur disponible, il ne reflète pas les modifications ultérieures, telles que l’ajout ou la suppression d’un fournisseur.
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

