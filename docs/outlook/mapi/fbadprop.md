---
title: FBadProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FBadProp
api_type:
- HeaderDef
ms.assetid: 929330c8-e6f2-4adf-a36e-fba18fa055d4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2274fa324425bfc3e04ec5a6a45ff1270cbfbca8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621149"
---
# <a name="fbadprop"></a>FBadProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide une propriété spécifiée. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a>Paramètres

 _lpprop_
  
> [in] Structure [SPropValue](spropvalue.md) définissant la propriété à valider. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> La propriété spécifiée n’est pas valide. 
    
FALSE 
  
> La propriété spécifiée est valide.
    
## <a name="remarks"></a>Remarques

Un fournisseur de services peut appeler la fonction **FBadProp** pour plusieurs raisons. Par exemple, pour effectuer un appel vers la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) définissant une propriété. **FBadProp** valide la propriété spécifiée en fonction du type de propriété. Par exemple, si la propriété est une booléenne, la fonction **FBadProp** s’assure que sa valeur est TRUE ou FALSE. Si la propriété est binaire, **FBadProp** vérifie son pointeur et sa taille, et s’assure qu’elle est correctement allouée. 
  
## <a name="see-also"></a>Voir aussi



[FBadPropTag](fbadproptag.md)

