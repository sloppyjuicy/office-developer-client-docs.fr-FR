---
title: MVI_PROP
description: Décrit les propriétés, paramètres et remarques pour MVI_PROP, qui définit le MVI_FLAG pour une propriété spécifiée.
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
ms.openlocfilehash: 93b46dc41c5056a2cd814cbecdab0ce3050b7643
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828093"
---
# <a name="mvi_prop"></a>MVI_PROP

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit la MVI_FLAG pour une propriété spécifiée. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure associée :  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a>Paramètres

 _tag_
  
> Balise de propriété à modifier.
    
## <a name="remarks"></a>Remarques

Le MVI_FLAG combine le paramètre de MV_FLAG, en identifiant une propriété comme à valeurs multiples et MV_INSTANCE, en demandant qu’une propriété à valeurs multiples soit affichée dans une table sur plusieurs lignes. Le type de propriété de la propriété affectée est modifié, mais l’identificateur reste inchangé. 
  
Par exemple, lorsque la macro MVI_PROP est appliquée à une propriété de type PT_FLOAT, son type est remplacé par PT_MV_FLOAT. Lorsqu’elles sont incluses dans un tableau, plusieurs lignes sont utilisées pour représenter la propriété qui a une ligne pour chaque valeur. Les propriétés des autres colonnes sont répétées. 
  
Pour plus d’informations sur ces indicateurs, consultez [vue d’ensemble du type de propriété MAPI](mapi-property-type-overview.md) et [Utilisation des colonnes à valeurs multiples](working-with-multivalued-columns.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Macros liées aux structures](macros-related-to-structures.md)

