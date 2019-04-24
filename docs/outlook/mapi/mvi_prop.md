---
title: MVI_PROP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MVI_PROP
api_type:
- COM
ms.assetid: d7f07524-6935-4a60-aaf3-3f753ea8d86a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 087d38face72e1e067350b1959b37313ebbd7c44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326291"
---
# <a name="mviprop"></a>MVI_PROP

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit le MVI_FLAG pour une propriété spécifiée. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Structure associée:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a>Paramètres

 _Numéro_
  
> Balise de propriété à modifier.
    
## <a name="remarks"></a>Remarques

Le MVI_FLAG combine le paramètre MV_FLAG, en identifiant une propriété comme étant à valeurs multiples et MV_INSTANCE, en demandant qu'une propriété à valeurs multiples s'affiche dans un tableau sur plusieurs lignes. Le type de propriété de la propriété affectée est modifié, mais l'identificateur reste inchangé. 
  
Par exemple, lorsque la macro MVI_PROP est appliquée à une propriété de type PT_FLOAT, son type est modifié en PT_MV_FLOAT. Lorsqu'elle est incluse dans un tableau, plusieurs lignes sont utilisées pour représenter la propriété qui contient une ligne pour chaque valeur. Les propriétés des autres colonnes sont répétées. 
  
Pour plus d'informations sur ces indicateurs, voir [MAPI Property type Overview](mapi-property-type-overview.md) et [Working with multivalued Columns](working-with-multivalued-columns.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Macros liées aux structures](macros-related-to-structures.md)

