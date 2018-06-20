---
title: Tableaux d’état
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f2b2aca7-757f-4260-96a5-d0af55189711
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: afbef333af46051284fa51d52c2e3f77607b0b13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787262"
---
# <a name="status-tables"></a>Tableaux d’état

  
  
**S’applique à**: Outlook 
  
La table d’état contient des informations relatives à l’état de la session en cours. Il existe une table d’état pour chaque session MAPI qui inclut les informations fournies par MAPI et par les fournisseurs de services. MAPI fournit les données de trois lignes : une ligne pour le sous-système MAPI, une ligne pour le spouleur MAPI et une ligne pour le carnet d’adresses intégré. Étant donné que les fournisseurs de transport requis pour fournir des informations d’état à la table d’état, il est une ligne pour chaque fournisseur de transport actif. Fournisseurs de magasin de messages et du carnet d’adresses peuvent choisir prendre en charge de la table d’état. 
  
Étant donné que chaque ligne est fournie par une ressource différente, l’ensemble des colonnes peut varier d’une ligne. Il existe un ensemble de colonnes de chaque objet de l’état est requis pour fournir et un ensemble de colonnes qui fournit les MAPI. Un fournisseur de services peut ajouter à ces jeux à exposer des propriétés spécifiques au fournisseur. Par exemple, les fournisseurs de magasins de message peuvent ajouter **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) pour fournir aux clients avec l’identificateur de leur banque de messages. Les clients doivent connaître avance de l’existence de ces informations supplémentaires pour pouvoir l’utiliser. 
  
Le tableau suivant répertorie les propriétés qui doivent se trouver dans chaque ligne du tableau état. L’implémentation de l’objet status fournit des propriétés ; d’autres personnes sont calculées par MAPI.
  
|**Propriétés fournies par l’objet d’état**|**Propriétés fournies par MAPI**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
Si l’objet d’état fournit une identité, il doit définir **PR_IDENTITY_SEARCH_KEY** ([ , **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) et **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) et incluez ces propriétés dans le tableau. 
  
Quatre propriétés sont calculées par MAPI pour chaque ligne de table d’état :
  
|||
|:-----|:-----|
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))  <br/> |
   
MAPI affecte un identificateur d’entrée à la ligne d’état pour permettre aux clients d’ouvrir l’objet état correspondant. Un identificateur de ligne est également assigné à identifier la ligne dans le tableau étant une instance key pour identifier les données dans l’objet d’état. La propriété **PR_OBJECT_TYPE** est définie à MAPI_STATUS. 
  
Pour accéder à la table d’état, les clients appeler la méthode [IMAPISession::GetStatusTable](imapisession-getstatustable.md) . Cet appel ne doit pas être apporté immédiatement au démarrage. Il s’agit car **GetStatusTable** doit attendre le spouleur MAPI initialiser les fournisseurs de transport, une opération est différée jusqu'à une fois que le client a terminé son ouverture de session. **GetStatusTable** est un appel relativement rapide après que le spouleur MAPI a terminé son traitement de démarrage. 
  
Informations de table d’état peuvent être utilisées dans de diverses façons, tels que pour accéder à un objet d’état, afin de déterminer si un client est en cours d’exécution en mode connecté ou hors connexion et de surveiller l’état d’un fournisseur. Par exemple, les clients peuvent ouvrir objet d’état d’un fournisseur de service spécifique en passant la valeur de la propriété **PR_ENTRYID** à la méthode [IMAPISession::OpenEntry](imapisession-openentry.md) . L’objet état prend en charge l’interface **IMAPIStatus** , une interface qui contient des méthodes pour modifier un mot de passe de fournisseur de service, vider la file d’attente, afficher une feuille de propriétés de configuration ou confirmer le statut directement avec un fournisseur. Informations d’état table peuvent également servir à créer une boîte de dialogue pour informer les clients de progression pendant une longue opération. 
  
Fournisseurs de services qui ne prennent pas en charge la table d’état utilisent la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) pour créer et mettre à jour leur ligne. Chaque fois qu’une modification est apportée à leur ligne, tous les conseiller objets récepteur inscrits pour recevoir des notifications d’état de tableau doivent être avertis. Fournisseurs de services peuvent appeler la méthode [IMAPISupport::Notify](imapisupport-notify.md) s’ils sont à l’aide de l’utilitaire de notification MAPI ou appellent directement la méthode de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de chaque récepteur de notifications. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

