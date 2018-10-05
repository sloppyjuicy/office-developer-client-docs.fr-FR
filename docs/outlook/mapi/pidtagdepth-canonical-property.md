---
title: Propriété canonique PidTagDepth
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDepth
api_type:
- HeaderDef
ms.assetid: 04d444a5-e97f-48e6-89a5-8a6cb2136408
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 75d390edd06aaf826f6b8c2d996e4e08bf6a7334
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384212"
---
# <a name="pidtagdepth-canonical-property"></a>Propriété canonique PidTagDepth

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un entier qui représente le niveau de retrait, ou la profondeur, d’un objet dans une table de hiérarchie relatif.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEPTH  <br/> |
|Identificateur :  <br/> |0x3005  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |MAPI courantes  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut également spécifier le niveau de la catégorisation d’une ligne dans une table des matières ou la profondeur de hiérarchie dans une table de hiérarchie. La profondeur est zéro, où zéro représente la catégorie plus à gauche. Dans tous les cas, la valeur de propriété représente une valeur relative plutôt qu’une valeur absolue. Dans la table de hiérarchie, par exemple, la valeur de profondeur est par rapport au conteneur à partir de laquelle la table de hiérarchie a été récupérée. La profondeur ne représente pas une profondeur absolue du conteneur racine. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclut les opérations autorisées pour les objets de la table principale.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[Propriété canonique PidTagSelectable](pidtagselectable-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

