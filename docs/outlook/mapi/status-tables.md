---
title: Tables d’état
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f2b2aca7-757f-4260-96a5-d0af55189711
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d612738ef8bf0e6925d89a5be7cb423695672d28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422361"
---
# <a name="status-tables"></a>Tables d’état

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La table d’état contient des informations relatives à l’état de la session en cours. Il existe une table d’état pour chaque session MAPI qui inclut les informations fournies par MAPI et par les fournisseurs de services. MAPI fournit des données pour trois lignes : une ligne pour le sous-système MAPI, une ligne pour lepooler MAPI et une ligne pour le carnet d’adresses intégré. Étant donné que les fournisseurs de transport sont tenus de fournir des informations d’état à la table d’état, il existe une ligne pour chaque fournisseur de transport actif. Les fournisseurs de carnet d’adresses et de magasin de messages peuvent choisir de prendre en charge la table d’état. 
  
Étant donné que chaque ligne est fournie par une ressource différente, l’ensemble des colonnes peut varier d’une ligne à l’autre. Chaque objet d’état doit fournir un ensemble de colonnes et un ensemble de colonnes que MAPI fournit. Un fournisseur de services peut ajouter à ces ensembles pour exposer des propriétés spécifiques au fournisseur. Par exemple, les fournisseurs de magasins de messages peuvent ajouter PR_STORE_RECORD_KEY **(** [PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) pour fournir aux clients l’identificateur de leur magasin de messages. Les clients doivent avoir une connaissance avancée de l’existence de ces informations supplémentaires pour pouvoir les utiliser. 
  
Le tableau suivant répertorie les propriétés qui doivent se trouver dans chaque ligne de tableau d’état. L’implémenteur de l’objet d’état fournit certaines des propriétés ; d’autres sont calculées par MAPI.
  
|**Propriétés fournies par l’objet status**|**Propriétés fournies par MAPI**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
Si l’objet d’état fournit une identité, il doit définir **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)), **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) et **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)), et inclure ces propriétés dans la table. 
  
Quatre propriétés sont calculées par MAPI pour chaque ligne de tableau d’état :
  
|||
|:-----|:-----|
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))  <br/> |
   
MAPI affecte un identificateur d’entrée à la ligne d’état pour permettre aux clients d’ouvrir l’objet d’état correspondant. Un identificateur de ligne est également affecté pour identifier la ligne dans le tableau comme il s’agit d’une clé d’instance pour identifier les données dans l’objet d’état. La **propriété PR_OBJECT_TYPE** est définie sur MAPI_STATUS. 
  
Pour accéder à la table d’état, les clients appellent la méthode [IMAPISession::GetStatusTable.](imapisession-getstatustable.md) Cet appel ne doit pas être effectué immédiatement au démarrage. Cela est dû au fait que **GetStatusTable** doit attendre que lepooler MAPI initialise les fournisseurs de transport, opération qui est différée jusqu’à ce que le client ait terminé sa ouverture de compte. **GetStatusTable est** un appel relativement rapide une fois que lepooler MAPI a terminé son traitement de démarrage. 
  
Les informations de la table d’état peuvent être utilisées de différentes manières, par exemple pour accéder à un objet d’état, pour déterminer si un client est en cours d’exécution en mode connecté ou hors connexion, et pour surveiller l’état d’un fournisseur. Par exemple, les clients peuvent ouvrir l’objet d’état d’un fournisseur de services spécifique en passant la valeur de la propriété **PR_ENTRYID** à la méthode [IMAPISession::OpenEntry.](imapisession-openentry.md) L’objet d’état prend en charge l’interface **IMAPIStatus,** une interface qui contient des méthodes pour modifier un mot de passe de fournisseur de services, vider la file d’attente des messages, afficher une feuille des propriétés de configuration ou confirmer l’état auprès d’un fournisseur directement. Les informations de la table d’état peuvent également être utilisées pour créer une boîte de dialogue afin d’informer les clients de la progression au cours d’une longue opération. 
  
Les fournisseurs de services qui utilisent la table d’état utilisent la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) pour créer et mettre à jour leur ligne. Chaque fois qu’une modification a lieu sur leur ligne, tous les objets de réception inscrits pour recevoir des notifications de table d’état doivent être avertis. Les fournisseurs de services peuvent appeler la méthode [IMAPISupport::Notify](imapisupport-notify.md) s’ils utilisent l’utilitaire de notification MAPI ou appeler directement la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de chaque réception de notification. 
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

