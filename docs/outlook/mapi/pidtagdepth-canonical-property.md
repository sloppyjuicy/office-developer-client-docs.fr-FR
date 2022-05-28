---
title: Propriété canonique PidTagDepth
description: Décrit la propriété canonique PidTagDepth, qui contient un entier indiquant le niveau relatif de retrait ou de profondeur d’un objet dans une table de hiérarchie.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDepth
api_type:
- HeaderDef
ms.assetid: 04d444a5-e97f-48e6-89a5-8a6cb2136408
ms.openlocfilehash: e7a2e9a8a85c483961defe2bd132abded4c44046
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769730"
---
# <a name="pidtagdepth-canonical-property"></a>Propriété canonique PidTagDepth

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un entier qui représente le niveau relatif de retrait ou de profondeur d’un objet dans une table de hiérarchie.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEPTH  <br/> |
|Identificateur :  <br/> |0x3005  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |MAPI commun  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut également spécifier le niveau de catégorisation d’une ligne dans une table de contenu ou la profondeur de hiérarchie dans une table de hiérarchie. La profondeur est de base zéro, où zéro représente la catégorie la plus à gauche. Dans tous les cas, la valeur de propriété représente une valeur relative plutôt qu’une valeur absolue. Dans la table de hiérarchie, par exemple, la valeur de profondeur est relative au conteneur à partir duquel la table de hiérarchie a été récupérée. La profondeur ne représente pas une profondeur absolue du conteneur racine. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclut les opérations autorisées pour les objets de table de base.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les listes d’utilisateurs, de contacts, de groupes et de ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[Propriété canonique PidTagSelectable](pidtagselectable-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

