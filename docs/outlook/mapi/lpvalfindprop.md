---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 05b8620469b289969bdcc2bb4f15f940d9c767e1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592185"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche une propriété spécifiée dans un jeu de propriétés.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services.  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a>Paramètres

 _ulPropTag_
  
> [in] Balise de la propriété à rechercher dans le jeu de propriétés, indiquée par le _paramètre lpPropArray._ 
    
 _cValues_
  
> [in] Nombre de propriétés dans le jeu de propriétés, indiqué par _le paramètre lpPropArray._ 
    
 _lpPropArray_
  
> [in] Tableau de **structures SPropValue** qui définit les propriétés à rechercher. 
    
## <a name="return-value"></a>Valeur renvoyée

La **fonction LpValFindProp** renvoie une structure **SPropValue** qui définit la propriété qui correspond à la balise de propriété d’entrée, ou NULL en l’absence de correspondance. 
  
## <a name="remarks"></a>Remarques

La **fonction LpValFindProp** est identique à **PpropFindProp**.
  
## <a name="see-also"></a>Voir aussi



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

