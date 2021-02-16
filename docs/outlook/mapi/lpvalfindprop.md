---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fa1588d4a58824b57c132fc8e66a0abd6e9acd0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419638"
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

