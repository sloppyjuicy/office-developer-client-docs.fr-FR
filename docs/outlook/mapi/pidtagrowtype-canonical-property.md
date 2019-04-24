---
title: Propriété canonique PidTagRowType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowType
api_type:
- COM
ms.assetid: d57ce5c8-1f60-4709-b86a-4468c4208dfe
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 962e8c92ae61e8b60862a3ae26a7cdfbf5034e89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359513"
---
# <a name="pidtagrowtype-canonical-property"></a>Propriété canonique PidTagRowType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur qui indique le type d'une ligne dans un tableau.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ROW_TYPE  <br/> |
|Identificateur :  <br/> |0x0FF5  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |MAPI non transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété s'affiche uniquement sur les tables de contenu. Une catégorie n'existe que lorsqu'elle a des éléments.
  
Cette propriété peut avoir exactement l'une des valeurs suivantes:
  
TBL_LEAF_ROW 
  
> Représente les données réelles, plutôt qu'une ligne de catégorie.
    
TBL_EMPTY_CATEGORY 
  
> Non utilisé actuellement.
    
TBL_EXPANDED_CATEGORY 
  
> La catégorie est développée; en règle générale, l'interface utilisateur affiche le signe moins (-) à côté.
    
TBL_COLLAPSED_CATEGORY 
  
> La catégorie est réduite; en règle générale, l'interface utilisateur affiche le signe plus (+) en regard de celle-ci.
    
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclut les opérations admissibles pour les objets de la table principale.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagRowid](pidtagrowid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

