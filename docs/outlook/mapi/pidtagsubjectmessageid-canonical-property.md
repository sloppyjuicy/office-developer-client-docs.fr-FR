---
title: Propriété canonique PidTagSubjectMessageId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSubjectMessageId
api_type:
- COM
ms.assetid: d4b1a087-0986-467a-aaa9-fc643f7c56fc
description: Contient une valeur binaire qui est copiée à partir du message pour lequel un rapport est généré. Cette propriété peut corréler un état avec le message d’origine.
ms.openlocfilehash: 287ea99ac7377f8d300aecc0cee4fa7ae39dc70b
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64456335"
---
# <a name="pidtagsubjectmessageid-canonical-property"></a>Propriété canonique PidTagSubjectMessageId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur binaire qui est copiée à partir du message pour lequel un rapport est généré. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SUBJECT_IPM  <br/> |
|Identificateur :  <br/> |0x0038  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété, comme la **propriété PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)), peut être utilisée pour corréler un état avec le message d’origine. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

