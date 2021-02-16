---
title: FBadSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadSortOrderSet
api_type:
- COM
ms.assetid: b7f80e0a-8ddd-4b24-ab63-2078a8152058
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 31840923e24cddd0dc3dfa9cc67b610d0dcd7e47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428458"
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
  

