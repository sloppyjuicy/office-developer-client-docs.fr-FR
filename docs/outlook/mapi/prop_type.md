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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0c33633c4decd697cf241f8b7c27360f776a1ade
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412834"
---
# <a name="prop_type"></a>PROP_TYPE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie le type de propriété d’une balise de propriété spécifiée.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a>Paramètres

 _ulPropTag_
  
> Balise de propriété qui contient le type de propriété à retourner.
    
## <a name="remarks"></a>Remarques

La **PROP_TYPE** macro peut être utilisée pour déterminer le type d’une propriété. Par exemple, l’appel PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) entraîne la PT_BINARY renvoyée.
  
Chaque balise de propriété contient le type de propriété dans le mot de bas ordre (bits 0 à 15) et l’identificateur de propriété dans le mot de haut niveau (bits 16 à 31). La **macro PROP_TYPE** extrait le type de propriété et le place en bits 0 à 15 de l’ensemble à retourner. Les autres bits de la valeur de retour sont des zéros. 
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Macros liées aux structures](macros-related-to-structures.md)

