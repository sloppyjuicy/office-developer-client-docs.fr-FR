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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 91a9d15544ebc71d27c8a9a6f930f3c32ecaa4fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786930"
---
# <a name="proptype"></a>PROP_TYPE

  
  
**S’applique à**: Outlook 
  
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


[Macros relatives aux Structures](macros-related-to-structures.md)

