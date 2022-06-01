---
title: FBadRowSet
description: Décrit FBadRowSet et fournit la syntaxe, les paramètres et la valeur de retour.
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
ms.openlocfilehash: 3b69f40db2da19455ef2880e4be41c7facaffb28
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815848"
---
# <a name="fbadrowset"></a>FBadRowSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide toutes les lignes de table incluses dans un ensemble de lignes de table.
  
|Propriété |Valeur |
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
  
> [in] Pointeur vers une structure [SRowSet](srowset.md) identifiant le jeu de lignes à valider. Si le pointeur a la valeur NULL, la structure n’est pas valide. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Une ligne du jeu de lignes spécifié n’est pas valide ou l’ensemble de lignes lui-même n’est pas valide. 
    
FALSE 
  
> Les lignes du jeu de lignes spécifié et le jeu de lignes lui-même sont toutes valides.
    
## <a name="see-also"></a>Voir aussi



[FBadRow](fbadrow.md)

