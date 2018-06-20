---
title: FBadPropTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadPropTag
api_type:
- HeaderDef
ms.assetid: 143bd3c6-5a55-4122-8522-9c48473aa781
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d1503aaa5bddd23a90035219901e1dc232dbd026
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783285"
---
# <a name="fbadproptag"></a>FBadPropTag

  
  
**S’applique à**: Outlook 
  
Valide une balise de propriété spécifiée. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Paramètres

 _ulPropTag_
  
> [in] La balise de propriété à valider.
    
## <a name="return-value"></a>Valeur renvoy�e

TRUE 
  
> La balise de propriété spécifié n’est pas une balise de propriété MAPI valide. 
    
FALSE 
  
> La balise de propriété spécifiée est une balise de propriété MAPI valide.
    
## <a name="remarks"></a>Remarques

La fonction **FBadPropTag** valide la balise de propriété spécifiée en fonction des définitions de MAPI. Il se sures que le type de propriété est un des types définis par MAPI et que l’identificateur de propriété est définie comme étant de ce type. 
  
## <a name="see-also"></a>Voir aussi



[FBadProp](fbadprop.md)

