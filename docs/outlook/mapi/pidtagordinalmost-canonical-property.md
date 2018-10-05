---
title: Propriété canonique PidTagOrdinalMost
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOrdinalMost
api_type:
- COM
ms.assetid: c18de08b-8c28-4cdf-bd2e-b9c650cd6da6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 31f39cfbd0e993bfc28003fd64e8af97e7e76818
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392423"
---
# <a name="pidtagordinalmost-canonical-property"></a>Propriété canonique PidTagOrdinalMost

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un nombre positif dont négatif est inférieure ou égale à la valeur de la propriété **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) de toutes les tâches dans le dossier.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORDINAL_MOST  <br/> |
|Identificateur :  <br/> |0x36E2  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit être mis à jour pour maintenir cette condition à chaque modification de la propriété **dispidTaskOrdinal** de tout objet de tâche dans le dossier d’une manière qui ne respecte pas la condition. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.
  
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

