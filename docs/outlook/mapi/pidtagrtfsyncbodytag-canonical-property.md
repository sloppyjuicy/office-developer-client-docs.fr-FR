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
ms.openlocfilehash: 24ef1d4e3e936426aea8216119e8ada9f6122e95
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331177"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a>Propriété canonique PidTagRtfSyncBodyTag

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des caractères significatifs qui apparaissent au début du texte du message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W  <br/> |
|Identificateur :  <br/> |0x1008  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Message MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

La fonction [RTFSync](rtfsync.md) utilise la balise de texte pour indiquer le début du texte du message. Lorsque le texte est modifié, la balise est utilisée pour rechercher le début du texte précédent. 
  
Ces propriétés sont des propriétés auxiliaires au format texte enrichi. Elles sont utilisées par la fonction **RTFSync** et ne sont pas destinées à être utilisées directement par les applications clientes. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Encode et décode les objets message et Attachment en une représentation de flux efficace.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

