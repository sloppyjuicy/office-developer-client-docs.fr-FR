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
ms.openlocfilehash: 3b3f88495cafbd6ea764ca8901ac67c23749aebe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578576"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide un ordre de tri défini par vérifier son allocation de mémoire. 
  
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
  
> [in] Pointeur vers une structure [SSortOrderSet](ssortorderset.md) qui identifie l’ordre de tri défini à valider. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> L’ensemble d’ordre de tri spécifié n’est pas valide. 
    
FALSE 
  
> L’ensemble d’ordre de tri spécifié est valide.
    
## <a name="remarks"></a>Remarques

La fonction **FBadSortOrderSet** peut être utilisée pour préparer un appel à une méthode de tri telles que la méthode [IMAPITable::SortTable](imapitable-sorttable.md) . 
  

