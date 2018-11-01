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
ms.openlocfilehash: 23b4ed78f4b65a5af4c2f3e11fa770030fe4eeee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590161"
---
# <a name="fbadrow"></a>FBadRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide une ligne dans une table.
  
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
  
> [in] Pointeur vers une structure [SRow](srow.md) qui identifie la ligne à valider. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> La ligne spécifiée n’est pas valide.
    
FALSE 
  
> La ligne spécifiée est valide.
    
## <a name="see-also"></a>Voir aussi



[FBadRowSet](fbadrowset.md)

