---
title: FBadPropTag
description: FBadPropTag valide une balise de propriété spécifiée. Cet article décrit sa syntaxe, ses paramètres, sa valeur de retour et ses remarques.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FBadPropTag
api_type:
- HeaderDef
ms.assetid: 143bd3c6-5a55-4122-8522-9c48473aa781
ms.openlocfilehash: de816aa473bc848fdc358a0013de544d59acf782
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815862"
---
# <a name="fbadproptag"></a>FBadPropTag

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide une balise de propriété spécifiée. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Paramètres

 _ulPropTag_
  
> [in] Balise de propriété à valider.
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> La balise de propriété spécifiée n’est pas une balise de propriété MAPI valide. 
    
FALSE 
  
> La balise de propriété spécifiée est une balise de propriété MAPI valide.
    
## <a name="remarks"></a>Remarques

La fonction **FBadPropTag** valide la balise de propriété spécifiée en fonction des définitions MAPI. Il vérifie que le type de propriété est l’un des types définis par MAPI et que l’identificateur de propriété est défini comme étant de ce type. 
  
## <a name="see-also"></a>Voir aussi



[FBadProp](fbadprop.md)

