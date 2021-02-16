---
title: Propriété canonique PidTagScheduleInfoMonthsMerged
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsMerged
api_type:
- COM
ms.assetid: b13b5d7b-413e-4405-8a35-0422477a9e86
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 53bc27b4ddd05b4a52328c605a6d4f673c91afd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336476"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a>Propriété canonique PidTagScheduleInfoMonthsMerged

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste des mois pendant lesquels les données de type occupé ou un message d’absence du bureau sont présents dans le message de libre/occupé. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_MONTHS_MERGED  <br/> |
|Identificateur :  <br/> |0x684F  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |Libre/Occupé  <br/> |
   
## <a name="remarks"></a>Remarques

Les événements de type de libre/occupé provisoire ne sont pas inclus dans cette propriété. La syntaxe/le format et les contraintes de cette propriété sont identiques à celles de **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)), mais font référence aux rendez-vous marqués comme étant OOF ou Occupé sur l’objet calendrier associé. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publie la disponibilité d’un utilisateur ou d’une ressource.
    
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

