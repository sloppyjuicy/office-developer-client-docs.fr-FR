---
title: FBadProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadProp
api_type:
- HeaderDef
ms.assetid: 929330c8-e6f2-4adf-a36e-fba18fa055d4
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2fbff399e088edaf3ad864f0ec7fecda3af6bc8e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578849"
---
# <a name="fbadprop"></a>FBadProp

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Valide une propriété spécifiée. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a>Paramètres

 _lpProp_
  
> [in] Une structure [SPropValue](spropvalue.md) définit la propriété à valider. 
    
## <a name="return-value"></a>Valeur renvoy�e

TRUE 
  
> La propriété spécifiée n’est pas valide. 
    
FALSE 
  
> La propriété spécifiée est valide.
    
## <a name="remarks"></a>Remarques

Un fournisseur de services peut appeler la fonction **FBadProp** pour plusieurs raisons, par exemple pour préparer un appel à la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) définition d’une propriété. **FBadProp** valide à la propriété spécifiée en fonction du type de propriété. Par exemple, si la propriété est Boolean, **FBadProp** mettre sures que sa valeur est TRUE ou FALSE. Si la propriété est binaire, **FBadProp** vérifie son pointeur et sa taille et permet de s’assurer qu’il est correctement alloué. 
  
## <a name="see-also"></a>Voir aussi



[FBadPropTag](fbadproptag.md)

