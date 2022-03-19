---
title: FBadRow
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 05489e55449dcaf354f439592628c1d7465047ea
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63626366"
---
# <a name="fbadrow"></a>FBadRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide une ligne dans un tableau.
  
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
  
> Ligne spécifiée valide.
    
## <a name="see-also"></a>Consultez aussi



[FBadRowSet](fbadrowset.md)

