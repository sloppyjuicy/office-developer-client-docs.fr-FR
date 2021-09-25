---
title: IAttach IMAPIProp
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c67ce8be8cd1389a985f8762759a0136c5f81c1b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580040"
---
# <a name="iattach--imapiprop"></a>IAttach : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Maintient et fournit l’accès aux propriétés des pièces jointes dans les messages. **L’interface IAttach** n’a aucune méthode unique. Pour plus d’informations sur l’utilisation des pièces jointes, voir [Pièces jointes MAPI](mapi-attachments.md) et tables de pièces [jointes.](attachment-tables.md) 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets de pièce jointe  <br/> |
|Implémenté par :  <br/> |Fournisseurs de magasins de messages  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IAttachment  <br/> |
|Type de pointeur :  <br/> |LPATTACH  <br/> |
|Modèle de transaction :  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

Cette interface n’a pas de méthode unique.
  
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
|**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

