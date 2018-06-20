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
ms.openlocfilehash: 7fee3c84d6a4d4a94397f5197f45637b0c7dd2be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783679"
---
# <a name="idistlist--imapicontainer"></a>IDistList : IMAPIContainer

  
  
**S’applique à**: Outlook 
  
Fournit des conteneurs du carnet d’accès aux listes de distribution dans la zone Adresse modifiable. **IDistList** peut créer, copier et supprimer des listes de distribution, en plus de la résolution de nom. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposés par :  <br/> |Objets de liste de distribution  <br/> |
|Implémentée par :  <br/> |Fournisseurs de carnet d’adresses  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
|Identificateur de l’interface :  <br/> |IID_IDistList  <br/> |
|Type de pointeur :  <br/> |LPDISTLIST  <br/> |
|Modèle de transaction :  <br/> |Traitées  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

Cette interface n’a pas de méthodes uniques.
  
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |En lecture-écriture.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |En lecture-écriture.  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

L’interface **IDistList** hérite de [IMAPIContainer](imapicontainerimapiprop.md) et inclut les mêmes méthodes que les conteneurs de carnet d’adresses. Par conséquent, étant donné que les méthodes de l’interface **IDistList** sont identiques à celles de l’interface [IABContainer](iabcontainerimapicontainer.md) , ils ne sont pas dupliquées ici. 
  
Une liste de distribution ou un objet qui implémente **IDistList** est une collection d’objets utilisateur de la messagerie ou des destinataires individuels. Une liste de distribution peut se composer de tous les objets utilisateur messagerie, ou un utilisateur de messagerie et des listes de distribution. 
  
Il existe généralement deux types de listes de distribution :
  
- Listes de distribution sont développés par le système de messagerie sous-jacent. Ce type de liste possède une adresse, **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) et est traité comme s’il s’agissait d’une personne de la même. 
    
- Listes de distribution qui existent dans un conteneur local et sont développés par l’application cliente.
    
Propriétés de liste de distribution facultatifs sont les suivants :
  
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) 
    
- **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) 
    
Notez que **TYPEADR_PR** est requis, mais n’est pas **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)). C’est parce qu’une liste de distribution sans une adresse de messagerie peut toujours recevoir des messages, mais sa liste de membres doit être développée. Si la propriété **TYPEADR_PR** est définie à MAPIPDL, MAPI effectue le développement. Si **TYPEADR_PR** est une valeur autre que MAPIPDL, le fournisseur de transport effectue le développement. 
  
Pour plus d’informations sur la façon d’utiliser les méthodes **IDistList** , voir les entrées de référence pour les méthodes parallèles de **IABContainer**.
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

