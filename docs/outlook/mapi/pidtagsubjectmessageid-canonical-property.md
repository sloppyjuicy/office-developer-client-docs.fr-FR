---
title: Propriété canonique PidTagSubjectMessageId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubjectMessageId
api_type:
- COM
ms.assetid: d4b1a087-0986-467a-aaa9-fc643f7c56fc
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c89a0a86ac733cd2cce1efc071e47fcb011fec18
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573067"
---
# <a name="pidtagsubjectmessageid-canonical-property"></a>Propriété canonique PidTagSubjectMessageId

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient une valeur binaire qui est copiée à partir du message pour lequel un rapport est généré. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SUBJECT_IPM  <br/> |
|Identificateur :  <br/> |0x0038  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété, comme la propriété **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)), peut être utilisée pour faire correspondre un rapport avec le message d’origine. 
  
## <a name="related-resources"></a>Ressources connexes

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

