---
title: FBadProp
description: FBadProp valide une propriété spécifiée. Cet article décrit sa syntaxe, ses paramètres, sa valeur de retour et ses remarques.
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
ms.openlocfilehash: 88d6d3e4dfa25a31a9cf38bb4cccaf1c40fa8f56
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816674"
---
# <a name="fbadprop"></a>FBadProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide une propriété spécifiée. 
  
|Propriété |Valeur |
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

