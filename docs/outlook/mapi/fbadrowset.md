---
title: FBadRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FBadRowSet
api_type:
- COM
ms.assetid: 3890dd50-e6ca-4859-bada-f6752ab61d41
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 241441c1aa516b366fdecd6c17f5d12cf12a2206
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630928"
---
# <a name="fbadrowset"></a>FBadRowSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide toutes les lignes de tableau incluses dans un ensemble de lignes de tableau.
  
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
  
> [in] Pointeur vers une structure [SRowSet](srowset.md) identifiant le jeu de lignes à valider. Si le pointeur est NULL, la structure n’est pas valide. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Une ligne du jeu de lignes spécifié n’est pas valide ou le jeu de lignes lui-même n’est pas valide. 
    
FALSE 
  
> Les lignes du jeu de lignes spécifié et du jeu de lignes lui-même sont toutes valides.
    
## <a name="see-also"></a>Voir aussi



[FBadRow](fbadrow.md)

