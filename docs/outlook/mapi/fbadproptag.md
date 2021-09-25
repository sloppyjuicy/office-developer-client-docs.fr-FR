---
title: FBadPropTag
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d1e5bac98f69080a3b534bfa8f96bbe3f5a3e4f8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596469"
---
# <a name="fbadproptag"></a>FBadPropTag

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide une balise de propriété spécifiée. 
  
|||
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

La **fonction FBadPropTag** valide la balise de propriété spécifiée en fonction des définitions MAPI. Il s’assure que le type de propriété est l’un des types définis par MAPI et que l’identificateur de propriété est défini comme étant de ce type. 
  
## <a name="see-also"></a>Voir aussi



[FBadProp](fbadprop.md)

