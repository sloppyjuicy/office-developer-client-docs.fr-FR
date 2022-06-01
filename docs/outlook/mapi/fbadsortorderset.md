---
title: FBadSortOrderSet
description: Décrit FBadSortOrderSet et fournit la syntaxe, les paramètres et la valeur de retour.
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
ms.openlocfilehash: cdc522d9b00f141cc4b07b064186739296bbfa6c
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816667"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide un ensemble d’ordres de tri en vérifiant son allocation de mémoire. 
  
|Clé|Valeur |
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
  
> [in] Pointeur vers une structure [SSortOrderSet](ssortorderset.md) identifiant le jeu d’ordres de tri à valider. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Le jeu d’ordres de tri spécifié n’est pas valide. 
    
FALSE 
  
> Le jeu d’ordres de tri spécifié est valide.
    
## <a name="remarks"></a>Remarques

La fonction **FBadSortOrderSet** peut être utilisée pour préparer un appel à une méthode de tri telle que la méthode [IMAPITable::SortTable](imapitable-sorttable.md) . 
  

