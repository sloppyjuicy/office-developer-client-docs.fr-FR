---
title: Propriété canonique PidTagFormCategorySub
description: Décrit la propriété canonique PidTagFormCategorySub, qui contient la sous-catégorie d’un formulaire, telle que définie par une application cliente.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFormCategorySub
api_type:
- HeaderDef
ms.assetid: 0e654152-c850-417a-8877-29d47cf85db5
ms.openlocfilehash: b6de5b8c1db3f6f64246dd5c6cab3808b6bc0f65
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770382"
---
# <a name="pidtagformcategorysub-canonical-property"></a>Propriété canonique PidTagFormCategorySub

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la sous-catégorie d’un formulaire, telle que définie par une application cliente. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FORM_CATEGORY_SUB, PR_FORM_CATEGORY_SUB_A, PR_FORM_CATEGORY_SUB_W  <br/> |
|Identificateur :  <br/> |0x3305  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |MAPI commun  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont subordonnées à la catégorie de formulaire principale fournie dans la propriété **PR_FORM_CATEGORY** ([PidTagFormCategory](pidtagformcategory-canonical-property.md)). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

