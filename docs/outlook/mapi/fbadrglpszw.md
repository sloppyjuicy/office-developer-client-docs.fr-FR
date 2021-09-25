---
title: FBadRglpszW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FBadRglpszW
api_type:
- COM
ms.assetid: 880eb35d-7045-4fdd-bb33-0f14557a7316
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2d677c6d4e1eb416e5dabf466f24d9b77c48c03e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621114"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide toutes les chaînes d’un tableau de chaînes Unicode. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a>Paramètres

 _lppszW_
  
> [in] Pointeur vers un tableau de chaînes Unicode terminées par null. 
    
 _cStrings_
  
> [in] Nombre de chaînes dans le tableau pointées par _le paramètre lppszW._ 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Une ou plusieurs des chaînes du tableau spécifié ne sont pas valides. 
    
FALSE 
  
> Les chaînes du tableau spécifié sont valides.
    

