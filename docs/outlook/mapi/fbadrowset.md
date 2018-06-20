---
title: FBadRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRowSet
api_type:
- COM
ms.assetid: 3890dd50-e6ca-4859-bada-f6752ab61d41
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e6963fc373f771289e3dbff3a0b41857352b4b9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783313"
---
# <a name="fbadrowset"></a>FBadRowSet

  
  
**S’applique à**: Outlook 
  
Valide toutes les lignes de tableau inclus dans un ensemble de lignes du tableau.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a>Paramètres

 _lpRowSet_
  
> [in] Pointeur vers une structure [SRowSet](srowset.md) qui identifie la ligne la valeur à valider. Si le pointeur est NULL, la structure n’est pas valide. 
    
## <a name="return-value"></a>Valeur renvoy�e

TRUE 
  
> Une ligne de l’ensemble de la ligne spécifiée n’est pas valide ou la ligne lui-même la valeur n’est pas valide. 
    
FALSE 
  
> Les lignes de l’ensemble de la ligne spécifiée et la ligne se sont valides.
    
## <a name="see-also"></a>Voir aussi



[FBadRow](fbadrow.md)

