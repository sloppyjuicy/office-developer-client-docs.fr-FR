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
ms.openlocfilehash: c7cd82dec7affe7f0f4668150875914865ccf08f
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63626373"
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

La **fonction FBadPropTag** valide la balise de propriété spécifiée en fonction des définitions MAPI. Il s’assure que le type de propriété est l’un des types définis par MAPI et que l’identificateur de propriété est défini comme étant de ce type. 
  
## <a name="see-also"></a>Consultez aussi



[FBadProp](fbadprop.md)

