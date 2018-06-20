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
ms.openlocfilehash: 7fdb8781c39d7814ff2c38ff4df4545511d28a5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786624"
---
# <a name="pidtagrowtype-canonical-property"></a>Propriété canonique PidTagRowType

  
  
**S’applique à**: Outlook 
  
Contient une valeur qui indique le type d’une ligne dans une table.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ROW_TYPE  <br/> |
|Identificateur :  <br/> |0x0FF5  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |MAPI non transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété s’affiche uniquement sur des tables des matières. Une catégorie existe uniquement lorsqu’il a des éléments.
  
Cette propriété peut avoir exactement une des valeurs suivantes :
  
TBL_LEAF_ROW 
  
> Représente les données réelles, plutôt qu’une ligne de la catégorie.
    
TBL_EMPTY_CATEGORY 
  
> N’est actuellement pas utilisé.
    
TBL_EXPANDED_CATEGORY 
  
> La catégorie est développée ; l’interface utilisateur affiche généralement avec le signe moins (-) à côté d’elle.
    
TBL_COLLAPSED_CATEGORY 
  
> La catégorie est réduite ; l’interface utilisateur affiche généralement avec le signe plus (+) en regard de son.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclut les opérations autorisées pour les objets de la table principale.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagRowid](pidtagrowid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

