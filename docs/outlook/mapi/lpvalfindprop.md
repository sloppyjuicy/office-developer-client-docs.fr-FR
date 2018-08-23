---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c4a201411e2232a3e5fdcd97dcbc9460f657b12a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578093"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Recherche une propriété spécifiée dans une propriété définie.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes et des fournisseurs de services.  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a>Paramètres

 _ulPropTag_
  
> [in] Balise de la propriété à rechercher dans le jeu de propriétés, indiqué par le paramètre _lpPropArray_ . 
    
 _cValues_
  
> [in] Nombre de propriétés dans le jeu de propriétés, indiquée par le paramètre _lpPropArray_ . 
    
 _lpPropArray_
  
> [in] Tableau des structures **SPropValue** qui définit les propriétés à rechercher. 
    
## <a name="return-value"></a>Valeur renvoy�e

La fonction **LpValFindProp** renvoie une structure **SPropValue** qui définit la propriété qui correspond à la balise de propriété d’entrée, ou NULL si aucune correspondance n’existe. 
  
## <a name="remarks"></a>Remarques

La fonction **LpValFindProp** est identique à **PpropFindProp**.
  
## <a name="see-also"></a>Voir aussi



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

