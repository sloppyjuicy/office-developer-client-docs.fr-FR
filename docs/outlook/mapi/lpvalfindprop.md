---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d7601eb50818fa6f39384a6b024215fc4917e83a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784527"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**S’applique à**: Outlook 
  
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

