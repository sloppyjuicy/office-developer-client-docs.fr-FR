---
title: Propriété canonique PidTagScheduleInfoMonthsMerged
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagScheduleInfoMonthsMerged
api_type:
- COM
ms.assetid: b13b5d7b-413e-4405-8a35-0422477a9e86
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 84f07b405d46381541d21799e1bb4c148a1d9e03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563314"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a>Propriété canonique PidTagScheduleInfoMonthsMerged

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste des mois pendant lesquels des données de type occupé ou un message d’absence du bureau (OOF) sont présents dans le message de libre/occupé. 
  
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

