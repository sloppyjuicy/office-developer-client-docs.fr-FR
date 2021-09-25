---
title: MVI_PROP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MVI_PROP
api_type:
- COM
ms.assetid: d7f07524-6935-4a60-aaf3-3f753ea8d86a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 22521bce4bec39c3d7c21cb7c69d1e1e20cdb0d6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556034"
---
# <a name="mvi_prop"></a>MVI_PROP

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit le MVI_FLAG d’une propriété spécifiée. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a>Paramètres

 _tag_
  
> Balise de propriété à modifier.
    
## <a name="remarks"></a>Remarques

Le MVI_FLAG combine les paramètres de MV_FLAG, en identifiant une propriété à valeurs multiples et en MV_INSTANCE, en demandant l’affichage d’une propriété à valeurs multiples dans un tableau en plusieurs lignes. Le type de propriété de la propriété concernée est modifié, mais l’identificateur reste inchangé. 
  
Par exemple, lorsque la macro MVI_PROP est appliquée à une propriété de type PT_FLOAT, son type est modifié en PT_MV_FLOAT. Lorsqu’elles sont incluses dans un tableau, plusieurs lignes sont utilisées pour représenter la propriété qui possède une ligne pour chaque valeur. Les propriétés des autres colonnes sont répétées. 
  
Pour plus d’informations sur ces indicateurs, voir [MapI Property Type Overview](mapi-property-type-overview.md) and [Working with Multivalued Columns](working-with-multivalued-columns.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Macros liées aux structures](macros-related-to-structures.md)

