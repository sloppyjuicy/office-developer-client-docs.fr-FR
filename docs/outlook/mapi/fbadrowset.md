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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e86e9fbf4901b5944775886f38db1ba12c4b122d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590959"
---
# <a name="fbadrowset"></a>FBadRowSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide toutes les lignes de tableau inclus dans un ensemble de lignes du tableau.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a>Paramètres

 _lpRowSet_
  
> [in] Pointeur vers une structure [SRowSet](srowset.md) qui identifie la ligne la valeur à valider. Si le pointeur est NULL, la structure n’est pas valide. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Une ligne de l’ensemble de la ligne spécifiée n’est pas valide ou la ligne lui-même la valeur n’est pas valide. 
    
FALSE 
  
> Les lignes de l’ensemble de la ligne spécifiée et la ligne se sont valides.
    
## <a name="see-also"></a>Voir aussi



[FBadRow](fbadrow.md)

