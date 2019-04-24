---
title: Propriété canonique PidTagFlagCompleteTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagCompleteTime
api_type:
- HeaderDef
ms.assetid: effc738a-30f4-4a5e-b21d-04b50dad1f45
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5dd0d4c19f30e189218b1aeddd333df58e42102a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316288"
---
# <a name="pidtagflagcompletetime-canonical-property"></a>Propriété canonique PidTagFlagCompleteTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie la date et l'heure au format UTC (Coordinated Universal Time) auxquelles l'objet message a été marqué comme étant terminé.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FLAG_COMPLETE_TIME  <br/> |
|Identificateur :  <br/> |0x1091  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est supprimée si l'objet message n'est pas marqué comme terminé. La plus petite résolution du temps doit être de minutes (la valeur doit être un multiple de 600 millions). Cette propriété ne doit pas exister si l'objet est un objet lié à la réunion et qu'il ne doit pas exister sur un objet Task.
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations relatives au marquage.
    
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

