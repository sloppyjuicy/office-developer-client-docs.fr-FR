---
title: FBadRow
description: FBadRow valide une ligne dans une table. Cet article décrit sa syntaxe, ses paramètres et sa valeur de retour.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FBadRow
api_type:
- COM
ms.assetid: 205d00df-488d-4888-8782-a1f70f54d720
ms.openlocfilehash: b4b3d9f05781097cd962d3274345a204e10e37dd
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817745"
---
# <a name="fbadrow"></a>FBadRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide une ligne dans une table.
  
|Propriété |Valeur |
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
  
> La ligne spécifiée est valide.
    
## <a name="see-also"></a>Voir aussi



[FBadRowSet](fbadrowset.md)

