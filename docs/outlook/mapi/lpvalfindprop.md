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
ms.openlocfilehash: 558e3f5168ebcc8a17197582c122b6adc9d7779d
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773235"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche une propriété spécifiée dans un jeu de propriétés.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services. |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a>Paramètres

 _ulPropTag_
  
> [in] Balise de la propriété à rechercher dans le jeu de propriétés, indiquée par le  _paramètre lpPropArray_ . 
    
 _cValues_
  
> [in] Nombre de propriétés dans le jeu de propriétés, indiquées par  _le paramètre lpPropArray_ . 
    
 _lpPropArray_
  
> [in] Tableau de **structures SPropValue** qui définit les propriétés à rechercher. 
    
## <a name="return-value"></a>Valeur renvoyée

La **fonction LpValFindProp** renvoie une structure **SPropValue** qui définit la propriété qui correspond à la balise de propriété d’entrée, ou NULL en l’absence de correspondance. 
  
## <a name="remarks"></a>Remarques

La **fonction LpValFindProp** est identique à **PpropFindProp**.
  
## <a name="see-also"></a>Voir aussi



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

