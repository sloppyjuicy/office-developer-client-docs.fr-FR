---
title: PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TYPE
api_type:
- COM
ms.assetid: 746d63fa-bfb7-479f-94dc-ba40011c1ec9
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7bcaf230eed9cf21388b68f06ab678dc143f64ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571821"
---
# <a name="proptype"></a>PROP_TYPE

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Renvoie le type de propriété d’une balise de propriété spécifiée.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a>Paramètres

 _ulPropTag_
  
> Balise de propriété qui contient le type de propriété à renvoyer.
    
## <a name="remarks"></a>Remarques

La macro **PROP_TYPE** peut être utilisée pour déterminer le type d’une propriété. Par exemple, l’appel PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) entraîne la valeur PT_BINARY renvoyés.
  
Chaque balise de propriété contient le type de propriété dans le mot de poids faible (bits 0 à 15) et l’identificateur de propriété dans le mot de poids fort (bits 16 à 31). La macro **PROP_TYPE** extrait le type de propriété et la place dans les bits 0 à 15 du nombre entier à renvoyer. Les bits restants de la valeur de retour sont définies sur zéro. 
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Macros liées aux structures](macros-related-to-structures.md)

