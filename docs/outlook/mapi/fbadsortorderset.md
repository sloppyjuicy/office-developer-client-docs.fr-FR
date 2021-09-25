---
title: FBadSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FBadSortOrderSet
api_type:
- COM
ms.assetid: b7f80e0a-8ddd-4b24-ab63-2078a8152058
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f051996cf6beb8b9a02889c9917eafa66e15c7d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567647"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide un ordre de tri en vérifiant son allocation de mémoire. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a>Paramètres

 _lpsos_
  
> [in] Pointeur vers une structure [SSortOrderSet](ssortorderset.md) identifiant l’ordre de tri à valider. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Le jeu d’ordre de tri spécifié n’est pas valide. 
    
FALSE 
  
> Le jeu d’ordre de tri spécifié est valide.
    
## <a name="remarks"></a>Remarques

La **fonction FBadSortOrderSet** peut être utilisée pour préparer un appel à une méthode de tri telle que la méthode [IMAPITable::SortTable.](imapitable-sorttable.md) 
  

