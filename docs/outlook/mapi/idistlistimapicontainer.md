---
title: IDistList IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IDistList
api_type:
- COM
ms.assetid: bd8e1ddb-3027-428b-8964-81614f80282d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 463d81a6692b6071cada0ad22e7343020563e41c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431546"
---
# <a name="idistlist--imapicontainer"></a>IDistList : IMAPIContainer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder aux listes de distribution dans les conteneurs de carnet d’adresses modifiables. **IDistList peut** créer, copier et supprimer des listes de distribution, en plus d’effectuer une résolution de nom. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets de liste de distribution  <br/> |
|Implémenté par :  <br/> |Fournisseurs de carnets d’adresses  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IDistList  <br/> |
|Type de pointeur :  <br/> |LPDISTLIST  <br/> |
|Modèle de transaction :  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

Cette interface n’a pas de méthode unique.
  
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

**L’interface IDistList** hérite d’IMAPIContainer et inclut les mêmes méthodes que les conteneurs de carnet d’adresses. [](imapicontainerimapiprop.md) Par conséquent, étant donné que les méthodes de l’interface **IDistList** sont identiques à celles de l’interface [IABContainer,](iabcontainerimapicontainer.md) elles ne sont pas dupliquées ici. 
  
Une liste de distribution ou un objet qui implémente **IDistList** est une collection d’objets utilisateur de messagerie ou de destinataires individuels. Une liste de distribution peut se composer de tous les objets utilisateur de messagerie, ou d’un utilisateur de messagerie et de certaines listes de distribution. 
  
Il existe généralement deux types de listes de distribution :
  
- Listes de distribution étendues par le système de messagerie sous-jacent. Ce type de liste a une adresse, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), et est traité comme s’il s’agit d’un destinataire individuel. 
    
- Listes de distribution qui existent dans un conteneur local et qui sont étendues par l’application cliente.
    
Les propriétés de liste de distribution facultatives sont les suivantes :
  
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) 
    
- **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) 
    
Notez **que PR_ADDRTYPE** est obligatoire, mais **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) ne l’est pas. En effet, une liste de distribution sans adresse de messagerie peut toujours recevoir des messages, mais sa liste de membres doit être étendue. Si la **PR_ADDRTYPE** est définie sur MAPIPDL, MAPI effectue l’expansion. Si **PR_ADDRTYPE** est une valeur autre que MAPIPDL, le fournisseur de transport effectue l’expansion. 
  
Pour plus d’informations sur l’utilisation des méthodes **IDistList,** voir les entrées de référence pour les méthodes parallèles de **IABContainer**.
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

