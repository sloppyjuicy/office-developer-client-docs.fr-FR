---
title: Propriété canonique PidTagLongTermEntryIdFromTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagLongTermEntryIdFromTable
api_type:
- HeaderDef
ms.assetid: d9457fea-4b1e-4cf6-9c4b-14c98fbec2a1
description: Obtient l’identificateur d’entrée à long terme d’un élément. Cette propriété peut être utilisée pour obtenir l’identificateur d’entrée d’un élément en tant qu’identificateur d’entrée à long terme.
ms.openlocfilehash: 4434bca9445fe9291483e0355bab0ded5c6263c3
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405243"
---
# <a name="pidtaglongtermentryidfromtable-canonical-property"></a>Propriété canonique PidTagLongTermEntryIdFromTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Obtient l’identificateur d’entrée à long terme d’un élément.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_LONGTERM_ENTRYID_FROM_TABLE  <br/> |
|Identificateur :  <br/> |0x6670  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés du tableau  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut être utilisée dans une table des matières pour obtenir l’identificateur d’entrée d’un élément en tant qu’identificateur d’entrée à long terme au lieu d’un identificateur d’entrée à court terme. Pour plus d’informations sur les identificateurs à long et court terme, voir **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagEntryId](pidtagentryid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

