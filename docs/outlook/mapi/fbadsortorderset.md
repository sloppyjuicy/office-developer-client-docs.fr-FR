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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0e200ea20c55cfd5729ce4c1f590de2d61ca73bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783287"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**S’applique à**: Outlook 
  
Valide un ordre de tri défini par vérifier son allocation de mémoire. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a>Paramètres

 _lpsos_
  
> [in] Pointeur vers une structure [SSortOrderSet](ssortorderset.md) qui identifie l’ordre de tri défini à valider. 
    
## <a name="return-value"></a>Valeur renvoy�e

TRUE 
  
> L’ensemble d’ordre de tri spécifié n’est pas valide. 
    
FALSE 
  
> L’ensemble d’ordre de tri spécifié est valide.
    
## <a name="remarks"></a>Remarques

La fonction **FBadSortOrderSet** peut être utilisée pour préparer un appel à une méthode de tri telles que la méthode [IMAPITable::SortTable](imapitable-sorttable.md) . 
  

