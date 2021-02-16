---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Last modified: February 20, 2012'
ms.openlocfilehash: 0e64df38afdb8ecce35eb0151d36dde3da35f0a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356853"
---
# <a name="mnls_isbadstringptrw"></a>MNLS_IsBadStringPtrW

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Vérifie qu’un pointeur vers une chaîne large est valide.
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a>Paramètres

 _lpsz_
  
> [in] Pointeur vers la chaîne de caractères large.
    
 _ucchMax_
  
> [in] Longueur maximale de la chaîne en caractères, y compris terminateur.
    
## <a name="return-value"></a>Valeur renvoyée

Renvoie un booléen qui est true si la chaîne est mauvaise.
  
## <a name="remarks"></a>Remarques

Cette fonction [encapsule IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx). Pour plus d’informations, [voir IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).
  

