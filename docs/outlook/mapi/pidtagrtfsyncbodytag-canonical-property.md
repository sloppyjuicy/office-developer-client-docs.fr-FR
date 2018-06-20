---
title: Propriété canonique PidTagRtfSyncBodyTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyTag
api_type:
- COM
ms.assetid: 2dab5018-4214-4162-93bc-e5565f3ac24c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bad754d21652d3f5278a6dad3ec06f4a0b533036
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786647"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a>Propriété canonique PidTagRtfSyncBodyTag

  
  
**S’applique à**: Outlook 
  
Contient des caractères significatifs qui s’affichent au début du texte du message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W  <br/> |
|Identificateur :  <br/> |0 x 1008  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |Message MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

La fonction [RTFSync](rtfsync.md) utilise la balise de texte pour indiquer le début du texte du message. Lorsque le texte est modifié, la balise est utilisée pour trouver le début du texte précédent. 
  
Ces propriétés sont des propriétés auxiliaires au Format RTF. Ils sont utilisés par la fonction **RTFSync** et ne sont pas destinés à être directement utilisé par les applications clientes. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

