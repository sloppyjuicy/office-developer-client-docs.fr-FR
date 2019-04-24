---
title: FBadRglpszW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpszW
api_type:
- COM
ms.assetid: 880eb35d-7045-4fdd-bb33-0f14557a7316
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ca436bc83d5170d55475c1dd9702a9d54e4b9d5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341054"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide toutes les chaînes dans un tableau de chaînes Unicode. 
  
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
  
> dans Pointeur vers un tableau de chaînes Unicode terminées par un caractère null. 
    
 _cStrings_
  
> dans Nombre de chaînes dans le tableau vers lequel pointe le paramètre _lppszW_ . 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Une ou plusieurs des chaînes du tableau spécifié ne sont pas valides. 
    
FALSE 
  
> Les chaînes du tableau spécifié sont valides.
    

