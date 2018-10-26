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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 943dab0141581adc32c184b0042a063a4ec05c3e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582881"
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
  
> [in] La balise de propriété à valider.
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> La balise de propriété spécifié n’est pas une balise de propriété MAPI valide. 
    
FALSE 
  
> La balise de propriété spécifiée est une balise de propriété MAPI valide.
    
## <a name="remarks"></a>Remarques

La fonction **FBadPropTag** valide la balise de propriété spécifiée en fonction des définitions de MAPI. Il se sures que le type de propriété est un des types définis par MAPI et que l’identificateur de propriété est définie comme étant de ce type. 
  
## <a name="see-also"></a>Voir aussi



[FBadProp](fbadprop.md)

