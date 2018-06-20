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
ms.openlocfilehash: f8f58ee18095dec8a222ae8b5a19cbefbaafa663
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784933"
---
# <a name="mviprop"></a>MVI_PROP

  
  
**S’applique à**: Outlook 
  
Définit le MVI_FLAG pour une propriété spécifiée. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a>Paramètres

 _balise_
  
> La balise de propriété à modifier.
    
## <a name="remarks"></a>Remarques

Le MVI_FLAG associe la valeur de MV_FLAG, qui identifie une propriété à valeurs multiples et MV_INSTANCE, demande qu’une propriété à valeurs multiples être affichée dans un tableau dans plusieurs lignes. Le type de propriété de la propriété concerné est modifié, mais l’identificateur reste inchangé. 
  
Par exemple, lorsque la macro MVI_PROP est appliquée à une propriété de type PT_FLOAT, son type est modifié en PT_MV_FLOAT. Lorsque inclus dans une table, plusieurs lignes sont utilisés pour représenter la propriété qui comporte une ligne pour chaque valeur. Les propriétés pour les autres colonnes sont répétées. 
  
Pour plus d’informations sur ces indicateurs, voir [Vue d’ensemble des types de propriété MAPI](mapi-property-type-overview.md) et [l’utilisation des colonnes à valeurs multiples](working-with-multivalued-columns.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Macros relatives aux Structures](macros-related-to-structures.md)

