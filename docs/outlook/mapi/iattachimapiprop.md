---
title: IAttach IMAPIProp
description: Cet article décrit IAttach IMAPIProp fournissant l’accès aux propriétés des pièces jointes dans les messages.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAttach
api_type:
- COM
ms.assetid: f47e20e1-2a30-4c9e-8ca6-e8c5e72f44a1
ms.openlocfilehash: d81fe90d161ed2817a5c7d7e544c06a29e645085
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812326"
---
# <a name="iattach--imapiprop"></a>IAttach : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Conserve et fournit l’accès aux propriétés des pièces jointes dans les messages. **L’interface IAttach** n’a pas de méthode unique. Pour plus d’informations sur l’utilisation des pièces jointes, consultez [Les pièces jointes MAPI et les](mapi-attachments.md) [tables de pièces jointes](attachment-tables.md). 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets de pièce jointe  <br/> |
|Implémenté par :  <br/> |Fournisseurs de magasins de messages  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IAttachment  <br/> |
|Type de pointeur :  <br/> |LPATTACH  <br/> |
|Modèle de transaction :  <br/> |Traitées  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

Cette interface n’a pas de méthodes uniques.
  
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
|**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

