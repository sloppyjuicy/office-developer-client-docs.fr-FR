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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 39e10e9139036cc86ec93ea24a89b98125ea6e83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783273"
---
# <a name="fbadprop"></a>FBadProp

  
  
**S’applique à**: Outlook 
  
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

