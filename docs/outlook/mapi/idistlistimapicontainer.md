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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 463d81a6692b6071cada0ad22e7343020563e41c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350889"
---
# <a name="idistlist--imapicontainer"></a>IDistList : IMAPIContainer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d'accéder à des listes de distribution dans des conteneurs de carnet d'adresses modifiables. **IDistList** peut créer, copier et supprimer des listes de distribution, en plus d'effectuer la résolution de noms. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Exposé par:  <br/> |Objets de liste de distribution  <br/> |
|Implémenté par :  <br/> |Fournisseurs de carnets d'adresses  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur de l'interface:  <br/> |IID_IDistList  <br/> |
|Type de pointeur:  <br/> |LPDISTLIST  <br/> |
|Modèle de transaction:  <br/> |Traitées  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

Cette interface n'a pas de méthodes uniques.
  
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |En lecture-écriture.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |En lecture-écriture.  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

L'interface **IDistList** hérite de [IMAPIContainer](imapicontainerimapiprop.md) et inclut les mêmes méthodes que les conteneurs de carnet d'adresses. Par conséquent, étant donné que les méthodes de l'interface **IDistList** sont identiques à celles de l'interface [IABContainer](iabcontainerimapicontainer.md) , elles ne sont pas dupliquées ici. 
  
Une liste de distribution ou un objet qui implémente **IDistList** est une collection d'objets utilisateur de messagerie ou de destinataires individuels. Une liste de distribution peut être constituée de tous les objets utilisateur de messagerie ou d'un utilisateur de messagerie et de certaines listes de distribution. 
  
Il existe généralement deux types de listes de distribution:
  
- Listes de distribution qui sont développées par le système de messagerie sous-jacent. Ce type de liste a une adresse, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) et est traité de la même manière que s'il s'agissait d'un destinataire individuel. 
    
- Les listes de distribution qui existent dans un conteneur local et sont développées par l'application cliente.
    
Les propriétés de liste de distribution facultatives sont les suivantes:
  
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) 
    
- **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) 
    
Notez que **PR_ADDRTYPE** est requis, mais que **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) ne l'est pas. En effet, une liste de distribution sans adresse de messagerie peut toujours recevoir des messages, mais sa liste de membres doit être développée. Si la propriété **PR_ADDRTYPE** est définie sur MAPIPDL, MAPI effectue l'expansion. Si **PR_ADDRTYPE** est une valeur autre que MAPIPDL, le fournisseur de transport effectue l'expansion. 
  
Pour plus d'informations sur l'utilisation des méthodes **IDistList** , voir les entrées de référence pour les méthodes parallèles de **IABContainer**.
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

