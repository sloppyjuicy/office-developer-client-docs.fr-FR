---
title: Propriété canonique PidTagRowType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRowType
api_type:
- COM
ms.assetid: d57ce5c8-1f60-4709-b86a-4468c4208dfe
description: Contient une valeur qui indique le type d’une ligne dans un tableau pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: cf7611dbff54a06daba6020e9f3b03b03ab05128
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524088"
---
# <a name="pidtagrowtype-canonical-property"></a>Propriété canonique PidTagRowType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur qui indique le type d’une ligne dans un tableau.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ROW_TYPE  <br/> |
|Identificateur :  <br/> |0x0FF5  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |MAPI non transmetteable  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété apparaît uniquement dans les tables des matières. Une catégorie n’existe que lorsqu’elle possède des éléments.
  
Cette propriété peut avoir exactement l’une des valeurs suivantes :
  
TBL_LEAF_ROW 
  
> Représente les données réelles, plutôt qu’une ligne de catégorie.
    
TBL_EMPTY_CATEGORY 
  
> Non utilisé actuellement.
    
TBL_EXPANDED_CATEGORY 
  
> La catégorie est étendue . L’interface utilisateur l’affiche généralement avec le signe moins ( - ) en face de celle-ci.
    
TBL_COLLAPSED_CATEGORY 
  
> La catégorie est réduire . L’interface utilisateur l’affiche généralement avec le signe plus (+) à côté de celle-ci.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclut les opérations autorisées pour les objets de table principale.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagRowid](pidtagrowid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

