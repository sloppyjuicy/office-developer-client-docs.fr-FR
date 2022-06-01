---
title: LpValFindProp
description: Décrit la fonction LpValFindProp et fournit, la syntaxe, les paramètres, la valeur de retour et des remarques supplémentaires.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
ms.openlocfilehash: de51ef2f76834b06e4478185b6d6e2d44249ee2b
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812067"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche une propriété spécifiée dans un jeu de propriétés.
  
|Propriété|Valeur|
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
  
> [in] Balise de la propriété à rechercher dans le jeu de propriétés, indiquée par le paramètre  _lpPropArray_ . 
    
 _cValues_
  
> [in] Nombre de propriétés dans le jeu de propriétés, indiqué par le paramètre  _lpPropArray_ . 
    
 _lpPropArray_
  
> [in] Tableau de structures **SPropValue** qui définit les propriétés à rechercher. 
    
## <a name="return-value"></a>Valeur renvoyée

La fonction **LpValFindProp** retourne une structure **SPropValue** qui définit la propriété qui correspond à la balise de propriété d’entrée, ou NULL en l’absence de correspondance. 
  
## <a name="remarks"></a>Remarques

La fonction **LpValFindProp** est identique à **PpropFindProp**.
  
## <a name="see-also"></a>Voir aussi



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

