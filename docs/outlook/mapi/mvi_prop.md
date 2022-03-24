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
ms.openlocfilehash: 3ffb3c8fcd979b962da7d9f7a3916b7d91cde9b6
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63720556"
---
# <a name="mvi_prop"></a>MVI_PROP

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit le MVI_FLAG d’une propriété spécifiée. 
  
|Propriété |Valeur |
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
  
Pour plus d’informations sur ces indicateurs, voir Vue d’ensemble du type de propriété [MAPI](mapi-property-type-overview.md) et [fonctionnement avec des colonnes à valeurs multiples](working-with-multivalued-columns.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Macros liées aux structures](macros-related-to-structures.md)

