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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360850"
---
# <a name="pidtagdepth-canonical-property"></a>Propriété canonique PidTagDepth

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un nombre integer qui représente le niveau relatif de retrait, ou profondeur, d’un objet dans un tableau hiérarchique.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEPTH  <br/> |
|Identificateur :  <br/> |0x3005  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |MAPI courant  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut également spécifier le niveau de catégorisation d’une ligne dans une table des matières ou la profondeur de hiérarchie dans un tableau hiérarchique. La profondeur est de base zéro, où zéro représente la catégorie la plus à gauche. Dans tous les cas, la valeur de la propriété représente une valeur relative plutôt qu’une valeur absolue. Dans le tableau hiérarchique, par exemple, la valeur de profondeur est relative au conteneur à partir duquel la table de hiérarchie a été récupérée. La profondeur ne représente pas une profondeur absolue à partir du conteneur racine. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server de protocole associées.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclut les opérations autorisées pour les objets de table principale.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[Propriété canonique PidTagSelectable](pidtagselectable-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

