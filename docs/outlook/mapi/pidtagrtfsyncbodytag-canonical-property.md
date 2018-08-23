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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c141ce5b4a8d44cc42a070d73e8e89f35e776fe9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576855"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a>Propriété canonique PidTagRtfSyncBodyTag

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient des caractères significatifs qui s’affichent au début du texte du message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W  <br/> |
|Identificateur :  <br/> |0 x 1008  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Message MAPI  <br/> |
   
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
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

