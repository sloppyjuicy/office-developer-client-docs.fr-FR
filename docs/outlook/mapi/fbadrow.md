---
title: FBadRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRow
api_type:
- COM
ms.assetid: 205d00df-488d-4888-8782-a1f70f54d720
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 153bcbfd87ea9e85d834cba2fd9028e98fa25750
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420618"
---
# <a name="fbadrow"></a>FBadRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide une ligne dans un tableau.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a>Paramètres

 _lprow_
  
> [in] Pointeur vers une structure [SRow](srow.md) identifiant la ligne à valider. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> La ligne spécifiée n’est pas valide.
    
FALSE 
  
> Ligne spécifiée valide.
    
## <a name="see-also"></a>Voir aussi



[FBadRowSet](fbadrowset.md)

