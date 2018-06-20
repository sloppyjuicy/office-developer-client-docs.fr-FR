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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c3025c353c71958a19303c5e79cec319a3bf8015
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783306"
---
# <a name="fbadrow"></a>FBadRow

  
  
**S’applique à**: Outlook 
  
Valide une ligne dans une table.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a>Paramètres

 _lprow_
  
> [in] Pointeur vers une structure [SRow](srow.md) qui identifie la ligne à valider. 
    
## <a name="return-value"></a>Valeur renvoy�e

TRUE 
  
> La ligne spécifiée n’est pas valide.
    
FALSE 
  
> La ligne spécifiée est valide.
    
## <a name="see-also"></a>Voir aussi



[FBadRowSet](fbadrowset.md)

